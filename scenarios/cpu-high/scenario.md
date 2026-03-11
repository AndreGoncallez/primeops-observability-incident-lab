\# Scenario: High CPU Usage



\## Objective



Simulate a high CPU load to observe how the monitoring stack reacts and how the incident can be investigated using Grafana and Prometheus.



\---



\## Simulation



Run the following command in the host system:



```bash

yes > /dev/null



This command continuously generates CPU load.



Expected Behavior



The Grafana dashboard should show:



CPU utilization spike



Increase in system load



Normal memory usage



Possible increase in network activity



Investigation



Steps to investigate the issue:



Open Grafana dashboard



Identify the spike in Host CPU Utilization



Check System Load panel



Correlate metrics with system behavior



Resolution



Stop the process generating CPU load:



killall yes



CPU metrics should return to normal levels after stopping the process.



Learning Outcome



This scenario helps practice:



incident detection



observability analysis



metric correlation



troubleshooting using monitoring dashboards

