This is the infra repo for KubeSphere community.

> As you can see, this repo located in [kubesphere-sigs](https://github.com/kubesphere-sigs) instead of [kubesphere](https://github.com/kubesphere). That means we only put those exploratory project in here.

We're using GitOps frameworks to keep all environments updated.

### Setup Environment

Install ArgoCD first

```shell
kubectl create ns argocd
kustomize build prod/argocd/core-install | kubectl apply -n argocd -f -
```

then install cert-manager:

```shell
hd install cert-manager
cmctl x install
```

*Please change the default namespace of your kubectl config to be argocd.*

then create ArgoCD Application:

```shell
argocd app create appset --repo https://github.com/kubesphere-sigs/ks-infra \
    --path appset --dest-namespace argocd \
    --sync-policy automated \
    --dest-server https://kubernetes.default.svc
```
