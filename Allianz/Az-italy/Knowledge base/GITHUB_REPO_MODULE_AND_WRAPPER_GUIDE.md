# Guida operativa: `terraform-allianz-github-repo` e pattern Wrapper (aderente al codice)

> Obiettivo di questa guida: spiegare **come funziona** il modulo base `github-repo` e **come creare un wrapper generico** nello stesso stile (come fa `microservice`), senza re-implementare logiche già presenti.

---

## TL;DR

- `terraform-allianz-github-repo` è il **motore** che:
  - crea il repository GitHub,
  - imposta branch di default,
  - applica branch protection con i required checks,
  - assegna permessi ai team (con team di default),
  - abilita Dependabot security updates,
  - crea un secret baseline (`SECURITY_WAIVER`),
  - **materializza** nel repo file standard (.github/workflows, CODEOWNERS, dependabot.yml) in base agli input.

- Un **wrapper** (es. `terraform-allianz-microservice`) è un modulo Terraform che:
  - chiama `terraform-allianz-github-repo` (versionato via `ref=...`),
  - passa-through le variabili “core”,
  - aggiunge risorse “specializzate” (secrets/variables/environments/file aggiuntivi, altri moduli come SonarQube),
  - mantiene **lo stesso contratto** verso i consumer: un modulo “opinionated”, ma compatibile con le baseline del base.

---

# 1) `terraform-allianz-github-repo`: come funziona (flusso reale)

Questa sezione è aderente ai file Terraform del modulo base:

- `main.tf`
- `locals.tf`
- `actions.tf`
- `provider.tf`
- `output.tf`
- `variables.tf`

### 1.1 Provider GitHub (`provider.tf`)

Il modulo dichiara e configura il provider GitHub usando:
- `var.github_owner` (default: `az-italy`)
- `var.github_token` (**sensitive**, PAT)

> Implicazione: chi usa il modulo deve fornire `github_token` (via var, env var o secrets della pipeline).

### 1.2 Creazione repository (`main.tf` → `github_repository.repo`)

`resource "github_repository" "repo"` crea il repository applicando:
- descrizione: `var.repo_description`
- features: `has_issues`, `has_projects`, `has_wiki`
- visibilità: `var.visibility` (default: `private`)
- topics: `var.topics`
- template opzionale: `var.template` (se non null)

Best practice già incorporata:
- `archive_on_destroy = true` (non hard-delete)
- `auto_init = true` (repo inizializzato)
- `lifecycle { ignore_changes = [template] }` (evita drift continuo sul template)

### 1.3 Default branch (`main.tf` → `github_branch_default.default_branch`)

`resource "github_branch_default" "default_branch"` imposta:
- `var.default_branch` (default: `main`)

Nota: dipende da `github_repository.repo`.

### 1.4 Branch protection (`main.tf` → `github_branch_protection_v3.branch_protection`)

`resource "github_branch_protection_v3" "branch_protection"` applica regole sul branch `var.default_branch`:

- Required status checks:
  - `required_status_checks { checks = var.security_check_list, strict = false }`
- Required PR reviews:
  - `required_approving_review_count = 1`
  - `dismiss_stale_reviews = true`
  - `require_code_owner_reviews = true`
  - `require_last_push_approval = true`
- `require_conversation_resolution = true`

**Punto critico**: `var.security_check_list` deve contenere i **context name esatti** dei checks GitHub Actions (vedi sezione 3).

### 1.5 Team permissions (`main.tf` → `github_repository_collaborators.collaborators` + `locals.tf`)

In `locals.tf`:

```hcl
default_teams = {
  "devops"                          = "push",
  "information-security-office-iso" = "pull"
}

teams = (var.teams_map != null ? merge(local.default_teams, var.teams_map) : local.default_teams)
```

In `main.tf`:

```hcl
resource "github_repository_collaborators" "collaborators" {
  dynamic "team" {
    for_each = tomap(local.teams)
    content {
      permission = team.value
      team_id    = team.key
    }
  }
}
```

