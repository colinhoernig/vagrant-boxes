# Vagrant Base Boxes

## Downloads

* **[CentOS-6.5-x86_64-v20140623.box](http://colinhoernig.io/downloads/vagrant-boxes/CentOS-6.5-x86_64-v2014023.box):** CentOS 6.5 x86\_64 Minimal *(VirtualBox Guest Additions 4.3.10, Chef 11.12.4, Puppet 3.5.1)*  
  <small>sha256sum: `9c3fa69e71615b7ec9884c1d4472dd83491dfe4353f209f4a7f21453fc68344c`</small>

## How these boxes were built

These boxes were automatically built using [packer](http://www.packer.io) (v0.6.0) and the definitions in this repo:

```sh
$ cd packer
$ ./build.sh
```

The definitions are based on the [veewee project's](https://github.com/jedi4ever/veewee) definitions for a minimal CentOS installation, but with a few modifications:

- The disk can grow to 40GB
- Provides 4GB of swap
- Fixes [slow DNS resolution](https://github.com/NREL/vagrant-boxes/issues/5)
