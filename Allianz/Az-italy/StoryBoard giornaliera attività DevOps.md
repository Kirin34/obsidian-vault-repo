
# 2/12 
- Ho aperto la PR per **gotenberg** in fcp-build-images; [feat(goztenberg): add new docker-image gotenberg by davide-manfredi · Pull Request #6 · az-italy/fcp-build-images](https://github.developer.allianz.io/az-italy/fcp-build-images/pull/6)
- Verificare l'immagine per **prediction** se sia tutto ok, capire se per prediction basta lanciare l'action di Github (utilizza python 3.6, quindi è da aggiornare)
---
# 2/13
-  Ho buildato l'immagine di az-gotenberg, ho verificato su ArgoCD e il deploy sembra andare;
- PREDICTION: L'immagine presente nel dockerfile è stata modificata più volte, ripristinata dagli sviluppatori da 3.11 a 3.6; Chiedere a Paolo come gestire la parte di deploy in quanto il file yaml build-and-push.yml non può essere triggerato manualmente.
-  Triggerata modificando con un commento il dockerfile e lanciata la PR.
---
# 2/16
- Analizzo il problema su prediction-platform in quanto il pod sta dando problemi di avvio, si esclude il problema dei secret, analizzando meglio il pod in scc e i manifest ho notato che i manifest sono relativi a 2 pod: motor e rv.

```
996348077441.dkr.ecr.eu-west-3.amazonaws.com/prediction-2/prediction-platform:{{DOCKER_TAG}}
996348077441.dkr.ecr.eu-west-3.amazonaws.com/prediction/prediction-platform:{{DOCKER_TAG}}
```
- L'applicativo è uguale, bisogna chiedere a Paolo Balzarotti la differenza tra i due.
- Per Prediction, dobbiamo aspettare il team applicativo per risolvere questo problema.
- Fornire a Diana il DNS corretto per far funzionare l'applicativo.
-  PER DOMANI: 
	- Analisi Claims Assistant, capire come gestire tutti i moduli;

---
# 2/17

## Backlog Attività:
- [[Governance] claims-assistant · Migrazione FCP](https://github.developer.allianz.io/orgs/az-italy/projects/23/views/1?pane=issue&itemId=68289&issue=az-italy%7Cdevops-governance%7C4581) - *IN CORSO*
- [[Governance] Migrate the application prediction to FCP · Migrazione FCP](https://github.developer.allianz.io/orgs/az-italy/projects/23/views/1?pane=issue&itemId=70110&issue=az-italy%7Cdevops-governance%7C4692) - *BLOCCATA*

## Daily overview:
In quanto PREDICTION aspettiamo la migrazione del database postgre, oggi mi concentro sulla parte di claims-assistant. Comincerò da **claims-va-engine**.
## Attività svolte: 

-  Mandati a Diana i relativi host per AZ gotenberg per dev,test, e preprod;
-  Creati moduli terraform per claims-va-engine;

## NOTE:
 - ==**AZ-GOTENBERG**==: da verificare lo stato della repository in quanto avendo messo Python come base, alle PR vengono avviati dei job automatici per python che bloccano la build in quanto non è una repository python;
 - Probabilmente gli applicativi di claims-assistant li migreremo a metà marzo, Paolo ha chiesto di trovare una soluzione del tipo togliere i branch protection ecc;
 - Parlando con Federico Silletti, mi ha detto di cambiare la repository di AZ-GOTENBERG con allianz-terraform-microservice invece di python, in modo da risolvere il problema.
 - Chiedere per le netpol proxy relative a az-gotenberg.

---
# 2/18

## Backlog Attività:
- [[Governance] claims-assistant · Migrazione FCP](https://github.developer.allianz.io/orgs/az-italy/projects/23/views/1?pane=issue&itemId=68289&issue=az-italy%7Cdevops-governance%7C4581) - *IN CORSO*
- [[Governance] Migrate the application prediction to FCP · Migrazione FCP](https://github.developer.allianz.io/orgs/az-italy/projects/23/views/1?pane=issue&itemId=70110&issue=az-italy%7Cdevops-governance%7C4692) - *BLOCCATA*

## Daily overview:
Oggi devo concentrarmi sulla parte di claims-va engine e az-gotenberg netpols.  Principalmente devo svolgere le attività per cambiare il modulo di AZ-gotenberg base, la questione delle netpols relative a AZ-Gotenberg. Poi per claims-va-engine, oggi l'obiettivo è quello di almeno migrare la sorgente e fare analisi sulle network policy.

## Attività svolte: 
- Finalizzati cambiamenti per claims-va-engine, PR e terraform import da fare;
- PR az-gotenberg: [fix(az-gotenberg): changed module az-gotenberg source from terraform-… by davide-manfredi · Pull Request #281 · az-italy/github-terraform](https://github.developer.allianz.io/az-italy/github-terraform/pull/281)

## NOTE:
 Paolo mi ha detto di creare una nuova repository partendo da terraform-allianz-github-repo per az-gotenberg, quindi immagino che debbano cambiare alcune cose, immagino i controlli e i dependabot.

---
# 2/19

## Backlog Attività:
- [[Governance] claims-assistant · Migrazione FCP](https://github.developer.allianz.io/orgs/az-italy/projects/23/views/1?pane=issue&itemId=68289&issue=az-italy%7Cdevops-governance%7C4581) - *IN CORSO*
- [[Governance] Migrate the application prediction to FCP · Migrazione FCP](https://github.developer.allianz.io/orgs/az-italy/projects/23/views/1?pane=issue&itemId=70110&issue=az-italy%7Cdevops-governance%7C4692) - *BLOCCATA*
-  Creazione repository terraform-allianz-docker - *TO DO*

## Daily overview:


## Attività svolte: 


## NOTE: