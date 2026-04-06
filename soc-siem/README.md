# SOC / SIEM Lab - Incident Detection & Response

![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-red)
![Security](https://img.shields.io/badge/Security-BlueTeam-darkred)
![Logs](https://img.shields.io/badge/Logs-Analysis-blue)
![Incident Response](https://img.shields.io/badge/IR-Response-orange)

A hands-on security lab focused on **incident detection, log analysis and response**, simulating real-world attack scenarios using SIEM concepts.

---

# Overview

This module simulates how a Security Operations Center (SOC) detects and responds to threats.

The lab focuses on:

- Log analysis
- Event correlation
- Suspicious behavior detection
- Incident response decision-making

---

# Security Stack

- **Wazuh** – SIEM for log collection and analysis  
- **Windows Event Logs** – authentication and system activity  
- **Correlation Rules** – detection of abnormal behavior  

---

# Simulated Attack Scenario

## 🚨 Brute Force Attack

A simulated brute force attack was performed against a system to generate multiple failed authentication attempts.

### Observed behavior:

- Multiple failed login attempts (EventID 4625)
- Short time interval between attempts
- Same source targeting different users

This pattern is consistent with a **password spraying attack**.

---

# Log Analysis

Relevant logs identified:

- EventID 4625 → Failed login attempts
- EventID 4624 → Successful login (if compromise occurs)

### Indicators:

- High number of failed authentication events
- Repeated login attempts across accounts
- Potential account compromise

---

# Detection

The SIEM (Wazuh) detects this pattern through:

- Threshold-based rules
- Event correlation
- Authentication anomaly detection

This generates alerts indicating suspicious login activity.

---

# Incident Response

The response follows structured incident response practices:

### 1. Identification
Suspicious authentication activity detected through logs.

### 2. Containment
- Block or restrict suspicious source (if applicable)
- Monitor affected accounts
- Prevent further login attempts

### 3. Analysis
- Review logs for successful authentication
- Identify targeted accounts
- Check for lateral movement

### 4. Preservation
- Avoid destructive actions
- Preserve logs for investigation

### 5. Documentation
- Record actions taken
- Document findings

---

# Analyst Mindset

This scenario demonstrates key SOC principles:

- Think before acting
- Contain before remediation
- Analyze before making decisions
- Avoid actions that destroy evidence

---

# Evidence

(Insert screenshots here)

Examples:

- Wazuh alerts
- Authentication logs
- Event correlation

---

# Skills Demonstrated

- SIEM usage (Wazuh)
- Log analysis (Windows Events)
- Attack detection (Brute Force / Password Spraying)
- Incident Response workflow
- Security event correlation
- Analytical thinking

---

# Use Cases

This module supports practice in:

- SOC operations
- Security monitoring
- Threat detection
- Incident response
- Log investigation

---

# Future Improvements

- Simulate lateral movement attacks
- Add PowerShell attack scenarios
- Implement alert tuning
- Integrate automated response (SOAR)
- Expand detection rules

---

# PrimeOps Method

> Think before acting  
> Understand before changing  
> Document to evolve
