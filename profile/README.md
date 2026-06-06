# kube-the-home

A collection of Helm charts and shared tooling for running a self-hosted Kubernetes homelab.

## Helm Charts

| Chart | Description |
|---|---|
| [generic-helm](https://github.com/kube-the-home/generic-helm) | Reusable chart for deploying any containerized application — supports ingress, Gateway API, health probes, and rolling updates |
| [aspire-dashboard-helm](https://github.com/kube-the-home/aspire-dashboard-helm) | Standalone .NET Aspire Dashboard for OpenTelemetry-based observability, with optional OTel Collector sidecar |
| [skooner-helm](https://github.com/kube-the-home/skooner-helm) | Lightweight Kubernetes dashboard UI with token-based authentication |
| [kanboard-helm](https://github.com/kube-the-home/kanboard-helm) | Kanban-style task management board with persistent storage |
| [system-upgrade-controller-helm](https://github.com/kube-the-home/system-upgrade-controller-helm) | Rancher's system-upgrade-controller for automated, rolling Kubernetes node upgrades |

## Other Repositories

| Repo | Description |
|---|---|
| [too-restful-api](https://github.com/kube-the-home/too-restful-api) | Minimal Go REST API that serves static content from Kubernetes ConfigMaps |
| [github-actions](https://github.com/kube-the-home/github-actions) | Reusable CI/CD workflows for Helm linting, chart releases, .NET builds, and semantic versioning |
| [renovate](https://github.com/kube-the-home/renovate) | Shared Renovate configuration for automated dependency updates across the org |
| [kube-the-home](https://github.com/kube-the-home/kube-the-home) | Documentation site (MkDocs) covering all charts and contribution guidelines |

## How It Works

Charts are versioned with semantic commits and released automatically via a `semantic-release → helm-release` pipeline. Dependency updates across all repos are handled by a shared Renovate preset. All charts support both traditional Kubernetes Ingress and Gateway API HTTPRoute.
