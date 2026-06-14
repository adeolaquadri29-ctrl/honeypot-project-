SSH Honeypot Monitoring Lab

Overview

This project demonstrates the deployment of a SSH honeypot environment using Cowrie, integrated with the Elastic Stack (ELK) for centralized log collection, monitoring, and visualization.

The objective of the project is to simulate a vulnerable SSH server, capture attacker activity, forward logs to Elasticsearch using Filebeat, and visualize attack data through Kibana dashboards.

Architecture

Attacker → Cowrie Honeypot → Filebeat → Elasticsearch → Kibana Dashboard

Technologies Used

* Cowrie Honeypot
* Filebeat
* Elasticsearch
* Kibana
* Docker
* Ubuntu Linux

Features

* Captures SSH login attempts
* Records attacker commands
* Tracks source IP addresses
* Monitors successful and failed logins
* Visualizes attack activity through Kibana dashboards
* Centralized log management using Elasticsearch

Dashboard Metrics

* Total Events
* Successful Logins
* Failed Logins
* Top Source IPs
* Commands Executed
* Attack Timeline

Screenshots

See the screenshots folder for dashboard images and attack visualizations.

Skills Demonstrated

* Security Monitoring
* Log Analysis
* Threat Detection
* SIEM Operations
* ELK Stack Administration
* Honeypot Deployment
* Cybersecurity Incident Analysis

Future Improvements

* GeoIP enrichment
* Threat intelligence integration
* Automated alerting
* SOAR-style response actions
* Email and Discord notifications

Author

Adeola Quadri

Cybersecurity Analyst | SOC Analyst | Security Monitoring Enthusiast
