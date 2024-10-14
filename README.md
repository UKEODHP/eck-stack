# Elastic Search | Logstash | Kibana Example Deployment

## Installation

```bash
kubectl apply -k apps/argocd  # install argocd
kubectl apply -f platform/apps.yaml  # install argocd apps
```

## ArgoCD UI

```bash
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo
kubectl port-forward service/argocd-server -n argocd 8080:443
```
