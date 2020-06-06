# Security

### Perform security administration tasks

`sudo find / -perm /u = s, g = s [| xargs ls -lad]` - find files with user permission set to S.U.ID bit and the group permission to S.G.ID

Can also work with different file types via `-type <f|l|...>`

`passwd` - change this user's password

Root can change ***anyone's*** password with: `sudo passwd <username>`

`nmap <host>` - port scanner (e.g `nmap localhost`)

`netstat -at` - all active Internet connections

`lsof` - list open files

`who` - who is logged in

`w` - `who` with more info

`last` - history of everyone who is logged in to the system (reeboots and who logged in)

`sudo visudo` - opens the *sudoers* file (or `/etc/sudoers.tmp`)
Sudoers file lets root decide who can have superuser privileges

`id` - check id and group membership

`ulimit` - provides control over the resources available to the shell and processes it creates, only on systems, which allow for such a control

`su (+ password prompt)` - change user (or go root)

### Set up host security

**Shadow passwords**

`/etc/hosts.allow` - shows whitelisted users or domains, which can access the system

`/etc/hosts.deny` - shows blacklisted users or domains with no access permission

`nologin` - prevents unprivileged users from logging into the system

`xinetd` - listens for incoming requests over a network and launches appropriate proigram to handle it; comes with protection from port scanning

`xinetd` files are in `/etc/xinetd.conf` and `/etc/inetd.conf`

`tcpd`
+ monitor incoming requests
+ program triggered by xinetd
+ xinetd starts tcpd instead of desired server
+ tcpd logs the request and additional checks
+ tcpd runs the appropriate program
+ logs are sent to syslog
+ has access control that also uses `/etc/hosts.allow` and `/etc/hosts.deny`

### systemd sockets

> A **socket** is a way for 2 different processes to share data, either locally or over a network.
> Useful and the basis of useful programs, such as *SSH*, *chat programs*, *file transfer*...

`/lib/systemd/system/ssh.socket`

### Securing data with encryption

SSH - remotely connect to any other Linux or Unix system securely (good for confidential or sensitive information or files)

`/etc/ssh/ssh_config` - change secure shell configuration

`/etc/ssh/sshd_config` - change setting of own shell for foreign connections

***ssh keys***
+ used for passwordless authentication
+ generate 2 keys (a "*keypair*")
	- private key is for personal use, to be kept save and never be given to anyone
	- public key can safely be copied to servers as needed

`ssh-keygen` - generates a key pair

`eval ssh-agent -s` - adds an .env variable

`ssh-add` - adds keys to env as recognizable

GPG - free implementation of PGP; allows encryption and signing of data and can prove some data is tampered or not

| Command                                                            | Return value                  |
| ------------------------------------------------------------------ | ----------------------------- |
| `gpg --gen-key`                                                    | generates a gpg key           |
| `gpg --list-keys`                                                  | lists gpg keys                |
| `gpg --send-keys --keyserver <server link> <key id>`               | sends a key to a server       |
| `gpg --search-keys --keyserver <server link> <email|key id|...>    | searches for a key on server  |
| `gpg --keyserver <server link> --recv-key <key id>                 | receive a key from the server |
| `gpg --encrypt --recipient <user id | name> <key id>               | encrypts a file with the key  |
| `gpg --decrypt <filepath & name> > <new filename>                  | decrypts a file with the key  |

### New encryption

1. ECDSA - OpenSSH 5.7
1. ED25519 - OpenSSH 6.5

`ssh-keygen -t ecdsa` - the `-t` flag allows for type specification
