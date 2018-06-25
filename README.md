# docker-node-zfs-base
Base docker image for node applications that interact with zfs and/or hard drive SMART status.

Based on [fedora](https://hub.docker.com/_/fedora/), adds:
1. [zfs](http://zfsonlinux.org/)
1. [node](https://nodejs.org/)
1. [yarn](https://yarnpkg.com)
1. [smartmontools](https://www.smartmontools.org/)

This image is really only useful when run with the [privileged flag](https://docs.docker.com/engine/reference/commandline/run/#full-container-capabilities---privileged) set to `true`.

```
docker run --privileged murrayju/node-zfs-base smartctl -a /dev/sda
```
