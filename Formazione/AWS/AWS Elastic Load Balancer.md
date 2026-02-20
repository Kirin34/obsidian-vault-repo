# 🧭 Cos'è un Load Balancer

Un **Load Balancer** (bilanciatore di carico) è un dispositivo fisico o virtuale che distribuisce il traffico di rete e i carichi di lavoro tra più server per:

- Ottimizzare l'utilizzo delle risorse
- Migliorare la disponibilità delle applicazioni
- Garantire un'esperienza utente affidabile

Agisce come punto di contatto unico per i client, reindirizzando le richieste ai server backend disponibili e performanti. Può anche rilevare server non funzionanti per evitare interruzioni del servizio.

---
## ⚙️ Funzionamento

- **Distribuzione del traffico**: riceve tutte le richieste in entrata dai client e le distribuisce tra un gruppo di server (backend)
- **Controllo di integrità**: monitora continuamente lo stato dei server backend, escludendo quelli non funzionanti o sovraccarichi
- **Ottimizzazione delle risorse**: instrada le richieste al server più adatto in quel momento
- **Scalabilità**: consente di aggiungere o rimuovere server dal pool in base al traffico

---
## 🧱 Tipologie di Load Balancer

### 🔹 Hardware
- Dispositivi fisici installati in loco (on-premise)
### 🔹 Software
- Applicazioni installate su server dedicati o fornite come servizio da un provider cloud

---
## ✅ Vantaggi Principali

- **Disponibilità**: garantisce accesso continuo all'applicazione anche in caso di guasto
- **Scalabilità**: adatta le risorse in base alla domanda
- **Performance**: ottimizza il carico di lavoro e i tempi di risposta
- **Sicurezza**: può integrare firewall e crittografia per protezione da attacchi (es. DDoS)

---
# ☁️ Tipi di Load Balancer in AWS

AWS offre **4 tipi** di Load Balancer:
## 1. 🧠 Application Load Balancer (ALB)

- **Livello OSI**: Layer 7
- **Porte supportate**: 80 (HTTP), 443 (HTTPS e gRPC)
- **Protocolli**: HTTP, HTTPS, gRPC
- **SSL Termination**: installazione certificati SSL sul load balancer
- **Integrazione**: Amazon Cognito e OpenID Connect
- **Supporto Lambda**: può reindirizzare le chiamate a Lambda Functions

  
---
## 2. ⚡ Network Load Balancer (NLB)

- **Livello OSI**: Layer 4
- **Porte supportate**: tutte
- **Protocolli**: TCP, UDP, TLS
- **SSL Termination**: supportata

---
## 3. 🔐 Gateway Load Balancer (GWLB)

Il **Gateway Load Balancer** trasforma strumenti di sicurezza (es. firewall) in soluzioni scalabili e ad alta disponibilità.
### 🔄 Funzionamento

1. Riceve tutto il traffico di rete (in entrata e uscita)
2. Lo inoltra a un'appliance di sicurezza (es. firewall virtuale)
3. Il firewall ispeziona i pacchetti
4. Il GWLB bilancia il carico e protegge:
   - Avvia più istanze del firewall se il traffico aumenta
   - Reindirizza il traffico a istanze sane in caso di guasto
1. Rispedisce il pacchetto alla destinazione finale

- **Livello OSI**: Layer 3 (rete) e Layer 4 (trasporto)
- **Protocolli**: TCP/UDP

---
## 4. 🏛️ Classic Load Balancer (CLB)

- **Livello OSI**: Layer 4/7
- **Protocolli**: TCP, SSL/TLS, HTTP, HTTPS
- **Note**: obsoleto, usato solo con EC2-Classic instances

