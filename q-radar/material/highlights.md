> The **Dashboard** tab supports multiple dashboards where you can display your views of network security,
activity, or data that QRadar collects. Five default dashboards are available. Each dashboard contains
items that provide summary and detailed information about offenses that occur on your network.
___
> From the **Offenses** tab, you can investigate an offense to determine the root cause of an issue, and then
work to resolve it.
___
> Investigate event logs that are sent to QRadar in real-time, perform powerful searches, and view log
activity by using configurable time-series charts.

> Use the **Log Activity** tab to perform in-depth investigations on event data.
___

> Use the **Network Activity** tab to investigate flows that are sent in real-time, perform powerful searches, and view network activity by using configurable time-series charts. A *flow* is a communication session between two hosts.
___

> QRadar automatically discovers assets, servers, and hosts that are operating on your network.
Automatic discovery is based on passive flow data and vulnerability data, allowing QRadar to build an
asset profile.
___

> Asset profiles provide information about each known asset in your network, including identity
information, if available, and what services are running on each asset. This profile data is used for
correlation purposes to help reduce false positives. Using the Assets tab, you can view the learned assets or search for specific assets to view their profiles.
___

> Use the Reports tab to create, distribute, and manage reports for any data within QRadar.
___

> IBM QRadar Risk Manager is a separately installed appliance for monitoring device configurations,
simulating changes to your network environment, and prioritizing risks and vulnerabilities in your
network.
___

*Viewing notifications*

> The Notifications menu provides access to a window in which you can read and manage your system notifications.

> For system notifications to show on the Notifications window, the administrator must create a rule that is
based on each notification message type and select the Notify check box in the Custom Rules Wizard.

> The Messages menu indicates how many unread system notifications you have in your system. This
indicator increments the number until you close system notifications. For each system notification, the Messages window provides a summary and the date stamp for when the system notification was created.
You can hover over a notification to view more details. You can use the functions on the Messages
window to manage the system notifications. If you close a system notification from the Messages window, the system notification is removed from all system notification displays.
___

> The Dashboard tab automatically refreshes every 60 seconds.
___

> The Log Activity and Network Activity tabs automatically refresh every 60 seconds if you are viewing the tab in Last Interval (auto refresh) mode. When you view the Log Activity or Network Activity tab in Real Time (streaming) or Last Minute (auto refresh) mode, you can use the Pause icon to pause the current display.
___

> The Offenses tab must be refreshed manually. The timer indicates the amount of time since the data was last refreshed. The timer flashes red when the timer is paused.

***The IP right-click tab***

| Tab         | Name                      |
| :---------- | :------------------------ |
| Navigate    | View by Network           |
| Navigate    | View Source Summary       |
| Navigate    | View Destination Summary  |
| Information | DNS lookup                |
| Information | WHOIS lookup              |
| Information | Port Scan                 |
| Information | Asset profile             |
| Information | Search Events             |
| Information | Search Flows              |
| Information | Search Connections        |
| Information | Switch port lookup        |
| Information | View Topology             |
| N/A         | Run vulnerability scan    |
___

> The upper right of the QRadar console displays the system time, which is the local time on the console. In a distributed deployment, the console might be in a different time zone from your desktop computer.
___

> QRadar user passwords are stored as a salted SHA-256 string.
___

> The Dashboard tab is the default view when you log in.

> The content that is displayed on the Dashboard tab is user-specific. Changes that are made within a session affect only your system.
___

> The Dashboard tab provides five default dashboards that are focused on security, network activity, application activity, system monitoring, and compliance.
___

*Application Overview*
+ Inbound Traffic by Country (Total Bytes)
+ Outbound Traffic by Country (Total Bytes)
+ Top Applications (Total Bytes)
+ Top Applications Inbound from Internet (Total
Bytes)
+ Top Applications Outbound to the Internet (Total
Bytes)
+ Top Services Denied through Firewalls (Event
Count)
+ DSCP - Precedence (Total Bytes)
___

