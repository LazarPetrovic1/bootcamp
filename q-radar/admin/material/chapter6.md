# Set up QRadar

### Network hierarchy

IBM QRadar uses the network hierarchy objects and groups to view network activity and monitor groups or services in your network.

##### Guidelines for defining your network hierarchy

Consider the following guidelines when you define your network hierarchy:
+ Organize your systems and networks by role or similar traffic patterns. For example, you might organize your network to include groups for mail servers, departmental users, labs, or development teams. Using this organization, you can differentiate network behavior and enforce behaviour-based network management security policies. However, do not group a server that has unique behavior with other servers on your network. Placing a unique server alone provides the server greater visibility in QRadar, and makes it easier to create specific security policies for the server.
+ Place servers with high volumes of traffic, such as mail servers, at the top of the group. This hierarchy provides you with a visual representation when a discrepancy occurs.
+ Do not configure a network group with more than 15 objects. Large network groups can cause difficulty when you view detailed information for each object. If your deployment processes more than 600,000 flows, consider creating multiple top-level groups.
+ Conserve disk space by combining multiple Classless Inter-Domain Routings (CIDRs) or subnets into a single network group.

> Related - Defining your network hierarchy (pg. 86)

### Automatic updates

The IBM QRadar Console must be connected to the Internet to receive the updates. If your Console is not connected to the Internet, you must configure an internal update server for your Console to download the files from

Update files can include the following updates:
+ Configuration updates that are based on content, including configuration file changes, vulnerabilities, QID maps, supportability scripts, and security threat information updates.
+ DSM, scanner, and protocol updates that include corrections to parsing issues, scanner changes, and protocol updates.
+ Major updates, such as updated JAR files or large patches, that require restarting the user interface service.
+ Minor updates, such as daily automatic update logs or QID map scripts, that do not restart the user interface service.

The default frequency of the automatic update is determined by the installation type and the QRadar version.
+ If you upgrade from QRadar versions earlier than V7.2, the value to which the update frequency is set remains the same after the upgrade. By default, the update is set to weekly, but you can manually change the frequency.
+ If you install a new installation of QRadar V7.2 or later, the default frequency of the update is daily. You can manually change the frequency.

> Related:
+ Viewing pending updates (pg. 88)
+ Configuring automatic update settings (pg. 89)
+ Configuring updates behind a proxy server that uses SSL or TLS interception (pg. 90)
+ Scheduling an update (pg. 91)
+ Clearing scheduled updates (pg. 91)
+ Checking for new updates (pg. 91)
+ Manually installing automatic updates (pg. 91)
+ Viewing your update history (pg. 92)
+ Restoring hidden updates (pg. 92)
+ Viewing the autoupdate log (pg. 92)

### Manual updates

If your deployment includes a IBM QRadar Console that is unable to access the Internet, or you want to manually manage updates to your system, you can manage the update process manually by setting up a IBM QRadar update server.

> Related:
+ Configuring an update server (pg. 93)
+ Configuring the QRadar Console as the update server (pg. 94)
+ Download updates to the update server (pg. 94)

### Configuring system settings

System settings specify how your IBM QRadar system components are configured for normal operation.

> Related:
+ Customizing the right-click menu (pg. 95)
+ Enhancing the right-click menu for event and flow columns (pg. 96)
+ Asset retention values overview (pg. 98)
+ Adding or editing a QRadar login message (pg. 99)
+ Turning on and configuring rule performance visualization (pg. 100)

### IF-MAP server certificates

The Interface For Metadata Access Points (IF-MAP) rule response enables the IBM QRadar console to publish alert and offense data that is derived from events, flows, and offenses to an IF-MAP server. Before you can configure IF-MAP authentication on the System Settings window, you must configure your IF-MAP server certificate.

> Related:
+ Configuring IF-MAP Server Certificate for Basic Authentication (pg. 102)
+ Configuring IF-MAP Server Certificate for Mutual Authentication (pg. 102)

### SSL certificates

