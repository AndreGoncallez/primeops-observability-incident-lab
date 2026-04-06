# PrimeOps Observability & Security Incident Lab

![Docker](https://img.shields.io/badge/Docker-Container-blue)
![Prometheus](https://img.shields.io/badge/Prometheus-Monitoring-orange)
![Grafana](https://img.shields.io/badge/Grafana-Dashboard-yellow)
![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-red)
![Security](https://img.shields.io/badge/Security-BlueTeam-darkred)
![Observability](https://img.shields.io/badge/Observability-Lab-green)

A hands-on lab designed to simulate real-world scenarios combining **infrastructure monitoring**, **observability**, and **security incident response**.

This project demonstrates how modern environments integrate metrics, logs, and security analysis to support operational and security investigations.

---

# Overview

This lab simulates a production-like environment where:

- Infrastructure metrics are collected and visualized
- Security events are detected and analyzed
- Incidents are investigated using observability and SIEM concepts

The goal is to develop a **real analyst mindset**, combining monitoring and security operations.

---

# Monitoring & Security Stack

## 📊 Observability
- Prometheus – metrics collection and storage
- Node Exporter – host-level metrics
- Grafana – dashboards and visualization

## 🔐 Security / SIEM
- Wazuh – log analysis and threat detection
- Event Logs – authentication and system activity
- Correlation rules – detection of suspicious behavior

## ⚙️ Infrastructure
- Docker – containerized deployment

---

# Monitored Metrics

- CPU Utilization
- Memory Utilization
- Network Traffic (Inbound/Outbound)
- System Load

These metrics help detect abnormal behavior and support troubleshooting and incident investigation.

---

# Security Scenarios (SOC / SIEM)

This lab includes simulated attack scenarios:

- Brute force (multiple failed logins)
- Suspicious PowerShell execution
- Anomalous login behavior
- Unauthorized user creation (persistence)

These scenarios simulate real-world attack patterns and detection workflows.

---

# Incident Simulation

This lab also demonstrates how incidents are analyzed:

Example flow:

- Alert triggered (e.g., high CPU or login anomaly)
- Investigation through Grafana metrics
- Correlation with logs and processes
- Identification of abnormal behavior
- Decision-making based on evidence

This reflects real-world incident response workflows.

---

# Security Integration

This project integrates monitoring with security concepts:

- Detection of anomalous behavior
- Log-based investigation (SIEM approach)
- Incident response mindset
- Correlation between metrics and security events

---

# Architecture

## Observability Flow

Host System  
│  
▼  
Node Exporter  
│  
▼  
Prometheus (metrics collection)  
│  
▼  
Grafana (dashboard visualization)  

---

## Security Flow (SIEM)

Host / Endpoint  
│  
▼  
Wazuh Agent  
│  
▼  
Wazuh Server (analysis & correlation)  
│  
▼  
Alerts & Investigation  

---

# Dashboard Example

![Grafana Dashboard](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/grafana-dashboard.png)

---

# Prometheus Targets

![Prometheus Targets](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/prometheus-targets.png)

---

# Running Containers

![Docker Containers](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/docker-containers.png)

---

# Alert Rules

**High CPU Usage Alert**

Triggers when CPU usage exceeds threshold.

![Prometheus Rules](https://raw.githubusercontent.com/AndreGoncallez/primeops-observability-incident-lab/main/evidence/prometheus-rules.png)

---

# Skills Demonstrated

- Infrastructure Monitoring
- Observability Fundamentals
- SIEM & Log Analysis (Wazuh)
- Incident Detection & Response
- Prometheus Metrics Collection
- Grafana Dashboard Design
- Docker-based Infrastructure
- Troubleshooting based on metrics and logs

---

# Project Structure


monitoring/ # Prometheus, Grafana and metrics stack
soc-siem/ # Security lab with incident scenarios
dashboards/ # Grafana dashboards
runbooks/ # Incident response procedures
scenarios/ # Simulated incidents
evidence/ # Screenshots and logs
scripts/ # Supporting scripts
docs/ # Documentation


---

# Use Cases

- Infrastructure monitoring
- Observability analysis
- Security event detection
- Log investigation
- Incident response workflows
- Troubleshooting based on metrics

---

# Future Improvements

- Wazuh alert tuning
- Advanced attack simulations
- Integration with automation (SOAR / n8n)
- Alertmanager integration
- Automated incident response
- Expanded dashboards

---

# Author

Andre Goncallez  
PrimeOps Project

---

# PrimeOps Mindset

> Think before acting  
> Understand before changing  
> Document to evolve
