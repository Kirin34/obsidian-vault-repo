
> Audience: DevOps / Platform engineer (livello **molto tecnico**).  
> Repo analizzate (zip forniti):  
> - **terraform-allianz-github-repo** (modulo *base* “repo factory”)  
> - **terraform-allianz-microservice** (modulo *wrapper* per microservizi)

---

## TL;DR

- **terraform-allianz-github-repo** è un **modulo Terraform “repo factory”**: crea un repository GitHub Enterprise e ci applica governance (branch protection, team access, dependabot security updates, secret standard, custom properties). Inoltre **copià dentro al repo** workflow GitHub Actions “preconfezionati” selezionati tramite `actions_list`.

- **terraform-allianz-microservice** è un **wrapper opinionato**: chiama il modulo base e aggiunge tutto ciò che serve a un microservizio nel vostro contesto (ambienti GitHub `dev/test/preprod/prod`, secrets per AWS per-environment, variabili standard come `AWS_ROLE`, bootstrap dei file `deploy/*/values.yaml` per Kubernetes, integrazione SonarQube, PAT per aggiornare automaticamente l’immagine nel deploy).

- La relazione tra i due è:  
  **microservice = github-repo (base) + “extra microservice”**.

---

## 1) Mappa mentale: “modulo base” vs “wrapper”

### 1.1 Modulo base = piattaforma
Il modulo base **non conosce il dominio applicativo** (microservice, docker, data-pipeline, ecc.).  
Fa solo “repo governance + bootstrap file standard (workflows, codeowners, dependabot)”.

### 1.2 Wrapper = dominio (microservice)
Il wrapper:
- decide quali workflow attivare
- crea secrets/vars extra richiesti da quei workflow
- crea risorse “di dominio” (environments, deploy templates, sonar, ecc.)

Questo pattern scala bene: si possono fare wrapper diversi (es. `terraform-allianz-docker`, `terraform-allianz-library`, ecc.) senza duplicare la logica base.

---

## 2) terraform-allianz-github-repo (modulo base) – come funziona davvero

### 2.1 File principali
- `main.tf`: crea repo + default branch + branch protection + collaborators + dependabot security updates + secrets/property standard
- `actions.tf`: copia nel repo i workflow e file `.github/*`
- `locals.tf`: costruisce mappa team e la mappa “workflow da copiare”
- `variables.tf`: input del modulo
- `provider.tf`: requirement provider
- `output.tf`: output del modulo

---

### 2.2 Creazione repository (`github_repository`)
In `main.tf`:

- crea il repo con:
  - `auto_init = true` (repo inizializzato)
  - `archive_on_destroy = true` (su destroy archivia)
  - `license_template = "mit"`
  - `visibility` variabile (default `private`)
  - `topics` variabile
  - `vulnerability_alerts = true`

- **template repo (opzionale)**:
  - se `var.template != null`, usa `dynamic "template" { ... }` per clonare da un template repo
  - `lifecycle.ignore_changes = [template]` evita drift/riconfigurazioni se GitHub cambia metadati del template

- **Security & Analysis**:
  - `advanced_security.status = var.enable_advanced_security` (`enabled|disabled`)
  - `secret_scanning` e `push_protection` sono impostati a `disabled`

> Implicazione: il modulo abilita GHAS solo se richiesto, ma non abilita secret scanning/push protection.

---

### 2.3 Default branch (`github_branch_default`)
Imposta il branch di default (`var.default_branch`, default `main`).

Dipende esplicitamente dalla creazione del repo.

---

### 2.4 Branch protection (`github_branch_protection_v3`)
Applica governance al branch di default:

- Required status checks:
  - `checks = var.security_check_list`
  - `strict = false` (non richiede che il branch sia aggiornato con base prima di merge)

- Pull request reviews:
  - 1 approvazione obbligatoria
  - dismiss stale reviews
  - code owner reviews
  - require last push approval

- Conversation resolution:
  - `require_conversation_resolution = true`

