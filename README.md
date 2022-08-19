# aitrain-helm3

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/aitrain-helm3)](https://artifacthub.io/packages/search?repo=aitrain-helm3)

<div class="artifacthub-widget" data-url="https://artifacthub.io/packages/helm/aitrain-helm3/aitrain" data-theme="light" data-header="true" data-stars="true" data-responsive="false"><blockquote><p lang="en" dir="ltr"><b>aitrain</b>: A Helm chart for deployment and management of Kubernetes in clusters.</p>&mdash; Open in <a href="https://artifacthub.io/packages/helm/aitrain-helm3/aitrain">Artifact Hub</a></blockquote></div>

## Prerequisites
- Kubernetes 1.22+
- Helm 3.5.0+

## Getting started
### Add repository
```
helm repo add aitrain-helm3 https://kaixiangc.github.io/aitrain-helm3/
```
### Install Chart
```
helm install my-aitrain aitrain-helm3/aitrain --version 0.2.0
```
### Uninstall Chart
To uninstall the `my-aitrain` deployment run:
```
helm uninstall my-aitrain
```
## Configuration
```
helm install my-aitrain --set [Parameters]=[Value] aitrain-helm3/aitrain
```
## Parameters
The following table lists the helpers available in the library

### common
| Key | Description | Default |
| --- | --- | --- |
| *common.destination* | Destion Cluster Type [ OpenShift: OCP , Kubernetes: K8S ] | `kubernetes` |
| *common.namespace_prefix* | Name Space Prefix | `aitrain` |
| *common.version* | Version Type [ v2021.12 , v2022.07 ] | `v2022.07` |
| *common.domian_name* | URL Domian | `"127-0-0-1.nip.io"` |
| *common.ingress_class* | Ingress Class Name | `nginx` |
| *common.k8s_dns_server* | DNS Server | `""` |
| *common.enable_vm* | VM Related Configuration | `false` |
| *common.oauth_type* | OAuth Provider Type [ go-oauth , google-oauth , github-oauth ] | `go-oauth` |

### storageclass
| Key | Description | Default |
| --- | --- | --- |
| *storageclass.install* | Install Storage Class | `false` |
| *storageclass.existing_sc_name* | Storage Class Name | `standard` |

### api
| Key | Description | Default |
| --- | --- | --- |
| *api.uid_start* | UID Start Value | `0` |
| *api.uid_count* | UID Count Value | `100000` |

**Useful links**
- https://helm.sh/docs/intro/using_helm/