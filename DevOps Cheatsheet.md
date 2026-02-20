---
title: DevOps Cheatsheet
tags:
  - kubernetes
  - powershell
  - windows
  - linux
  - openssl
  - devops
  - "#Docker"
created: 2026-02-10
---
## ▶️ Kubernetes

### 🔹 Visualizzare pod
```
kgp
```
### 🔹 Tutti i pod nel cluster
```
kgp -A
```
### 🔹 Cercare un pod per nome
```
kgp -A | grep 'pod_name'
```

### 🔹 Pod non in running
```
kgp -A | grep -v -E '1/1|2/2|3/3|4/4|5/5'
```

### 🔹 Scadenza di un secret TLS
```
k get secret areariservatanext-tls-secret -o jsonpath='{.data.tls\.crt}' | base64 -d | openssl x509 -noout -subject -enddate
```


## ▶️ PowerShell / Windows

### 🔹 Headers HTTP
```
$response = Invoke-WebRequest -Uri url_name
$response.Headers

```
### 🔹 Event Log – ultimi 50 Application
```
Get-EventLog -LogName Application -Newest 50 | Format-List
```

### 🔹 Filtrare eventi WAS con keyword
```
Get-WinEvent -LogName System | Where-Object { $_.ProviderName -eq "Microsoft-Windows-WAS" -and $_.Message -like "*VPS*" }
```

### 🔹 Controllare variabile di ambiente
```
gci env: | findstr /i $NOME_VARIABILE_ENV
```

### 🔹 Verifica connettività Windows
```
Test-NetConnection -ComputerName $HOST -Port $PORT

Alias:
tnc $host -p $port
```

---

## ▶️ Linux

### 🔹 Test connettività
```
nc -zv $HOST $PORT
```
### Cercare una cartella
```
find / -type d -name "nome_cartella" 2>/dev/null
```

### 🔹 Eseguire strace su dd
```
strace -f dd if=/dev/zero of=./deleteme.txt bs=8196 count=2
```

---

## ▶️ OpenSSL / Certificati

### 🔹 Estrarre private key da PFX
```
openssl pkcs12 -in yourfile.pfx -nocerts -out private.key -nodes
```

### 🔹 Estrarre certificato da PFX
```
openssl pkcs12 -in yourfile.pfx -clcerts -nokeys -out certificate.crt
```

### 🔹 Verifica certificato remoto
```
echo | openssl s_client -connect areaclienti.allianznext.it:443 -servername areaclienti.allianznext.it 2>/dev/null | openssl x509
```

### 🔹 Estrarre certificato (variante)
```
openssl pkcs12 -in file.pfx -clcerts -nokeys -out certificato.crt
```

---

## ▶️ Verifica GAC (.NET)

```
Get-Content SetupInstallerAllianz-installation.log | Select-String "Prodotto: InstallerAllianz"

$partialName = "Allianz"
$gacPath = "$env:windir\Microsoft.NET\assembly"

$matches = Get-ChildItem -Path $gacPath -Recurse -ErrorAction SilentlyContinue | Where-Object { $_.PSIsContainer -and $_.Name -like "*$partialName*" }

if ($matches) {
    Write-Host "Trovati i seguenti assembly con nome parziale '$partialName' nella GAC:`n"
    $matches | ForEach-Object { Write-Host $_.FullName }
} else {
    Write-Host "Nessun assembly trovato."
}

```

## Docker 

Comando per controllare la versione di Debian nell'immagine gotenberg lanciando un container effimero e poi eliminandolo:

```
docker run --rm -it --entrypoint sh gotenberg/gotenberg:8.26.0 -lc '
cat /etc/os-release; echo "----";
grep -R "deb .*backports" -n /etc/apt/sources.list /etc/apt/sources.list.d 2>/dev/null || true
'

```

Versione Generica: 

```
IMAGE="gotenberg/gotenberg:8.26.0"

docker run --rm -it --entrypoint sh "$IMAGE" -lc '
echo "=== OS DETECTION ==="
if [ -f /etc/os-release ]; then
  cat /etc/os-release
else
  echo "No /etc/os-release found"
fi

echo ""
echo "=== PACKAGE MANAGER DETECTION ==="

if command -v apt >/dev/null 2>&1; then
  echo "APT detected"
  grep -R "deb " -n /etc/apt 2>/dev/null
elif command -v apk >/dev/null 2>&1; then
  echo "APK (Alpine) detected"
  cat /etc/apk/repositories
elif command -v yum >/dev/null 2>&1; then
  echo "YUM detected"
elif command -v dnf >/dev/null 2>&1; then
  echo "DNF detected"
else
  echo "Unknown package manager"
fi
'

```

Mostra tutti i layer dell'immagine:

```
docker history $REPOSITORY/$IMAGE:$TAG
```

Ispeziona i metadati dell'immagine, mostra variabili d'ambiente impostate a build time e estrae sezione config.env

```
docker image inspect $REPOSITORY/$IMAGE:$TAG | jq '.[0].Config.Env'
```