Cosa significa operativamente:
- il modulo assegna **sempre** almeno:
  - team `devops` con permesso `push`
  - team `information-security-office-iso` con permesso `pull`
- se passi `var.teams_map`, viene fatto `merge()` con i default.

### 1.6 Dependabot security updates (`main.tf`)

`resource "github_repository_dependabot_security_updates"` abilita gli update di sicurezza automatici.

> Nota: questo NON è la config `dependabot.yml` per i version updates (quella è gestita via file, vedi 1.8).

### 1.7 Secret baseline `SECURITY_WAIVER` (`main.tf`)

Il modulo crea:

- `github_actions_secret.security_waiver` con valore default:
  - `"DISABLED|9999-12-31"`

e con:

```hcl
lifecycle { ignore_changes = [plaintext_value] }
```

Significato:
- Terraform crea il secret una volta.
- Se qualcuno (security/ops) aggiorna il valore manualmente in GitHub, Terraform **non lo sovrascrive**.

### 1.8 Materializzazione file nel repo (workflows + CODEOWNERS + dependabot.yml)

Qui ci sono 3 meccanismi distinti:

#### (A) Workflows: `actions_list` → `.github/workflows/*`
In `locals.tf`:

```hcl
repo_action_map = {
  for idx, wf in var.actions_list :
  "${var.repo_name}-${idx}" => {
    repository = var.repo_name
    file       = ".github/workflows/${basename(wf)}"
    content    = file("${path.module}/github-actions/workflows/${wf}")
  }
}
```

In `actions.tf`:

```hcl
resource "github_repository_file" "github_action" {
  for_each = local.repo_action_map
  file     = each.value.file
  content  = each.value.content
}
```

Cosa succede davvero:
- Tu passi `var.actions_list` (lista di file, es. `"pre-commit.yml"`, `"terraform-test.yml"`, ecc.).
- Il modulo legge i template da: `github-actions/workflows/<nomefile>`
- Li scrive nel repo target in: `.github/workflows/<basename(nomefile)>`

⚠️ Gotcha: se `actions_list` contiene un file che non esiste in `github-actions/workflows/`, `terraform apply` fallisce (file() non trova il path).

#### (B) CODEOWNERS
Il modulo crea/copia un file CODEOWNERS nel repo (nel codice sono presenti sia `.github/CODEOWNERS` che `github-actions/CODEOWNERS` come sorgente/asset). Il comportamento effettivo dipende dal resource nel modulo (nel base è esposto anche in output come `codeowners_file`).

#### (C) `dependabot.yml` (version updates)
`var.dependabot` è una stringa che rappresenta il contenuto di un dependabot.yml per version updates.
Se `var.dependabot` è valorizzata, il modulo scrive un file `.github/dependabot.yml` nel repo.

> Nota: nel repo base sono presenti esempi in `github-actions/dependabot/*` (dotnet/gradle/maven/npm/terraform).

---

# 2) Contratto del modulo base (variabili che devi conoscere)

Queste variabili sono quelle che contano davvero quando crei wrapper.

## 2.1 Governance e repo settings
- `repo_name` (string, required)
- `project_name` (string, required) — “grouping” del progetto; il modulo lo usa anche come secret/grouping concettuale.
- `repo_description` (string, optional)
- `visibility` (string, default `private`)
- `topics` (list(string), default `[]`)
- `default_branch` (string, default `main`)
- `template` (string|null)

## 2.2 Security e compliance
- `security_check_list` (list(string), default `[]`)  
  → required checks per branch protection.
- `enable_advanced_security` (string: `enabled|disabled`, default `disabled`)
- `adoit_it_service_sysid` (list(string), default `[]`)  
  → validazione: ogni elemento deve essere `"skip"` oppure match regex (sysid ADOIT). Serve per DORA compliance (doc dedicata nel base).

## 2.3 Automation (workflows, dependabot)
- `actions_list` (list(string), default include `postman-test.yml` + `summarize-pr.yml`)
- `dependabot` (string, default `""`) — contenuto del dependabot.yml per version updates

