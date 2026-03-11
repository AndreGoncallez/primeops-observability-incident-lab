# PrimeOps Observability Incident Lab

A hands-on observability lab built to simulate infrastructure monitoring and incident analysis using open-source tools.

## Objective

This project demonstrates a basic monitoring and observability stack focused on host-level infrastructure metrics, dashboard visualization and incident investigation.

## Stack

- Docker
- Prometheus
- Node Exporter
- Grafana

## Monitored Metrics

- CPU utilization
- Memory utilization
- Network inbound traffic
- Network outbound traffic
- System load

## Architecture

Node Exporter exposes host metrics through an HTTP endpoint.  
Prometheus scrapes and stores these metrics as time series data.  
Grafana queries Prometheus and visualizes the collected metrics through dashboards.

## Dashboard

The Grafana dashboard includes panels for:

- Host CPU Utilization
- Host Memory Utilization
- Network Inbound Traffic
- Network Outbound Traffic

## Evidence

Screenshots of the running environment are available in the `evidence/` directory.

## Project Structure

```text
monitoring/   # Docker Compose and Prometheus configuration
dashboards/   # Dashboard-related files
runbooks/     # Incident response documentation
scenarios/    # Incident simulation ideas
evidence/     # Screenshots of the lab
