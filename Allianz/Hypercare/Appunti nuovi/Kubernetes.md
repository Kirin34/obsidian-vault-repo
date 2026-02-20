# ☸️ Kubernetes 

## 📌 Contesto generale
- Accesso al cluster EKS tramite **macchina bastion** (richiesta tramite AVC GIAM).
- Connessione SSH con PuTTY.  
- Cluster:
  - Produzione → Parigi
  - Disaster Recovery → Francoforte
- Namespace condivisi: possono contenere applicazioni Windows e Linux.

---

## 🧭 Alias e Accesso Rapido

- Alias personalizzati per semplificare i comandi Kubernetes:
  ```bash
  alias nome_alias='path script e/o comando'
  alias kns='/k8s/kns.sh'
  alias kl='kubectl logs'
  ```

- Controllo iniziale cluster:
  ```bash
  kubectl get pods --all
  ```
  → Verifica se qualche pod è down.

---

## 🐧 Pod Linux

- Middleware usati:
  - JBoss
  - Tomcat
- Filtri per immagini Linux:
  ```bash
  --selector=middleware=jboss
  --selector=middleware=tomcat
  ```

## 🪟 Pod Windows

- Identificabili dal suffisso `-prisma`.
- Applicazioni deployate come **AppPool**:
  ```powershell
  Get-IISAppPool
  Restart-AppPool <nome_app>
  Start-AppPool <nome_app>
  ```

- Log di sistema:
  ```powershell
  Get-EventLog
  Get-EventLog -LogName System -Newest 10
  ```

- Filtri per immagini Windows:
  ```bash
  --selector=os=windows
  ```

---

## 📜 Log e Monitoraggio

- Log Linux:
  ```bash
  kubectl logs <nome-pod>
  ```

- Log Windows:
  `C:\Logs\DebugTrace.log`

- Copia log dal bastion:
  ```bash
  kubectl cp
  ```

- **Fluentbit** (sidecar container):
  - Monitora cartella log
  - Invia i log a Dynatrace

---

## 🧩 Deployment vs StatefulSet

### Deployment
- Pod con suffissi casuali
- Gestiti da ReplicaSet
- Scale-down casuale

### StatefulSet
- Pod con nomi indicizzati (`nome-STS-0`, `nome-STS-1`, ...)
- Scale-down ordinato
- Scale-up sequenziale

---

## 🔹 ReplicaSet

- Gestisce il numero di repliche di un deployment.
- Ogni modifica genera un nuovo ReplicaSet.

---

## 🛠️ Comandi Utili Kubernetes

```bash
kubectl get pods -n <namespace>
kubectl get deployment -n <namespace>
kubectl get statefulset -n <namespace>
kubectl logs -f <nome-pod> -n <namespace>
kubectl logs <nome-pod> -c <nome-container> -n <namespace>
kubectl get pod -A | grep -E -v "1/1|2/2|3/3|4/4|5/5"
```

### Scaling

```bash
kubectl scale statefulset <nome-STS> --replicas=<numero> -n <namespace>
```
- Se il numero non cambia → nessuna azione.
- Se aumenta → nuovi pod.
- Se diminuisce → elimina pod con indice più alto.

---

## 🧰 Modifica Risorse YAML

- Possibile modificare CPU, RAM e altri parametri in `resources.requests` e `resources.limits`.
- Ogni modifica comporta **riciclo dei pod**.

### Modifica temporanea
- `kubectl edit` → non persistente.

### Modifica permanente
- Aggiornare i template in Kustomize repo Git.

---

## 🧠 Kustomize – Gestione dei Manifest

- Templatizza risorse Kubernetes.
- Repository diviso in:
  - `Resources`: template base
  - `Apps`: customizzazioni app
  - `Components`: moduli riutilizzabili (es. FluentBit)

### Esempi di risorse base
- `ingress.yaml`: cookie affinity + patch per path/host
- `service.yaml`: espone porte (80/8080)
- `statefulset.yaml`: container app + FluentBit

### Processo di Deploy con Kustomize
```bash
kustomize build kustomize/${NOME_APP}/env/${environment_name} > app.yaml
```
- Imposta namespace
- Definisce immagine
- Aggiorna tag immagine per ogni build

---

## 🌐 Ingress

- **Ingress Haproxy** → traffico standard con affinity
- **Ingress Nginx** → cloudification e traffico separato
- Patch per URL e ingressClassName.

Header per targeting pod:
```
pod: mk-prisma-all-0
```

---

## 🏷️ Naming e Limiti Windows

- `namePrefix` usato per prefissare nomi risorse.
- Limitazione Windows hostname: max 15 caratteri.
- Uso di `disableSuffixHash` per evitare hash automatici.

---

## 🧠 Warm-Up

- ConfigMap `warmup` con script PowerShell per eseguire chiamate HTTP e caricare cache.

---

## 🚨 Applicazioni critiche
- Motor
- Danni
- Anagrafe

---

## 🧪 Deploy Graduale vs Completo

- Durante business hours → rollout graduale.
- Fuori orario → scale to zero + restart rapido.

Comandi principali:
```bash
kubectl apply -k
kubectl rollout restart
kubectl rollout status
kubectl scale --replicas=0
```

Timeout rollout:
- 20 min per test/preprod
- 60 min per prod

---

📄 **Riferimenti nei tuoi appunti**:  
- Video 2 → Accesso, Pod, Log, Fluentbit  
- Video 3 → Deployment vs StatefulSet, Scaling, Modifica manifest  
- Video 5 → Kustomize, ingress, naming, warmup  
- Video 6 → Deploy graduale/completo, rollout, scaling
