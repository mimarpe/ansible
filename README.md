# ansible
Ansible roles and playbooks to deploy and configure Apache Casandra and Spark, and create a full monitoring stack (that can be run independently from Cassandra). It is based on Prometheus+Alertmanager+Grafana+Blackbox+Cadvisor+Cassandra-Reaper and optionally Nginx, over Docker.

The roles for Cassandra allow to:
  - setup and tuning
  - post-setup
  - start
  - stop
  - create root and node certificates to run with TLS
  - create snapshots and upload to IBM Tivoli (TSM) servers
  - restore from snapshots in IBM Tivoli (TSM) servers
  
The roles for Spark allow to:
- setup
- start
- stop
  
The monitoring over Docker roles allow to:
- prometheus setup and configuration  (possibility of 2+ instances)
- alertmanager (possibility to clusterize 2+ instances)
- blackbox exporter to check certificate expiration and endpoint availability (for https and tls sockets)
- grafana with dashboards for cassandra, machine info and prometheus
- cadvisor for containers information and metrics
- cassandra-reaper to run and schedule cassandra repairs
- nginx to provide tls and proxying
