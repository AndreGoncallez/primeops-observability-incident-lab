# PrimeOps Observability & Security Incident Lab

![Docker](https://img.shields.io/badge/Docker-Container-blue)
![Prometheus](https://img.shields.io/badge/Prometheus-Monitoring-orange)
![Grafana](https://img.shields.io/badge/Grafana-Dashboard-yellow)
![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-red)
![Security](https://img.shields.io/badge/Security-BlueTeam-darkred)
![Observability](https://img.shields.io/badge/Observability-Lab-green)

A hands-on lab designed to simulate both **observability and security incident response**, combining infrastructure monitoring with SIEM-based threat detection.

This project demonstrates how modern environments integrate monitoring, logging and security analysis to support real-world incident investigation.

---

# Overview

This lab simulates a production-like environment where:

- Infrastructure metrics are collected and visualized
- Security events are detected and analyzed
- Incidents are investigated using logs and observability data

The goal is to build a **real analyst mindset**, combining monitoring with security operations.

---

# Monitoring & Security Stack

The environment includes:

### 📊 Observability
- **Prometheus** – time-series metrics collection
- **Node Exporter** – host-level metrics
- **Grafana** – dashboards and visualization

### 🔐 Security / SIEM
- **Wazuh** – log analysis and threat detection
- **Event Logs** – authentication and system activity
- **Correlation Rules** – detection of suspicious behavior

### ⚙️ Infrastructure
- **Docker** – containerized environment

---

# Monitored Metrics

The monitoring layer includes:

- Host CPU Utilization
- Host Memory Utilization
- Network Inbound Traffic
- Network Outbound Traffic
- System Load

These metrics support performance analysis and incident investigation.

---

# Security Scenarios (SOC / SIEM)

This lab also simulates security events such as:

- Brute force attacks (multiple failed logins)
- Suspicious PowerShell execution
- Anomalous login behavior
- Unauthorized user creation (persistence)

These scenarios help practice detection and response using logs.

---

# Architecture

### Observability Flow

Host System  
│  
▼  
Node Exporter  
│  
▼  
Prometheus (metrics collection)  
│  
▼  
Grafana (visualization)  

---

### Security Flow (SIEM)

Host / Endpoint  
│  
▼  
Wazuh Agent  
│  
▼  
Wazuh Server (log analysis & correlation)  
│  
▼  
Alerts & Investigation  

---

# Dashboard Example

Grafana dashboard displaying infrastructure metrics.

![Grafana Dashboard](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/grafana-dashboard.png)

---

# Prometheus Targets

Prometheus scraping Node Exporter metrics.

![Prometheus Targets](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/prometheus-targets.png)

---

# Running Containers

Docker containers used in the environment.

![Docker Containers](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/docker-containers.png)

---

# Alert Rules

Basic alerting is implemented using Prometheus rules.

**High CPU Usage Alert**

Triggers when CPU usage remains above threshold.

![Prometheus Rules](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/prometheus-rules.png)

---

# Skills Demonstrated

This project demonstrates practical experience with:

- Infrastructure Monitoring
- Observability Fundamentals
- SIEM & Log Analysis (Wazuh)
- Incident Detection & Response
- Prometheus Metrics Collection
- Grafana Dashboard Design
- Docker-based Infrastructure
- Troubleshooting Based on Metrics and Logs

---

# Project Structure


monitoring/ # Prometheus, Grafana and metrics stack
soc-siem/ # Security lab with Wazuh and incident scenarios
dashboards/ # Grafana dashboards
runbooks/ # Incident response procedures
scenarios/ # Simulated incidents
evidence/ # Screenshots and logs
scripts/ # Supporting scripts
docs/ # Documentation


---

# Use Cases

This lab was created to practice:

- Infrastructure monitoring
- Observability analysis
- Security event detection
- Log investigation
- Incident response workflows
- Troubleshooting based on data

---

# Future Improvements

Planned improvements include:

- Wazuh alert rule customization
- Advanced attack simulations (lateral movement, persistence)
- Integration with automation (SOAR / n8n)
- Alertmanager integration
- Automated incident response workflows
- Expanded dashboards and metrics

---

# Author

**Andre Goncallez**  
PrimeOps Project

---

# PrimeOps Mindset

> Think before acting  
> Understand before changing  
> Document to evolve
