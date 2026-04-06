# SOC / SIEM Module - Security Operations Lab

![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-red)
![Security](https://img.shields.io/badge/Security-Operations-darkred)
![Blue Team](https://img.shields.io/badge/BlueTeam-Defense-blue)
![Incident Response](https://img.shields.io/badge/IR-Workflow-orange)

This module simulates a Security Operations Center (SOC) environment, focused on detection, investigation and response to security incidents.

---

# Overview

This SOC module complements the observability lab by introducing:

- security monitoring
- log analysis
- threat detection
- incident response workflows

It demonstrates how infrastructure monitoring and security operations work together in real-world environments.

---

# SOC Architecture

## Detection Layer
- Wazuh (SIEM)
- Windows Event Logs
- Process monitoring

## Analysis Layer
- Event correlation
- Behavioral analysis
- Timeline investigation

## Response Layer
- Incident containment
- Evidence preservation
- Documentation

---

# Attack Scenarios

This module includes realistic attack simulations:

- Brute Force → initial access attempts
- PowerShell Attack → execution phase
- User Creation → persistence technique

These scenarios reflect common attacker behavior patterns.

---

# Investigation Workflow

Each scenario follows a structured SOC workflow:

1. Detection
2. Validation
3. Investigation
4. Containment
5. Analysis
6. Documentation

---

# Integration with Observability

This project integrates:

- metrics (Prometheus)
- dashboards (Grafana)
- logs (SIEM)

This allows correlation between:

- system performance issues
- security incidents
- anomalous behavior

---

# Skills Demonstrated

- SIEM analysis (Wazuh)
- Windows log investigation
- Incident response workflow
- Threat detection
- Event correlation
- Analyst decision-making

---

# Project Structure


soc-siem/
├── scenarios/
│ ├── brute-force/
│ ├── powershell-attack/
│ ├── user-creation/
│
├── runbooks/
│ └── incident-response.md
│
└── logs/
└── windows-events.md


---

# Use Cases

- SOC training
- Security monitoring practice
- Incident response simulation
- Blue team skill development

---

# PrimeOps Method

> Think before acting  
> Understand before changing  
> Document to evolve
