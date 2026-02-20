Macchina che fa da bastion che serve ad accedere ad EKS(Dobbiamo fare richiesta tramite AVC Giam) (Utilizza PuTTY?)

AVC serve per fare anche le richieste tipo accesso a DynaTrace, ecc.


Samuele ORSO richiesta per GitHub Cloudification-open-Systems che contiene tutti i progetti di Allianz

Serve acceso a ServiceNOW

prima cosa da fare quando entri nel cluster: kp -a per verificare se qualche pod è down

cluster produzione parigi
cluster DR Francoforte

Hanno creato degli alias per Kubernetes


Linux due tipi di immagine:
Hostati tramite JBoss o Tomcat

per vedere le immagini windows --selector=os=windows

in un namespace puoi avere applicazioni windows e linux contemporaneamente

per le linux selector=middleware=jboss/tomcat

Di solito i pod windows contengono il suffisso -prisma al 99%

Tutte le applicazioni windows vengono deployate come AppPool, per poterle vedere basta lanciare il comando Get-IISAppPool

Per riavviare un AppPool ( Conviene quando sia solo un applicazione) Restart-AppPool $nome_app

se è in stop
Start-AppPool $nome_app

Get-EventLog per vedere i log di sistema

Per vedere i restart Get-EventLog -LogName System -Newest 10

Applciazioni critiche: Motor, Danni e Anagrafe

per mandare i logs  ti sposti sotto C:\Logs\CONTESTO_APP\Nome_AppPool\ e la copi in C

File principale DebugTrace.log

poi fai un kubectl cp sul tuo bastion 

loro hanno fluentbit che è una sidecar component che sta in ascolto sulla cartella dei file di logs e li manda a Dynatrace