# Overview

Flux configuration for a multi-tenant AKS cluster.

# Notes

- Tenants are separated by namespaces
- Pod Identity
  - supported through managed AAD Pod Identity (NOTE: will migrate to workload identities (v2), once managed identities are available)
  - AAD Pod Identity resources are deployed via the Azure CLI

# TODO

- HAProxy does not update CRDs when upgrading chart
- [NGINX Ingress hardening](https://kubernetes.github.io/ingress-nginx/deploy/hardening-guide/)
- Move charts to signed OCI artifacts after this is done -> [FluxCD: Support Helm charts from OCI registries](https://github.com/fluxcd/source-controller/issues/124)
- NetworkPolicy
  - core-platform - keda, ingress

- Document
  - <https://kubernetes.io/docs/concepts/services-networking/network-policies/>
  - <https://github.com/servicemeshinterface/smi-spec>
  - IngressBackend
