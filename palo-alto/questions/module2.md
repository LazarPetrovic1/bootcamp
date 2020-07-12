### 2.1 Knowledge Check

Questions:
1. A (blank) sends data packets to destination networks along a network path using logical addresses.
2. Which option is an example of a static routing protocol?
(Choose one.)

+ Open Shortest Path First (OSPF)
+ Border Gateway Protocol (BGP)
+ Routing Information Protocol (RIP)
+ split horizon

3. Which three options are dynamic routing protocols? (Choose three.)

+ distance-vector
+ path-vector
+ link-state
+ point-to-point

4. The internet is an example of a wide-area network (WAN). T/F
5. The (blank) is a distributed, hierarchical internet database that maps FQDNs to IP addresses.

Answers:
1. router
2. [b] Routing Information Protocol (RIP)
3. [a] distance-vector, [b] path-vector, and [c] link-state
4. True
5. Domain Name System (DNS)

___

### 2.2 Knowledge Check

Questions:
1. Which option is an example of a logical address? (Choose one.)

+ IP address
+ hardware address
+ MAC address
+ burned-in address

2. An IPv4 address consists of four (blank)-bit octets.
3. (blank) is a technique used to divide a large network into smaller, multiple subnetworks by segmenting an IPv4 address into a network and host portion.

Answers:
1. [a] IP address
2. 8
3. Subnetting

___

### 2.3 Knowledge Check

Questions:
1. The OSI model consists of how many layers? (Choose one.)

+ four
+ six
+ seven
+ nine

2. Which two protocols function at the Transport layer of the OSI model? (Choose two).

+ Transmission Control Protocol (TCP)
+ Internet Protocol (IP)
+ User Datagram Protocol (UDP)
+ Hypertext Transfer Protocol (HTTP)

3. The Data Link layer of the OSI model is further divided into these two sublayers: (blank) and (blank).
4. Which four layers comprise the TCP/IP model? (Choose four.)

+ Application
+ Transport
+ Physical
+ Internet
+ Network Access

5. The process that wraps protocol information from the (OSI or TCP/IP) layer immediately above in the data section of the layer immediately below is known as (blank).

Answers:
1. [c] seven
2. [a] Transmission Control Protocol (TCP), [c] User Datagram Protocol (UDP)
3. media access control (MAC), Logical Link Control (LLC)
4. [a] Application, [b] Transport, [d] Internet, [e] Network Access
5. data encapsulation

___

### Section 2.4 Knowledge Check

Questions:
1. What is the primary issue with a perimeter-based network security strategy today?
2. A Zero Trust network security model is based on which security principle? (Choose one.)

+ due diligence
+ least privilege
+ non-repudiation
+ negative control

Answers:
1. The primary issue with a perimeter-centric network security strategy is that it relies on the assumption that everything on the internal network can be trusted.
2. [b] least privilege

___

### 2.5 Knowledge Check

Questions:
1. List some of the principles of cloud computing that are contrary to network security best practices.
2. Intra-VM traffic is also known as which type of traffic? (Choose one.)

+ north-south
+ unknown
+ east-west
+ untrusted

3. What does the first phase of implementing security in virtualized data centers consist of? (Choose one.)

+ consolidating servers across trust levels
+ consolidating servers within trust levels
+ selectively virtualizing network security functions
+ implementing a dynamic computing fabric

Answers:
1. Cloud computing doesn’t mitigate existing network security risks; security requires isolation and segmentation, whereas the cloud relies on shared resources; security deployments are process-oriented, whereas cloud computing environments are
dynamic.
2. [c] east-west
3. [b] consolidating servers within trust levels

___

### 2.6 Knowledge Check

Questions:
1. A dynamic packet filtering firewall inspects each individual packet during a session to determine if the traffic should be allowed, blocked, or dropped by the firewall. T/F
2. What are three characteristics of application firewalls? (Choose three.)

