```yaml
# $XDG_CONFIG_HOME/k9s/aliases.yaml
aliases:
  # Use `pp` as an alias for Pod
  pp: v1/pods

  # Use `dep` as an alias for Deployments
  dep: apps/v1/deployments

  # Use `fred` as an alias for CRD Frederick
  fred: acme.io/v1alpha1/fredericks

  # Defines a `pos` alias for a command listing all pod in kube-system matching labels app=fred and blee=duh
  pos: pod kube-system app=fred,blee=duh
```