### Categorize Responsibilities
|Prometheus and Grafana Screenshots|
|---|
|Provide a screenshot of the Prometheus node_exporter service running on the EC2 instance. Use the following command to show that the system is running: sudo systemctl status node_exporter|
|---|
|![default ns](/evidence/status_node_exporter.png)|
|---|


|Host Metric (CPU, RAM, Disk,  Network)|Dashboard|
|---|---|
|CPU|![default ns](/evidence/CPU.png)|
|---|---|
|Memory Total|![default ns](/evidence/Memory.png)|
|---|---|
|Disk I/O|![default ns](/evidence/Disk-IO.png)|
|---|---|
|Network Transmit|![default ns](/evidence/Network.png)|
|---|---|

|Responsibilities|
|---|
|1. The development team wants to release an emergency hotfix to production. Identify two roles of the SRE team who would be involved in this and why.|
|---|
|Release Engineer and Monitoring Engineer. Because Release Engineer will manage the release and Monitoring Engineer will monitor the new hotfix will run well in production|
|---|
|2. The development team is in the early stages of planning to build a new product. Identify two roles of the SRE team that should be invited to the meeting and why.|
|---|
|System Architect and Infrastructure Engineer. Because System architects have a knowledge about the architecture so they will provide solutions faster and Infrastructure will know infrastructure that will map with the new feature|
|---|
|3. The emergency hotfix from question 1 was applied and is causing major issues in production. Which SRE role would primarily be involved in mitigating these issues?|
|---|
|Release Engineers will be better, because their responsibility of them is to manage release, so they will know about the issue will come from exact role|


### Team Formation and Workflow Identification
|API Monitoring and Notifications|
|---|
|Display the status of an API endpoint: Provide a screenshot of the Grafana dashboard that will show at which point the API is unhealthy (non-200 HTTP code), and when it becomes healthy again (200 HTTP code).|
|---|
|![default ns](/evidence/API_HealthCheck.png)|
|---|
|Create a notification channel: Provide a screenshot of the Grafana notification which shows the summary of the issue and when it occurred.|
|---|
|![default ns](/evidence/alert_flaskApp_1.png)
 ![default ns](/evidence/alert_flaskApp_2.png)|
|---|
|Configure alert rules: Provide a screenshot of the alert rules list in Grafana.|
|---|
|![default ns](/evidence/status_alert-rule_1.png)
 ![default ns](/evidence/status_alert-rule_2.png)|


### Applying the Concepts
|API Heathcheck|
|---|
|![default ns](/evidence/API_HealthCheck.png)|
|---|
|4a. Given the above graph, where does it show that the API endpoint is down? Where on the graph does this show that the API is healthy again?|
|---|
|API endpoint is down at 00:37:30 and it healthy again at 00:45:30|
|---|
|4b. If there was no SRE team, how would this outage affect customers?|
|---|
|The API endpoint of customers will not be known and maybe the downtime will be more than the metrics|
|---|
|4c. What could be put in place so that the SRE team could know of the outage before the customer does?|
|---|
|I think the SRE team rely on metrics healthcheck of instance to know when server outage|
|---|
|Netwok Receive|
|---|
|![default ns](/evidence/Network_received.png)|
|---|
|5a. Given the above graph, which instance had the increase in traffic, and approximately how many bytes did it receive (feel free to round)?|
|---|
|10.0.0.68:9100 had the increase in traffice, the latest in graph that it receive about 4900 bytes|
|---|
|5b. Which team members on the SRE team would be interested in this graph and why?|
|---|
|Monitoring Engineer  would be intersted in this graph, because in this role, they will need to monitoring |