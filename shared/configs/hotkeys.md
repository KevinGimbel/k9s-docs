```yaml
# $XDG_DATA_HOME/k9s/hotkeys.yaml
hotKeys:

  # Hitting Shift-0 navigates to your pod view matching pods with labels app=kindnet
  shift-0:
    shortCut:    Shift-0
    description: Viewing pods
    command:     pods app=kindnet

  # Hitting Shift-1 navigates to your deployments
  shift-1:
    shortCut:    Shift-1
    description: View deployments
    command:     dp # <-- A shortcode `dp` can be used instead of `deployments`

  # Hitting Shift-2 navigates to your xray deployments
  shift-2:
    shortCut:    Shift-2
    description: XRay Deployments
    command:     xray deploy
```