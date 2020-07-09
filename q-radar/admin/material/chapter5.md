# System management

IBM QRadar has a modular architecture that supports deployments of varying sizes and topologies.

### View system health information

The QRadar Deployment Intelligence app is a powerful monitoring application that consolidates historical health data for each managed host in your deployment. Use the app to monitor the health of your QRadar deployment.

### QRadar component types

Each IBM QRadar appliance that is added to the deployment has configurable components that specify the way that the managed host behaves in QRadar.

##### QRadar Console
The QRadar Console provides the QRadar product interface, real-time event and flow views, reports, offenses, asset information, and administrative functions. In distributed environments, the QRadar Console is used to manage the other components in the deployment.

##### Event Collector
The Event Collector collects events from local and remote log sources, and normalizes the raw event data so that it can be used by QRadar. To conserve system resources, the Event Collector bundles identical events together and sends the data to the Event Processor.

##### Event Processor
The Event Processor processes events that are collected from one or more Event Collector components. If events are matched to the custom rules that are defined on the Console, the Event Processor follows the action that is defined in the rule response. Each Event Processor has local storage. Event data is stored on the processor, or it can be stored on a Data Node.

##### QRadar QFlow Collector
QRadar QFlow Collector collects network flows from devices on your network. Live and recorded feeds
are included, such as network taps, span ports, NetFlow, and QRadar flow logs.
Restriction: QRadar Log Manager doesn't support flow collection.

##### Flow Processor
The Flow Processor processes flows from one or more QRadar QFlow Collector appliances. The Flow
Processor appliance can also collect external network flows such as NetFlow, J-Flow, and sFlow directly
from routers in your network.
Flow Processors include an on-board processor and internal storage for flow data.

##### Data Node
The Data Node receives security events and flows from event and flow processors, and stores the data to
disk.
The Data Node is always connected to either an Event Processor or a Flow Processor.

##### Off-site source and target appliances
An off-site appliance is a QRadar appliance that is not part of the deployment that is monitored by the QRadar Console. An off-site source appliance forwards normalized data to an Event Collector. You can configure an off-site source to encrypt the data before forwarding. An off-site target appliance receives normalized event or flow data from any Event Collector, or any processor in your deployment. Later versions of QRadar systems can receive data from earlier versions of QRadar systems, but earlier versions can't receive data from later versions. To avoid problems, upgrade all receivers before you upgrade senders.

### Data nodes

A data node is an appliance that you can add to your event and flow processors to increase storage capacity and improve search performance. Each data node can be connected to only one processor, but a processor can support multiple data nodes.

> Related topics:
+ How _ works? (pg. 59)
+ Viewing the progress of data rebalancing (pg. 60)
+ Saving all event data to a Data Node appliance (pg. 61)
+ Archiving Data Node content (pg. 61)

### Network interface management

Use extra network interfaces for the following purposes:
+ Provide a dedicated crossover connection between high-availability (HA) peers. You configure a crossover connection during HA setup.
+ Provide a dedicated data collection interface for inbound events or external flow sources. TCP-based data sources must be in the same subnet as the data collection interface.
+ Connect to backup and network storage systems (iSCSI).
+ Increase bandwidth and add fault tolerance by bonding interfaces.

**Note**: WinCollect configurations that are connected to a non-managed port are not supported.

> Related: Configuring network interfaces (pg. 62)

### QRadar system time

When your deployment spans multiple time zones, configure all appliances to use the same time zone as the IBM QRadar Console. Alternatively, you can configure all appliances to use Greenwich Mean Time (GMT). The time is automatically synchronized between the QRadar Console and the managed hosts.

> Related: Configuring system time (pg. 64)

### NAT-enabled networks

Network address translation (NAT) converts an IP address in one network to a different IP address in another network. NAT provides increased security for your IBM QRadar deployment because requests are managed through the conversion process and internal IP addresses are hidden. Use NAT to map individual internal IP addresses to individual external IP addresses.

> Related:
+ Configuring a NAT group (pg. 65)
+ Changing the NAT status for a managed host (pg. 66)

### Managing off-site hosts

An off-site host is a QRadar appliance that can't be accessed through the QRadar Console in your current deployment. You can configure an off-site host to transfer data to or to receive data from your QRadar deployment.

> Related:
+ Configuring an off-site source (pg. 67)
+ Configuring an off-site target (pg.67)
+ Generating public keys for QRadar products (pg.68)
+ Forwarding filtered flows (pg. 68)
+ Example: Forwarding normalized events and flows (pg. 69)

### Managed hosts

For greater flexibility over data collection and event and flow processing, build a distributed IBM QRadar deployment by adding non-console managed hosts, such as collectors, processors, and data nodes.

### Bandwidth considerations for managed hosts

To replicate state and configuration data, ensure that you have a minimum bandwidth of 100 Mbps between the IBM QRadar console and all managed hosts. Higher bandwidth is necessary when you search log and network activity, and you have over 10,000 events per second (EPS).

### Encryption

To provide secure data transfer between each of the appliances in your environment, IBM QRadar has integrated encryption support that uses OpenSSH. Encryption occurs between managed hosts; therefore, you must have at least one managed host before you can enable encryption.

> Related tasks:
+ Adding a managed host (pg.72)
+ Adding an IPv4-only managed host in a dual-stack environment (pg.74)
+ Configuring a managed host (pg. 74)
+ Removing a managed host (pg. 75)
+ Configuring your local firewall (pg. 75)
+ Configuring email (pg. 76)

### Making changes in your QRadar environment

When you make configuration changes to IBM QRadar, the changes are saved to a staging area, and the deployment banner on the Admin tab is updated indicating that changes need to be deployed. Deploying the changes might require QRadar services to restart.

**Standard deployment** for:
+ Adding or editing a new user or user role.
+ Setting a password for another user.
+ Changing a users' role or security profile.

**Full configuration deployment** for:
+ Adding a managed host.
+ Changing the configuration for a managed host.
+ Configuring offsite hosts for sending or receiving data from the QRadar Console.
+ Restoring a configuration backup.

**Changes that impact event collection**

The following situations can cause an interruption in event collection:
+ Rebooting an appliance that collects events.
+ Adding an HA managed host.
+ During HA failover.
+ Restoring a configuration backup.
+ Adding or removing an off-site source connection
+ Whenever a partition's disk usage exceeds the maximum threshold.

> Related:
+ Configuring an Event Collector (pg. 77)
+ Deploying changes (pg. 78)
+ Shutting down a system (pg. 79)
+ Restarting a system (pg. 79)
+ Collecting log files (pg. 80)
+ Changing the root password of your QRadar Console (pg. 80)
+ Resetting SIM (pg. 80)
