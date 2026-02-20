IT UAV è un team , è presente su Github enterprise e ci sono molte repository, ci sono anche gli applicativi

Giro 

Jenkins -> Build -> Deploy su Nexus

I metodi di build di questa repo sono diversi rispetto a quelli di Cloudification, mentre di la si utilizzano gli slave, qui si utilizzano direttamente gli agent Kubernetes, lo fa tramite BuildKit di Kubernetes e utilizza il suo container Engine

Jenkins shared library prettamente proprietario, diversa da quella di cloudification

adp-toolchain-configuration, ha solo una leggera differenza, nella cartella Image Builder ha solo buildkit-custom.yml e registries.yml dove sono definiti tutti i registry

Il file che riguarda l'IaC del nostro repository si chiama cloudification.yml

Per kustomize -> repository AZtech-linux

creditasweb -> nginx con contenuti statici

fluent-bit - > sidecar container

uav-haproxy -> - È stato creato un **deployment HAProxy** dedicato.
- All’interno c’è un **StatefulSet** con configurazione HAProxy:
    - Gestisce **cookie di persistenza**.
    - Fa routing verso i **Service** dei workload.
- È stato definito un **Ingress specifico solo per questo StatefulSet**.
- Gli altri workload nel cluster hanno **solo Service**, senza Ingress.

- Il traffico viene gestito correttamente da HAProxy.
- La persistenza è garantita tramite cookie.
- Il routing funziona: Ingress → HAProxy → Service → Pod.


## 🧩 **Contesto Tecnico**

- Il cluster è **condiviso** tra più team (es. Allianz) e ha una configurazione **molto restrittiva**.
- Usa **Istio come ingress controller**, con limitazioni su namespace, risorse e accessi.
- Per comunicare verso l’esterno o tra servizi, servono **aperture specifiche**:
    - **Firewall**
    - **NetworkPolicy**
    - **ServiceEntry**

---

## 🔄 **Problema iniziale**

- Le chiamate verso l’**Ingress** non arrivavano correttamente ai pod.
- Senza l’annotazione `service-upstream`, il traffico non veniva instradato.
- Inoltre, **l’affinità (sticky session)** non funzionava, causando problemi di persistenza.

---

## 🛠️ **Soluzione con HAProxy**

- È stato creato un **StatefulSet con HAProxy** dedicato solo a un workload specifico (es. Frontend).
- HAProxy gestisce:
    - **Routing verso i Service**
    - **Persistenza tramite cookie**
    - **DNS statico** puntato a `CoreDNS` per risolvere correttamente i nomi interni.

---

## 🍪 **Gestione dei Cookie**

- Per il Frontend, HAProxy usa **cookie statici** per garantire la persistenza.
- Questo è necessario perché il browser usato dalla banca (probabilmente sotto **Citrix o CyberArk**) **non accetta cookie dinamici**.
- Negli altri casi, si usa un **cookie dinamico** basato su IP, destinazione e nome.

---

## 🧼 **Pulizia degli URL**

- La banca, per qualche motivo, **raddoppia parti dell’URL** nelle chiamate.
- HAProxy usa una **regex** per intercettare e correggere questi pattern duplicati, evitando errori.

---

## 📦 **Routing e Backend**

- HAProxy legge gli ingress e, in base alle condizioni (es. URL richiesto), instrada verso il backend corretto.
- Ogni backend è definito staticamente, perché la configurazione dinamica non ha funzionato.
- Anche se ci sono più backend, HAProxy li gestisce senza problemi.

---

## ✅ **Risultato**

- Il traffico viene gestito correttamente.
- La persistenza è garantita dove serve.
- Le chiamate della banca non causano errori.
- Il DNS interno è stabile grazie alla configurazione fissa su CoreDNS.