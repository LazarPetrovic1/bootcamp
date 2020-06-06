1. Where are settings stored related to your local ssh server that a remote user will connect to? /etc/ssh/sshd_config is the correct file to configure your local ssh server. 
1. Which command will unencrypt a file using gpg? gpg --decrypt is used to unencrypt a file. 
1. Which application will monitor incoming connections on particular ports and then launch the appropriate daemon to handle the process? While tcpd will launch the appropriate program after logging it, xinetd is the application doing the monitoring and launching of tcpd and other applications. 
1. Which command will generate an ssh keypair for you? ssh-keygen will generate a ssh keypair. 
1. Which command is used to change someone elses's password? passwd can be used to change both yours and someone else's password. 
1. What does ulimit -u set? -u will set the maximum number of user processes. See 'help ulimit' for further information. 
1. Which command will let you edit the sudoers file? visudo will open the proper sudoers file, /etc/sudoers. 
1. Which command can be used to discover all open ports of a remote system? nmap is a port scanning application which will you show all open ports. 
1. Which file will stop all users but root logging in? /etc/nologin is the correct file. See man 5 nologin for further information. 
1. How can I change to the root user from my current terminal without logging out, using my own password? sudo su will use sudo to change to the superuser root, whereas su and ssh would both require root's password. 
