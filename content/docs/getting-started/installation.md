---
title: "Installation"
linkTitle: "Installation"
type: docs
weight: 10
description: All you need to know to install k9s
---

K9s is available on Linux, macOS and Windows platforms.
Binaries for Linux, Windows and Mac are available as tarballs in the [release page](https://github.com/derailed/k9s/releases).

## MacOS

### Homebrew

Via [Homebrew](https://brew.sh/) for macOS or Linux

 ```shell
 brew install derailed/k9s/k9s
 ```

### MacPorts

Via [MacPorts](https://www.macports.org)

 ```shell
 sudo port install k9s
 ```

## Linux

### Snap

Via [snap](https://snapcraft.io/k9s) for Linux

```shell
snap install k9s --devmode
```

### Arch

On Arch Linux

```shell
pacman -S k9s
```

### OpenSUSE

On OpenSUSE Linux distribution

```shell
zypper install k9s
```

## BSD

On FreeBSD

```shell
pkg install k9s
```

## Windows

### Winget

[Winget](https://github.com/microsoft/winget-cli) for Windows

```shell
winget install k9s
```

### Scoop

[Scoop](https://scoop.sh) for Windows

```shell
scoop install k9s
```

### Chocolatey

[Chocolatey](https://chocolatey.org/packages/k9s) for Windows

```shell
choco install k9s
```

## Generic

## Go

**Note:** Installing via Go will install the dev version of the master branch! It is recommended to use another installation method.

```shell
go install github.com/derailed/k9s@latest
```

## pkgx

[pkgx](https://pkgx.dev/pkgs/k9scli.io/) for Linux and macOS

```shell
pkgx k9s
```


## Webi
[Webi](https://webinstall.dev) for Linux and macOS...

```shell
curl -sS https://webinstall.dev/k9s | bash
```

...and Windows

```shell
curl.exe -A MS https://webinstall.dev/k9s | powershell
```

## Docker Desktop Extension

As a [Docker Desktop Extension](https://docs.docker.com/desktop/extensions/) (for the Docker Desktop built in Kubernetes Server)

```shell
docker extension install spurin/k9s-dd-extension:latest
```

## Building From Source

K9s is currently using GO v1.22.X or above.
In order to build K9s from source you must:

1. Clone the repo [derailed/k9s](https://github.com/derailed/k9s)
2. Build and run the executable

```shell
make build && ./execs/k9s
```

## Docker

For a guide on Running k9s via Docker, see [Docker](/docs/getting-started/docker)