> **Punto critico**: `security_check_list` deve contenere i **nomi esatti** dei check contexts creati da GitHub Actions (es. `workflow-name / job-name`). Se sbagli stringa, la protection non “vede” quel check.

---

### 2.5 Team access (`github_repository_collaborators`)
Il modulo gestisce team via `local.teams`:

- `local.default_teams`:
  - `devops = push`
  - `information-security-office-iso = pull`

- `local.teams`:
  - se `var.teams_map` esiste -> merge con `default_teams`
  - altrimenti solo `default_teams`

Poi `github_repository_collaborators` crea blocchi `team { team_id, permission }`.

> Nota: `teams_map` è un map di “team id -> permission”. Non è un map di “nome team”. Serve conoscere l’id team.

---

### 2.6 Dependabot security updates
`github_repository_dependabot_security_updates` viene sempre abilitato (`enabled = true`).  
Questo è **diverso** da “dependabot version updates” (che richiede `.github/dependabot.yml`).

---

### 2.7 Secrets / properties standard

#### 2.7.1 `PROJECT_NAME` come secret (opzionale)
Se `var.project_name != null` crea secret `PROJECT_NAME` nel repo.

Uso tipico: raggruppare repo per team/progetto nei workflow o automazioni.

#### 2.7.2 Custom property “ADOIT sysid” (DORA compliance)
Se `var.adoit_it_service_sysid` ha elementi, crea custom property:

- property name: `fcp-adoit-it-service-sysid`
- type: `string`
- value: set di sysid

La variabile valida che ogni sysid sia:
- `skip` oppure
- alfanumerico con `-`

#### 2.7.3 Security waiver (`SECURITY_WAIVER`)
Crea secret `SECURITY_WAIVER` con valore di default `DISABLED|9999-12-31`.

- Commento nel codice: formato `TICKET|YYYY-MM-DD` (es. `SEC-1234|2026-03-15`)
- `lifecycle.ignore_changes` sul valore: significa che il secret può essere gestito “out-of-band” (es. SecOps) senza che Terraform lo resetti.

Uso tipico: workflow di scansione (es. Wiz) controlla se c’è waiver valido e decide se bloccare o meno.

---

## 3) Come il base “installa” workflow nel repo

### 3.1 Il meccanismo `actions_list` → copia file `.github/workflows/*`
In `locals.tf` del base:

- costruisce `local.repo_action_map` scorrendo `var.actions_list`:
  - `file = ".github/workflows/${basename(wf)}"`
  - `content = file("${path.module}/github-actions/workflows/${wf}")`

In `actions.tf`:
- `github_repository_file.github_action` crea i file nel repo target sul branch di default.

In pratica:
- i workflow “template” vivono nel modulo **sotto** `github-actions/workflows/`
- tu li abiliti passando una lista.

> Questo è il cuore del “repo factory”: il codice Terraform governa quali workflow esistono nel repo.

---

### 3.2 File `.github` sempre presenti
Sempre in `actions.tf`:
- copia `.github/CODEOWNERS` da `github-actions/CODEOWNERS`
- copia `.github/dependabot.yml` se `var.dependabot != ""` prendendo il file da `github-actions/dependabot/<file>`

---

### 3.3 Workflow disponibili nel base (quelli presenti nello zip)
Nel base, sotto `github-actions/workflows/` ci sono (lista dall’artefatto):
- `build-and-push.yml`
- `codeql.yml`
- `devskim.yml`
- `postman-test.yml`
- `release.yml`
- `secret-*.yml` (create/delete/list/update secrets)
- `summarize-pr.yml`

> Nota: sono workflow “riusabili” dalla factory. Il wrapper decide quali includere.

---

### 3.4 Workflow “build-and-push” (importante per microservice)
`github-actions/workflows/build-and-push.yml` fa:

- Trigger: `pull_request` con `types: [closed]`
- Condizione: `if: github.event.pull_request.merged == true`

Job `build-and-publish`:
- usa un **reusable workflow**:
  - `uses: az-italy/github-reusable-workflow/.github/workflows/docker-build.yml@2.0.1`
