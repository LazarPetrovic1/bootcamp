### Flow bias
A flow records characteristics of the network activity that it represents, including its flow bias. The
bias of a flow marks the ratio between bytes leaving from and arriving at your organization’s
perimeter. QRadar SIEM distinguishes between the following flow biases:
+ Out only: Unidirectional outbound

This bias indicates outbound connection attempts that are being blocked by a firewall, such as
beaconing attempts by a malware to its command-and-control (C&C) servers.
+ In only: Unidirectional inbound

This bias indicates inbound connection attempts that are being blocked by a firewall or a port
scan attempt of a publicly reachable IP address of your organization.
+ Mostly out: 70% to 99% of bytes outbound

This bias indicates data leaving your organization. Only your publicly reachable servers should
have many flows with this bias.
+ Mostly in: 70% to 99% of bytes inbound

This bias is typical for end-user machines.
+ Near same: inbound-outbound byte ratio between 31% and 69%

This bias is typical for VOIP, chat, and SSH.
+ Other

This bias usually indicates traffic between local machines. It can also indicate traffic between
two remote machines that either points to a misconfiguration of an organization’s network or
notifies you that a local network is missing in the network hierarchy of QRadar SIEM.
