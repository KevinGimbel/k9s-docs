---
title: "🔌 Define plugins to integrate tools with k9s"
linkTitle: "Plugins"
type: docs
weight: 40 #<-- weight for pages under /docs/congiguration/
description: >
    k9s + your-fav-tool = 💞
---
{{< content-info title="Warning" color="warning" >}}
Work in progress... Options and layout may change in future K9s releases as this feature solidifies.
{{< /content-info >}}

K9s allows you to extend your command line and tooling by defining your very own cluster commands via plugins. K9s looks at `$XDG_CONFIG_HOME/k9s/plugins.yaml` to locate all available plugins. You can further extend plugins behavior in a context specific configuration using `$XDG_DATA_HOME/k9s/clusters/clusterX/contextY/plugins.yaml`.

A plugin is defined as follows:

- `shortcut`: option represents the key combination a user would type to activate the plugin
- `description`: will be printed next to the shortcut in the k9s menu
- `scopes`: defines a collection of resources name/short-name for the views associated with the plugin. You can specify `all` to provide this shortcut for all views.
- `command`: represents ad-hoc commands the plugin runs upon activation
- `background`: specifies whether or not the command runs in the background
- `args`: specifies the various arguments that should apply to the command above

K9s does provide additional environment variables for you to customize your plugins arguments. Currently, the available environment variables are as follows:


| Variable                        | Description                                                                |
|---------------------------------|----------------------------------------------------------------------------|
| `$NAMESPACE`                    | the selected resource namespace                                            |
| `$NAME`                         | the selected resource name                                                 |
| `$CONTAINER`                    | the current container if applicable                                        |
| `$FILTER`                       | the current filter if any                                                  |
| `$KUBECONFIG`                   | the KubeConfig location                                                    |
| `$CLUSTER`                      | the active cluster name                                                    |
| `$CONTEXT`                      | the active context name                                                    |
| `$USER`                         | the active user                                                            |
| `$GROUPS`                       | the active groups                                                          |
| `$POD`                          | while in a container view                                                  |
| `$COL-<RESOURCE_COLUMN_NAME>`   | use a given column name for a viewed resource. Must be prefixed by `COL-`! |

{{< content-info title="Info" color="info" >}}
Take a look at some of the <a href="https://github.com/derailed/k9s/tree/master/plugins">Community Custom Plugins</a> contributed by your K9sers friends.
{{< /content-info >}}

## Example plugin

The example plugin runs the following `kuebctl` command when hitting the `Ctrl-L` key combination in the `pods` view.

```sh
kubectl logs -f $NAME -n $NAMESPACE --context $CONTEXT`
```

```yaml
# $XDG_CONFIG_HOME/k9s/plugins.yaml
plugins:

  # Defines a plugin to provide a `ctrl-l` shortcut to tail the logs while in pod view.
  fred:
    # Define a mnemonic to invoke the plugin
    shortCut: Ctrl-L
    # What will be shown on the K9s menu
    description: Pod logs
    # Collections of views that support this shortcut. (You can use `all`)
    scopes:
    - po
    # The command to run upon invocation. Can use Krew plugins here too!
    command: kubectl
    # Whether or not to run the command in background mode
    background: false
    # Defines the command arguments
    args:
    - logs
    - -f
    - $NAME
    - -n
    - $NAMESPACE
    - --context
    - $CONTEXT
```