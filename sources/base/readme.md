# Drone Control yocto

This repository aims to provide a quick way to grab yocto layers and
build a demo image for the Kimchi Micro SBC with the drone-control daughter board

## Quick Start

Clone and update submodules

```
git clone https://github.com/teledatics/drone-control-yocto.git
cd drone-control-yocto
git submodule update --init
```

Create a build directory

```
MACHINE=drone-control DISTRO=fslc-wayland . ./setup-environment build-drone-control
```

Build an image

```
bitbake -k core-image-base
```

## Reusing an existing build directory

If you've already run a build and want to enter the bitbake environment again, you can simply run:

```
. ./setup-environment build-drone-control
```
