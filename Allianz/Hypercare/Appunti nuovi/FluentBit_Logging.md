
## 📌 Contesto generale
Il sistema di logging utilizza **FluentBit come sidecar container** per monitorare i log applicativi e inoltrarli a **Dynatrace**, piattaforma di monitoring e observability.

- Presente su **Linux** e **Windows**.  
- Configurato come container secondario in tutti i pod applicativi.  
- Log accessibili anche manualmente tramite bastion host.

---

## 🐧 Logging su Linux

- Log visualizzabili tramite:
  ```bash
  kubectl logs <nome-pod>
  kubectl logs -f <nome-pod>
  ```

- Copia log dal bastion:
  ```bash
  kubectl cp <namespace>/<pod>:/path/del/file ./file_locale
  ```

- FluentBit:
  - Monitora la cartella log nel container.  
  - Invia i log a Dynatrace.

---

## 🪟 Logging su Windows

- I log applicativi si trovano nella cartella:
  ```
  C:\Logs  ```
  - File principale: `DebugTrace.log`

- Comandi PowerShell utili:
  ```powershell
  Get-EventLog
  Get-EventLog -LogName System -Newest 10
  ```

- Per visualizzare e gestire AppPool:
  ```powershell
  Get-IISAppPool
  Restart-AppPool <nome_app>
  Start-AppPool <nome_app>
  ```

---

## 📤 FluentBit – Funzionamento

- Presente come container secondario in ogni StatefulSet o Deployment.
- Raccoglie i log dalla directory applicativa.
- Li inoltra a Dynatrace per centralizzazione e monitoraggio.

### Risorse
- Le risorse assegnate a FluentBit possono variare in base al volume di log:
  - Applicazioni con alti volumi (es. Motor) → CPU/memoria aumentate.
  - Patch dedicate in `Components` nella struttura Kustomize.

---

## ☁️ Dynatrace Integration

- Dynatrace riceve i log da FluentBit.  
- Permette:
  - Correlazione tra pod, log e metriche.  
  - Visualizzazione centralizzata per troubleshooting.  
  - Monitoraggio proattivo su ambienti test, preprod e prod.

- In Windows, l’agent Dynatrace viene installato tramite initcontainer nella Golden Image.

---

## 🧰 Troubleshooting Deploy

- In caso di errore:
  - Verifica pod `kubectl get pods --all`.
  - Controlla log:
    - Linux → `kubectl logs`
    - Windows → `DebugTrace.log`
  - FluentBit → verifica sidecar nei pod.

- In caso di errore in pipeline Jenkins, viene inviata una **notifica alla sala macchine Allianz**.

---

📄 **Riferimenti nei tuoi appunti**:  
- Video 2 → Log Windows/Linux, FluentBit, Dynatrace  
- Video 5 → FluentBit come component Kustomize  
- Video 6 → Logging e monitoring in pipeline
