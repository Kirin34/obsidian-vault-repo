Installa Slack per passare informazioni/ testo;

Repository adp-toolchain-configuration contiene le configurazioni salvate su jenkins (Plugin, definizione dei Job)
### **1. Certificati nei container Windows**

- Due applicazioni principali: **Vita** e **Anagrafe**.
- Nei **Dockerfile** è stato necessario installare certificati.
- I certificati **.PFX** vengono posizionati in una cartella nel container.
- Installazione su Windows richiede:
    - **Thumbprint**.
    - Password del certificato.
- Certificati forniti da un’altra persona del team (es. **Marazzato EEA**), che li riceve da **Marco Carone** (interno Allianz).
### Nome del repo docker:
- aztech-${OS-SYSTEM}-${AREA}
### **3. Jenkins – Pipeline e viste**

- Interfaccia Jenkins con diverse viste:
    - **Linux JBoss**, **Linux Tomcat**, **Windows HS**.
- Ogni vista contiene le pipeline delle applicazioni.
- Pipeline principali:
    - **preprod**, **prod**, **test** → usate per i rilasci.
    - Ogni pipeline lancia il deploy nell’ambiente corrispondente.
- Pipeline di **restart**:
    - Windows: **scale** notturno.
    - Linux: **restart** alle 05:00.
- Restart schedulati come **cronjob** (eseguiti automaticamente).
- In caso di errore:
    - Notifica inviata alla **sala macchine Allianz** tramite sistema di monitoraggio.

---
### **4. Troubleshooting**
- Possibile fare troubleshooting su applicazioni e log per capire problemi di deploy.
