---
title: "🐕 Learn how to configure k9s"
linkTitle: "k9s"
type: docs
weight: 10 #<-- weight for pages under /docs/congiguration/
description: >
    Learn the basics about configuring k9s
---

## Under the hood

K9s leverages [XDG](https://specifications.freedesktop.org/basedir-spec/latest/) to keep its configuration files under `$XDG_CONFIG_HOME/k9s`. The default configuration will vary across operating system so be sure to read up on the default location if you choose not to set that environment variable. The main configuration file is named config.yaml and stores various K9s specific bits.

For information on the default locations for your OS please see [this link](https://github.com/adrg/xdg/blob/master/README.md). If you are still confused a quick k9s info will reveal where k9s is loading its configurations from.

|Unix|MacOS|Windows|
|----|-----|-------|
|`~/.config/k9s`|`~/Library/Application Support/k9s`|`%LOCALAPPDATA%\k9s`|

Alternatively, you can set `K9S_CONFIG_DIR` to tell k9s the directory location to pull its configurations from.

## k9s CLI configuration

{{% pageinfo color="warning" %}}
This is still in flux and will change while in pre-release stage!
{{% /pageinfo %}}

| Option                  | Comment / Description  |  Default |
|-------------------------|---------------------------------------------------------------------------------------|----------------|
| liveViewAutoRefresh                   | Enable periodic refresh of resource browser windows.| `false` |
| refreshRate                           | Represents ui poll intervals.| `2s` |
| maxConnRetry                          | Number of retries once the connection to the api-server is lost.| `15` |
| readOnly                              | Specifies if modification commands like delete/kill/edit are disabled.| `false` |
| noExitOnCtrlC                         | Toggles whether k9s should exit when CTRL-C is pressed.| `false` |
| ui.enableMouse                        | Enable mouse support.| `false` |
| ui.headless                           | Set to true to hide K9s header.| `false` |                        
| ui.logoless                           | Set to true to hide K9s logo.| `false` |                           
| ui.crumbsless                         | Set to true to hide K9s crumbs.| `false` |
| ui.reactive                           | Toggles reactive UI.|`false` |              
| ui.noIcons                            | Toggles icons / emoji display as not all terminal support these chars | `false` | 
| skipLatestRevCheck                    | Toggles whether k9s should check for the latest revision from the Github repository releases. | `false` |
| disablePodCounting                    | Disable count pods while in node view.| `false` |
| shellPod.image                        | The shell pod image to use | `busybox:1.35.0` |
| shellPod.namespace                    | The namespace to launch to shell pod into | `default` |
| shellPod.limits.cpu                   | CPU limit on the shell pod | `100m`|
| shellPod.limits.memory                | Memory limit on the shell pod | `100Mi` |
| shellPod.tty                          | Enable TTY | `true` |
| imageScans.enable                     | Enables image scans | `false` |
| imageScans.exclusions.namespaces      | List of namespaces to exclude |  |
| imageScans.exclusions.labels          | Key-Value pairs of labels to exclude |  |


## @TODO: rewrite/reformat/etc
| Option                  | Comment / Description  |  Default |
|-------------------------|---------------------------------------------------------------------------------------|----------------|
| logger.tail                           | Defines the number of lines to return | `100` |
| logger.buffer                         | Defines the total number of log lines to allow in the view | `1000` | 
| logger.sinceSeconds                   | Represents how far to go back in the log timeline in seconds | `-1`|
| logger.fullScreen                     | Go full screen while displaying logs.| `false` |    
| logger.textWrap                       | Toggles log line wrap.| `false` |                     
| logger.showTime                       | Toggles log line timestamp info.| `false` |
| thresholds.cpu.critical               | Global memory/cpu thresholds. When set will alert when thresholds are met. |  |
| thresholds.cpu.warn                   | Global memory/cpu thresholds. When set will alert when thresholds are met. | |
| thresholds.memory.critical            | Global memory/cpu thresholds. When set will alert when thresholds are met.|
| thresholds.memory.warn                | Global memory/cpu thresholds. When set will alert when thresholds are met.|


## Example config file

{{< readfile "/shared/configs/k9s-default-config.md" >}}