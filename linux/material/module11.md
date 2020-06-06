# FUNDAMENTALS OF INTERNET PROTOCOLS

### IP address

+ Number assigned to your computer
+ Allows other computers to communicate with yours
+ Public and private IP addresses are available
+ IPv4 and IPv6

##### IPv4
	+ 32 bit addresses
	+ max 2^32 addresses (~ 4.3B)
	+ contains 4 octets
	+ Router > Router > Router > Your network's router > Your computer
	+ Needs:
		- Network address (e.g 172.16.254)
		- Host address (e.g 0.0.0.1)
		- Subnet mask (255.255.255.0) - turn on network bit and turn off host bits
	+ CIDR - classless interdomain routing (method of splitting IP addresses)
	+ 172.16.254.0/24 - means there are only 24 IP addresses in this network (24 of 32 bits are used)

##### IPv6
	+ 128 bit addresses
	+ allows for over to **340 undecillion** (~ 340 * 10^36) addresses
	+ leading zeroes in 4 bit groups can be omitted
	+ consecutive groups of zeroes can be replaced with double colon (::)
	+ 2001:0db8:0000:0000:0000:ff00:0042:8329 becomes 2001:db8::ff00:42:8329

When a PC is added machines on the network try to determine its MAC or hardware address; needed before sending anything

IPv4 uses `ARP` - address resolution protocol
+ Determines IP via `DNS`
+ Sends packet to all computers asking for Hardware/MAC address
+ Computer responds from known IP with its Hardware/MAC address

IPv6 uses Neighbourhood discovery
+ Improvements over `ARP`
+ Unreachability detection
+ Improves robustness of packet delivery

Private IPs
+ Uses private IP address space
+ Not allocated to any specific organization
+ Can be used by anyone anytime they want
+ `NAT` or proxy are required to connect to the Internet

Packet types;
+ TCP
	- Transmission control protocol
	- Connection oriented protocol
	- Siuted for high reliability applications
+ UDP
	- User datagram protocol
	- Connectionless protocol
	- Suited for applications that need fast but stateless transmission (e.g streaming videos)
+ ICMP
	- Internet control message protocol
	- Used by network devices
	- Send error messages and operational information

### PORTS

| PORT | SERVICE |
| ---- | ------- |
|  21  |   FTP   |
|  22  |   SSH   |
|  23  |  Telnet |
|  25  |   SMTP  |
|  53  |   DNS   |
|  80  |   HTTP  |
| 110  |   POP3  |
| 143  |   IMAP  |
| 443  |  HTTPS  |

`/etc/services`

Ports up to 1024 are **privileged** (root only)

### Basic network configuration

`ifconfig` - *interface configuration* (shows all of the active interfaces) (`-a` flag to see all available)

`ifdown` - *takes an interface down*

`ifup` - *brings the interface up*

`/etc/network/interfaces`

`sudo ifconfig <interface> <new ip addr>` - *changes the IP address of the interface*

`ip a` - *list all the interfaces as well*

`route`

`sudo route add default gw [gateway] <gateway>` - *add a default gateway*

`/etc/host` - used for talking to other computers before `DNS` existed

`/etc/host` is a table of: `<ip> <domain> <alias>`

`/etc/nsswitch.conf` - how to look up certain name server information and in what order

Files > (host to IP *done* or **not found**) > mdns4 (resolve IP *done* or **not found**) > res w/ NOTFOUND

DNS for external addresses

### More network configuration

`nmcli` - network manager cli

`nmcli general permissions` - lists all of the permissions

`nmcli general logging` - print logs

`hostnamectl` - admin separate classes of hostnames on the system

`hostnamectl set-hostname <hostname>` - changes the hostname on next shell login


### Basic network troubleshooting

`ifdown` and `ifup` in conjunction will also reset the IP address of the interface

`host <address>` - gets IP from DNS or the other way around

`hostname` - get hostname

`dig <address>` - similar to host, DNS lookup utility used to query name servers

`netstat` - network connections, routing tables & network interface statistics

`ping` - sends an ICMP packet to the remote server and waits to receive one & measures time it took

`ping6` - ping for IPv6

`traceroute <link>` - tracks the path the machine to a given point (<link>)

`traceroute6 <link>` - traceroute for IPv6

`netcat` - read and write traffic over a network (`netcat -l 12345`)

### ss

**A utility to investigate sockets and their statistics**

`-l` - flag for listening sockets

`-i` - flag for internal tcp information

`-p` - processes using sockets

### Configure client-side DNS

`/etc/dhcp/dhclient.conf` - tcp configuration

`getent hosts` - query hosts
