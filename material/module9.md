# User and group account management and relates system files

+ `/etc/passwd` - **username, encrypted password, userid, groupid (primary), comment/info field, homedir, shell** of *user*
+ `/etc/shadow` - **username, password, number of days since 1.1.1970 since the pass was changed, minimum nr of days required between 2 pass changes, 0 and 5 nines means the pass won't expire (when it expires is the field), days before the pass will expire - warning delay**
+ `/etc/skel` - **skeleton directory** - *base for user*

### Adding

`useradd`, `adduser` (can be used to add to groups)
``groupadd``, ``addgroup``
`chage` - for password changing
`userdel`, `groupdel`

### Automating the system

+ `at` - custom shell for jobs at different time
+ `atq` - checks jobs
+ `atrm` <JOB ID> - remove job
+ `atd` - run jobs queued for execution

```bash
name@host:/$ at 4 PM
at> ps aux
at> <Ctrl + D>
```

`/etc/at.deny` - list of blackilisted users
`/etc/at.allow` - list of users who can run `at`

+ `crontab -e` (prompts: minute, hour, month, day of week, user, command)
+ files: `/etc/cron.daily|weekly|monthly`
+ `/etc/cron.allow`
+ `anacron`: `/etc/anacrontab` - runs immediately

### Unit use

`systemctl list-timers`
`/lib/systemd/system/apt-daily.timer`
`systemd-run --on-active=60 /bin/touch /tmp/file.txt`

### Localization and internationalization

`date` - date
`timezone` - timezone
`/etc/localtime` - symlink to /usr/share/zoneinfo/<country>/<city>
`tzselect` - select a timezone
`timedatectl` - query + change system clock
`locale` - formatted times and countries
`iconv` - convert between different character encodings (shows supported)
`file` - gives back the encoding

`/etc/group` - group passwords stored
