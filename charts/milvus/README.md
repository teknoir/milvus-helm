# Milvus Standalone Helm Chart

This chart deploys Milvus Standalones to a Kubernetes cluster.

> The implementation of the Helm chart is right now the bare minimum to get it to work.

## Usage in Teknoir platform
Use the HelmChart to deploy the Milvus Standalone to a Device.

```yaml
---
apiVersion: helm.cattle.io/v1
kind: HelmChart
metadata:
  name: milvus
  namespace: default
spec:
  repo: https://teknoir.github.io/milvus-helm
  chart: milvus
  targetNamespace: default
  valuesContent: |-
    # Example for minimal configuration
    
```

## Adding the repository

```bash
helm repo add teknoir-milvus https://teknoir.github.io/milvus-helm/
```

## Installing the chart

```bash
helm install milvus teknoir-milvus/milvus -f values.yaml
```