
## 📌 Cos'è una Golden Image
Una **Golden Image** è un'immagine Docker base costruita internamente a partire da immagini pubbliche (Windows o Linux), su cui vengono installati:
- Middleware come JBoss o Tomcat.
- Componenti e tool comuni a tutti gli applicativi.

Le Golden Image rappresentano lo **strato di base** su cui si appoggiano tutte le build successive delle applicazioni.

---

## 🧬 Tipologie di Golden Image

### 🔹 Linux
- Varianti principali:
  - `jboss`
  - `tomcat`
- Struttura identica tra le due.

### 🔹 Windows
- Struttura più articolata, include:
  - **Fluentbit** → cartella dedicata per la build del sidecar.  
  - **Initcontainer** → installazione del OneAgent di Dynatrace.  
  - **layers/** → cartelle per build in 4 step:
    1. Installazione ASP.NET
    2. Inizializzazione Db2
    3. Finalizzazione Db2
    4. Installazione tool Allianz

Le immagini Windows sono molto pesanti (20–25 GB).

---

## 🏗️ Jenkins e Shared Library

- Ogni repository Golden Image contiene un `Jenkinsfile`.
- Utilizza funzioni della **Shared Library Jenkins**.
- La pipeline seleziona dinamicamente l’agent tramite:
  ```groovy
  utils.getImageOS()
  ```
- Per Windows → `skipDefaultCheckout` (per evitare errori clone).

---

## 🧱 Stage della Pipeline di Build

1. **Clone Git Repository**  
   - Solo per Windows (per via del `skipDefaultCheckout`).

2. **Pull Golden Image**  
   - Solo per Linux.
   - Le EC2 Windows usano una AMI che contiene già la Golden Image.

3. **Workspace Preparation**  
   - Recupera file da `configuration/${env}/${app_name}`.

4. **Build Docker Image**  
   - `SetBuildArguments` + `docker build`.
   - Per Windows → rimozione path `.src`.

5. **Push Docker Image to ECR**  
   - Tag immagine: `${currentDate}-${BuildNumber}`.

6. **Push to DR ECR Registry**  
   - Solo in produzione.

7. **Clean Local Built Image**  
   - Pulizia per ottimizzare risorse su EC2 effimere.

8. **Deploy**  
   - Richiamo della pipeline di deploy.  
   - Recupera job folder con `getJobFolder`.

9. **Additional Deploy**  
   - Deploy extra per alcuni servizi (es. Motor Auto, AutoSEM).

---

## ☁️ Infrastruttura di Build

### Linux
- Build eseguita tramite bastion host.

### Windows
- Build su macchine EC2 **effimere**.
- Limite: max 2 build contemporanee (immagini pesanti).

---

## 🚀 Deploy su Kubernetes

- La pipeline di deploy è collegata a quella di build.
- L’immagine da deployare viene passata come parametro `imageTag`.
- Deploy agnostico rispetto all’OS.

### Agent Central
- 3 agent preconfigurati: test, preprod, prod.
- Utilizzati per `kustomize build` e `kubectl apply`.

---

## ⏳ Deploy Graduale vs Completo

- **Business Hours** → deploy graduale (pod aggiornati uno alla volta).  
- **Fuori orario** → scale to zero + restart completo (più veloce).

Timeout rollout:
- 20 minuti per test/preprod
- 60 minuti per prod

---

## 🧪 Validazione e Controllo

- Stage preliminare per validare `imageTag`.
- Evita deploy errati e consente rollout controllato per app con molti pod.

---

## 🧹 Pulizia e Manutenzione

- Le EC2 Windows vengono create e distrutte per ogni build.
- Le immagini locali vengono pulite dopo il push.
- Strategia per ottimizzare spazio e performance build.

---

📄 **Riferimenti nei tuoi appunti**:  
- Video 6 → sezioni “Build delle Golden Image”, “Pipeline Jenkins”, “Deploy e agent centralizzati”
