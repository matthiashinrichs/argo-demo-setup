# DEMO Setup

Requirements: Local Kubernetes Cluster with Traefik 2 (in this case I will use Rancher Desktop)

Installation:
kubectl apply -k install-argocd

This will install ArgoCD in the namespace argocd and create an initial admin secret to login.

To get the the initial admin secret use this command:
kubectl -n argocd get secret argocd-initial-admin-secret -o jsonpath="{.data.password}" | base64 -d; echo

Open the web ui
open https://argocd.127.0.0.1.nip.io

kubectl apply -k install-argocd
