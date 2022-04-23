# Sample - Mult-tenant GitOps on AKS with Flux
**This is a work in progress. This repo is a part of a larger effort to demonstrate secure workloads on Azure. This is for reference only and not meant for production workloads**

Flux configuration for a multi-tenant AKS cluster.


## Features
* Managed Identity data plane access to Cosmos DB.
* Custom JSON serialization for HTTP (Newtonsoft) and CosmosDB (System.Text.Json) bindings
* Custom authentication & authorization using Azure B2C
* Generates OpenApi documentation for Azure API Management consumption 

## Related GitHub repositories

### Supporting
|Item|Description|
|----|-----|
|[Utility Docker Images](https://github.com/colincmac/oink-docker-images)|Images used to support Ops scenarios. Built using [ACR Tasks](https://docs.microsoft.com/en-us/azure/container-registry/container-registry-tasks-overview)|
|[Helm Charts](https://github.com/colincmac/oink-helm-charts)|Helm charts to support GitOps scenarios|
|[AKS GitOps - Core Platform](https://github.com/colincmac/aks-lz-manifests)|Flux multi-tenant configuration in AKS - Core Platform|
|[AKS GitOps - Shared Services](https://github.com/colincmac/aks-lz-shared-services-manifests)|Flux multi-tenant configuration in AKS - Shared Services|

### Application Workloads
|Item|Description|
|----|-----|
|[Shared .NET Libraries](https://github.com/colincmac/oink-core-dotnet)|Base .NET seedwork for implementing CQRS, EventSourcing, and DDD|
|[Financial Account Management](https://github.com/colincmac/oink-financial-account-mgmt)|Serverless Azure Function used to demonstrate several concepts|


# TODO

- [NGINX Ingress hardening](https://kubernetes.github.io/ingress-nginx/deploy/hardening-guide/)
- Move charts to signed OCI artifacts after this is done -> [FluxCD: Support Helm charts from OCI registries](https://github.com/fluxcd/source-controller/issues/124)
- NetworkPolicy
  - core-platform - keda, ingress

- Document
  - <https://kubernetes.io/docs/concepts/services-networking/network-policies/>
  - <https://github.com/servicemeshinterface/smi-spec>
  - IngressBackend