## 2.4 Access management
- `teams_map` (map(any), required in schema ma gestibile come input)  
  → merge con `default_teams` in locals.

---

# 3) Branch protection: come farla funzionare senza bloccarsi

Il base imposta required checks direttamente da `security_check_list`. Il problema tipico è che i context names devono essere ESATTI.

## 3.1 Come sono fatti i nomi dei check
Di solito GitHub mostra i check come:
- `<workflow name> / <job name>`

Esempio: se il workflow ha `name: terraform-test` e il job si chiama `test`, GitHub potrebbe mostrarti:
- `terraform-test / test`

⚠️ Non esiste una garanzia assoluta: dipende dal `name:` del workflow, dal `name:` del job e da come GitHub renderizza quel check.

## 3.2 Procedura consigliata (enterprise-friendly)
1. Crea repo + copia workflow con `actions_list`.
2. Fai una PR “dummy” (o push su branch) che triggeri il workflow.
3. Vai nella PR → tab “Checks” → copia **i nomi esatti**.
4. Popola `security_check_list` con quei nomi.
5. `terraform apply` → branch protection diventa enforceabile e non “fantasma”.

---

# 4) Come costruire un wrapper generico (pattern aderente a `terraform-allianz-microservice`)

Il wrapper **non** reinventa il base. Lo chiama e aggiunge specializzazioni.

## 4.1 Il pattern di chiamata del base (come in `microservice/main.tf`)
`terraform-allianz-microservice` fa:

```hcl
module "microservice" {
  providers = { github = github }

  source                   = "git::https://github.developer.allianz.io/az-italy/terraform-allianz-github-repo?depth=1&ref=5.4.0"

  repo_name                = var.repo_name
  repo_description         = var.repo_description
  project_name             = var.project_name
  default_branch           = var.default_branch
  actions_list             = var.actions_list
  dependabot               = var.dependabot
  teams_map                = var.teams_map
  topics                   = var.topics
  template                 = var.template
  security_check_list      = var.security_check_list
  enable_advanced_security = var.enable_advanced_security
  adoit_it_service_sysid   = var.adoit_it_service_sysid

  github_token             = var.github_token
}
```

Cose importanti da copiare nel tuo wrapper generico:
- **versionare** il base via `ref=...`
- pass-through pulito delle variabili core
- `providers = { github = github }` per evitare ambiguità provider
- tenere `security_check_list` come input wrapper (non hardcodare)

## 4.2 “Aggiunte” tipiche in un wrapper (esempio reale: microservice)

### (A) Moduli aggiuntivi (SonarQube)
`microservice` aggiunge un modulo esterno:

```hcl
module "microservice_sonarqube" {
  source = "…/terraform-allianz-sonarqube?ref=1.3.1"
  providers = {
    github                  = github
    github.global_sonarqube = github.global_sonarqube
    aws                     = aws
  }
  depends_on = [module.microservice]
}
```

Takeaway:
- Il wrapper può comporre più moduli.
- Usa `depends_on = [module.microservice]` per evitare race conditions (repo deve esistere prima).

### (B) Creazione environments GitHub (dev/test/preprod/prod)
In `repo-environments.tf`:

- `github_repository_environment.repo_envs` crea gli environments per `local.environments = ["dev","test","preprod","prod"]`
- `github_actions_environment_variable.aws_role` crea variabili environment-specific (ARN role AWS)
- `github_actions_variable.nexus_url` crea una variable globale repo-level

Takeaway:
- Gli environment secrets/variables sono una “specializzazione” perfetta da mettere nei wrapper.

### (C) Secrets presi da AWS Secrets Manager e messi su GitHub
In `secrets.tf`:
- legge secret `fcp-tag-version-pat`
- crea `github_actions_secret.TAG_VERSION` nel repo

In `aws-role-secrets.tf`:
- legge secret `tu-azit-secret-manager`
- crea `AWS_ACCESS_KEY_ID` / `AWS_SECRET_ACCESS_KEY` come **environment secrets** per ogni environment

