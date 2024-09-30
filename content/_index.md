---
title: "k9s docs"
linkTitle: Home
weight: 0
---

{{< blocks/cover title="Welcome to the k9s-docs!" image_anchor="top" height="auto" color="primary" >}}
{{< readfile "/shared/k9s-about-short.md" >}}

Want to learn how to use k9s? Jump right into the [Docs](docs)!
{{< /blocks/cover >}}

{{< blocks/section type="row" color="primary" >}}

{{% blocks/section color="white" %}}

## Who let the pods out? 🐕

{{< readfile "/shared/k9s-about-long.md" >}}
{{% / blocks/section %}}

{{% blocks/section color="white" %}}

## Features 🤖

**Information At Your Finger Tips!**
Tracks in real-time activities of resources running in your Kubernetes cluster.

**Standard or CRD?**
Handles both Kubernetes standard resources as well as custom resource definitions.

**Cluster Metrics**
Tracks real-time metrics associates with resources such as pods, containers and nodes.

**Power Users Welcome!**
Provides standard cluster management commands such as logs, scaling, port-forwards, restarts…

Define your own command shortcuts for quick navigation via command aliases and hotkeys.

Plugin support to extend K9s to create your very own cluster commands.

Powerful filtering mode to allow user to drill down and view workload related resources.

**Error Zoom**
Drill down directly to what’s wrong with your cluster’s resources.

**Skinnable and Customizable**
Define your very own look and feel via K9s skins.
Customize/Arrange which columns to display on a per resource basis.

**Narrow or Wide?**
Provides toggles to view minimal or full resource definitions

**MultiResources Views**
Provides for an overview of your cluster resources via Pulses and XRay views.

**We’ve got your RBAC!**
Supports for viewing RBAC rules such as cluster/roles and their associated bindings.
Reverse lookup to asserts what a user/group or ServiceAccount can do on your clusters.

**Built-in Benchmarking**
You can benchmark your HTTP services/pods directly from K9s to see how your application fare and adjust your resources request/limit accordingly.

**Resource Graph Traversals**
K9s provides for easy traversal of Kubernetes resources and their associated resources.

{{% / blocks/section %}}
{{< / blocks/section >}}