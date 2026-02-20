
Build delle Golden Image: le immagini applicative vengono buildate da un immagine base costruita sempre da noi basate su immagini pubbliche di windows o linux che hanno Jboss o tomcat integrati e andiamo ad installare alcune applicazioni che sono utilizzate da tutti gli applicativi
Esempio: windows installiamo Db2, Allianz dispatch, mentre sulle linux installiamo certificati, varie utility

Abbiamo due tipi di Golden image diverse per linux:
jboss e tomcat

all'interno delle repository delle golden Image si trova un Jenkinsfile che si basa sui metodi scritti nella Shared Library

A differenza delle immagini applicative il processo differisce

Cosa fa:
Builda la golden image  e le pusha sui vari ecr per gli environment

La struttura delle due linux è identica, per quanto riguarda le golden image windows,
ci sono tre cartelle:
-  Fluentbit;
- Initcontainer per installare il OneAgent di Dynatrace;
Le prime due servono per buildare l'immagine di Fluentbit
mentre layers/ contiene 4 folder(contengono Dockerfile) diverse che servono al jenkinsfile che costruisce l'immagine windows di costruirla in 4 step; Ad esempio nel primo viene installato ASPDotnet,in due step inizializzazione e finalizzazione di db2, e l'ultimo sono dei tool proprietari di Allianz.


Jenkins shared Library:

Per le immagini linux viene utilizzato un bastion host per le build,
	mentre per le immagini Windows vengono utilizzate delle macchine ec2 effimere che durano nel tempo di build(il massimo di build che può fare contemporaneamente è 2 a causa delle immagini molto pesanti di windows(Server Core 2019) e l'applicativo allianz, installando poi tutti i tool e app pool si arriva ad un immagine di 20-25 gb)
DockerBuild.groovy:

Il label viene preso dinamicamente tramite un metodo utils.getImageOS(), in base a quello sceglie l'agent che si occuperà della build (Va a prendere semplicemente il nome della repo, se contiene windows o linux)

Nelle options troviamo lo skipDefaultCheckout per windows;

Il primo stage è un clone git repository che viene eseguito solo per windows, infatti si lega all'option SkipDefaultCheckout, perchè per windows ci sono stati alcuni problemi nel clone


Stage "Pull golden Image" viene eseguito solo per linux, in quanto le EC2 di windows si basano su una AMI che contiene già la golden image di windows, quindi non serve fare la pull

conviene per Windows perchè le sue build sono di per sè già più lente.


In questo stage fa la pull della golden image e identifica se è tomcat o Jboss;


Stage Workspace Preparation andiamo a prendere tutti i file che stanno all'interno della content share che servono durante la build dell'immagine, la struttura della content share è molto simile, configuration/${env}/${app_name}, questi file sono specificati nel dockerfile.


Stage build Docker image  builda sostanziamente l'immagine, C'è uno step di SetBuildArguments e poi build, per Windows rimuove il path .src


Stage "Push docker image to ECR registry" pusha l'immagine sugli ECR dei vari ambienti, lo fa con il tag ${currentDate}-${BuildNumber}


Stage push docker image to DR ECR Registry solo in caso di produzione, pusha l'immagine anche sul registry 


Stage Clean local built image pulisce il nodo dall'immagine caricata (Questo perchè anche se effimero può gestire più pipeline, e potrebbe rallentarsi)

Stage Deploy essenzialmente richiama la pipeline di deploy che prima si ricava la folder del Job tramite la funzione getJobFolder, e poi fa la build del job di deploy
 Stage Additional Deploy per alcuni servizi di Motor come Auto e AutoSEM per deployare l'immagine Previvas


KubernetesDeploy.groovy:


Nel deploy qua utilizzando solo comandi kustomize, non abbiamo bisogno di un OS specifico e quindi utilizziamo degli agent che ci fornisce Central (Uno per ogni ambiente)

stage Check tag valididy Si prende il tag tramite sed dall'immagine precendente e fa la validazione del tag se esiste o meno

Stage Clone Kustomize repository

Si clona la repository kustomize in base al sistema operativo

Stage Clone and copy configuration repository (Immagini Linux)

Si clona la repo dove si trovano le configurazioni dell'applicativo e le copia

nella repository aztech-linux ci sono delle configurazioni per la macchina linux, e le troviamo nella repository aztech-linux-configuration e si trovano sotto azetch-linux-configuration/${env}/${area_name}/${application_NAME}


Per tomcat troviamo principalmente 3 files: 
- content.xml
- server.xml
- setenv.sh

per Jboss:
- env.conf
- standalone.xml


Generate manifest Kustomize praticamente fa kustomize build;

Apply Manifest stage applica i manifest tramite kubectl apply

Deployment rollout aspetta che tutti i pod siano in running, quando finisce la pipeline termina

Post Deploy Action serve per Vita, che ha bisogno di eseguire un suo script custom per i suoi AppPool (Fa Operazione ADB sostanzialmente)
