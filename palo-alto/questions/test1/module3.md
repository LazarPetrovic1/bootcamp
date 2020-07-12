
### 3.1 Knowledge Check

Questions:
1. (blank) is a purpose-built, fully integrated cybersecurity approach that helps organizations get control of their networks and protect critical assets.
2. Which three options are key components of the Security Operating Platform? (Choose three.)

+ network security
+ advanced endpoint protection
+ cloud security
+ application development security

Answers:
1. Security Operating Platform
2. [a] network security, [b] advanced endpoint protection, [c] cloud security
___

### 3.2 Knowledge Check

Questions:
1. Which option is not a defining characteristic of an NGFW? (Choose one.)

+ low latency packet processing with minimal throughput loss
+ adherence to strict port and protocol enforcement for allow or block decisions
+ integrated security tools
+ bidirectional full-stack analysis of packets

2. List the three core capabilities of an NGFW.
3. Which option is not a core technique for identifying applications in Palo Alto Networks NGFWs? (Choose one.)

+ packet headers
+ application signatures
+ protocol decoding
+ behavioral analysis

4. List three methods of mapping user identification to an IP address within an NGFW.
5. Describe stream-based malware scanning and explain its benefits.
6. What is the advantage of using templates in Panorama?
7. Panorama does not integrate with which option? (Choose one.)

+ WildFire
+ Splunk
+ Palo Alto Networks NGFWs
+ traditional port-based firewalls

Answers:
1. [b] adherence to strict port and protocol enforcement for allow or block decisions
2. application identification, user identification, and content identification
3. [a] packet headers
4. Any three of the following: security event log monitoring (Active Directory, Novell eDirectory, and Microsoft Exchange), user provided credentials, client probing, receiving user information through XML API from an external LDAP directory
5. Unlike file-based malware scanning that waits until an entire file is loaded into memory to begin scanning, stream-based malware scanning begins scanning as soon as the first packets of the file are received. Stream-based malware scanning reduces latency and improves performance by receiving, scanning, and sending traffic to its intended destination immediately, without having to first buffer and then scan the file.
6. Templates eliminate manual, repetitive, risky, and error-prone configuration changes to multiple, individual firewalls deployed throughout the enterprise network.
7. [d] traditional port-based firewalls
___

### 3.3 Knowledge Check

Questions:
1. The key to Traps is blocking core exploit and malware techniques, not the individual attacks.
2. Describe the basic function of Traps exploit prevention modules (EPMs).
3. What are the three keys to safely enabling mobile devices in the enterprise?

Answers:
1. True
2. The Traps agent injects itself into each process as it is started. If the process attempts to execute any of the core attack techniques, the corresponding EPM kills the process and prevents the exploit.
3. manage the device, protect the device, control the data
___

### 3.4 Knowledge Check

Questions:
1. (blank) provides continuous monitoring of public clouds and helps organizations achieve a continuous state of compliance in their public cloud workloads.
2. What are some of the organizational security risks associated with unsanctioned SaaS application usage?
3. Explain why traditional perimeter-based firewalls are not effective for protecting data in SaaS environments.
4. Aperture is deployed as a standalone inline service between the organization’s traditional perimeter-based firewalls and requires a software agent to be installed on mobile devices. T/F
5. Aperture protects data in hosted files and application entries. T/F

Answers:
1. Evident
2. The organizational security risks associated with unsanctioned SaaS application usage include regulatory non-compliance or compliance violations, loss of corporate intellectual property (IP) or other sensitive data, and malware distribution.
3. Traditional perimeter-based firewalls only have visibility of traffic that passes through the firewall. SaaS applications and data can be accessed from mobile devices that don’t necessarily traverse a perimeter-based firewall, and many SaaS-based applications are designed to circumvent firewalls for performance and ease of use.
4. False. Aperture is used to protect sanctioned SaaS usage, as part of an integrated security solution that includes NGFWs to prevent unsanctioned SaaS use. Aperture communicates directly with the SaaS applications themselves and therefore does not need to be deployed inline and does not require any software agents, proxies, additional hardware, or network configuration changes.
5. True
___

### 3.5 Knowledge Check

Questions:
1. Magnifier leverages to analyze network, endpoint, and cloud data, which helps security analysts rapidly confirm threats by reviewing actionable alerts.
2. Which three options are threat intelligence sources for AutoFocus? (Choose three.)

+ WildFire
+ URL filtering with PAN-DB service
+ Unit 42 threat intelligence and research team
+ third-party intrusion prevention systems

3. AutoFocus is an optional module that can be installed on NGFWs.
4. (blank) is an open-source application, available directly on GitHub, that streamlines the aggregation, enforcement, and sharing of threat intelligence.
5. WildFire operates on which concept? (Choose one.)

+ file-based scanning against a signature database
+ IPS and SIEM tool correlation
+ cloud-based reputation service
+ virtualized sandbox

6. WildFire prevents known and unknown malware threats. T/F
7. WildFire performs deep packet inspection of malicious outbound communications to disrupt C&C activity. T/F

Answers:
1. machine learning
2. [a] WildFire, [b] URL filtering with PAN-DB service, [c] Unit 42 threat intelligence and research team
3. False. AutoFocus is a subscription-based threat intelligence cloud that fully integrates with the Security Operating Platform, but does not require any configuration changes to NGFWs or Traps Advanced Endpoint Protection.
4. MineMeld
5. [d] virtualized sandbox
6. False. WildFire prevents unknown malware threats. Known malware threats are prevented by the other components of the Security Operating Platform, including NGFWs, Traps Advanced Endpoint Protection, and Aperture SaaS-based security.
7. True
