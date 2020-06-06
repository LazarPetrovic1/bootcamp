getent - Which command can be used to query certain database files on your system, such as /etc/services?
batch - Which command will let you run commands based on your system load? batch will run your specified commands when your system load is lower than a specified number, defaulting to 1.5.
anacron - Which application will run your scheduled jobs even if your machine was shut down when it was scheduled to run? anacron will run your scheduled jobs a certain amount of time after you turn your machine on if it was off when the job was scheduled to run.
group - Where are encrypted group passwords stored? While rarely used, a group can have a password. They are stored in /etc/group.
at - Which command will let you run another command at a specific time? 'at' is correct; although cron *will* run commands at a specific time, cron isn't a command. It's a daemon.
/etc/skel - Which directory is copied to a new user's home directory when a new user iscreated with adduser? /etc/skel is copied to a new users home directory when created with the adduser command.
chage - Which command can change user password expiry information? chage is used to change user password expiry information.
/etc/shadow - Where are encrypted user passwords stored? Encrypted passwords are stored in /etc/shadow. That's why only root can access it.
LC_ALL - Which LC variable shown by the 'locale' command will override all other LC variables? If it is set, LC_ALL will override all locales shown when you type locale.
