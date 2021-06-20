## Setup
- Command:
  - Windows and Mac Docker desktop:
    - `kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/controller-v0.47.0/deploy/static/provider/cloud/deploy.yaml`
  - minikube:
    - `minikube addons enable ingress`
  - microk8s:
    - `microk8s enable ingress`
---

## Setup for GCE:
- [GKE Setup](https://kubernetes.github.io/ingress-nginx/deploy/#gce-gke)
---

## Setup Documentation:
- [Setup Link](https://kubernetes.github.io/ingress-nginx/deploy/#provider-specific-steps)
- [Ingress Information](https://kubernetes.io/docs/concepts/services-networking/ingress/)
---