*Compliance Overview*
+ Top Authentications by User (Time Series)
+ Top Authentication Failures by User (Event
Count)
+ Login Failures by User (real-time)
+ Compliance: Username Involved in Compliance
Rules (time series)
+ Compliance: Source IPs Involved in Compliance
Rules (time series)
+ Most Recent Reports
___

*Network Overview*
+ Top Talkers (real time)
+ ICMP Type/Code (Total Packets)
+ Top Networks by Traffic Volume (Total Bytes)
+ Firewall Deny by DST Port (Event Count)
+ Firewall Deny by DST IP (Event Count)
+ Firewall Deny by SRC IP (Event Count)
+ Top Applications (Total Bytes)
+ Link Utilization (real-time)
+ DSCP - Precedence (Total Bytes)
___

*System Monitoring*
+ Top Log Sources (Event Count)
+ Link Utilization (real-time)
+ System Notifications
+ Event Processor Distribution (Event Count)
+ Event Rate (Events per Second Coalesced -
Average 1 Min)
+ Flow Rate (Flows per Second - Peak 1 Min)
___

*Threat and Security Monitoring*
+ Default-IDS/IPS-All: Top Alarm Signatures (real-
time)
+ Top Systems Attacked (Event Count)
+ Top Systems Sourcing Attacks (Event Count)
+ My Offenses
+ Most Severe Offenses
+ Most Recent Offenses
+ Top Services Denied through Firewalls (Event
Count)
+ Internet Threat Information Center
+ Flow Bias (Total Bytes)
+ Top Category Types
+ Top Sources
+ Top Local Destinations
___

> 255 dashboards per user is the maximum

> To create custom items, you can create saved searches on the Network Activity or Log Activity tabs and choose how you want the results that are represented in your dashboard.

> Time series graphs on the dashboard refresh every 5 minutes.

> Flow search items are listed in the **Add Item > Network Activity > Flow Searches** menu.

> On a flow search dashboard item, search results display real-time last-minute data on a chart. The supported chart types are ***time series, table, pie, and bar***.

> **Note:** Hidden or closed offenses are not included in the values that are displayed in the **Dashboard** tab.

*Offense items*:
+ Most Recent Offenses
+ Most Severe Offenses
+ Most Severe Offenses
+ Top Sources
+ Top Local Destinations
+ Categories
___

*Log Activity items*

> The **Log Activity** dashboard items will allow you to monitor and investigate events in real time.

> **Note:** Hidden or closed events are not included in the values that are displayed in the **Dashboard** tab.

+ Event Searches
+ Events By Severity
+ Top Log Sources
___

> The **System Summary** dashboard item provides a high-level summary of activity within the past 24 hours.
___

> You use the **Risk Monitoring** dashboard to monitor policy risk and policy risk change for assets, policies and policy groups.

> The Risk Monitoring dashboard items do not display any results unless IBM QRadar Risk Manager is licensed.

> To view the default **Risk Monitoring** dashboard, select **Show Dashboard > Risk Monitoring** on the
**Dashboard** tab.
___

> Create a dashboard item that shows policy compliance pass rates and policy risk score for selected assets, policies, and policies groups.
___

> Vulnerability Management dashboard items are only displayed when IBM QRadar Vulnerability Manager is purchased and licensed.
___

> The Systems Notification dashboard item displays event notifications that are received by your system.

*On the System Notifications dashboard item, you can view the following information:*
+ Flag - Displays a symbol to indicate severity level of the notification. Point to the symbol to view more
detail about the severity level.
  – Health icon
  – Information icon (?)
  – Error icon (X)
– Warning icon (!)
+ Created - Displays the amount of time elapsed since the notification was created.
+ Description - Displays information about the notification.
+ Dismiss icon (x) - Will allow you to close a system notification.

*You can point your mouse over a notification to view more details:*
+ Host IP - Displays the host IP address of the host that originated the notification.
+ Severity - Displays the severity level of the incident that created this notification.
+ Low Level Category - Displays the low-level category that is associated with the incident that
generated this notification. For example: Service Disruption.
+ Payload - Displays the payload content that is associated with the incident that generated this
notification.
+ Created - Displays the amount of time elapsed since the notification was created.

