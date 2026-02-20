
## 📌 Contesto generale
L’accesso all’infrastruttura Kubernetes avviene tramite **Bastion Host** e viene regolato da richieste di accesso formali.  
Questa sezione riassume i flussi di accesso, la gestione degli alias e la struttura dei cluster.

---

## 🔐 Accesso al Cluster EKS

### 🧭 Bastion Host
- L’accesso al cluster avviene **esclusivamente tramite macchina bastion**.  
- Connessione tramite SSH utilizzando **PuTTY**.

### 📝 AVC GIAM
- Tutti gli accessi devono essere richiesti tramite **AVC GIAM**:
  - Bastion Host
  - Cluster EKS
  - Dynatrace
  - GitHub (`Cloudification-open-Systems`)
  - ServiceNOW

### 📍 Cluster EKS
- **Produzione** → Parigi  
- **Disaster Recovery (DR)** → Francoforte

---

## 🧭 Alias Utili

Per velocizzare le operazioni quotidiane sono stati creati alias personalizzati:
```bash
alias nome_alias='path script e/o comando'
alias kns='/k8s/kns.sh'
alias kl='kubectl logs'
```
- Consentono di eseguire comandi ricorrenti in modo più rapido e standardizzato.

---

## ☸️ Accesso e Controlli Iniziali

Dopo essere entrati nel bastion, si consiglia:
```bash
kubectl get pods --all
```
- Verifica dello stato generale dei pod su tutti i namespace.  
- Individuazione rapida di eventuali anomalie o pod down.

---

## 🧱 Struttura Infrastrutturale

- Ambiente multi-cluster (prod e DR).  
- Namespace condivisi → supportano app Windows e Linux nello stesso contesto.
- Architettura basata su:
  - Bastion host per accesso
  - Cluster EKS per orchestrazione
  - Dynatrace per osservabilità

---

## 🧰 Best Practice Operative

- Evitare modifiche dirette ai manifest in produzione → usare repository Kustomize.  
- Verificare sempre il namespace e l’ambiente prima di lanciare comandi distruttivi.  
- Aggiornare alias e script locali per mantenere standard operativi.  
- Coordinarsi con la sala macchine per restart pianificati.

---

📄 **Riferimenti nei tuoi appunti**:  
- Video 2 → Accesso EKS, AVC GIAM, Bastion, Alias  
- Video 3 → Comandi iniziali e alias operativi
