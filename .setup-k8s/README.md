# Required microk8s specific addons

- dns
- ingress
- storage

# Initial setup with helm

```bash

helm upgrade --install argo-cd argo/argo-cd --namespace=argo-cd  --version 4.5.7 --create-namespace -f ./argo-cd/values.yaml --wait

kubectl apply -f ./argo-cd/repo-credentials.yaml -n=argo-cd

kubectl apply -f argocd-root-app.yaml -n=argo-cd


```