Secure Sockets Layer (SSL) is an industry standard security protocol used by websites to protect online transactions. It provides communication privacy so that client/server applications can communicate in a way that is designed to prevent eavesdropping, tampering, and message forgery.

Types:
+ **Self-signed certificates** - because self-signed certificates cannot be authenticated by any existing known root certificate authorities, users are warned about this unknown certificate and must accept it to proceed.
+ **Internal CA signed certificates** - this certificate is supported by QRadar, and the internal root CA is also imported into the QRadar environment.
+ **Public CA / Intermediate CA signed** - Certificates that are signed by known public CAs and intermediate certificates are supported by QRadar.

##### SSL connections between QRadar components

To establish all internal SSL connections between components, QRadar uses the web server certificate that is preinstalled on the QRadar Console.

All trusted certificates for QRadar must meet the following requirements:
+ The certificate must be an X.509 certificate and have PEM base64 encoding.
+ The certificate must have a .cert, .crt, .pem, or .der file extension.
+ Keystore files that contain certificates must have the .truststore file extension.
+ The certificate file must be stored in the /opt/qradar/conf/trusted_certificates directory.

> Related:
+ Creating an SSL certificate signing request with 2048-bit RSA keys (pg. 104)
+ Creating a multi-domain (SAN) SSL certificate signing request (pg. 105)
+ Using certificates that are signed by an internal certificate authority (pg. 106)
+ Installing a new SSL certificate (pg. 106)
+ Revert to using a self-signed certificate (pg. 107)
+ Advanced iptables rules examples (pg. 109)
+ Configuring iptables rules (pg. 111)

### Data retention

As QRadar receives events and flows, each one is compared against the retention bucket filter criteria. When an event or flow matches a retention bucket filter, it is stored in that retention bucket until the deletion policy time period is reached. The default retention period is 30 days; then, the data is immediately deleted.

> Related:
+ Configuring retention buckets (pg. 112)
+ Managing retention bucket sequence (pg. 114)
+ Enabling and disabling a retention bucket (pg. 114)
+ Deleting a Retention Bucket (pg. 114)

### System notifications

IBM QRadar continuously monitors all appliances and delivers information, warning, and error notifications to the QRadar Console, making it easier for you to monitor the status and health of your deployment.

> Related:
+ Configuring system notifications (pg. 115)
+ Configuring custom email notifications (pg. 116)

### Custom offense close reasons

You can manage the options listed in the **Reason for Closing** list box on the **Offenses** tab. When a user closes an offense on the **Offenses** tab, the Close Offense window is displayed. The user is prompted to select a reason from the **Reason for Closing** list box. Three default options are listed:
+ False-positive, tuned
+ Non-issue
+ Policy violation

Administrators can add, edit, and delete custom offense close reasons from the **Admin** tab.

> Related:
+ Adding a custom offense close reason (pg. 120)
+ Editing a custom offense close reason (pg. 120)
+ Deleting a custom offense close reason (pg. 120)
+ Configuring a custom asset property (pg. 121)

### Index management

Use Index Management to control database indexing on event and flow properties. To improve the speed of searches in IBM QRadar, narrow the overall data by adding an indexed field in your search query.

The Index Management feature also provides statistics, such as:
+ The percentage of saved searches running in your deployment that include the indexed property
+ The volume of data that is written to the disk by the index during the selected time frame

> Related:
+ Enabling indexes (pg. 122)
+ Enabling payload indexing to optimize search times (pg. 122)
+ Configuring the retention period for payload indexes (pg. 123)

### Set restrictions to prevent resource-intensive searches

You can balance the usage of your QRadar infrastructure by setting resource restrictions on event and flow searches.

Types of resource restrictions:
+ User-based restrictions
+ Role-based restrictions
+ Tenant-based restrictions

##### Resource restrictions in distributed environments

In a distributed environment, the timing of the data transfer between the IBM QRadar console and managed hosts can impact the search results

+ Canceled searches
+ Empty search results
+ Inconsistent search results
+ Limited search results
