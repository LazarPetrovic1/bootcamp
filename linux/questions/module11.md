
1. What packet type does ping use? ping uses ICMP packets.
2. Which file is a 'local' version of DNS where you can give IP addresses their own entries for personal use? /etc/hosts is where you can list your own alias entries for IP addresses and hosts. 
3. Which command will display your route table and not resolve any of the IP addresses to hostnames? route -n will display the route table without resolving IP addresses. 
4. Which Linux command will list your active network interfaces? ipconfig may work in Windows, but ifconfig is the command used in Linux. -a will show all interfaces, not just your active ones. 
5. Which command will give you detailed information about a DNS entry, including the TTL it may use? dig will give you detailed information about a DNS entry. 
6. Which file lists the DNS nameservers which will be used to resolve IP addresses to hostnames? The nameservers to be used by the system are listed in /etc/resolv.conf. 
7. How many IP addresses are useable in a /29 subnet? A /29 covers 8 IP addresses (2^3 or 2^(32-29)). 2 must be reserved for the network and broadcast, so the remaining number of useable IP addresses is 6.
8. Which command will test the latency between your computer and a remote computer? ping will test the latency between two computers. 
9. Which Linux command can be used to track the path a packet takes between your computer and another target computer on the internet? traceroute and tracert do the same thing, but traceroute is the Linux command. tracert is the Windows command. 
10. Which file determines the order of which different services are used to resolve hostnames to IP addresses? nsswitch will list in order which services to use to resolve hostnames. 
