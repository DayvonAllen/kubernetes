## GKE(Google Kubernetes Engine)
- Create a github repo
- Setup github actions
- Create a google cloud project
- Enable billing for the project
- Add deployment scripts to the repo
---

## Helm Setting Up HTTPS
- `kubectl create namespace cert-manager` - create namespace for cert manager
- `helm repo add jetstack` - Add the Jetstack Helm repository
  - `https://charts.jetstack.io`
- `helm repo update` - Update your local Helm chart repository cache
- `helm install cert-manager jetstack/cert-manager --namespace cert-manager --version v1.2.0 --create-namespace` - Install the cert-manager Helm chart
- `kubectl apply -f https://github.com/jetstack/cert-manager/releases/download/v1.2.0/cert-manager.crds.yaml` - Install the CRDs
---