# License management


License keys entitle you to specific IBM QRadar products, and control the event and flow capacity for your QRadar deployment. You can add licenses to your deployment to activate other QRadar products, such as QRadar Vulnerability Manager.

To apply a license key to the system, follow these steps:
1. Obtain the license key. For new or updated license keys, contact your local sales representative.
2. Upload the license key.
3. Allocate the license to a system.
4. Deploy the full configuration.

The temporary license key allows for 5,000 events per second (EPS) on the QRadar Console, and 10,000 EPS on each managed host.
The FPM rate for the temporary license is 200,000 on both the QRadar Console and the managed hosts.

### Event and flow processing capacity

The capacity of a deployment is measured by the number of events per second (EPS) and flows per minute (FPM) that IBM QRadar can collect, normalize, and correlate in real time. The event and flow capacity is set by the licenses that are uploaded to the system.

##### Shared license pool

The EPS and FPM rate that is set by each license is combined into a shared license pool. From the shared license pool, you can distribute the processing capacity to any host within a specific deployment or that is managed by a single console, regardless of which host the original license is allocated to.

##### Capacity sizing

The best way to deal with spikes in data is to ensure that your deployment has enough events per second (EPS) and flows per minute (FPM) to balance peak periods of incoming data. The goal is to allocate EPS and FPM so that the host has enough capacity to process data spikes efficiently, but does not have large amounts of idle EPS and FPM.

##### Incremental licensing

Incremental licensing streamlines the license distribution process and saves you time and effort because you don't need separate licenses for each appliance. Purchase monthly capacity increases that can be applied to your deployment, without running the risk that these temporary keys might shut down the entire system when they expire. Now, you can add more flows and events to the Console license and redistribute to your pool of appliances as you see fit.

##### Internal events

IBM QRadar appliances generate a small number of internal events when they communicate with each other as they process data. To ensure that the internal events are not counted against the allocated capacity, the system automatically returns all internal events to the license pool immediately after they are generated.

### Burst handling

IBM QRadar uses burst handling to ensure that no data is lost when the system exceeds the allocated events per second (EPS) or flows per minute (FPM) license limits. When QRadar receives a data spike that causes it to exceed the allocated EPS and FPM limits, the extra events and flows are moved to a temporary queue to be processed when the incoming data rate slows. *When burst handling is triggered, a system notification alerts you that the appliance exceeded the EPS or FPM license limit.*

> Example: Incoming data spike (PG. 50)

> Related tasks
+ Uploading a license key (pg. 51)
+ Allocating a license key to a host (pg. 52)
+ Distributing event and flow capacity (pg. 53)
+ Viewing license details (pg. 54)
+ Deleting licenses (pg. 54)
+ Exporting license information (pg. 55)
