## 📌 Contesto generale
- Jenkins è **deployato come pod Kubernetes**.  
- Le pipeline sono gestite tramite **adp-toolchain**, che crea automaticamente:
  - Le **folder** per il progetto.
  - Le pipeline in base al nome della repository.
  - Le viste dedicate per ambienti/applicazioni (Linux JBoss, Linux Tomcat, Windows HS).

---

## 🪜 Tipologie di Pipeline

- `build.groovy` → build immagine Docker  
- `deploy.groovy` → deploy su cluster EKS tramite Kustomize  
- `restart.groovy` → riavvio applicazioni  
- Pipeline di restart:
  - Windows: scale notturno
  - Linux: restart alle 05:00  
  - Schedulazione tramite cronjob.

📁 **Esempio naming pipeline**:  
per `aztech-linux-nome_repo` → `build.groovy`, `deploy.groovy`, `restart.groovy`.

---

## 🧱 Shared Library

- Tutti i Jenkinsfile (incluso quelli per Golden Image) si basano su metodi definiti nella Shared Library Jenkins.
- Le pipeline leggono i parametri dai file nei repository applicativi e **deployano con i manifest generati da Kustomize**.

---

## 🏗️ Jenkins e Golden Image

- I repository delle Golden Image contengono un `Jenkinsfile`.
- La pipeline utilizza `utils.getImageOS()` per selezionare dinamicamente l’agent (Windows/Linux).
- Per Windows è abilitato `skipDefaultCheckout` per evitare problemi di clone.

### Stage principali della pipeline di build:
1. Clone Git (solo Windows)  
2. Pull Golden Image (solo Linux)  
3. Workspace Preparation  
4. Build Docker Image  
5. Push ECR  
6. Push DR ECR (solo prod)  
7. Clean local image  
8. Deploy  
9. Additional Deploy (alcuni servizi Motor)

---

## 🚀 Pipeline di Deploy

- Deploy agnostico rispetto all’OS.
- Utilizza 3 agent centralizzati: test, preprod, prod.
- Deploy tramite `kustomize build` + `kubectl apply`.

### Deploy Graduale vs Completo
- Durante business hours → **graduale** (pod aggiornati uno alla volta).  
- Fuori orario → **scale to zero** + restart completo.

⏱️ Timeout:
- 20 min per test/preprod
- 60 min per prod

---

## 🔁 Pipeline di Restart

- Riavvia tutte le app in test e preprod.
- In produzione riavvia solo app Linux.
- Windows → `restartStatefulSet`  
- Linux → `restartDeployment`  
- Timeout 20 min.

---

## 📊 Monitoraggio e Notifiche

- In caso di errore in pipeline → notifica inviata alla **sala macchine Allianz**.  
- Log e troubleshooting vengono eseguiti su cluster (kubectl logs, pod status).

---

## 📎 Note aggiuntive

- Viste e configurazioni Jenkins create automaticamente da adp-toolchain.  
- Le modifiche manuali ai manifest sono temporanee e vengono sovrascritte se non riportate in Kustomize.  
- Naming e strutturazione pipeline fortemente standardizzati.

---

📄 **Riferimenti nei tuoi appunti**:  
- Video 1 → sez. “Jenkins – Pipeline e viste”  
- Video 3 → sez. “Pipeline Jenkins”  
- Video 6 → sezioni “Jenkins e Shared Library”, “Build Golden Image”, “Pipeline Deploy/Restart”