- input principali:
  - `image: ${{ github.repository }}`
  - `tag: latest`
  - `target_registry: registry.regional.devops-services.ew3.aws.aztec.cloud.allianz`
  - `target_project: az-italy-rkljr`
  - `target_registry_user: ${{ vars.HARBOR_USERNAME }}`
- secrets:
  - `target_registry_password: ${{ secrets.HARBOR_TOKEN }}`
  - `wiz_user/password`: `WIZ_USER` / `WIZ_PASSWORD`
  - `security_waiver`: `SECURITY_WAIVER`

Job `tag-version` (dopo build):
- aggiorna `deploy/dev/values.yaml` sostituendo la `tag:` con `${{ needs.build-and-publish.outputs.image_sha }}`
- committa e pusha usando PAT `secrets.TAG_VERSION`

> Questo collega direttamente “CI build/push immagine” con “repo deploy manifest” (GitOps-style), almeno per `dev`.

---

## 4) terraform-allianz-microservice (wrapper) – cosa aggiunge e perché

### 4.1 Cosa “eredita” dal base
In `microservice/main.tf`, il wrapper chiama:

```hcl
module "microservice" {
  source = ".../terraform-allianz-github-repo?...&ref=5.4.0"
  actions_list        = var.actions_list
  security_check_list = var.security_check_list
  teams_map           = var.teams_map
  ...
}
```

Quindi: il wrapper **non ricrea** repo governance. La delega al base.

---

### 4.2 Environments GitHub per ambienti runtime (dev/test/preprod/prod)
In `repo-environments.tf`:

- crea 4 environments nel repo:
  - `dev`, `test`, `preprod`, `prod`

- per ogni environment, crea una **environment variable**:
  - nome: `AWS_ROLE`
  - valore: `arn:aws:iam::<account>:role/<project_name>-<env>`

- crea una **repository variable** globale (non per-environment):
  - `NEXUS_URL`

Perché è utile:
- i workflow possono fare deploy per-environment usando `environment: dev` e poi leggere `vars.AWS_ROLE` (o environment var) per assumere un ruolo AWS specifico.

---

### 4.3 Secrets AWS per-environment (bootstrap credenziali)
In `aws-role-secrets.tf`:

- legge un secret AWS Secrets Manager: `tu-azit-secret-manager`
- dal JSON estrae:
  - `AWS_ACCESS_KEY_ID`
  - `AWS_SECRET_ACCESS_KEY`

- scrive questi valori come **github_actions_environment_secret** in *ogni* environment:
  - `AWS_ACCESS_KEY_ID`
  - `AWS_SECRET_ACCESS_KEY`

- scrive `AWS_REGION` per-environment (mappa `local.aws_region`, qui sempre `eu-west-3`).

Perché così:
- i job GitHub Actions che dichiarano `environment: dev` hanno accesso ai secrets AWS specifici del contesto.
- separazione chiara per ambiente.

**Nota sicurezza** (importante):
- distribuire static credentials in GitHub Secrets è una scelta discutibile in enterprise; spesso si preferisce OIDC + AssumeRole. Ma questo wrapper implementa la strada “secrets-based”.

---

### 4.4 Secrets Wiz (scansioni security container/code)
In `wiz-secrets.tf`:

- legge `wiz-techuser` da AWS Secrets Manager e crea repo secrets:
  - `WIZ_USER` = `Access_Key_ID`
  - `WIZ_PASSWORD` = `Secret_Key`

Questi secrets servono al workflow `build-and-push.yml` (che passa `wiz_user/wiz_password` al reusable workflow di build).

---

### 4.5 PAT per “tag version” (aggiornamento values.yaml)
In `secrets.tf`:

- legge secret `fcp-tag-version-pat` da AWS Secrets Manager
- crea secret nel repo: `TAG_VERSION`

Serve al job `tag-version` del workflow `build-and-push.yml` per committare/pushare la modifica su `deploy/dev/values.yaml`.

---

### 4.6 Bootstrap file di deploy (Kubernetes values)
In `deploy-repo-files.tf`:

