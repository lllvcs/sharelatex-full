# sharelatex-full (Overleaf)

[![GitHub license](https://img.shields.io/github/license/lllvcs/sharelatex-full)](https://github.com/lllvcs/sharelatex-full/blob/master/LICENSE)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/lllvcs/sharelatex-full/build-test.yml)](https://github.com/lllvcs/sharelatex-full/actions/workflows/build-test.yml)
[![GitHub issues](https://img.shields.io/github/issues/lllvcs/sharelatex-full)](https://github.com/lllvcs/sharelatex-full/issues)
[![Docker Pulls](https://img.shields.io/docker/pulls/lvcs/sharelatex-full)](https://hub.docker.com/r/lvcs/sharelatex-full)

Extended Overleaf Docker Image.
Current Features include:

- fully updated TeX Live installation, including all available packages
- support for minted
- support for `svg`-images through the addition of inkscape
- support for lilipond
- shell-escape enabled by default
- Additional fonts: `texlive-fonts-recommended`, `texlive-fonts-extra`, `fonts-noto`, `fonts-dejavu` and other Chinese fonts.

Have a look at the [Dockerfile](./Dockerfile) to find out more.

## Installation

### Overleaf Toolkit

Use the [Overleaf Toolkit](https://github.com/overleaf/toolkit) as described in the [Quick-Start Guide](https://github.com/overleaf/toolkit/blob/master/doc/quick-start-guide.md).
Make sure to set the `OVERLEAF_IMAGE_NAME=tuetenk0pp/sharelatex-full` variable in `config/overleaf.rc`.

Alternatively, you can use a `compose.override.yaml` file as described [here](https://github.com/overleaf/toolkit/blob/master/doc/configuration.md#the-docker-composeoverrideyml-file).
Example:

``` yml
services:
    sharelatex:
        image: lvcs/sharelatex-full
```

### Docker Compose

> [!WARNING]
> This method is not recommended. Use the Overleaf Toolkit instead.

Use the [docker-compose.yml](https://github.com/overleaf/overleaf/blob/main/docker-compose.yml) provided in the [official GitHub](https://github.com/overleaf/overleaf), but change the image to ``lvcs/sharelatex-full``.
Also, note the additional instructions in the [official Wiki](https://github.com/overleaf/overleaf/wiki/Release-Notes--4.x.x#manually-setting-up-mongodb-as-a-replica-set).
