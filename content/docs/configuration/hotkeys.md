---
title: "🔑 Define hotkeys for maximum productivity!"
linkTitle: "Hotkeys"
type: docs
weight: 20 #<-- weight for pages under /docs/congiguration/
description: >
    Hot, Hotter, 🔥🔑
---

## Quick overview

Config file
: `$XDG_DATA_HOME/k9s/hotkeys.yaml`

Format
: `hotKeys` top-level object with items in format
```yaml
shortCut:    String
description: String
command:     String
```

See [complete example]({{< relref "#example" >}}) below

## Overview

Entering the command mode and typing a resource name or alias could be cumbersome for navigating thru often visited resources. By leveraging `hotkeys`, k9s can be configured to quickly navigate to your favorite resources. To enable custom hotkeys, first create a config file in `$XDG_DATA_HOME/k9s/hotkeys.yaml`, then add your hotkeys to the new and shiny `hotkeys.yaml` file. 

{{< content-info title="Tip" color="info" >}}
You can use resource names and short name to specify a command the same way as if typed in <a href='{{< ref "docs/getting-started/modes#command-mode" >}}'>command mode</a>.
{{< /content-info >}}

Not feeling so hot? Your custom hotkeys will be listed in the help view, which can be accessed by typing `?`. The hotkey file will be automatically reloaded so you can readily use your hotkeys as you define them.

You can choose any keyboard shortcuts that make sense to you, provided they are not part of the standard k9s shortcuts list.

## Example

{{< content-info title="Warning" color="warning" >}}
This configuration might change in the future!
{{< /content-info >}}

{{< readfile "/shared/configs/hotkeys.md" >}}