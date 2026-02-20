# Introduzione
## Cos'è una Network?
 
**Una rete (NETWORK)** è un insieme di entità interconnesse (dispositivi, persone, organizzazioni) che comunicano e condividono risorse, dati o informazioni, basandosi su regole comuni chiamate **protocolli di rete**.

_Una rete deve avere queste capacità:_

1. **Alta larghezza di banda**: trasferire grandi quantità di dati in poco tempo.
2. **Bassa latenza**: il tempo di risposta tra due nodi deve essere minimo.
3. **Alta disponibilità**: deve essere sempre operativa, senza interruzioni.
4. **Scalabilità**: deve essere possibile aggiungere nuovi componenti senza perdere prestazioni.

**Componenti principali**:

- **End nodes**: dispositivi che generano o ricevono dati (_server, PC, storage_).
- **Intermediate nodes**: dispositivi che instradano il traffico (_switch, router_).

## Come si forma una rete?

Per formare una rete, abbiamo bisogno di:
- Due End nodes;
- Un intermediate Node.
#### ESEMPIO:

![[Pasted image 20251222183657.png]]
- **Ogni end node** (es. PC, server) ha una **NIC (Network Interface Card)**.
    
    - La NIC è il componente hardware che permette al dispositivo di **interfacciarsi con la rete**.
    - Ha una porta di rete dove si collega il cavo Ethernet.
- **Connessione fisica**:
- 
    - Il cavo Ethernet collega la porta della NIC al **switch**.
    - Lo **switch** è il dispositivo che **instrada il traffico** tra i nodi collegati, permettendo loro di comunicare.
- **Comunicazione logica**:
    
    - Perché i due nodi possano scambiarsi dati, devono usare **la stessa suite di protocolli di comunicazione** (es. TCP/IP).
    - Questi protocolli definiscono le regole per inviare, ricevere e interpretare i dati.

## Protocol Suite

La comunicazione tra i nodi richiede l'interazione tra una serie di protocolli, dove ognuno è responsabile di uno specifico set di attività.


> [!NOTE] Esempio:
> I due nodi, per mandare messaggi tra di loro, devono implementare lo stesso protocollo di comunicazione, dove ogni protocollo è responsabile di una determinata serie di attività.


Ogni protocollo definisce un formato comune e un set di regolo per scambaire messaggi tra i terminali fisici.
- Setup e terminazione di sessione di trasmissione di dati;
- formato dei messaggi;
- Errore e messaggi di sistema.

Una suite di protocolli è un gruppo di protocolli che funzionano contemporaneamente per implementare la comunicazione di rete.
Le diverse suite di protocolli sono combinazioni differenti di protocolli utilizzati per vari tipi di comunicazione.

# Modello OSI

Considerando tutto il lavoro che una rete deve svolgere, è più semplice suddividere le varie funzionalità della comunicazione in **livelli**, per rendere la comunicazione più gestibile.  
Il **modello OSI (Open Systems Interconnection)** è uno standard ISO che descrive **7 livelli** (_Layer_)che i sistemi informatici utilizzano per comunicare su una rete.
