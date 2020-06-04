# BIOS

### Device boot order
*UEFI* vs *Legacy*

Bootable options: ***e*** to edit in *GRUB*
Important lines: linux line & initrd || initramfs
After root `filesys` attachment, `init` program executed, w/ `PID` of 1
(as seen by `ps aux | head`)

`sysvinit` - first commercial unix os
`systemd` - API and concurrent parallel processing during boot time
`upstart` - developed by Ubuntu

`dmesg` (`-T` => gives the date) - read all kernel msgs since boot time

`sudo loadkeys <lang>`

`udev`
	- Device manager
	- Low lvl access to linux device tree
	- Handles user space events like loading firmware
	- Mounted to `/dev` on startup

`dbus`
	- Inter process communication mechanism
	- Framework that allows processes to talk to each other
	- Secure and reliable
	- Provides high lvl object oriented programming interface
	- Can create rules

`sysfs`
	- Virtual filesystem
	- Presents information about various kernel subsystems: hardware devices and drivers eg
	- It's mounted to `/sys`

`procfs`
	- Similar to sysfs
	- Presents information about processes
	- Presents information about system information
	- Mounted to `/proc`
	- Can be used to interface with the kernel
	- Parameters can be changed on the fly

`lsmod` - see all modules in use
	- `rmmod` - **remove a module on the fly**
	- `modprobe` - **add a module on the fly**
	- `lspci` - **lists all pci devices**

**Run levels, boot targets and how to shutdown and reboot a system**

`run lvs:`
	**0 - halt or shutdown the system
	1 - single user mode - root password changing or recovery mode
	2 - multi-user mode without networking
	3 - normal boot
	4 - unused/customizable
	5 - run lv 3 + GUI display manager
	6 - reboot**

script execution

`sysvinit` way: `/etc/inittab`
`systemd` way:` /etc/systemd/system`; `/usr/lib/systemd/system`

`systemd` targets:

|   run lv  |  systemd target   |
| --------- | ----------------- |
|    -0-    | poweroff.target   |
|    -1-    | rescue.target     |
|  -2- -4-  | multi-user.target |
|    -3-    | multi-user.target |
|    -5-    | graphical.target  |
|    -6-    | reboot.target     |
| emergency | emergency.target  |

`init` || `telinit` - change runlevel

`init 0` - shutdown
`init 6` - reboot
`wall` - write message to all users
`systemctl` - all of the units that systemd is running
`sudo systemctl status <what>.target` - shows status of <what>
`sudo systemctl stop <what>.target` - kills <what> processes
`sudo systemctl start <what>.target` - starts <what> processes
