# Hermes

Hermes is a Basecamp Pull Request Automation that manages the interaction between Pull Requests and Basecamp To-dos.

## Prerequisites

* Kubernetes 1.15+

## Installing the Chart

## Uninstalling the Chart

To uninstall/delete the my-release deployment:

```
helm delete my-release
```

## Parameters

| Parameter                        | Description                                   | Default                           |
|----------------------------------|-----------------------------------------------|-----------------------------------|
| `nameOverride`                   | String to partially override hermes.fullname  | `nil`
| | |
| `fullnameOverride`               | String to fully override hermes.fullname      | `nil`
| | |
| `replicaCount`                   | Number of Hermes pods to run                  | `1`
| | |
| `environment`                    | Holds required env vars to hermes             | `{}`
| | |
| `image.repository`               | Hermes image name                             | `runhermes/hermes`
| | |
| `image.tag`                      | Hermes image tag                              | `{TAG_NAME}`
| | |
| `image.pullPolicy`               | Hermes image pull policy                      | `IfNotPresent`
| | |
| `ingress.enabled`                | Enable ingress controller resource            | `false`
| | |
| `ingress.annotations`            | Ingress annotations                           | `{}`
| | |
| `ingress.hosts`                  | List of hosts objects                         | `{}`
| | |
| `ingress.hosts.host`             | Hostname                                      | `[]`
| | |
| `ingress.hosts.paths`            | List of paths within each host                | `[]`
| | |
| `ingress.tls`                    | TLS specification                             | `[]`
| | |
| `service.port`                   | Service HTTP port                             | `3000`
| | |
| `service.type`                   | Kubernetes Service type                       | `ClusterIP`
| | |
| `resources`                      | Resources allocation (Requests and Limits)    | `{}`
| | |
| `tolerations`                    | Tolerations for pod assignment                | `[]`
| | |
| `nodeSelector`                   | Node labels for pod assignment                | `{}`
| | |
| `affinity`                       | Affinity for pod assignment                   | `{}`
| | |
| `autoscaling.enabled`            | Enables horizontal pod autoscaler             | `false`
| | |
| `autoscaling.minReplicas`        | Minimum number of replicas to auto-scale      | `1`
| | |
| `autoscaling.maxReplicas`        | Maximum number of replicas to auto-scale      | `100`
| | |
| `autoscaling.targetCPUUtilizationPercentage` | CPU percentage to trigger autos-cale  | `80`
| | |
