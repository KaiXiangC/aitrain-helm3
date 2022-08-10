# aitrain-helm3

[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/aitrain-helm3)](https://artifacthub.io/packages/search?repo=aitrain-helm3)

<div class="artifacthub-widget" data-url="https://artifacthub.io/packages/helm/aitrain-helm3/aitrain" data-theme="light" data-header="true" data-stars="true" data-responsive="false"><blockquote><p lang="en" dir="ltr"><b>aitrain</b>: A Helm3 chart for Kubernetes</p>&mdash; Open in <a href="https://artifacthub.io/packages/helm/aitrain-helm3/aitrain">Artifact Hub</a></blockquote></div>

## Getting started
### Add repository
```
helm repo add aitrain-helm3 https://kaixiangc.github.io/aitrain-helm3/
```
### Install Chart
```
helm install my-aitrain aitrain-helm3/aitrain --version 0.1.0
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
| Key | Description | Default |
| --- | --- | --- |
| NS_PREFIX | Name Space Prefix | `aitrain` |
| VERSION | Version Type [ v2021-12 , v2022-07 ] | `v2022-07` |
| OAUTH_TYPE | OAuth Provider Type [ go-oauth , google-oauth , github-oauth ] | `go-oauth` |
| DOAMINNAME | URL Domian | `nchc.org.tw` |
| EXISTING_SC_NAME | Storage Class Name | `standard` |
| INGRESS_CLASS | Ingress Class Name | `nginx` |
