# QRadar functional architecture and deployment models

+ Functional requirements of Q-Radar
![funcreq](funcreq.png)

+ SIOS - the top row describes all the apps that can be or are intergrated into Q-Radar
![sios+](sios+.png)

The benefits of *Security Intelligence Operative Systems* are:
+ Convergence
+ Simplicity
+ Scalability
_________________________________________________________________________________________________

![cmdcsl1](cmdcsl1.png)

Amongst the benefits you'll learn later on:

![cmdcsl2](cmdcsl2.png)

The Q-Radar console is the central interface for all analyst-related tasks. It's completely configurable.

![console](console.png)

The tabs of Q-Radar are used in the following manner:
+ *Offenses*: view all the offenses that occur in the IT environment. You can investigate:
  - offenses
  - source and destination IP addresses
  - network behaviours
  - anomalies
+ *Log activity* - view event information as records from a log source. You can investigate:
  - event data
  - monitor log activity
+ *Network activity* - view event information of network communication. You can investigate:
  - flows sent in real time
  - monitor network activity
+ *Assets* - view assets in the IT environment. They also:
  - discover and create asset profiles, by using *passive flow data* and *vulnerability data*
  - store information about assets (including *running services* and *vulnerability information*). This:
    + helps reduce false positives
    + gives more details for investigations
+ *Reports* - create, distribute and manage reports. There are a few kinds of reports:
  - Compliance
  - Device
  - Executive
  - Network
  - Custom
+ *Vulnerability* - create and manage scan policies and profiles. They allow for:
  - vulnerability scan execution
  - creation and distribution of vulnerability reports
+ *Admin* - tools that help with Q-Radar deployment management and maintenance
+ **If 3rd party Q-Radar additions are installed, they will show up next to these existing tabs**
_______________________________________________________________________________________________________

Q-Radar SIEM can analyze large amounts of data and use context to transform it into a useful format.

The following image is what a security analyst sees when investigating an offense record that was triggered by a correlation rule.

![attacks](attacks.png)

The *who* (username), *what* (description) and *where* (location) can immediately be seen in order to determine whether it's a legitimate threat or a false positive.

Q-Radar continuously monitors data sources across the IT infrastructure, leveraging the context in which systems are operating.

That context includes:
+ network device logs
+ vulnerabilities
+ configuration data
+ network traffic telemetry
+ application events and activities
+ user identities
+ asset information
+ geolocation
+ application content

![what](what.png)
___________________

To enable security analysts to perform investigations, Q-Radar SIEM correlates information such as:
+ Point in time
+ Offending users
+ Origins
+ Targets
+ Asset information
+ Vulnerabilities
+ Known threats
+ Behavioural analytics
+ Cognitive analytics
______________________

![flow1](flow1.png)

Q-Radar has an extensible architecture.

![efacogan](efacogan.png)
![efaoes](efaoes.png)
![efadtia](efadtia.png)
_________________________________________

![software](software.png)

![dplmod1](dplmod1.png)
![dplmod2](dplmod2.png)
_________________________________________

**Architecture**

![hlcads](hlcads.png)

![fca1](fca1.png)
![fca2](fca2.png)
![fca3](fca3.png)

![eca](eca.png)

![epa](epa.png)

![ca](ca.png)

There are 3 types of Anomaly Detection Rule types (image below):

![ca2](ca2.png)

![qradarend2](qradarend2.png)
