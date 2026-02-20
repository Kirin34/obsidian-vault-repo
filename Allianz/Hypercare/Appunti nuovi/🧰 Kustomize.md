
## 📌 Cos'è Kustomize
Kustomize è uno strumento utilizzato per **templatizzare e gestire manifest YAML** in ambienti Kubernetes.  
Permette di creare risorse **modulari, riutilizzabili e facilmente patchabili** per diversi ambienti (test, preprod, prod).

---

## 🗂️ Struttura dei Repository

Ogni applicazione è organizzata in **due repository** (Windows e Linux), ognuna contenente una cartella `kustomize` con tre sottocartelle principali:

- `Resources` → template base comuni.  
- `Apps` → customizzazioni specifiche per ogni applicazione.  
- `Components` → risorse modulari riutilizzabili (es. configurazioni FluentBit).

Esempio:
```
kustomize/
├── resources/
├── apps/
└── components/
```

---

## ⚙️ Funzionamento di Kustomize

Kustomize si basa su un approccio **incrementale**:
1. Le risorse in `Resources` definiscono la struttura base dei manifest.
2. Le app in `Apps` importano le risorse base.
3. Le modificano tramite **patch** (inline o file separati).
4. Si buildano i manifest finali per l’ambiente target.

---

## 🧱 Esempi di Risorse Base (WINDOWS)

### `ingress/ingress.yaml`
- Annotation HAProxy per affinity via cookie.  
- `session-cookie-dynamic: true`.  
- Host e path generici (placeholder).  
- Patch per ogni app per specificare:
  - Path corretto.
  - Cookie specifico.

### `service/service.yaml`
- Espone la porta del pod:
  - 8080 → 8080
  - 80 → 80

### `base/statefulset.yaml`
- Definisce struttura principale pod:
  - Container app + FluentBit sidecar.
  - Variabili d’ambiente comuni.
  - Risorse base modificabili via patch.

---

## 🧩 Personalizzazione delle Applicazioni

Esempio: `apps/marketing`
- Importa i file base da `Resources`.
- Applica patch per ingress e service.
- Aggiunge ingress secondario per Nginx.
- Imposta label comuni.
- Usa `namePrefix` per distinguere le risorse.

---

## 🌐 Gestione degli Ingress

### Ingress HAProxy
- Traffico standard con session affinity.
- Path e host generici → patchati per ogni app.

### Ingress Nginx
- Usato per cloudification.  
- Gestisce traffico separato.  
- Definito direttamente nella cartella dell’app.  
- Condivide controller con app Linux.

Header utile per targeting pod:
```
pod: mk-prisma-all-0
```

---

## 🏷️ Naming e Limitazioni Windows

- Per le app Windows si utilizza `namePrefix` per aggiungere un prefisso ai nomi delle risorse (service, ingress, statefulset...).  
- Limitazione hostname Windows: **max 15 caratteri**.  
  - Utilizzo di `disableSuffixHash` per evitare hash automatici.  
  - Prefissi applicati solo dove necessario (file separati per ingress/service e statefulset).

---

## 🧠 Warm-Up delle Applicazioni

- Gestito tramite ConfigMap dedicata `warmup`.  
- Contiene script PowerShell per:
  - Effettuare chiamate HTTP agli endpoint.  
  - “Risvegliare” l’applicazione (caricamento cache e risorse).

---

## 🚀 Processo di Deploy con Kustomize

1. Build dei manifest:
   ```bash
   kustomize build kustomize/${NOME_APP}/env/${environment_name} > app.yaml
   ```

2. Impostazione:
   - Namespace corretto (es. `pp-marketing-prisma`).
   - Immagine da usare per l’applicazione.
   - Tag immagine aggiornato ad ogni build.

3. Applicazione con `kubectl`:
   ```bash
   kubectl apply -f app.yaml
   # oppure
   kubectl apply -k kustomize/${NOME_APP}/env/${environment_name}
   ```

---

## 📎 Note pratiche
- Le modifiche **temporanee** fatte con `kubectl edit` non sono persistenti: vanno riportate nei template Kustomize.  
- L’uso modulare riduce la duplicazione dei manifest.  
- Patch separate facilitano la gestione di ingress/service e la compatibilità Windows/Linux.

---

📄 **Riferimenti nei tuoi appunti**:  
- Video 3 → Gestione dei manifest con Kustomize  
- Video 5 → Struttura repository, ingress, naming e warm-up  
- Video 6 → Processo di deploy con Kustomize
