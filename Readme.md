# Overview

Flux configuration for a multi-tenant AKS cluster.

# TODO

- HAProxy does not update CRDs when upgrading chart
- [NGINX Ingress hardening](https://kubernetes.github.io/ingress-nginx/deploy/hardening-guide/)
- Move charts to signed OCI artifacts after this is done -> [FluxCD: Support Helm charts from OCI registries](https://github.com/fluxcd/source-controller/issues/124)
- cleanup platform vs team based releases
