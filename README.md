# Kubernetes GitOps Pipeline with Helm & Argo CD

This repository demonstrates an end-to-end **GitOps continuous delivery workflow** on Kubernetes using **Helm** for templating and **Argo CD** for declarative state management.

## Architecture Flow
`GitHub (Single Source of Truth) ➔ Argo CD (Sync & Self-Heal) ➔ Helm Chart ➔ Kubernetes (Frontend, Backend, Services) ➔ NGINX Ingress`

## Key DevOps Practices Implemented
- **Parameterized Helm Chart:** Manages multi-tier workloads (`fe-deploy`, `be-deploy`), ClusterIP Services, and Layer-7 Ingress rules via `values.yaml`.
- **Declarative GitOps with Argo CD:** Automated sync policies (`prune: true`, `selfHeal: true`) prevent configuration drift between Git and the live cluster.
- **Zero-Downtime Rollouts & Rollbacks:** Supports instant versioned rollbacks via Git commit history.
