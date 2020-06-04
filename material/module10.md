# Essential system services

+ Keep your computers synchronized and accurate
+ Helps with scheduled jobs e.g Backups
+ Helps with caching and logging
+ Helps identify when issues may occur
+ Time-dependent applications require very accurate clocks

`date +%s` // UNIX time (*seconds since 1.1.1970*)

ntpdate query remote time server
`ntp` - ensures computer always has the right time

pool.ntp.org
`hwclock` - hardware clock
`sudo hwclock --systohc --localtime`
`/etc/adjtime` - type of time UTC/LOCAL/...

### chrony and timedatectl

__________________________________________________________________
chrony - versatile implementation of Network Time Protocol (ntp)  |
can use reference clocks like a GPS receiver                      |
manual input using a wristwatch and keyboard                      |
designed to perform well in a wide range of conditions            |
* intermittent network connections                                |
* changing temperatures                                           |
* virtual machines                                                |
__________________________________________________________________|

`chronyc` - CLI program
`chronyc tracking` (see time info)
`chronyc sources` (get the sources list)
`timedatectl` - gives local, universat, rtc time, timezone and more
`sudo timedatectl set-time "YYYY-MM-DD HH:MM:SS"` // not allowed when time synchronization is enabled
`timedatectl list-timezones` - lists the timezones
`timedatectl set-timezone <timezone name>`
`timedatectl set-ntp false/true` - use the `ntp` or not

### System logging

##### syslog

+ Message logging standard
+ Separates
+ Message generator
+ Message storage
+ Message reporter
+ Message analyser
+ Each message has a facility code indicating:
+ Software type
+ Severity label
+ Used for:
+ System management
+ Security auditing
+ General information
+ Analysis
+ Debugging messages

`rsyslogd` is used
lives in `/etc/rsyslog.d`
logs found `/var/log/syslog`
`/etc/logrotate.conf` - additional information and settings about logs

`journalctl`
- Queries and displays messages from the `systemd` journal
- with `-b` - see messages from this boot
- with `-<num>` - see logs from `<num>` boots ago
- with `-u <service>` - logs from services

`rsyslog` is the system logging implementation on the system
+ can be configured to receive logs from systemd-journald

`systemd-cat` - manually send logs to `systemd-journal` with `systemd-cat`

##### Mail Transfer Agent basics - MTA

+ `sendmail`
+ `postfix`
+ `qmail`
+ `exim`

##### Aliases

ceo@domain.com => ryan@domain.com
staff@domain.com => will forward to anyone in staff (with `@domain.com`)


`mutt` - m to prompt to & subject fields, $ refreshes the window
`newaliases` - rebuilds the aliases

`.forward` - file in home directory; where to forward the mails
`mailq` - the mail queue

##### Printers and printing in Linux

`CUPS` - common UNIX printing system
  + The new standard
  + Manages print jobs and queues
  + Provides networking printing
  + Supports a very large range of printers
  + Provides web-based configuration and administration tool

install `cups` and `cups-bsd`
`/etc/cups/cupsd.conf`

`lpr` - printing command
`cupsdisable <printer name>` - disables the printer
`cupsenable <printer name>` - enables the printer
