### 2.1 Identify and configure firewall management interfaces - questions

21. What are two firewall management methods? (Choose two.)
+ [x] CLI
+ [ ] RDP
+ [ ] VPN
+ [x] XML API
22. Which two devices are used to connect a computer to the firewall for management purposes?
(Choose two.)
+ [ ] rollover cable
+ [x] serial cable
+ [x] RJ-45 Ethernet cable
+ [ ] USB cable
23. What is the default IP address on the MGT interfaces of a Palo Alto Networks firewall?
+ [x] 192.168.1.1
+ [ ] 192.168.1.254
+ [ ] 10.0.0.1
+ [ ] 10.0.0.254
24. What are the two default services that are available on the MGT interface? (Choose two.)
+ [x] HTTPS
+ [x] SSH
+ [ ] HTTP
+ [ ] Telnet
25. True or false. Service route traffic has Security policy rules applied against it.
+ [x] true
+ [ ] false
26. Service routes may be used to forward which two traffic types out a data port? Choose two.)
+ [x] External Dynamic Lists
+ [ ] MineMeld
+ [ ] Skype
+ [x] Palo Alto Networks updates
___

### 2.2 Identify how to manage firewall configurations - questions

27. Which firewall plane does the running configuration reside on?
+ [ ] management
+ [ ] control
+ [x] data
+ [ ] security
28. Which firewall plane does the candidate configuration reside on?
+ [ ] management
+ [x] control
+ [ ] data
+ [ ] security
29. Candidate config and running config files are saved as which file type?
+ [ ] TXT
+ [ ] HTML
+ [x] XML
+ [ ] RAR
30. Which command must be performed on the firewall to activate any changes?
+ [x] commit
+ [ ] save
+ [ ] load
+ [ ] save named
+ [ ] import
+ [ ] copy
31. Which command backs up configuration files to a remote network device?
+ [ ] import
+ [ ] load
+ [ ] copy
+ [x] export
32. The command load named configuration snapshot overwrites the current candidate
configuration with which three items? (Choose three.)
+ [x] custom-named candidate configuration snapshot (instead of the default snapshot)
+ [x] custom-named running configuration that you imported
+ [ ] snapshot.xml
+ [x] current running configuration (running-config.xml)
+ [x] Palo Alto Networks updates
___

### 2.3 Identify and schedule dynamic updates - questions

33. What is the shortest time interval that you can configure a Palo Alto Networks firewall to download WildFire updates?
+ [x] 1 minute
+ [ ] 5 minutes
+ [ ] 15 minutes
+ [ ] 60 minutes
34. What is the publishing interval for WildFire updates, with a valid WildFire license?
+ [ ] 1 minute
+ [x] 5 minutes
+ [ ] 15 minutes
+ [ ] 60 minutes
35. True or false. A Palo Alto Networks firewall automatically provides a backup of the configuration during a software upgrade.
+ [x] true
+ [ ] false
36. If you have a Threat Prevention subscription but not a WildFire subscription, how long must you wait for the WildFire signatures to be added into the antivirus update?
+ [ ] 1 to 2 hours
+ [ ] 2 to 4 hours
+ [ ] 10 to 12 hours
+ [x] 12 to 48 hours
37. Which three actions should you complete before you upgrade to a newer version of software? (Choose three.)
+ [x] Review the release notes to determine any impact of upgrading to a newer version of
software.
+ [x] Ensure the firewall is connected to a reliable power source.
+ [ ] Export the device state.
+ [x] Create and externally store a backup before you upgrade.
38. What are five ways to download software? (Choose five.)
+ [x] over the MGT interface on the control plane
+ [x] over a data interface on the data plane
+ [x] upload from a computer
+ [x] from the Palo Alto Networks Customer Support Portal
+ [ ] from the PAN-DB database
+ [x] from Panorama
___

### 2.4 Configure internal and external services for account administration - questions

