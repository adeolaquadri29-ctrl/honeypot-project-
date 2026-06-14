Setup Guide

Prerequisites

* Ubuntu Linux
* Docker
* Internet Connectivity

Step 1: Deploy Elasticsearch

Run Elasticsearch container:

docker run -d 
–name elasticsearch 
-p 9200:9200 
-e discovery.type=single-node 
docker.elastic.co/elasticsearch/elasticsearch:8.12.0

Step 2: Deploy Kibana

docker run -d 
–name kibana 
-p 5601:5601 
–link elasticsearch 
docker.elastic.co/kibana/kibana:8.12.0

Step 3: Deploy Cowrie

docker run -d 
–name cowrie 
-p 2222:2222 
cowrie/cowrie

Step 4: Install Filebeat

Install Filebeat on Ubuntu.

Configure filebeat.yml to monitor:

/var/lib/docker/volumes/…/cowrie.json

Step 5: Start Filebeat

sudo systemctl enable filebeat

sudo systemctl start filebeat

Step 6: Verify Data Ingestion

Check Elasticsearch:

curl localhost:9200/_cat/indices?v

Verify Cowrie events are being indexed.

Step 7: Create Kibana Data View

Pattern:

filebeat-*

Time field:

@timestamp

Step 8: Build Dashboard

Create visualizations for:

* Total Events
* Successful Logins
* Failed Logins
* Source IPs
* Commands Executed

Verification

Generate SSH activity against the honeypot and confirm events appear in Kibana.