- se `var.deploy_on_k8s == true`:
  - copia tutti i file sotto `deploy/**` nel repository target
  - usa `templatefile()` per sostituire:
    - `${REPO_NAME}`
    - `${SERVICE_PORT}`

- `lifecycle { ignore_changes = all }`:
  - dopo la prima creazione, Terraform **non** forza aggiornamenti su quei file (così il team può modificarli nel repo senza che Terraform li ripristini).

I file `deploy/<env>/values.yaml` includono:
- `image.repository` (registry)
- `image.path` che include `${REPO_NAME}`
- `tag: "latest"` (che poi viene aggiornato dal workflow tag-version)

Quindi il flusso è:
1) Terraform crea deploy templates con tag `latest`
2) dopo merge PR, build-and-push produce `image_sha`
3) workflow aggiorna `deploy/dev/values.yaml` con `image_sha`

---

### 4.7 Integrazione SonarQube
In `main.tf`:

- chiama un altro modulo: `terraform-allianz-sonarqube` (`ref=1.3.1`)
- provider multipli:
  - `github`
  - `github.global_sonarqube` (alias)
  - `aws`

Input principali:
- `repo_name`, `default_branch`
- `sonar_host_url`, `sonarqube_config_repo`
- `aws_secret_id` (token sonar)
- `service_ids`, `sonarqube_project_type`

Questa parte è “microservice-specific”: non sta nel base perché non tutti i repo richiedono sonar.

---

### 4.8 moved.tf
Presenza di `moved.tf` indica che sono state fatte migrazioni Terraform (es. rename risorse/moduli) e si vuole evitare “destroy+recreate”.  
È un elemento di manutenzione importante se il modulo è già usato in produzione.

---

## 5) Come lavorano assieme (end-to-end)

### Scenario tipico (microservice)
1) Applichi Terraform su `terraform-allianz-microservice` passando:
   - `repo_name`, `project_name`, `teams_map`
   - `actions_list` (es. include `build-and-push.yml`, `release.yml`, ecc.)
   - `security_check_list` con i check da rendere required

2) Il wrapper crea:
   - repo GitHub (via base)
   - branch protection (via base)
   - team access (via base)
   - files `.github/workflows/*` scelti (via base)
   - secret standard `SECURITY_WAIVER` (via base)

3) Il wrapper poi aggiunge:
   - environments `dev/test/preprod/prod`
   - secrets AWS per-environment + region
   - secrets Wiz
   - secret TAG_VERSION (PAT)
   - bootstrap file `deploy/**`
   - integrazione SonarQube

4) Workflow `build-and-push`:
   - su merge PR: build+push su Harbor (via reusable workflow)
   - security scan (Wiz) con possibilità waiver
   - aggiorna `deploy/dev/values.yaml` con `image_sha` e pusha la modifica

---

## 6) Cose che devi assolutamente sapere (gotcha / anti-pattern / best practice)

### 6.1 `security_check_list` non è “magico”
Devi mettere esattamente i nomi check GitHub.
Pratica consigliata:
- crea repo con protection “soft” (lista vuota)
- fai girare una PR (così compaiono i check reali)
- copia i nomi dalla tab “Checks”
- aggiorna `security_check_list`

### 6.2 Secrets “centrali” vs secrets “per repo”
In microservice, molti secrets vengono creati *per repo* leggendo AWS Secrets Manager.  
Questo funziona, ma:
- aumenta blast radius di Terraform (apply può toccare segreti sensibili)
- richiede permessi AWS a chi fa terraform apply
- rende la rotazione segreti “Terraform-driven”

In enterprise spesso si preferisce:
- org-level secrets gestiti da SecOps
- oppure OIDC + AssumeRole (evitare long-lived `AWS_ACCESS_KEY_ID`)

### 6.3 Workflow build-and-push è opinionato
- trigger solo su merge PR
- tag di default `latest`
- registry e project sono hard-coded nel workflow template del base
- job `tag-version` presuppone che esista `deploy/dev/values.yaml`

