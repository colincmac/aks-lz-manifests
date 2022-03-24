# Overview

Flux configuration for a multi-tenant AKS cluster.

# Notes

- Tenants are separated by namespaces
- Pod Identity
  - supported through managed AAD Pod Identity (NOTE: will migrate to workload identities (v2), once managed identities are available)
  - AAD Pod Identity resources are deployed via the Azure CLI

# TODO

- PCI
  - Update default flux deployment with appropriate labels
- HAProxy does not update CRDs when upgrading chart
- [NGINX Ingress hardening](https://kubernetes.github.io/ingress-nginx/deploy/hardening-guide/)
- Move charts to signed OCI artifacts after this is done -> [FluxCD: Support Helm charts from OCI registries](https://github.com/fluxcd/source-controller/issues/124)
- NetworkPolicy
  - core-platform - keda, ingress
  
- OSM will break the NGINX Helm deployment, unless the admission job pods are opt-ed out
