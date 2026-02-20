### 🔹 Cos’è NoSQL?

**NoSQL** (che significa "Not Only SQL") è una **categoria di database** che non usa il classico modello relazionale basato su tabelle e righe, come i database SQL (es. MySQL, PostgreSQL).

Invece, i database NoSQL **memorizzano i dati in modo più flessibile**, ad esempio:

- Come **documenti** (tipo JSON) → es. DynamoDB, MongoDB
- Come **chiave-valore** → es. Redis
- Come **grafi** → es. Neo4j
- Come **colonne** → es. Cassandra

---

### 🔹 Caratteristiche principali

- ✅ **Flessibilità**: ogni record può avere attributi diversi.
- ⚡ **Alta scalabilità**: ottimo per gestire grandi volumi di dati e traffico.
- 🚀 **Prestazioni elevate**: ideale per applicazioni moderne e distribuite.
- 🔄 **Schema dinamico**: non serve definire una struttura fissa prima di inserire i dati.

---

### 🔹 Quando usare NoSQL?

- Quando hai **dati non strutturati o semi-strutturati**.
- Quando serve **velocità e scalabilità**, ad esempio in app web, mobile, IoT.
- Quando il modello relazionale è troppo rigido per il tipo di dati.

### 🔹 Esempio semplice

Immagina di voler salvare informazioni su diversi tipi di giocattoli:

- Una **macchina**: `{ "id": 1, "tipo": "macchina", "colore": "rosso", "velocità": 120 }`
- Una **bambola**: `{ "id": 2, "tipo": "bambola", "nome": "Anna", "altezza": 30 }`

In un database NoSQL come DynamoDB, **puoi salvare entrambi senza problemi**, anche se hanno attributi diversi.