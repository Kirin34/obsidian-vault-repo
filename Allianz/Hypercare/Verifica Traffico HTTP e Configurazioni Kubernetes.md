
## 📌 Obiettivo

Verificare:

- Configurazione **Ingress**, **Service**, **Deployment**.
- Presenza di **probe** (liveness/readiness).
- Eventuale **service mesh**.
- Cause di traffico su una porta (es. 8080).

---

## 🔍 1. **Verifica Ingress**

Verifica l'ingress tramite Visual studio code

---

##  2. **Verifica Service**

Mostra configurazione:


kubectl get svc nome-service -n namespace -o yaml  


Controlla:

port (porta esposta dal Service) 
TargetPort (porta del container)


## 🔍 3. **Verifica Deployment**

Controlla probe e container:

Shell

kubectl describe deploy nome-deploy -n namespace | grep -A3 Liveness  

kubectl describe deploy nome-deploy -n namespace | grep -A3 Readiness  

Mostra più linee

Oppure:

Shell

kubectl get deploy nome-deploy -n namespace -o yaml | grep -A10 probe  


## 🔍 4. **Verifica Service Mesh**

### CRD installati:

Shell

kubectl get crd | grep -E 'istio|linkerd|appmesh'  

Mostra più linee

### Label/annotazioni sul namespace:



kubectl get ns namespace --show-labels 

### Sidecar nei pod:

kubectl get pods -n namespace -o jsonpath='{range .items[*]}{.metadata.name}{" => "}{range .spec.containers[*]}{.name}{" "}{end}{"\n"}{end}' | grep -E 'istio-proxy|linkerd-proxy|envoy'  



---

## 🔍 5. **Verifica traffico interno (probe script)**

Se le probe usano script, controlla il contenuto:

Esempio tipico:


curl http://localhost:8080/context/snooper.jsp  


✔ Conferma che il traffico è interno al pod.

---

## 🔍 6. **Recupero cartella da un pod**

Comprimi e copia:

Shell

kubectl exec -n namespace pod-name -- tar -czf /tmp/lib.tar.gz /path/to/lib  

kubectl cp namespace/pod-name :/tmp/lib.tar.gz ./lib.tar.gz  

Mostra più linee

---

## ✅ Interpretazione dei risultati

- Se **Ingress → Service → Pod** lavorano sulla stessa porta (es. 8080), il traffico è atteso.
- Se le **probe** fanno curl su localhost:8080, il traffico interno è normale.
- Se **service mesh assente**, nessun proxy aggiuntivo intercetta il traffico.

---

## 📧 Risposta standard (quando il traffico è atteso)

```
Il traffico su <porta> è coerente con la configurazione:
- Ingress e Service instradano su <porta>.
- Le probe interne effettuano controlli di salute sulla stessa porta.
Non risultano chiamate HTTP in uscita dal codice applicativo.
```

---

### 🔒 **Checklist rapida**

- [ ]  `kubectl get ingress ...`
- [ ]  `kubectl get svc ...`
- [ ]  `kubectl describe deploy ...`
- [ ]  `kubectl get crd | grep istio`
- [ ]  `kubectl get ns --show-labels`
- [ ]  `kubectl get pods ... | grep sidecar`
- [ ]  Verifica script probe (`curl localhost:<porta>`)