### **Cos'è Karpenter?**

È un componente che **crea automaticamente i nodi EC2** quando ci sono pod che non trovano spazio per essere eseguiti.

---

### 🔍 **Cosa fa esattamente?**

1. **Guarda i pod pending** (in attesa).
2. **Capisce quante risorse servono** (CPU, RAM).
3. **Crea nuovi nodi** solo se servono davvero.
4. **Distribuisce i pod** in modo intelligente per **usare meno nodi possibile**.

---

### ⚖️ **Differenza con Auto Scaling Group (ASG)**

- **ASG**: tu imposti quanti nodi vuoi (min, max, desired).
- **Karpenter**: decide lui **quanti e quali nodi servono**, in base ai pod.
- Karpenter è **più flessibile e ottimizzato**.

---

### 🧱 **Componenti principali**

- **NodePool**: definisce le regole (es. tipo OS, istanza, limiti CPU/RAM).
- **NodeClass**: come un launch template AWS (AMI, disco, SG, subnet, ecc.).

---

### 🧠 **Consolidamento**

- Di notte (es. 21:00–07:00), Karpenter può:
    - Spostare i pod tra nodi.
    - **Spegnere i nodi vuoti o poco usati**.
    - Lo fa **poco alla volta** (max 40% dei nodi per volta) per non creare disservizi.

---

### ✅ **Vantaggi di Karpenter**

- Più **intelligente** e **dinamico**.
- Riduce i **costi**.
- Migliora l’**efficienza** del cluster.
- Si adatta meglio a carichi variabili.

---


### 🔧 **Cosa fa Karpenter nel tuo cluster**

- È un componente Kubernetes **installato di default**.
- Serve per **schedulare i pod** sui nodi (worker nodes).
- Analizza la **capacità dei nodi** e le **richieste dei pod**.
- Decide **dove piazzare i pod** in modo da **ottimizzare le risorse**.

---

### 🔁 **Karpenter vs Auto Scaling Group (ASG)**

- Entrambi **creano nodi EC2** quando servono.
- **ASG** lavora con un numero minimo, massimo e desired di nodi.
- **Karpenter** lavora invece su **limiti di risorse** (es. max 1000 CPU, 8000 GB RAM).
- Karpenter può anche **ottimizzare i nodi esistenti**, non solo crearne di nuovi.

---

### 🧱 **NodePool e NodeClass**

- **NodePool**: definisce i gruppi di nodi (es. Linux, Windows, ecc.) e le subnet su cui lavorano.
- **NodeClass**: è come un launch template AWS, dove definisci:
    - AMI
    - Tipo istanza (es. `c7i.4xlarge`)
    - Disco, subnet, security group, tag, user data, ecc.

---

### 🧠 **Consolidamento**

- Karpenter può **spostare i pod** da un nodo all’altro per **spegnere i nodi sottoutilizzati**.
- Questo succede **solo fuori orario lavorativo** (es. dalle 21:00 alle 07:00).
- Può agire **su massimo il 40% dei nodi alla volta** per evitare disservizi.
- Esempio: se hai 10 nodi, ne può ottimizzare al massimo 4 per volta.

---

### 🌙 **Pipeline notturna**

- Di notte parte una pipeline che:
    - **Scala verso il basso** le repliche delle app Windows (es. da 38 a 4).
    - Al mattino le **riporta al numero originale**.
- Questo serve per **risparmiare sui costi**.
- Le app Linux non vengono toccate perché hanno pochi nodi e poco impatto.

---
### ✅ **In sintesi**

- Karpenter **decide in autonomia** come e quando creare o ottimizzare i nodi.
- È più **flessibile** rispetto agli ASG.
- Ti aiuta a **ridurre i costi** e a **gestire meglio le risorse**.
- La configurazione è fatta tramite oggetti Kubernetes (`NodePool`, `NodeClass`) e policy di consolidamento.