> When you add the **System Notifications** dashboard item, system notifications can also display as pop-up notifications in the QRadar user interface. These pop-up notifications are displayed in the lower right corner of the user interface, regardless of the selected tab.

> Pop-up notifications are only available for users with administrative permissions and are enabled by default. To disable pop-up notifications, select **User Preferences** and clear the **Enable Pop-up
Notifications** check box.

The **system notification** pop-up window provides the following options:
+ Next icon (>) - Displays the next notification message. For example, if the current notification message is 3 of 6, click the icon to view 4 of 6.
+ Close icon (X) - Closes this notification pop-up window.
+ (details) - Displays more information about this system notification.
___

> To view a summary of the advisory, click the **Arrow** icon next to the advisory. To investigate the full advisory, click the associated link.
___

Create a custom **Dashboard**:
1. Click the Dashboard tab.
2. Click the New Dashboard icon.
3. In the Name field, type a unique name for the dashboard. The maximum length is 65 characters.
4. In the Description field, type a description of the dashboard. The maximum length is 255 characters. This description is displayed in the tooltip for the dashboard name in the Show Dashboard list box.
5. Click OK.
___

> Search-based dashboard items provide a link to the Log Activity or Network Activity tabs, allowing you to further investigate log or network activity.
___

> The chart types that are displayed on the **Log Activity** or **Network Activity** tab depend on which chart is configured in the dashboard item:
___

> Your custom chart configurations are retained, so that they are displayed as configured each time that you access the **Dashboard** tab.
___

> When you remove an item from the dashboard, the item is not removed completely.
___

> To add an event and flow search dashboard item to the Add Item menu on the Dashboard tab, you must access the Log Activity or Network Activity tab to create search criteria that specifies that the search results can be displayed on the Dashboard tab. The search criteria must also specify that the results are grouped on a parameter.
___

The magnitude rating of an offense is calculated based on relevance, severity, and credibility.
+ *Relevance* determines the impact of the offense on your network. For example, if a port is open, the relevance is high.
+ *Credibility* indicates the integrity of the offense as determined by the credibility rating that is configured in the log source. Credibility increases as multiple sources report the same event.
+ *Severity* indicates the level of threat that a source poses in relation to how prepared the destination is for the attack.

The following information is considered when the offense magnitude is calculated:
+ the number of events and flows that are associated with the offense
+ the number of log sources
+ the age of the offense
+ the weight of the assets associated with the offense
+ the categories, severity, relevance, and credibility of the events and flows that contribute to the offense
+ the vulnerabilities and threat assessment of the hosts that are involved in the offense
___

> IBM QRadar chains offenses together to reduce the number of offenses that you need to review.

> Offense chaining is based on the offense index field that is specified on the rule.
___

> Offense indexing provides the capability to group events or flows from different rules indexed on the same property together in a single offense.

> If the field that you want to index on is not included in the normalized fields, create a custom event or a custom flow property to extract the data from the payload and use it as the offense indexing field in your rule. The custom property that you index on can be based on a regular expression, a calculation, or an AQL-based expression.
___

***Rule action and response***

> When the indexed property value is null, an offense is not created, even when you select the **Ensure the detected event is part of an offense** check box in the rule action.

> When the response limiter uses a custom property, and the custom property value is null, the limit is applied to the null value.

> An event rule accepts custom event properties in the rule index and response limiter fields, while a flow rule accepts only custom flow properties.
___

> The offense retention period determines how long inactive and closed offenses are kept before they are removed from the QRadar console,

*Active offenses*
> When new events are evaluated, the offense clock is reset to keep the offense active for another 30 minutes.

*Dormant offenses*
> An offense becomes dormant if new events or flows are not added to the offense within 30 minutes, or if QRadar did not process any events within 4 hours. An offense remains in a dormant state for 5 days. If an event is added while an offense is dormant, the five-day counter is reset.

