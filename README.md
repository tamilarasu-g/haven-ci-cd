Convert argocd server service to Loadbalancer type
```shell
kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
```

Get the initial admin password of argocd
```shell
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
```

Command to enable public access on Azure Container Registry
```shell
az acr update --name <yourRegistryName> --anonymous-pull-enabled true
```

Git Url for Azure Repo in ArgoCD
```shell
https://dev.azure.com/{organization}/{project}/_git/{repository}
```
