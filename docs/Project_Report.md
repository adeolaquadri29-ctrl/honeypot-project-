Project Report: SSH Honeypot Monitoring Lab

Introduction

Organizations face continuous attacks from malicious actors attempting to gain unauthorized access to systems. Honeypots provide valuable insight into attacker behavior by intentionally exposing controlled environments designed to attract threats.

This project implements a Cowrie SSH honeypot integrated with the Elastic Stack to collect, analyze, and visualize attacker activity.

Objectives

* Deploy a functional SSH honeypot
* Capture attacker interactions
* Centralize logs using Elasticsearch
* Visualize attack activity through Kibana
* Develop hands-on SOC monitoring skills

Environment

Operating System

Ubuntu Linux

Components

* Cowrie Honeypot
* Filebeat
* Elasticsearch
* Kibana
* Docker Containers

Implementation

Honeypot Deployment

Cowrie was deployed inside a Docker container and configured to listen for SSH connections.

Log Collection

Cowrie generated JSON logs containing:

* Connection events
* Login attempts
* Session information
* Commands executed

Log Forwarding

Filebeat was configured to monitor Cowrie logs and forward them to Elasticsearch.

Data Visualization

Kibana dashboards were created to provide visibility into:

* Login attempts
* Source IP addresses
* Command execution activity
* Event volume trends

Results

The honeypot successfully captured attacker interactions including:

* Successful logins
* Failed logins
* Command execution attempts
* Reconnaissance activities

Example command captured:

wget malware.sh

Challenges Encountered

* Filebeat log parsing issues
* Data view configuration in Kibana
* Elasticsearch indexing verification
* Dashboard visualization setup

Lessons Learned

This project improved practical understanding of:

* SIEM technologies
* Log ingestion pipelines
* Security monitoring
* Incident detection workflows
* Honeypot deployment strategies

Conclusion

The project successfully demonstrated end-to-end monitoring of attacker activity using a honeypot integrated with the Elastic Stack. The implementation provides a realistic SOC-style environment for threat detection and security analysis.