Takeaway:
- Pattern standard: `data aws_secretsmanager_secret_version` → `github_actions_secret` o `github_actions_environment_secret`
- Nota bene: questi secrets sono **per-repo** (non org-level). Se un domani li centralizzate a livello organization, togliete questa parte dal wrapper e documentate i nomi attesi dai workflow.

### (D) File aggiuntivi nel repo (cartella `deploy/`)
In `deploy-repo-files.tf`:
- copia TUTTI i file in `deploy/**` dentro al repo target sotto `deploy/<...>`
- usa `templatefile()` per sostituire placeholder (REPO_NAME, SERVICE_PORT)
- `lifecycle { ignore_changes = all }` per non gestire drift su quei file (scelta deliberata)

Takeaway:
- Il wrapper può “bootstrappare” contenuto repository oltre a `.github/*`.

### (E) Migrazioni state (`moved.tf`)
`microservice/moved.tf` usa blocchi `moved { from = … to = … }` per migrare risorse quando sono state spostate dentro un nested module (SonarQube).

Takeaway:
- Se evolvi il wrapper e sposti risorse, usa `moved` per non rompere lo state.

---

# 5) Template: come creare un wrapper *generico* “pronto per specializzazioni”

Questa è una ricetta pratica aderente ai vostri standard (come `microservice`).

## 5.1 Struttura minima wrapper
Consigliata (identica a microservice come idea):

- `main.tf`  
  → chiama `terraform-allianz-github-repo` e (opzionale) altri moduli.
- `variables.tf`  
  → espone le variabili core (pass-through) + variabili extra wrapper.
- `provider.tf`  
  → pin version providers (github ~>6.0, aws ~>5.0 se necessario)
- `output.tf`  
  → espone almeno `name`, `id`, `git_repo_url` dal base
- (opzionale) `locals.tf`  
  → default env list, map account id, ecc.
- (opzionale) `moved.tf`  
  → migrazioni state quando si refactor.

## 5.2 Regole d’oro
- **Non duplicare** logica `actions_list`: il base già copia workflows.
- **Non cambiare** branch protection a meno di motivazioni forti: usa `security_check_list`.
- Versiona sempre il base: `ref=x.y.z` (come microservice: `ref=5.4.0`).
- Se aggiungi secrets:
  - preferisci leggere da AWS Secrets Manager come fa microservice,
  - usa environment secrets se sono legati a env (`dev/test/preprod/prod`).
- Se i secrets sono gestiti centralmente (org secrets / env secrets configurati a mano), il wrapper deve **solo documentare** i nomi richiesti, non crearli.

## 5.3 Checklist “non mi si blocca la PR”
1. `actions_list` contiene solo workflow esistenti nel base (`github-actions/workflows/*`).
2. Workflows girano e producono checks.
3. `security_check_list` matcha i check name reali.
4. Branch protection applicata sul branch corretto (`default_branch`).

---

# 6) Appendice: dove trovare cosa nel base

- Workflows template: `terraform-allianz-github-repo/github-actions/workflows/*`
- Dependabot templates: `terraform-allianz-github-repo/github-actions/dependabot/*`
- Docs (utili per compliance e feature):
  - `doc/features.md`
  - `doc/dora-compliance.md`
  - `doc/troubleshooting.md`
  - `doc/usage.md`

---

## 7) Cosa “devi sapere” (valutazione da senior)

- Il modulo base è pensato come **golden path**: crea repo e baseline governance e poi *scrive file* nel repo.
- Il vero “API” del base è:
  - `actions_list` (abilita automazioni)
  - `security_check_list` (enforce governance)
  - `teams_map` (access control)
  - `dependabot` (policy dependency updates)
- I wrapper sono la strategia corretta per evitare fork del base:
  - microservice dimostra il pattern “composizione”: base + sonarqube + env + secrets + deploy files.
- Il principale rischio operativo è **branch protection** impostata troppo presto o con check names errati.
  - Risolvilo con la procedura in 3.2 (PR → copia checks → apply).

---

