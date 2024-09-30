---
title: "🥸 Custom Resource Aliases"
linkTitle: "Aliases"
type: docs
weight: 30 #<-- weight for pages under /docs/congiguration/
description: >
    Define custom aliases to reach resources faster
---


## Quick overview

Config file
: `$XDG_DATA_HOME/k9s/aliases.yaml`

Format
: `aliases` top-level object with `key-value` pairs

## Aliases

In k9s, you can define your very own command aliases (short-names) to access your resources. In your `$XDG_CONFIG_HOME/k9s` define a file called aliases.yaml. A k9s alias defines pairs of `alias:gvr` or `alias:command`. A `gvr` (Group/Version/Resource) represents a fully qualified Kubernetes resource identifier. The command can be any commands that you would normally use while in command prompt mode.

Aliases can be defined a two levels: global and context specific. At the global level you would create a file in `$XDG_CONFIG_HOME/k9s/aliases.yaml`. For context specific aliases, you can define `$XDG_DATA_HOME/k9s/clusters/clusterX/contextY/aliases.yaml`.


{{< content-info title="Warning" color="warning" >}}
As of v0.30.0 this file must have a `.yaml` extension. Also note the file name is pluralize as well as the top section of the section aka `aliases`
{{< /content-info >}}

## Example

The key is always the shortcut, the value the resource. So for example `pr: prometheusrule` defines `pr` as shortcut for the custom resource definition `prometheusrule`.

{{< readfile "/shared/configs/aliases.md" >}}