# Devices, filesystems and filesystem hierarchy

### Partitions

`lsblk` - see the disks

`sudo fdisk /<path>` - creates a partition of a disk

`sudo parted /<path>` - creates a partition

`mkpart` - parted make partition command

### Filesystem

- `ext`
- `ext2` - dev'd in 1993
- `ext3` - dev'd in 2001
- `ext4` - dev'd in 2008
- `reiserfs` - 2001
- `btrfs` - binary tree
___

`mkfs` - make filesystem

with sudo

Mount

1. `mkdir`
1. `mount /mountee /mounter`
1. `umount /mounter`
1. `mkswap /mountee`
1. `swapon /mountee`


### iNodes

+ Describe file or directory
+ Stores attributes
	- Last time of change/access/modification
	- Owner/permission data
+ Stores Disk Location
+ Directory is a list of names assigned to iNodes
	- Contains entry for itself, its parent and its children
+ You can run out of iNodes

1. `ls -i <file>` - lets you see the iNode
1. `df -i` - also iNodes
1. `du` - also iNodes
1. `[sudo] du -h [--max-depth=1] /<path>` - size and files in this folder

> `fsck` - check or repair any problems it may find with the filesystem

### Misc with fs

+ `dumpe2fs`
+ `tune2fs`
+ `xfs_db /<path>` - examines or debugs
+ `cat /proc/self/mounts` - same as mount command
+ `/etc/fstab` - mountable
+ `blkid` - lists filesystems with ID

### Manage disk quota

defaults, usrquota

`sudo quotacheck -avugc`

User sees only their stuff or all if root.

`edquota -u [username]` - opens default editor with quota info

`repquota /<path>` - shows used quotas

### Permissions and ownership

+ rwx rw- r--
+ => file: d = directory, l = link

`rwx` => user permissions

`rw-` => group permissions

`r--` => other permissions

`chmod u+[options: r,w,x, rw,rx, xw, rwx] <filename>`

##### Numerical presentation: BASIC

| Notation | Octal | Decimal | Description       |
| -------- | ----- | ------- | ----------------- |
| ---      | 000   | 0       | No permissions    |
| --x      | 001   | 1       | Execute-only      |
| -w-      | 020   | 2       | Write-only        |
| -wx      | 021   | 3       | Write and execute |
| -r-      | 040   | 4       | Read-only         |
| r-x      | 401   | 5       | Read and execute  |
| rw-      | 420   | 6       | Read and write    |
| rwx      | 421   | 7       | All permissions   |

> `setuid/setgid` - run the program as the owner (`+s` in letters, so `rwxs`)
> `sticky bit` - prevents the user from deleting a folder (`+t`) even with permission

##### Numerical presentation: ADDITIONAL

| # | Description         | Notation            |
| - | ------------------- | ------------------- |
| 0 | nothing set         | --- --- ---         |
| 1 | sticky bit set      | --- --- --t         |
| 2 | setgid set          | --- --s ---         |
| 3 | setgid & sticky bit | --- --s --t         |
| 4 | setuid              | --s --- ---         |
| 5 | setuid & sticky bit | --s --- --t         |
| 6 | setuid & setgid     | --s --s ---         |
| 7 | all 3 set           | --s --s --t         |

`chmod 1764 filename`

`chown` & `chgrp`

`chown/chgrp <username> <filename>`

`chown uname:grp <file>`

`umask` - see default permissions and supressed permissions

`umask 0044` - changes umask defaults

### Links

+ Files are represented by iNode
+ Files are only deleted when all links to an iNode are removed
+ A hard link is a link to another file's iNode and it can only occur on the same filesystem
+ A soft (symbolic) link is a link to another filename, ant it can occur across different filesystems


`ln <file to link> <file to link with>` - links the first file to the second (this is a hard link)

`ln -s (symbolic link) /etc/ blah` - makes a symbolic link between etc and blah


### Find files and place them in the correct place

`which` - find the source exec

`type` - tells what type of command the word is

`whereis` - locates the binary, source and man page if exists

`locate` - builds a db of fs and can be queried directly

`updatedb` - updates the previous command database