39. Which two statements are true about a Role Based Admin Role profile role? (Choose two.)
+ [ ] It is a built-in role.
+ [x] It can be used for CLI commands.
+ [x] It can be used for XML API.
+ [ ] Superuser is an example.
40. PAN-OS software supports which two authentication types? (Choose two.)
+ [x] RADIUS
+ [ ] SMB
+ [x] TACACS+
+ [ ] AWS
41. Which two Dynamic Admin Role types are available on the PAN-OS software? (Choose two.)
+ [x] superuser
+ [ ] superuser (write only)
+ [ ] device user
+ [x] device administrator (read-only)
42. Which type of profile does an Authentication Sequence include?
+ [ ] Security
+ [ ] Authorization
+ [ ] Admin
+ [x] Authentication
43. An Authentication Profile includes which other type of profile?
+ [x] Server
+ [ ] Admin
+ [ ] Customized
+ [ ] Built-in
44. True or False: Dynamic Admin Roles are called “dynamic” because you can customize them.
+ [ ] true
+ [x] false
45. What is used to override global Minimum Password Complexity Requirements?
+ [ ]Authentication Profile
+ [ ]Local Profile
+ [ ]Password Role
+ [x] Password Profile
___

### 2.5 Given a network diagram, create the appropriate security zones - questions

46. Which two default zones are included with the PAN-OS software? (Choose two.)
+ [x] Interzone
+ [ ] Extrazone
+ [x] Intrazone
+ [ ] Extranet
47. Which two zone types are valid? (Choose two.)
+ [ ] trusted
+ [x] tap
+ [x] virtual wire
+ [ ] untrusted
+ [ ] dmz
48. The External zone type is used to pass traffic between which type of objects?
+ [ ] Layer 2 interfaces
+ [ ] Layer 3 interfaces
+ [ ] virtual routers
+ [x] virtual systems
49. Which two statements about interfaces are correct? (Choose two.)
+ [ ] Interfaces must be configured before you can create a zone.
+ [x] Interfaces do not have to be configured before you can create a zone.
+ [x] An interface can belong to only one zone.
+ [ ] An interface can belong to multiple zones.
50. Which three interface types can belong in a Layer 3 zone? (Choose three.)
+ [x] loopback
+ [x] Layer 3
+ [x] tunnel
+ [ ] virtual wire
51. What are used to control traffic through zones?
+ [ ] access lists
+ [ ] security policy lists
+ [x] security policy rules
+ [ ] access policy rules
___

### 2.6 Identify and configure firewall interfaces - questions

52. Which two actions can be done with a Tap interface? (Choose two.)
+ [ ] encrypt traffic
+ [x] decrypt traffic
+ [ ] allow or block traffic
+ [x] log traffic
53. Which two actions can be done with a Virtual Wire interface? (Choose two.)
+ [x] NAT
+ [ ] route
+ [ ] switch
+ [x] log traffic
54. Which two actions can be done with a Layer 3 interface? (Choose two.)
+ [x] NAT
+ [x] route
+ [ ] switch
+ [ ] create a Virtual Wire object
55. Layer 3 interfaces support which two items? (Choose two.)
+ [x] NAT
+ [x] IPv6
+ [ ] switching
+ [ ] spanning tree
56. Layer 3 interfaces support which three advanced settings? (Choose three.)
+ [ ] IPv4 addressing
+ [ ] IPv6 addressing
+ [ ] NTP configuration
+ [x] NDP configuration
+ [x] link speed configuration
+ [x] link duplex configuration
57. Layer 2 interfaces support which three items? (Choose three.)
+ [ ] spanning tree blocking
+ [x] traffic examination
+ [x] forwarding of spanning tree BPDUs
+ [x] traffic shaping via QoS
+ [ ] firewall management
+ [ ] routing
58. Which two interface types support subinterfaces? (Choose two.)
+ [x] virtual wire
+ [x] Layer 2
+ [ ] loopback
+ [ ] tunnel
59. Which two statements are true regarding Layer 3 interfaces? (Choose two.)
+ [x] You can configure a Layer 3 interface with one or more as a DHCP client.
+ [ ] You can assign only one IPv4 addresses to the same interface.
+ [ ] You can enable an interface to send IPv4 Router Advertisements by selecting the
Enable Router Advertisement check box on the Router Advertisement tab.
+ [x] You can apply an interface management profile to the interface.
___

