# k8s-manifests

Kubernetes manifests, Helm charts, and Kustomize overlays for EKS workloads.

## Usage

```bash
# Apply dev overlay
kubectl apply -k overlays/dev/

# Apply production overlay
kubectl apply -k overlays/prod/
```

## Structure

- **base/** — Base Kustomize resources (namespaces, networking, storage)
- **apps/** — Application-specific manifests
- **overlays/** — Environment-specific Kustomize overlays
- **helm-charts/** — Custom Helm charts

## Prerequisites

- kubectl configured with EKS cluster
- Kustomize >= 5.0 (or kubectl >= 1.27)
- Helm >= 3.12 (for Helm charts)
