# Design hard disk layout

### Hard disk stuff

1. `/usr` - **user binaries**
1. `/home` - **place to store own files**
1. `/boot` - **stuff for boot**
1. `/var` - **variable data**
1. `/tmp` - **temporary directory**

### Partitions

Dividing storage into separate pieces
- Allows dual booting
- Separation of files
- Data organization
- System protection

*Swap* partition - if RAM is full, this is used in its stead; cannot be accessed by a user

*LVM* - Logical volume manager
- Can split disks into pools (physical extents, PEs or pools)
- Create partitions from pools
- Can grow or shrink partitions depending on the circumstance when the need arises

GRUB commands
+ `grub-probe` --version - Gives grub version
+ `/boot` contains `/grub`
+ `menu.lst`, `grub.conf` or `grub.cfg` is the grub file (***NEVER EDIT***)
+ `/etc/grub.d` - scripts used to generate the grub files
+ `/etc/grub/defaults` - contains grub's defaults (CAN EDIT)
+ `which` - tells you where the command is running from
+ `update-grub` - updates grub config
+ `grub-install` - installs grub on another partition (e.g `/dev`)

### Libraries
  - write file to a disk
  - display something on screen
  - send files over networks

### Linking
  - static linking - library in the application
  - dynamic linking - the same library can be shared between links

`/etc/ls.so.conf/*.conf` - shared libraries

`ldconfig` - configure dynamic linker run-time bindings

Environment variables example

`export LD_LIBRARY_PATH=/home/<username>`

`echo $LD_LIBRARY_PATH` - prints what it is

`ldd` - shows what libraries the argument is linked to

`dpkg` - Debian package manager

`apt` - advanced packaging tool

`dpkg -l | less` - lists installed packages

`dpkg -i <packagename>` - installs package

`/etc/apt/sources.list` - txtfile with urls which apt checks for installations

`apt dist-upgrade` - deletes unneeded and updates needed

`RPM` and `YUM` packages

`rpm` - RedHat package manager like `dpkg`

`yum` - yellowdog updater modified, like `apt`

`sudo yum update` - updates centos

`yumdownloader` - used before `yum`

1. `rpm -qf /folder/item` - query format; tells what package it belongs to
1. rename the file `sudo mv`...
1. `rpm --verify <package name>`
1. rename it back
1. `sudo rpm -Va`
1. / in man file allows searching

`zypper` and `dnf`

`zypper` - used in `opensuse`

`zypper repos` - lists available repositories and those enabled

`sudo zypper refresh` - checks if all packages are up to date

`sudo zypper in git` - installs git

`sudo zypper remove --clean-deps git` - removes git and dependencies

`dnf` - can be installed to centos

`dnf info get` - looks at the details of the git package (might update stuff first)

`sudo dnf list` - compiles a long list of available packages

`dnf list installed` - lists installed

`dnf check-update` - checks which packages to update

`sudo dnf install git` - install the git package

`sudo dnf remove git` - removes the git package

### Linux as a virtualization guest

Advantages:
  - Multiple OS on the same computer
  - Extra hardware not necessary
  - Entire machines can be cloned, backed up and easily restored
  - Easy to manage and maintain
  - Protect the host machine

Disadvantages:
  - Less efficient due to accessing hardware indirectly
  - Performance may be hindered by the host

Containers - `Docker` && `Kubernetes`

> Data flow w/ containers: Computer > container > application

> Data flow w/o containers: Computer > hypervisor > different VMs with apps

Cloud computing - `AWS`, `Microsoft Azure`, `Google Cloud`

> The cloud > networking > storage service instead of managing own servers

cloud-init + docker image
+ Cloud instance initialization
+ A set of scripts that are executed when an instance is started
+ Applies user data to your instances automatically
+ Works with many popular operating systems
+ Works on almost all public clouds
	- `AWS`
	- `Microsoft Azure`
	- `Google Cloud Platform`
	- `Rackspace`, `IBM`, `Alibaba`, `CloudStack`, `Bigstep`, `Hetzner`, `Joyent`
