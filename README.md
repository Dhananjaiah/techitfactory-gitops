# TechITFactory GitOps

This repo contains the desired Kubernetes state.
ArgoCD reads from this repo and applies changes (pull-based GitOps).

## Layout
- apps/root/         -> App-of-Apps (root ArgoCD Application)
- apps/platform/     -> platform apps (argocd, monitoring, ingress, etc.)
- apps/services/     -> microservices apps (frontend/product/cart/order)
- environments/dev/  -> dev values (image tags, env settings)
- environments/prod/ -> prod values (image tags, env settings)

## Promotion Model
- Dev: auto update image tags on merge to main (from app CI)
- Prod: update prod values only on GitHub Release/Tag