Implicazioni:
- se un repo non è “deployable” o non ha `deploy/*`, quel job fallirà a meno di cambiare workflow.
- se cambiano registry/project, va aggiornato il workflow template nel base.

### 6.4 `ignore_changes` sui file deploy
`ignore_changes = all` su `github_repository_file.deploy` è una scelta intenzionale:
- Terraform crea i file come bootstrap
- poi “lascia vivere” il repo senza imporre drift

È bene, ma devi ricordarti:
- aggiornare il template nel modulo non aggiorna i repo già creati
- per propagare cambi, devi scegliere una strategia (nuovo commit manuale, o rimuovere ignore_changes temporaneamente)

### 6.5 Team IDs
Il base richiede `teams_map` con team_id.  
Se cambi org/team, è facile sbagliare. Una best practice è avere una data source o un mapping centralizzato (non in questi moduli).

---

## 7) Come si usa (esempio minimo)

### 7.1 Usare direttamente il base (repo generico)
```hcl
module "repo" {
  source       = "git::https://.../terraform-allianz-github-repo?ref=5.4.0"
  repo_name    = "my-repo"
  project_name = "my-project"
  github_token = var.github_token
  teams_map    = { "<team_id>" = "push" }

  actions_list = [
    "summarize-pr.yml",
    "release.yml"
  ]

  security_check_list = []
}
```

### 7.2 Usare il wrapper microservice
```hcl
module "microservice" {
  source       = "git::https://.../terraform-allianz-microservice?ref=<tag>"
  repo_name    = "my-service"
  project_name = "my-project"
  github_token = var.github_token
  teams_map    = { "<team_id>" = "push" }

  actions_list = [
    "build-and-push.yml",
    "release.yml"
  ]
}
```

> Nota: `build-and-push.yml` vive nel base, ma è abilitato passando `actions_list`.

---

## 8) Checklist operativa per chi deve “capirli e usarli”

- [ ] Ho capito che **microservice chiama github-repo** (non duplicare logica)
- [ ] Ho definito `teams_map` con team IDs corretti
- [ ] Ho scelto `actions_list` coerente con il tipo repo
- [ ] Se uso `build-and-push.yml`, ho:
  - [ ] `vars.HARBOR_USERNAME`
  - [ ] `secrets.HARBOR_TOKEN`
  - [ ] `secrets.WIZ_USER` / `secrets.WIZ_PASSWORD`
  - [ ] `secrets.SECURITY_WAIVER` (creato dal base)
  - [ ] `secrets.TAG_VERSION` (creato dal microservice wrapper)
  - [ ] `deploy/dev/values.yaml` presente
- [ ] Ho configurato `security_check_list` usando nomi check reali

---

## 9) Cosa NON è coperto da questi moduli (ma spesso serve)

- gestione org-level secrets (scelta volontaria)
- policy avanzate GitHub (rulesets, required signatures, secret scanning push protection)
- OIDC per AWS (al posto di static credentials)
- standardizzazione del naming dei check per branch protection (dipende dai workflow)

---

## Appendice A – “Dove sta cosa” (mappa file → responsabilità)

### Base: terraform-allianz-github-repo
- `main.tf` → repo + branch + protection + teams + dependabot security updates + secrets/property standard
- `actions.tf` → copia workflows + CODEOWNERS + dependabot.yml
- `locals.tf` → default teams + costruzione mappa workflow
- `variables.tf` → API del modulo
- `provider.tf` → versioni provider
- `output.tf` → output (nome repo, ecc.)

### Wrapper: terraform-allianz-microservice
- `main.tf` → chiama base + chiama modulo sonar
- `repo-environments.tf` → environments + AWS_ROLE + NEXUS_URL
- `aws-role-secrets.tf` → AWS creds/region per-environment
- `wiz-secrets.tf` → WIZ_USER/WIZ_PASSWORD
- `secrets.tf` → TAG_VERSION PAT
- `deploy-repo-files.tf` → bootstrap deploy templates in repo
- `locals.tf` → account/region map + lista environments
- `variables.tf` → API del wrapper
- `moved.tf` → migrazioni/rename Terraform state

