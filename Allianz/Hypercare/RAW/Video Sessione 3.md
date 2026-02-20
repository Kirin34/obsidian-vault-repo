
Creazione Alias per Kubernetes:

alias nome_alias='path script e/o comando'

esempio:

alias kns='/k8s/kns.sh'

alias kl ='kubectl logs'

fluent_bit è stato aggiunto anche su Linux per Apache Kafka

### 🔹 **Deployment vs StatefulSet**

#### ✅ **Deployment**

- I pod hanno nomi con suffissi casuali (es. `nome-replicaset-nomepod`)
- Gestiti da **ReplicaSet**, che controlla il numero di repliche.
- Se modifichi il deployment, viene creato un nuovo ReplicaSet.
- Lo scale-down è **casuale**: non si sa quale pod verrà eliminato.

#### ✅ **StatefulSet**

- I pod hanno nomi **indicizzati** (es. `nome-STS-0`, `nome-STS-1`, ...)
- Lo scale-down è **ordinato**: elimina prima il pod con indice più alto.
- Lo scale-up crea nuovi pod con indice successivo.

---

### 🔹 **ReplicaSet**

- È una risorsa Kubernetes che gestisce il numero di repliche di un deployment.
- Ogni modifica al deployment genera un nuovo ReplicaSet.

---

### 🔹 Comandi Utili Kubernetes
- Per vedere i pod:

```
    kubectl get pods -n <namespace>  #Mostra i pod presenti nel namespace
    kubectl get deployment -n <namespace> #Mostra lo stato dei deployment
    kubectl get statefulset -n <namespace> #Mostra lo stato degli statefulset
    kubectl logs -f <nome-pod> -n <namespace>  #mostra i log di un pod
    kubectl logs <nome-pod> -c <nome-container> -n <namespace>
    kubectl get pod -A | grep -E -v "1/1|2/2|3/3|4/4|5/5"
 
```


### 🔹 **Scaling**

- Per scalare uno StatefulSet:

```
    kubectl scale statefulset <nome-STS> --replicas=<numero> -n <namespace>      
```
		- Se il numero è uguale a quello attuale, non succede nulla.
		- Se aumenti, vengono creati nuovi pod.
		- Se diminuisci, vengono eliminati quelli con indice più alto.




 ## 🔹 **Concetti chiave**

- Un **Deployment** o **StatefulSet** gestisce **repliche di pod**.
- Ogni **pod** può contenere **uno o più container**.
- Le modifiche si fanno sul Deployment o StatefulSet, **non sui singoli pod**.


---

## ⚙️ **Modifica dei manifest YAML in Kubernetes**

### 🔧 **Modificare parametri come CPU, RAM, ecc.**

- È **possibile** modificare parametri come `resources.requests` e `resources.limits` (es. CPU e memoria).
- Tuttavia, **ogni modifica** a un **Deployment** o **StatefulSet** comporta:
    - **Riciclo dei pod**: quelli esistenti vengono **terminati** e ne vengono creati di nuovi con la nuova configurazione.
    - Kubernetes considera la modifica come una **nuova versione** della risorsa.

---
### ⚠️ **Attenzione in produzione**

- In **pre-produzione** è accettabile fare modifiche direttamente.
- In **produzione**, è **sconsigliato** fare modifiche manuali ai manifest direttamente nel cluster.
- Le modifiche dovrebbero essere fatte tramite i **template ufficiali** nel repository Git.

---

## 📁 **Gestione dei manifest con Kustomize**

### 🧰 **Cos'è Kustomize**

- È uno strumento per **templatizzare** le risorse Kubernetes.
- Permette di definire manifest YAML **modulari e riutilizzabili**.

### 📦 **Repository**

- Ogni applicazione ha **due repository principali**:
    
    1. **Applicativo** (es. `aztech-windows-anagrafe`)
    
    - Contiene pipeline Jenkins (`build`, `deploy`, `restart`, ecc.)
    - Cartelle per ogni container (es. `ccd`, `script`, `dockerfile`)
    
    1. **Kustomize** (es. `aztech-windows`)
    
    - Contiene i **template YAML** usati per generare i manifest.
    - Qui vanno fatte le **modifiche permanenti** (es. CPU, RAM, env vars, ecc.)

---

## 🔁 **Effetti delle modifiche**

### 🧪 **Modifica temporanea (test)**

- Può essere fatta direttamente nel cluster (`kubectl edit`).
- I pod vengono **ricreati** con la nuova configurazione.
- **Non è persistente**: al prossimo deploy, i manifest originali sovrascrivono la modifica.

### 🛠️ **Modifica permanente**

- Va fatta nel **template Kustomize** nel repository Git.
- Quando viene eseguita la pipeline di deploy:
    - I manifest vengono **rigenerati** con i nuovi parametri.
    - Le modifiche restano **persistenti**.

---
## 🚀 **Pipeline Jenkins**

- Le pipeline leggono i parametri dai file nel repository applicativo.
- Eseguono il deploy usando i manifest generati da Kustomize.
- Se non aggiorni Kustomize, le modifiche fatte manualmente vengono **perse**.

---


## 📁 Struttura del repository GitHub
  
Il repository è organizzato in tre cartelle principali:

- `cicd/`: contiene gli script Groovy che fanno riferimento alle **shared pipeline Jenkins**.
- `scripts/`: contiene gli script che vengono **eseguiti all’interno del container**.
- `Dockerfile`: definisce l’immagine del container
## ⚙️ Jenkins di Allianz 
Jenkins è **deployato come pod Kubernetes**. 
   - Le pipeline vengono gestite tramite il sistema **adp-toolchain**. 
   - Ogni volta che viene creato un progetto, il sistema genera: 
	   - Le **folder** per il progetto. 
	   - Le pipeline in base al nome della repository. 
	   - ### 📂 Esempio di naming pipeline 
		   - Per una repository chiamata `aztech-linux-nome_repo`, vengono generate pipeline come: 
			   - `build.groovy`
			   - `deploy.groovy` 
			   - `restart.groovy` 
			   - Questi file si trovano nella cartella `cicd/` e negli script si fa riferimento alle shared pipelines nella  **Shared Library di Jenkins**. 

--- 
## 🧠 Note aggiuntive 
- Le viste e le configurazioni di Jenkins vengono create automaticamente da `adp-toolchain`. - Ogni progetto ha una sua struttura dedicata, con pipeline e script associati.

lavorare in modo dev -> release -> preprod


