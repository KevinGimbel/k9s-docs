---
title: "🔑 Define hotkeys for maximum productivity!"
linkTitle: "Hotkeys"
type: docs
weight: 20 #<-- weight for pages under /docs/congiguration/
description: >
    Hot, Hotter, 🔥🔑
---

Entering the command mode and typing a resource name or alias could be cumbersome for navigating thru often visited resources. By leveraging `hotkeys`, k9s can be configured to quickly navigate to your favorite resources. In order to enable hotkeys please follow these steps:

- Create a file named `$XDG_DATA_HOME/k9s/hotkeys.yaml`
- Add thehotkeys to your new and shiny `hotkeys.yaml` ✨ 

{{< content-info title="Tip" color="info" >}}
You can use resource names and short name to specify a command the same way as if typed in <a href='{{< ref "docs/getting-started/modes#command-mode" >}}'>command mode</a>.
{{< /content-info >}}

Not feeling so hot? Your custom hotkeys will be listed in the help view `?`. Also your hotkey file will be automatically reloaded so you can readily use your hotkeys as you define them.

You can choose any keyboard shortcuts that make sense to you, provided they are not part of the standard k9s shortcuts list.

{{< content-info title="Warning" color="warning" >}}
This configuration might change in the future!
{{< /content-info >}}

{{< readfile "/shared/configs/hotkeys.md" >}}