## 🏗️ Build delle Golden Image

### 📌 Cos'è una Golden Image?

Una **Golden Image** è un'immagine base Docker, costruita internamente a partire da immagini pubbliche (Windows o Linux), su cui vengono installati:

- Middleware come **Jboss** o **Tomcat**
- Componenti comuni a tutti gli applicativi

#### Esempi:

- **Windows**: installazione di _Db2_, _Allianz Dispatch_
- **Linux**: installazione di _certificati_, _utility varie_

---
### 🧬 Tipologie di Golden Image

#### 🔹 Linux
- Due varianti:
    - **Jboss**
    - **Tomcat**
- Struttura identica tra le due

#### 🔹 Windows
- Struttura più articolata:
    - **Fluentbit**: cartella per la build dell'immagine Fluentbit
    - **Initcontainer**: installazione del OneAgent di Dynatrace
    - **layers/**: contiene 4 folder con Dockerfile per la build in 4 step:
        1. Installazione di ASP.NET
        2. Inizializzazione di Db2
        3. Finalizzazione di Db2
        4. Installazione di tool proprietari Allianz

---

## ⚙️ Jenkins e Shared Library

### 📁 Jenkinsfile

Ogni repository di Golden Image contiene un **Jenkinsfile** che utilizza metodi definiti nella **Shared Library**.
### 🧠 Differenze rispetto alle immagini applicative

- Il processo è **diverso**: non si parte da un'applicazione, ma da una base comune.
- L'immagine viene **buildata** e poi **pushata** su vari ECR (uno per ambiente).

---
## 🧰 Dettagli Tecnici della Build

### 🖥️ Infrastruttura di Build

#### Linux

- Utilizza un **bastion host** per la build.

#### Windows

- Utilizza **macchine EC2 effimere**, create e distrutte per ogni build.
- Limite: **massimo 2 build contemporanee** per via del peso delle immagini.
- Le immagini Windows (Server Core 2019 + Allianz tools) arrivano a **20–25 GB**.

---

### 📜 DockerBuild.groovy – Funzionamento

#### 🔍 Selezione dell’agent

- Il label dell’agent viene scelto dinamicamente tramite:

```
utils.getImageOS()  
```

- Il metodo analizza il nome della repository (se contiene "windows" o "linux").

#### ⚙️ Options

- Per Windows viene usato `skipDefaultCheckout` a causa di problemi nel clone automatico.

---

## 🧱 Stage della Pipeline

### 1. **Clone Git Repository**

- Eseguito **solo per Windows**
- Legato all’opzione `skipDefaultCheckout`

### 2. **Pull Golden Image**

- Eseguito **solo per Linux**
- Le EC2 Windows usano una AMI che contiene già la Golden Image → niente pull

### 3. **Workspace Preparation**

- Recupera i file dalla **content share**:
    
    ```
    configuration/${env}/${app_name}
    ```
    
- Questi file sono referenziati nei Dockerfile

### 4. **Build Docker Image**

- Costruzione dell’immagine
- Step:
    - `SetBuildArguments`
    - `docker build`
- Per Windows, rimozione del path `.src`

### 5. **Push Docker Image to ECR Registry**

- Push dell’immagine su ECR per ogni ambiente
- Tag usato:
  ```
   ${currentDate}-${BuildNumber}
   ```

### 6. **Push to DR ECR Registry**

- Eseguito **solo in produzione**
- Push dell’immagine anche sul registry di Disaster Recovery

### 7. **Clean Local Built Image**

- Pulizia dell’immagine dal nodo
- Utile anche su EC2 effimere, che possono gestire più pipeline

### 8. **Deploy**

- Richiama la pipeline di deploy
- Recupera la folder del job con `getJobFolder`
- Esegue la build del job di deploy

### 9. **Additional Deploy**

- Deploy aggiuntivo per alcuni servizi di Motor (es. Auto, AutoSEM)
- Serve per deployare l’immagine **Previvas**

---
## 📌 Considerazioni Finali

- La pipeline è ottimizzata per gestire le differenze tra OS e ambienti.
- Le EC2 Windows sono lente e pesanti, quindi si usano strategie dedicate.
- La struttura modulare (Shared Library + Jenkinsfile) permette riuso e manutenzione centralizzata.

## 🚀 Pipeline di Deploy su Kubernetes

### 🔧 Contesto generale

- La pipeline di deploy è **collegata** a quella di build.
- L'immagine da deployare viene **passata come parametro** (`imageTag`) dalla pipeline di build.
- Non è necessario selezionare il nodo in base al sistema operativo (come nella build): il deploy avviene tramite comandi `kustomize`.

---

### 🧠 Selezione degli agent

- Vengono utilizzati **3 agent** forniti da Central, uno per ciascun ambiente (test, preprod, prod).
- Ogni agent è associato all’ambiente di destinazione e viene utilizzato per:
    - eseguire `kustomize build`
    - applicare la configurazione con `kubectl apply`

---

### 🧪 Validazione del tag immagine

- Lo **stage preliminare** serve a validare il tag dell’immagine.
- Utile per gestire deploy graduali, ad esempio:
    - Applicazioni con molti pod (es. Motor con 40 pod in produzione).
    - Durante il giorno, il deploy è **graduale** (i pod vengono aggiornati uno alla volta).
    - Fuori dalle business hours, i pod vengono **scalati a zero** e rialzati tutti insieme (più veloce).

---

### ⏰ Gestione orari e timeout

- Le **Business Hours** sono in UTC (es. 18:51 UTC).
- Vanno aggiornate manualmente in caso di cambio orario (es. ottobre).
- Fuori orario:
    - Tutti i pod vengono scalati a zero con il metodo `scaleToZero`.
    - Il restart è più veloce perché non avviene un rollout graduale.

---

### 🔄 Wait Rollout

- Comando usato: `kubectl rollout status`
- Il sistema attende che il rollout sia completato.
- Timeout:
    - **20 minuti** per test/preprod
    - **60 minuti** per prod
- Se il timeout viene superato:
    - La pipeline termina in errore.
    - È necessario **verificare manualmente** sul cluster se i pod sono saliti.
    - Possibile **falso positivo**: errore segnalato ma deploy riuscito.

---

## 🔁 Pipeline di Restart

### 🎯 Obiettivo

- Riavvia tutte le applicazioni in test e preprod.
- Riavvia **solo le applicazioni Linux** in produzione.

### 🧠 Logica di funzionamento

- Controlla se il restart va **skippato**.
- Verifica il sistema operativo dell’immagine.
- In base al tipo di applicazione:
    - Linux → `restartDeployment`
    - Windows → `restartStatefulSet`

### 📌 Parametri

- Per Windows, si aspetta `deploymentName`.
- Se non presente, viene impostato come stringa vuota.
- Stessa logica per lo `statefulSetName`.

### ⏱️ Timeout

- Timeout di **20 minuti** anche per il restart.
- I metodi `restartDeployment` e `restartStatefulSet` usano `kubectl rollout restart` e attendono il completamento.

---

## 📁 Comandi principali usati

- `kubectl rollout restart`
- `kubectl rollout status`
- `kubectl apply -k`
- `kubectl scale --replicas=0`

---



### 1. **Differenze tra Build e Deploy**

Nel processo di **build**, è necessario selezionare il nodo su cui eseguire la build dell’immagine Docker, in base al sistema operativo:

- Immagini **Linux** → nodo Linux
- Immagini **Windows** → nodo Windows

Questo perché la build deve essere compatibile con l’OS dell’immagine.

Nel **deploy**, invece, questa selezione non è necessaria. Non si costruisce nulla, ma si applicano manifest tramite `kustomize` e `kubectl`. Il deploy è quindi **agnostico rispetto al sistema operativo**, e si basa su agent preconfigurati.

---

### 2. **Utilizzo degli Agent Central**

Central mette a disposizione **tre agent**:

- Uno per **test**
- Uno per **preprod**
- Uno per **prod**

Questi agent sono utilizzati per:

- Eseguire `kustomize build`
- Applicare i manifest con `kubectl apply`

La pipeline fa riferimento a questi agent in base all’ambiente target, senza dover gestire direttamente la selezione del nodo.

---

### 3. **Passaggio del Tag dell’Immagine**

La pipeline di deploy riceve come **parametro in ingresso** il tag dell’immagine da deployare (`imageTag`), generato nella pipeline di build.

Questo parametro viene validato in uno **stage preliminare**, utile per:

- Verificare che il tag sia corretto
- Preparare il deploy graduale (se previsto)

---

### 4. **Deploy Graduale vs Deploy Completo**

Durante le **business hours**, il deploy è **graduale**:

- I pod vengono aggiornati uno alla volta
- Utile per applicazioni con molti pod (es. Motor con 40 pod)

Fuori dalle business hours:

- I pod vengono **scalati a zero** con il metodo `scaleToZero`
- Poi vengono rialzati tutti insieme
- Questo approccio è **più veloce**, ma meno controllato

---

### 5. **Gestione delle Business Hours**

Gli orari sono gestiti in **UTC**, non nella timezone locale:

- Es. 18:51 UTC → corrisponde a 20:51 in Italia (quando c’è l’ora legale)
- Se cambia l’ora (es. in ottobre), gli orari vanno **aggiornati manualmente**

È in programma una **parametrizzazione più comoda** per evitare modifiche manuali.

---

### 6. **Wait Rollout – Controllo dello Stato**

Dopo il deploy, viene eseguito il comando:

Shell

kubectl rollout status  

Show more lines

Questo comando verifica se il rollout è stato completato correttamente. Il controllo è ciclico:

- Continua a ciclare finché non riceve una risposta positiva
- Si ferma se riceve una delle stringhe di successo
- Ha un **timeout**:
    - **20 minuti** per test/preprod
    - **60 minuti** per prod

Se il timeout viene superato:

- La pipeline termina con **errore**
- Ma non è detto che il deploy sia fallito → può essere un **falso positivo**
- In quel caso, bisogna **verificare manualmente** sul cluster se i pod sono saliti

---

### 7. **Effetti sullo Step di Build**

Se il deploy fallisce (anche per timeout), l’errore viene **propagato** alla pipeline di build:

- Lo step finale della build risulta fallito
- Anche se il deploy è andato a buon fine
- Serve quindi un controllo manuale per evitare falsi allarmi

---

## 🔁 Pipeline di Restart – Approfondimento

### 1. **Funzione della Pipeline**

Questa pipeline serve a:

- Riavviare **tutte le applicazioni** in test e preprod
- Riavviare **solo le applicazioni Linux** in produzione

---

### 2. **Logica di Controllo**

La pipeline:

- Verifica se il restart deve essere **skippato**
- Controlla il sistema operativo dell’immagine
- In base al tipo di applicazione:
    - Linux → `restartDeployment`
    - Windows → `restartStatefulSet`

---

### 3. **Gestione dei Parametri**

Per distinguere tra deployment e statefulset:

- Se l’app è Windows, si aspetta `deploymentName`
- Se non è presente, viene impostato come stringa vuota
- Stessa logica per `statefulSetName`

---

### 4. **Comandi e Timeout**

I metodi `restartDeployment` e `restartStatefulSet` eseguono:

Shell

kubectl rollout restart  

Show more lines

Poi attendono il completamento del restart, con lo stesso timeout del deploy:

- **20 minuti** per tutti gli ambienti

---

## 📌 Comandi Kubernetes Utilizzati

- `kubectl apply -k` → applicazione dei manifest
- `kubectl rollout restart` → riavvio dei pod
- `kubectl rollout status` → verifica dello stato del rollout
- `kubectl scale --replicas=0` → scale to zero