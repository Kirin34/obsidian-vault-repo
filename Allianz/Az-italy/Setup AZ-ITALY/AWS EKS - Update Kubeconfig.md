
## Login SSO (una volta per profilo)

```
aws sso login --profile fcp-az-italy-dt
aws sso login --profile fcp-az-italy-preprod
aws sso login --profile fcp-az-italy-prod
aws sso login --profile scc-az-italy
aws sso login --profile scc-az-italy-dr
```

## scc-az-italy-dr

```
aws eks update-kubeconfig \
  --region eu-central-1 \
  --name adpk8s-azit-prod \
  --profile scc-az-italy-dr \
  --alias scc-dr

```

## scc-az-italy

```
aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-azit-eksp-noprod \
  --profile scc-az-italy \
  --alias scc-noprod

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-azit-eks-nopr-2 \
  --profile scc-az-italy \
  --alias scc-noprod-2

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-azit-eksp-prod \
  --profile scc-az-italy \
  --alias scc-prod

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-azit-eks-prod-2 \
  --profile scc-az-italy \
  --alias scc-prod-2

```

## fcp-az-italy-dt

```
aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-dt-ent \
  --profile fcp-az-italy-dt \
  --role-arn arn:aws:iam::471466593195:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-dt-ent

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-dt-int \
  --profile fcp-az-italy-dt \
  --alias fcp-dt-int

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-dt-mng \
  --profile fcp-az-italy-dt \
  --role-arn arn:aws:iam::471466593195:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-dt-mng

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-dt-tra \
  --profile fcp-az-italy-dt \
  --role-arn arn:aws:iam::471466593195:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-dt-tra

```

## fcp-az-italy-preprod

```
aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-pp-ent \
  --profile fcp-az-italy-preprod \
  --role-arn arn:aws:iam::058264287770:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-pp-ent

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-pp-int \
  --profile fcp-az-italy-preprod \
  --role-arn arn:aws:iam::058264287770:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-pp-int

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-pp-mng \
  --profile fcp-az-italy-preprod \
  --role-arn arn:aws:iam::058264287770:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-pp-mng

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-pp-tra \
  --profile fcp-az-italy-preprod \
  --role-arn arn:aws:iam::058264287770:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-pp-tra

```

## fcp-az-italy-prod

```
aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-ent \
  --profile fcp-az-italy-prod \
  --role-arn arn:aws:iam::767398069155:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-prod-ent

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-int \
  --profile fcp-az-italy-prod \
  --role-arn arn:aws:iam::767398069155:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-prod-int

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-mng \
  --profile fcp-az-italy-prod \
  --role-arn arn:aws:iam::767398069155:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-prod-mng

aws eks update-kubeconfig \
  --region eu-west-3 \
  --name adpk8s-az-italy-tra \
  --profile fcp-az-italy-prod \
  --role-arn arn:aws:iam::767398069155:role/adpk8s-crp-account-admin-assumerole \
  --alias fcp-prod-tra

```

## Verifica

```
kubectl config get-contexts | egrep '^(CURRENT|\*|)\s*(scc-|fcp-)' || true
```