### 2.7 Given a scenario, identify steps to create and configure a virtual router - questions

60. What is the default administrative distance of a static route within the PAN-OS software?
+ [ ] 1
+ [ ] 5
+ [x] 10
+ [ ] 100
61. Which two dynamic routing protocols are available in the PAN-OS software? (Choose two.)
+ [ ] RIP1
+ [x] RIPv2
+ [x] OSPFv3
+ [ ] EIGRP
62. Which value is used to distinguish the preference of routing protocols?
+ [ ] metric
+ [ ] weight
+ [ ] distance
+ [ ] cost
+ [x] administrative distance
63. Which value is used to distinguish the best route within the same routing protocol?
+ [x] metric
+ [ ] weight
+ [ ] distance
+ [ ] cost
+ [ ] administrative distance
64. In path monitoring, what is used to monitor remote network devices?
+ [x] ping
+ [ ] SSL
+ [ ] HTTP
+ [ ] HTTPS
+ [ ] link state
___

### 2.8 Identify the purpose of specific security rule types.

65. What are the two default (predefined) security policy rule types in PAN-OS software? (Choose two.)
+ [ ] Universal
+ [x] Interzone
+ [x] Intrazone
+ [ ] Extrazone
66. True or false. Because the first rule that matches the traffic is applied, the more specific rules must follow the more general ones.
+ [ ] true
+ [x] false
67. Which statement is true?
+ [ ] For Intrazone traffic, traffic logging is enabled by default.
+ [ ] For Interzone traffic, traffic logging is enabled by default.
+ [x] For Universal traffic, traffic logging is enabled by default.
+ [ ] For any rule type, traffic logging is enabled by default.
___

### 2.9 Identify and configure security policy match conditions, actions, and logging options - questions

68. What are the two default (predefined) security policy rule types in PAN-OS software? (Choose two.)
+ [ ] Universal
+ [x] Interzone
+ [x] Intrazone
+ [ ] Extrazone
69. True or false? Best practice is to enable logging for the two predefined security policy rules.
+ [x] true
+ [ ] false
70. What will be the result of one or more occurrences of shadowing?
+ [ ] a failed commit
+ [ ] an invalid configuration
+ [x] a warning
+ [ ] an alarm window
71. Which type of security policy rules most often exist above the two predefined security policies?
+ [ ] Intrazone
+ [ ] Interzone
+ [x] Universal
+ [ ] Global
___

### 2.10 Given a scenario, identify and implement the proper NAT solution - questions

72. What are two source NAT types? (Choose two.)
+ [ ]universal
+ [x] static
+ [x] dynamic
+ [ ]extrazone
73. A simple way to remember how to configure security policy rules where NAT was implemented is to memorize the following:
+ [ ] post-NAT zone, post-NAT zone
+ [ ] post-NAT IP, post-NAT zone
+ [x] pre-NAT IP, post-NAT zone
+ [ ] pre-NAT IP, pre-NAT zone
74. What are two types of destination NAT? (Choose two.)
+ [x] dynamic IP (with session distribution)
+ [ ] DIPP
+ [ ] global
+ [x] static
75. What are two possible values for DIPP NAT oversubscription? (Choose two.)
+ [x] 1x
+ [x] 4x
+ [ ] 16x
+ [ ] 32x
76. Which statement is true regarding bidirectional NAT?
+ [x] For static translations, bidirectional NAT enables the firewall to create a corresponding translation in the opposite direction of the translation you configure.
+ [ ] For static translations, bidirectional NAT enables the firewall to create a corresponding translation in the same direction of the translation you configure.
+ [ ] For dynamic translations, bidirectional NAT enables the firewall to create a corresponding translation in the opposite direction of the translation you configure.
+ [ ] For dynamic translations, bidirectional NAT enables the firewall to create a corresponding translation in the same direction of the translation you configure.