+ proxies traffic rather than permitting direct communication between hosts
+ can be used to implement strong user authentication
+ masks the internal network from untrusted networks
+ is extremely fast and has no impact on network performance

3. Briefly describe the primary difference between intrusion detection systems and intrusion prevention systems.
4. Which VPN technology is currently considered the preferred method for securely connecting a remote endpoint device back to an enterprise network? (Choose one.)

+ point-to-point tunneling protocol (PPTP)
+ secure socket tunneling protocol (SSTP)
+ Secure Sockets Layer (SSL)
+ Internet Protocol Security (IPsec)

5. Which is NOT a characteristic of Unified Threat Management (UTM)? (Choose one.)
+ It combines security functions such as firewalls, intrusion detection systems (IDS), anti-malware, and data loss prevention (DLP) in a single appliance.
+ enabling all of the security functions in a UTM device can have a significant performance impact.
+ It fully integrates all the security functions installed on the device.
+ It can be a convenient solution for small networks.

Answers:
1. False. A dynamic packet filtering (also known as stateful packet inspection) firewall only inspects individual packet headers during session establishment to determine if the traffic should be allowed, blocked, or dropped by the firewall. Once a session is established, individual packets that are part of the session are not inspected.
2. [a] proxies traffic rather than permitting direct communication between hosts, [b] can be used to implement strong user authentication, [c] masks the internal network from
untrusted networks
3. IDS is considered to be a passive system because it only monitors, analyzes, and alerts. IPS is an active system that performs all of the functions of IDS, but can also block or drop suspicious, pattern-matching traffic on the network.
4. [c] Secure Sockets Layer (SSL)
5. [c] It fully integrates all the security functions installed on the device.
___

### 2.7 Knowledge Check

Questions:
1. Signature-based anti-malware software is considered a proactive security countermeasure. T/F
2. (blank) endpoint protection wraps a protective virtual barrier around vulnerable processes while they’re running.
3. What is the main disadvantage of application whitelisting related to exploit prevention?
4. What are three typical mobile device management
software capabilities? (Choose three.)

+ data loss prevention (DLP)
+ policy enforcement
+ intrusion detection
+ malware prevention

Answers:
1. False. Signature-based anti-malware software is considered a reactive countermeasure because a signature file for new malware can’t be created and delivered until the malware is already "in the wild".
2. Container-based
3. The main disadvantage of application whitelisting related to exploit prevention is that an application that has been whitelisted is permitted to run – even if the application has a vulnerability that can be exploited.
4. [a] data loss prevention (DLP), [b] policy enforcement, [d] malware prevention
___

### 2.8 Knowledge Check

Questions:
1. Which three cloud computing service models are defined by
NIST? (Choose three.)

+ software as a service (SaaS)
+ platform as a service (PaaS)
+ desktop as a service (DaaS)
+ infrastructure as a service (IaaS)

2. A (blank) cloud infrastructure comprises two or more cloud deployment models, bound by standardized or proprietary technology that enables data and application portability.
3. The (blank) defines who (customer and/or provider) is responsible for what, related to security, in the public cloud.
4. A (blank) allows multiple, virtual operating systems to run concurrently on a single physical host computer.
5. Which three important security considerations are
associated with virtualization? (Choose three.)

+ dormant VMs
+ hypervisor vulnerabilities
+ hypervisor sprawl
+ intra-VM communications

6. A storage area network (SAN) uses (blank)-based storage.

Answers:
1. [a] software as a service (SaaS), [b] platform as a service (PaaS), [d] infrastructure as a service (IaaS)
2. hybrid
3. Shared Responsibility Model
4. hypervisor
5. [a] dormant VMs, [b] hypervisor vulnerabilities, [d] intra-VM communications
6. block
___

### 2.9 Knowledge Check

Questions:
1. (blank) is a network directory service developed by Microsoft for Windows networks.
2. (blank) is a set of IT service management best practices.

Answers:
1. Active Directory
2. ITIL
