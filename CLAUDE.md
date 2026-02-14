# k8s-manifests

Kubernetes manifests, Helm charts, and Kustomize overlays for EKS.

## Structure
```
├── base/             # Base Kustomize resources
│   ├── namespaces/   # Namespace definitions
│   ├── networking/   # Ingress, NetworkPolicies, Services
│   └── storage/      # StorageClasses, PVCs
├── apps/             # Application-specific manifests
├── overlays/         # Environment-specific Kustomize overlays
│   ├── dev/
│   ├── staging/
│   └── prod/
└── helm-charts/      # Custom Helm charts
```

## Conventions
- Kustomize for environment differentiation (base + overlays)
- Helm for complex third-party dependencies
- All manifests pass `kubeval` / `kubeconform` validation
- Labels follow: `app.kubernetes.io/*` convention
- Resource requests/limits defined for all workloads

## Org
- GitHub: https://github.com/marksrv/k8s-manifests
- Part of: [marksrv SRE/DevOps Portfolio](../CLAUDE.md)
