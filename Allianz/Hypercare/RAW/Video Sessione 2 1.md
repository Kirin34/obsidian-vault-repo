
## 🛡️ **Accesso a EKS e strumenti correlati**

### 🔐 **Accesso al cluster EKS**

- Si accede tramite una **macchina bastion**.
- Per ottenere l’accesso, bisogna fare **richiesta tramite AVC GIAM**.
- Si utilizza **PuTTY** per la connessione SSH.

### 🧾 **AVC GIAM**

- Serve per richiedere accessi a vari strumenti:
	- Macchina Bastion
    - EKS
    - Dynatrace
    - GitHub (es. `Cloudification-open-Systems` con progetti Allianz)
    - ServiceNOW

---

## ☸️ **Kubernetes – Operazioni base**

### 📍 **Cluster**

- **Produzione**: Parigi
- **Disaster Recovery (DR)**: Francoforte

### 🧭 **Namespace e alias**

- Sono stati creati **alias personalizzati** per semplificare i comandi Kubernetes.
- È possibile avere **applicazioni Windows e Linux nello stesso namespace**.

### 🔍 **Controllo iniziale**

- Primo comando da eseguire quando si entra nel cluster: Kubectl get pods --all Serve per verificare se qualche pod è **down**.

---

## 🐧 **Pod Linux**

### 📦 **Tipi di immagine**

- Hostate tramite:
    - **JBoss**
    - **Tomcat**

### 🔎 **Filtri**

- Per vedere solo le immagini Linux:
    
    --selector=middleware=jboss
    
    --selector=middleware=tomcat
    

---

## 🪟 **Pod Windows**

### 📦 **Identificazione**

- I pod Windows hanno **quasi sempre il suffisso `-prisma`**.

### 🧩 **AppPool**

- Tutte le applicazioni Windows vengono deployate come **AppPool**.
- Comandi utili:
    - Visualizzare AppPool: Get-IISAppPool
    - Riavviare un AppPool: Restart-AppPool <nome_app>
    - Avviare un AppPool fermo: Start-AppPool <nome_app>

### 📜 **Log di sistema**

- Visualizzare log: Get-EventLog
- Visualizzare ultimi restart: Get-EventLog -LogName System -Newest 10


### 🔎 **Filtri**

- Per vedere solo le immagini Windows:
    
    --selector=os=windows
    

---

## 📈 **Log applicativi e Dynatrace**

### 📁 **Percorso log**

WINDOWS:
	 I log si trovano in: C:\Logs\\\
	 File principale: `DebugTrace.log`
LINUX:
	 Kubectl logs;
### 📤 **Copia log dal bastion**

- Copia il file con: kubectl cp

### 🔄 **Fluentbit**

- È un **sidecar container** che:
    - Monitora la cartella dei log.
    - Invia i log a **Dynatrace**.

---

## 🚨 **Applicazioni critiche**

- **Motor**
- **Danni**
- **Anagrafe**

