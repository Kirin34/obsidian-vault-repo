### 🗂️ Struttura dei Repository

- Sono stati creati **due repository distinti**:
    
    - Uno per le applicazioni **Windows**
    - Uno per le applicazioni **Linux**
- Ogni repository contiene una cartella `kustomize` con **tre sottocartelle principali**:
    
    - `Resources`: contiene i **template base** (ossatura comune)
    - `Apps`: contiene le **customizzazioni specifiche** per ogni applicazione
    - `Components`: contiene risorse modulari riutilizzabili (es. props per FluentBit)

---
### ⚙️ Funzionamento di Kustomize

- Kustomize si basa su un **sistema incrementale**:
    - I file in `Resources` definiscono la **struttura base** dei manifest.
    - Le app in `Apps` importano questi file e li **modificano tramite patch**.
    - Le patch possono essere:
        - Inline nel file `kustomization.yaml`
        - Esterne, referenziate come file separati

---
### 📄 Esempi di Risorse Base

Questi sono degli esempi per le risorse presenti nella repository aztech-windows sotto la folder `kustomize/resources`:
#### `ingress/ingress.yaml`

- Contiene:
    - Annotation Haproxy per affinity via cookie
    - `session-cookie-dynamic: true`
    - Host e path generici (placeholder)
- Viene patchato per ogni app per:
    - Specificare il path corretto
    - Impostare il cookie specifico

#### `service/service.yaml`

- Espone la porta del pod
- In alcuni casi:
    - Pod espone `8080` → Service espone `8080`
    - Pod espone `80` → Service espone `80`

#### `base/statefulset.yaml`

- Struttura principale del pod:
    - Include due container (es. app + FluentBit)
    - Variabili d’ambiente comuni
    - Risorse base per FluentBit (modificabili via patch)

---
### 🧩 Personalizzazione delle Applicazioni

#### Esempio: `apps/marketing`

- Struttura simile per tutte le app:
    - Importa i file base da `Resources`
    - Applica patch specifiche (es. ingress, service)
    - Aggiunge ingress secondario per nginx
    - Imposta label comuni
    - Usa `namePrefix` per distinguere le risorse


---
### 🌐 Gestione degli Ingress

#### Ingress Haproxy

- Usato per il traffico standard
- Gestisce affinity e sessioni
- Path e host generici → patchati per ogni app
#### Ingress Nginx
- Usato per la **cloudification**
- Gestisce traffico separato
- Viene definito direttamente nella cartella dell’app
- Condivide lo stesso controller con le app Linux

L’ingress viene patchato per:

- Impostare il `ingressClassName` corretto
- Definire l’**URL specifico** per l’ambiente
- È possibile inviare richieste dirette a un pod usando un header:

```
	pod: mk-prisma-all-0
```
---

### 🔄 FluentBit e Risorse

- FluentBit è presente come container secondario
- Le risorse assegnate possono variare:
    - In ambienti con molti log (es. Motor), si aumentano CPU/memoria
    - Patch specifiche per FluentBit sono gestite via `Components`

---
### 🚀 Processo di Deploy

1. **Build dell’immagine Docker**
    
    - L’immagine viene creata e pushata su **AWS ECR**
    - Il tag immagine è legato al **numero della pipeline** (es. `PH`)
2. **Deploy con Kustomize**
    - Kustomize builda l'environment puntando al file `kustomize/apps/${NOME_APP}/env/${environment_name}/kustomization.yaml` dell’app
```
	kustomize build kustomize/${NOME_APP}/env/${environment_name} > app.yaml
```
- Questo file importa:
        - La cartella base dell’applicazione
        - I template principali da `Resources`
        - Le patch specifiche per l’ambiente
3. **Modifiche applicate**
    - Viene impostato il **namespace** corretto (es. `pp-marketing-prisma`)
    - Viene definita l’**immagine** da usare per l’applicazione
    - Il tag immagine cambia ad ogni build, **solo per l’app principale**, non per FluentBit
### 🏷️ Gestione dei Nomi con `namePrefix`

- Per le applicazioni **Windows**, si usa `namePrefix` per **applicare un prefisso ai nomi delle risorse** (es. `marketing-prisma-`)
- Questo è necessario per uniformare i nomi di:
    - Service
    - Ingress
    - StatefulSet
    - Altre risorse
#### ⚠️ Limitazione su Windows

- Windows ha una **limitazione sull’hostname**: massimo **15 caratteri**
- Questo impatta la variabile d’ambiente `HOSTNAME` nei pod
- Per evitare problemi:
    - Si usa `disableSuffixHash` per **evitare l’aggiunta automatica di hash**
    - Si applicano prefissi solo dove necessario, con file separati:
        - Uno per `disableSuffixHash` su ingress/service
        - Uno per `enablePrefix` su StatefulSet

#### 🔥 Warm-Up dell’Applicazione

- Gestito tramite una **ConfigMap dedicata** chiamata `warmup`
- Contiene uno **script PowerShell** che:
    - Esegue chiamate HTTP verso gli endpoint esposti dal container
    - Serve a “risvegliare” l’applicazione, pre-caricando cache e risorse
### 🧠 Considerazioni Finali
- Il sistema è **modulare e scalabile**:
    - Ogni app eredita l’ossatura base
    - Le modifiche sono isolate e gestibili
- Le configurazioni **cross-environment** (es. path, cookie) sono definite a livello di app
- È possibile **aggiungere nuove risorse** oltre a quelle base, senza vincoli