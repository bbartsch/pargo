# ArgoCD

# Install
1. Deploy with kubectl + kustomize
```bash
kubectl apply -k ./
```
2. Deploy tls secret
   (TODO)

3. Get init admin password
```
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo

# Delete after password change
 
```

## Kustomize

### normal install:

```bash
https://raw.githubusercontent.com/argoproj/argo-cd/$branch/manifests/install.yaml

# master
https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/install.yaml

# stable
https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

# specific tags (see releases on GitHub)
https://raw.githubusercontent.com/argoproj/argo-cd/v2.5.4/manifests/install.yaml
```

### ha install:
```bash
https://raw.githubusercontent.com/argoproj/argo-cd/$branch/manifests/ha/install.yaml

# master
https://raw.githubusercontent.com/argoproj/argo-cd/master/manifests/ha/install.yaml
```

### normal install with release/version ref
see releases on GitHub


```bash
github.com/argoproj/argo-cd/manifests/cluster-install?ref=$tag

# release v2.5.4
github.com/argoproj/argo-cd/manifests/cluster-install?ref=v2.5.4
```