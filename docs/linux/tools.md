# Linux Tools

## In ramdisk

### BusyBox

Self-explanatory. We need some basic tools and a shell and BusyBox is exactly that.

### xzminidec

Used to decompress BusyBox before `xzcat` is available.

### vtchmod

Used to make BusyBox before `chmod` is accessible.

On x86 it's also used to verify if 64-bit binaries are runnable.

### dmsetup

Used to create a block device from a list of blocks created by grub.

### vtoy_fuse_iso

Creates a fuse filesystem with an iso from the block map.

Used to mount the iso to extract the kernel module for `device-mapper`.

Required by:

- Puppy Linux

### vblade

Alternative to using `device-mapper`.

It's essentially an ATA over Ethernet server.

It's set up using the block map. Then kernel module `aoe` is loaded with `aoe_iflist=lo` (or loopback).

It's more layers of abstraction, so it's only used in extreme cases.

Required by:

- Tiny Core Linux