*Inactive offenses*
> An offense becomes inactive after 5 days in a dormant state. In the inactive state, new events that trigger the offense rule test do not contribute to the inactive offense. They are added to a new offense. Inactive offenses are removed after the offense retention period elapses.

*Closed offenses*
> The default offense retention period is 30 days. You can protect an offense to prevent it from being removed when the retention period expires.
___

> You can protect offenses to prevent them from being removed from QRadar after the retention period has elapsed.
___

> IBM QRadar uses rules to monitor the events and flows in your network to detect security threats. When the events and flows meet the test criteria that is defined in the rules, an offense is created to show that a security attack or policy breach is suspected.

> All users who have access to the network can view all offenses regardless of which log source or flow source is associated with the offense
___

> The Offenses tab shows the suspected security attacks and policy breaches that are occurring on your network. Offenses are listed with the highest magnitude first.

> To view offenses grouped on the high-level category, click **By Category**.

> To view low-level category groups for a particular high-level category, click the arrow icon next to
the high-level category name.

> The bottom of the Offense Summary page groups information about top contributors to the offense.

> **Status:** QRadar does not display a status icon when an offense is active.

Review the information in the top portion of the **Offense Summary** window to learn more about the type of attack and the time frame when it occurred.

> **Offense Type:** The offense type is determined by the rule that created the offense. The offense type determines what type of information is displayed in the **Offense Source Summary** pane.

> **Event/Flow count:** To see the list of events and flows that contributed to the offense, click the **Event** or **Flow** links.

> **Source IP:** Specifies the device that attempts to breach the security of a component on your network. The device can have an IPv4 or IPv6 address.

> **Destination IP:** Specifies the network device that the source IP address attempted to access. The network device can have an IPv4 or IPv6 address.

> **Start:** Specifies the date and time when the first event or flow occurred for the offense.

> **Duration:** Specifies the amount of time that elapsed since the first event or flow associated with the offense was created.

> **Network(s):** Specifies the local networks of the local destination IP addresses that were targeted. The system does not associate remote networks to an offense, even if they are specified as a remote network or a remote service on the **Admin** tab.

The information that is shown in the **Offense Source Summary** window depends on the **Offense Type** field.

> **Chained:** Specifies whether the destination IP address is chained. A chained IP address is associated with other offenses.

> **Destination IP(s):** Specifies the network device that the source IP address attempted to access.

> **Source IP(s):** Specifies the device that attempted to breach the security of a component on your network.

> **Username:** Specifies the user name that is associated with the event or flow that created the offense.

> **Vulnerabilities:** Specifies the number of identified vulnerabilities that are associated with the source or destination IP address. This value also includes the number of active and passive vulnerabilities.

When you view the summary information for historical offenses, the Last Known data fields are not populated.

In the bottom portion of the **Offense Summary** window, review additional information about the offense top contributors, including notes and annotations that are collected about the offense.
___

> An event is a record from a log source, such as a firewall or router device, that describes an action on a network or host.

| Field           | Description                                                      |
| :-------------- | :--------------------------------------------------------------- |
| Start Time      | The time that QRadar received the raw event from the log source. |
| Storage Time    | The time that QRadar stored the normalized event.                |
| Log Source Time | The time that is recorded in the raw event from the log source.  |
___

> QRadar adds an icon to the Flag column when you assign an offense to a user, protect or hide an offense, add notes, or mark the offense for follow-up.
___

> If you have the **Manage Offense Closing** permission, you can add custom closing reasons.
___

> You can export offenses in Extensible Markup Language (XML) or comma-separated values (CSV) format. The resulting XML or CSV file includes the parameters that are specified in the Column Definition pane of the search parameters.
___

> By default, all new offenses are unassigned. You can assign an offense to an IBM QRadar user for investigation. **You must have the Assign Offenses to Users permission to assign offenses to users.**

> You can assign offenses to users from either the **Offenses** tab or **Offense Summary** pages.

> The **Assign To User** list displays only those users who have privileges to view the Offenses tab. The security profile settings for the user are followed as well.

***Sending email notifications***

*Share the offense summary information with another person by sending an email.*

