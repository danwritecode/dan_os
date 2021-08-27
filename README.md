# Building OS from Scratch

All credit goes to [this YouTube tutorial series](https://www.youtube.com/playlist?list=PLZQftyCk7_SeZRitx5MjBKzTtvk0pHMtp).


## Setup

Build an image for our build-environment:
```
docker build buildenv -t dansos
```

## Build

Enter build environment:
```
docker run --rm -it -v "$(pwd)":/root/env myos-buildenv
```

Build for x86:
```
make build-x86_64
```

## Emulate
```
qemu-system-x86_64 -cdrom dist/x86_64/kernel.iso
```
