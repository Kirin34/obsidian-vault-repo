
## 📌 Cos'è Amazon ElastiCache?

Amazon ElastiCache è un **servizio AWS completamente gestito** che consente di eseguire e gestire **database in-memory**, ovvero archivi di dati che risiedono interamente nella **memoria RAM** invece che su disco.


> [!NOTE] Esempio:
> Immagina di avere una **grande biblioteca piena di libri** (i tuoi dati), ma ogni volta che vuoi leggerne uno, devi andare in un **magazzino lontano** (database tradizionale). Questo richiede tempo. 
> ElastiCache è come avere **uno scaffale veloce accanto a te** con i libri più richiesti:
> - Se il libro è sullo scaffale → lo prendi subito.
> - Se non c’è → lo prendi dal magazzino e lo metti sullo scaffale per la prossima volta.
   Più persone chiedono lo stesso libro → più veloce sarà ottenerlo!

### ✅ Vantaggi principali
- **Velocità**: L'accesso ai dati è molto più rapido rispetto ai database tradizionali.
- **Bassa latenza**: Ideale per applicazioni che richiedono risposte immediate.
- **Gestione automatica**: AWS si occupa di tutto (scalabilità, backup, patch, recupero da errori).

---

## 🧠 Tecnologie supportate

ElastiCache supporta due motori principali:
- **Redis**
- **Memcached**

> 🔍 Se vedi domande su Redis, Memcached o database in-memory, pensa subito a **ElastiCache** come soluzione.

---

## 🚀 Quando usare ElastiCache?

### 1. Applicazioni a bassa latenza
Esempio: **Classifiche nei videogiochi**
- Gli utenti inviano e ricevono punteggi in tempo reale.
- Serve una risposta **istantanea** e **frequente** → ElastiCache è perfetto.

### 2. Caching dei dati
Esempio: **Siti web ad alto traffico**
- ElastiCache può **memorizzare in cache** le richieste frequenti al database.
- Se il dato è già in cache → risposta immediata.
- Se non è in cache → lo prende dal database, lo salva in cache per la prossima volta.

> Questo riduce il carico sul database e **accelera i tempi di risposta** del sito/app.


---

## 📝 Riepilogo per l'esame

- ✅ Servizio AWS per **database in-memory**
- 🔧 Supporta **Redis** e **Memcached**
- ⚡ Veloce e a **bassa latenza**
- 🔄 Gestione automatica da AWS
- 🎯 Use case:
  - Classifiche videogiochi (real-time)
  - Caching dati frequenti (siti web, app)
  - Riduzione del carico sul database
  - Miglioramento delle performance