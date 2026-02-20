
1.Creare il secret sul bastion:

```
	kubectl create secret generic name_secret --from-file=path/to/file -n  namespace --dry-run=client -o yaml > secret.yaml

```
2.Modificare il manifest di kustomize al seguente path: 
```
aztech-${OS}/kustomize/apps/${nome_app}/env/${env_name}
```

3.Fare le modifiche , confrontare il manifest vecchio con quello nuovo;
4.Committare le nuove modifiche;
5.Applicare il manifest al cluster creato prima (secret.yaml);
