## Cos'è Amazon DynamoDB?

È un database [[NoSQL]] Gestito da AWS. In poche parole, Amazon si cura di tutto (Infrastruttura,software ecc), quindi a noi tocca solo utilizzarlo, senza occuparci di gestirlo o del database in sè.


> [!NOTE] Esempio:
> Immagina di avere una scatola piena di giocattoli. Ogni giocattolo può avere caratteristiche diverse: uno potrebbe essere una macchina con un colore e una velocità, mentre un altro potrebbe essere una bambola con un nome e un'altezza.
  In **DynamoDB**, puoi memorizzare questi giocattoli (chiamati _item_) con le loro caratteristiche uniche (chiamate _attributi_) **senza dover seguire un formato rigido**.
Questa flessibilità permette a DynamoDB di essere **molto veloce e scalabile**, cioè può gestire grandi quantità di dati e molti utenti contemporaneamente **senza rallentamenti**.
### Differenze tra DynamoDB e RDS

- **DynamoDB** è un database **NoSQL**, ideale per applicazioni che richiedono **alta scalabilità e prestazioni**.
- **Amazon RDS** è un servizio per database **relazionali** (SQL), come MySQL, PostgreSQL, ecc.
- Non puoi sostituire un database relazionale con uno NoSQL senza **riscrivere l’applicazione**, perché i modelli di dati sono diversi.

###  Come sono strutturati i dati in DynamoDB?

- Gli elementi (items) sono simili a **oggetti JSON**.
- Ogni attributo ha un tipo:
    - `S` = stringa
    - `N` = numero
    - `L` = lista
- L’**ID** è la chiave primaria, usata per cercare l’elemento.
  ESEMPIO:
```
{
  "ID": { "S": "204" },
  "Titolo": { "S": "Bicicletta" },
  "Prezzo": { "N": "299.99" },
  "Categorie": { "L": [ { "S": "Sport" }, { "S": "Outdoor" } ] },
  "Disponibile": { "BOOL": true }
}
```

In DynamoDB, non tutti gli item devono avere gli stessi attributi ed è questo che lo rende così flessibile.
### Prestazioni e configurazioni

- DynamoDB è **molto veloce e scalabile**.
- Puoi **ottimizzare le prestazioni o i costi**:
    - Produzione → impostazioni più performanti (es. throughput provisionato).
    - Test/pre-produzione → impostazioni più economiche.

### Limiti nella ricerca dei dati

- Non puoi cercare facilmente su tutti gli attributi.
- Puoi creare **indici secondari** (es. per categoria prodotto) per facilitare alcune ricerche.
- Questo è diverso dai database relazionali, dove puoi fare query complesse su più colonne.


###  DynamoDB Global Tables

- Le **Global Tables** permettono di **replicare automaticamente i dati in più regioni**.
- AWS gestisce tutto: la replica è **veloce (sotto il secondo)** e **affidabile**.
- È una funzionalità reale e importante da ricordare per l’esame.


