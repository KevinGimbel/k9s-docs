---
title: "☸️ Use k9s' per-cluster configuration"
linkTitle: "Cluster"
type: docs
weight: 80 #<-- weight for pages under /docs/congiguration/
description: >
    Learn how to configure k9s on a per-cluster basis
---

## Quick overview

- k9s can use per-cluster config files which overwrite the global configuration in `$XDG_DATA_HOME/k9s`
- Base path `$XDG_DATA_HOME/k9s/cluster-x/context-y/` where `cluster-x` is the cluster name and `context-y` the context
- All config files can be placed in a sub-directory for cluster specific configuration.
    - `$XDG_DATA_HOME/k9s/cluster-x/context-y/config.yaml`
    - `$XDG_DATA_HOME/k9s/cluster-x/context-y/skin.yaml`
    - `$XDG_DATA_HOME/k9s/cluster-x/context-y/aliases.yaml`
    - `$XDG_DATA_HOME/k9s/cluster-x/context-y/hotkeys.yaml`
    - `$XDG_DATA_HOME/k9s/cluster-x/context-y/plugins.yaml`

## Overview