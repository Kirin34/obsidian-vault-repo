per trovare la variabile MFCLOUD:
Per Windows:

GetChild-Item :Env | findstr /i MFCLOUD

Per vedere la variabile dentro ad un AppPool:
.\Windows\System32\inetsrv\appcmd.exe list apppool /name:"NOME_APPPOOL" /config

Prima di tutto devi fare l'edit dello statefulset e mettere mfcloud a 1;
	k edit sts $nome_sts;
Se il pod ci mette tempo a scendere, forza il delete;
		k delete pod $Nome_pod --force;
Dopodichè entra nel pod e verifica se la  variabile è stata settata a 1.
	
Modifica dello script ContainerName e Namespace;


**POD NAME:** mt-prs-all-*

**NAMESPACE:** prod-motor-prisma

**STS:** mt-prs-all

**Replicas**: 4

**Container**: auto-prisma-all

**POD NAME:** mt-prs-ngr-*

**NAMESPACE**: prod-motor-prisma

**STS:** mt-prs-ngr

**Replicas**: 28

**Container**: auto-ngr-prisma

**POD NAME:** mt-prs-sem-*

**NAMESPACE**: prod-motor-prisma

**STS:** mt-prs-ngr

**Replicas**: 5

**Container**: auto-prisma-sem 

**POD NAME:** ct-prs-all-*

**NAMESPACE**: prod-contabilita-prisma

**STS:** ct-prs-all

**Replicas**: 4

**Container**: dacontabilita-prisma-all

.\Windows\System32\inetsrv\appcmd.exe list apppool /name:"NOME_APPPOOL" /config