*The body of the email message includes the following information, if available:*
+ Source IP address
+ Source user name, host name, or asset name
+ **Total number of sources**
+ **Top five sources by magnitude**
+ Source networks
+ Destination IP address
+ Destination user name, host name, or asset name
+ **Total number of destinations**
+ Top five destinations by magnitude
+ Destination networks
+ Total number of events
+ Rules that caused the offense or event rule to fire
+ Full description of the offense or event rule
+ Offense ID
+ **Top five categories**
+ Start time of the offense or the time the event was generated
+ Top five annotations
+ Link to the offense user interface
+ Contributing CRE rules

| Option          | Description                                                                                       |
| :-------------- | :------------------------------------------------------------------------------------------------ |
| Parameter       | Description                                                                                       |
| To              | Type the email address of the user you want to notify when a change occurs to theselected offense |
| From            | Type the originating email address. The default is root@localhost.com.                            |
| E-mail Subject  | Type the subject for the email. The default is Offense ID.                                        |
| Email Message   | TEmail Message Type the standard message that you want to accompany the notification email.       |
___

> Mark an offense for follow-up when you want to flag it for further investigation.
___

***An event is a record from a log source***

The **Log Activity** tab specifies which events are associated with offenses.

*Rules*
+ A threshold rule tests event traffic for activity that exceeds a configured threshold.
+ A behavioral rule tests event traffic for abnormal activity, such as the existence of new or unknown traffic
+ An anomaly rule tests event traffic for abnormal activity, such as the existence of new or unknown traffic

*Actions*
+ Show All
+ Print
+ Export to XML > Visible Columns
+ Export to XML > Full Export (All Columns)
+ Export to CSV >Visible Columns
+ Export to CSV > Full Export (All Columns)
+ Delete
+ Notify

**Quick Filter**

> Select Quick Filter from the list box to search payloads by using simple words or phrases.

The default view on the **Log Activity** tab is a stream of real-time events.

**Status bar**

> When streaming events, the status bar displays the average number of results that are received per second.

> This is the number of results the Console successfully received from the Event processors. If this number is greater than 40 results per second, only 40 results are displayed. The remainder is accumulated in the result buffer. To view more status information, move your mouse pointer over the status bar.

> When events are not being streamed, the status bar displays the number of search results that are currently displayed on the tab and the amount of time that is required to process the search results.
___

> Streaming mode will enable you to view event data that enters your system. This mode provides you with a real-time view of your current event activity by displaying the last 50 events. Streaming mode does not support searches that include grouped events. If you enable streaming mode on grouped events or grouped search criteria, the **Log Activity** tab displays the normalized events.

> When the streaming is paused, the last 1,000 events are displayed.
___

> Events are collected in raw format, and then normalized for display on the **Log Activity** tab.

*Current Statistics*
+ **Total Results** - Specifies the total number of results that matched your search criteria.
+ **Data Files Searched** - Specifies the total number of data files searched during the specified time span.
+ **Compressed Data Files Searched** - Specifies the total number of compressed data files searched within the specified time span.
+ **Index File Count** - Specifies the total number of index files searched during the specified time span.
+ **Duration** - Specifies the duration of the search.
___

+ *You can view raw event data, which is the unparsed event data from the log source.*
+ *You can view a list of events in various modes, including streaming mode or in event groups.*
+ *If an event matches a rule, an offense can be generated on the Offenses tab.*
+ *You can manually map a normalized or raw event to a high-level and low-level category (or QID).*
+ **Note:** *The Map Event icon is disabled for events when the high-level category is SIM Audit or the log source type is Simple Object Access Protocol (SOAP).*
___

**Before beginning**: You can tune false positive events from the **event list** or **event details** page.

You can tune false positive events from the **event list** or **event details** page.
___

You can export events in Extensible Markup Language (XML) or Comma-Separated Values (CSV) format.

*Actions list box*:
+ **Export to XML > Visible Columns**
+ **Export to XML > Full Export (All Columns)**
+ **Export to CSV > Visible Columns**
+ **Export to CSV > Full Export (All Columns)**
___
