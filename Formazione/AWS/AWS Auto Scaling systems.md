# 🧠 Scaling in AWS

## 🚀 Quando abbiamo bisogno di scalare?

- Quando si verificano **picchi di traffico**, sia **prevedibili** che **imprevedibili**.
- Per **mantenere le prestazioni** durante i picchi.
- Per **ridurre i costi** nei periodi di bassa attività.

> ⚙️ [[Auto-scaling]] è il meccanismo che consente di adattare dinamicamente le risorse alla domanda.

---

## 🛠️ Tipi di Auto Scaling in AWS

### 🔹 Amazon EC2 Auto Scaling

- Supporta **solo Amazon EC2**
- Tipi di scaling:
  - [[Step Scaling]]
  - [[Scheduled Scaling]]
- Supporta:
  - **Multi-purchase model** (Reserved, Spot, On-Demand)
  - **Multi-AZ model**
  - **Multi-instance sizes** per una singola app

### 🔹 AWS Auto Scaling

- Supporta:
  - **Amazon EC2**
  - **Amazon ECS**
  - **Amazon DynamoDB**
  - **Amazon Aurora**
- Tipi di scaling:
  - [[Target Tracking Scaling]]
  - [[Predictive Scaling]]
- Funzionalità:
  - Crea e gestisce [[Triggering Scaling|CloudWatch Alarms]] per attivare lo scaling
  - **Scansione automatica** dei servizi scalabili (tramite tag o CloudFormation Stack)

> ❗ **Attenzione alle domande trabocchetto**:
> - ❌ [[Step Scaling]] **non** è disponibile in AWS Auto Scaling.
> - ❌ Amazon EC2 Auto Scaling **non** supporta Amazon ECS.

---

## 📦 Modelli di acquisto EC2

### 🟩 Reserved Instances

- Ideali per **traffico costante e prevedibile**
- Pagamento **anticipato** (parziale o totale)
- Durata: **1 o 3 anni**
- **Costo più basso**

### 🟨 On-Demand Instances

- Ideali per **picchi moderati**
- Paghi **solo per l’uso**
- Nessun impegno a lungo termine

### 🟦 Spot Instances

- Utilizzano **capacità inutilizzata** di AWS
- Prezzo **molto ridotto**
- Ideali per carichi **flessibili e non critici**
- Possono essere **interrotte da AWS** con breve preavviso

### 🔄 Strategia combinata

> 📌 Usa una combinazione per ottimizzare costi e prestazioni:
> - **Reserved** per il traffico base
> - **Spot** quando i prezzi sono bassi
> - **On-Demand** per gestire i picchi

---

## 📈 Tipi di Scaling

### 🔸 [[Step Scaling]]

> 🔧 Scala in **passaggi graduali** in base all’intensità del carico.

- Basato su **metriche** (es. CPU)
- Definisci **soglie multiple**

#### 📊 Esempio:

- CPU > 50% → +1 istanza
- CPU > 70% → +2 istanze
- CPU > 90% → +3 istanze

### 🔸 [[Scheduled Scaling]]

> 🔧 Scala in base a un **orario prestabilito**.

- Utile quando **conosci in anticipo** un picco di traffico

#### 📊 Esempio:

- Campagna pubblicitaria alle 16:00 → scaling programmato alle 15:00

### 🔸 [[Predictive Scaling]]

> 🔮 Prevede i picchi di traffico e **scala in anticipo**.

- Basato su **trend storici**
- Non serve raggiungere un target: il sistema **prepara le istanze prima**

---

## 🔍 Rilevamento automatico delle risorse scalabili

- AWS Auto Scaling può **scansionare automaticamente** il tuo account:
  - Tramite **tag**
  - Tramite **CloudFormation Stack**

> ✅ Utile per includere tutte le risorse scalabili **senza configurazioni manuali**
