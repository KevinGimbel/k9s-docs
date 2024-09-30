---
title: "Running with Docker"
linkTitle: "Running with Docker"
type: docs
weight: 15
description: Learn how to use k9s in Docker
---

## Running with Docker

### Running the official Docker image

You can run k9s as a Docker container by mounting your `KUBECONFIG`:

```shell
docker run --rm -it -v $KUBECONFIG:/root/.kube/config quay.io/derailed/k9s
```

For default path it would be:

```shell
docker run --rm -it -v ~/.kube/config:/root/.kube/config quay.io/derailed/k9s
```

### Building your own Docker image

You can build your own Docker image of k9s from the [Dockerfile](Dockerfile) with the following:

```shell
docker build -t k9s-docker:v0.0.1 .
```

You can get the latest stable `kubectl` version and pass it to the `docker build` command with the `--build-arg` option.
You can use the `--build-arg` option to pass any valid `kubectl` version (like `v1.18.0` or `v1.19.1`).

```shell
KUBECTL_VERSION=$(make kubectl-stable-version 2>/dev/null)
docker build --build-arg KUBECTL_VERSION=${KUBECTL_VERSION} -t k9s-docker:0.1 .
```

Run your container:

```shell
docker run --rm -it -v ~/.kube/config:/root/.kube/config k9s-docker:0.1
```