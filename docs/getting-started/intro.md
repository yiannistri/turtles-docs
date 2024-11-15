---
slug: /
sidebar_position: 1
---

# Introduction

:::warning
Starting with Turtles `v0.9.0`, the process used for importing CAPI clusters into Rancher is now based on a different controller logic. If you are a new user of Turtles, you can proceed normally and simply install the extension. If you have been using previous versions of Turtles and are upgrading to `v0.9.0`, we recommend you take a look at the migration mechanisms and their implications:
- [Automatic migration](../tasks/maintenance/automigrate_to_v3_import.md).
- [Manual migration](../tasks/maintenance/import_controller_upgrade.md)
:::

Rancher Turtles is a Kubernetes Operator that provides integration between Rancher Manager and Cluster API (CAPI) with the aim of bringing full CAPI support to Rancher. With Rancher Turtles, you can:

- Automatically import CAPI clusters into Rancher, by installing the Rancher Cluster Agent in CAPI provisioned clusters.
- Configure the CAPI Operator.

## Demo

This demo shows how to use the Rancher UI to install Rancher Turtles, create/import a CAPI cluster, and install monitoring on the cluster:

<iframe width="560" height="315" src="https://www.youtube.com/embed/lGsr7KfBjgU?si=ORkzuAJjcdXUXMxh" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## Prerequisites

| Name                     | Version                                  | Details                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| ------------------------ | ---------------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Kubernetes cluster       | `>=1.30.0`                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Helm                     | `>=3.12.0`                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Rancher                  | `>=2.9.0` | Using [helm based](https://ranchermanager.docs.rancher.com/pages-for-subheaders/install-upgrade-on-a-kubernetes-cluster#install-the-rancher-helm-chart) installation on any kubernetes cluster directly or on a newly created [Amazon](https://ranchermanager.docs.rancher.com/getting-started/installation-and-upgrade/install-upgrade-on-a-kubernetes-cluster/rancher-on-amazon-eks), [Azure](https://ranchermanager.docs.rancher.com/getting-started/installation-and-upgrade/install-upgrade-on-a-kubernetes-cluster/rancher-on-aks) or [Google](https://ranchermanager.docs.rancher.com/getting-started/installation-and-upgrade/install-upgrade-on-a-kubernetes-cluster/rancher-on-gke) service based options. |
| Cert-manager             | `>=v1.15.2`                              | Using [helm](https://cert-manager.io/docs/installation/helm/#installing-with-helm) based installation or via [kubectl apply](https://cert-manager.io/docs/installation/#default-static-install).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| Cluster API Operator     | `>=v0.14.0`                               | Using [Rancher UI](./install-rancher-turtles/using_rancher_dashboard.md) (recommended) or [Helm install](https://github.com/kubernetes-sigs/cluster-api-operator/blob/main/docs/README.md#method-2-use-helm-charts) (for development use cases)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| Cluster API              | `v1.7.7`                                 |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| Rancher Turtles | `>v0.13.0`                                | Using [Rancher UI](./install-rancher-turtles/using_rancher_dashboard.md) (recommended) or [Helm install](./install-rancher-turtles/using_helm.md) (for advanced use cases)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |

## Reference Guides

This section focuses on implementation details including
[architecture](./reference-guides/architecture/intro), how Rancher Turtles integrates with Rancher, and [Helm Chart configuration values](./reference-guides/rancher-turtles-chart/values).

## Tasks

In this section we cover additional [operational tasks](./tasks/intro) including basic `CAPIProvider` [installation](./tasks/capi-operator/basic_cluster_api_provider_installation), an [example](./tasks/capi-operator/add_infrastructure_provider) AWS infrastructure provider install using `CAPIProvider`, and [upgrade instructions](./tasks/maintenance/early_adopter_upgrade) for early adopters of Rancher Turtles.

## Developer Guide

This section describes [how to get involved](./developer-guide/contributing_guidelines) in the development of Rancher Turtles as well as [how to setup a local development environment](./developer-guide/development), if you wish to do so.

## Reference

This section has a useful [glossary](./reference/glossary) to help you navigate Rancher and Cluster API concepts.


## Security

Rancher Turtles meets [SLSA Level 3](https://slsa.dev/spec/v1.0/levels#build-l3) requirements as an appropriate hardened build platform, with consistent build processes, and provenance distribution. This section contains more information on security-related topics:

- [SLSA](./security/slsa)
