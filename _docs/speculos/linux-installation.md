---
title: Linux installation
subtitle:
tags: []
author:
layout: doc_sp
---

#### Sections in this article
{:.no_toc}
* TOC
{:toc}

## Requirements

For Debian (version 10 "Buster" or later) and Ubuntu (version 18.04 or later):

```sh
sudo apt install \
    cmake gcc-arm-linux-gnueabihf libc6-dev-armhf-cross gdb-multiarch \
    python3-pyqt5 python3-construct python3-flask-restful python3-jsonschema \
    python3-mnemonic python3-pil python3-pyelftools python3-requests \    
    qemu-user-static
```

For optional VNC support, please also install `libvncserver-dev`:

```sh
sudo apt install libvncserver-dev
```

## Build

### speculos

```sh
cmake -Bbuild -H.
make -C build/
```

Please note that the first build can take some time because a tarball of OpenSSL
is downloaded (the integrity of the downloaded tarball is checked) before being
built. Further invocations of `make` skip this step.

The following command line can be used for a debug build:

```sh
cmake -Bbuild -DCMAKE_BUILD_TYPE=Debug -H.
```

### VNC support (optional)

Pass the `WITH_VNC` option to CMake:

```sh
cmake -Bbuild -H. -DWITH_VNC=1
```
