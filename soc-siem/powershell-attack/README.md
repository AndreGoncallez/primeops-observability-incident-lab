# Suspicious PowerShell Execution Scenario

![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-red)
![Windows Logs](https://img.shields.io/badge/Windows-Event_Logs-blue)
![PowerShell](https://img.shields.io/badge/PowerShell-Suspicious-darkblue)
![Incident Response](https://img.shields.io/badge/IR-Workflow-orange)

A hands-on security scenario focused on detecting and analyzing suspicious PowerShell execution through Windows logs, process behavior and SIEM concepts.

---

# Overview

This scenario simulates suspicious PowerShell activity commonly associated with:

- malicious script execution
- encoded command usage
- remote payload download
- attacker post-exploitation behavior
- defense evasion techniques

The objective is to practice how a SOC analyst identifies suspicious execution patterns and decides how to respond without destroying evidence.

---

# Scenario Description

A PowerShell process is executed in a suspicious way to simulate attacker behavior on a Windows endpoint.

Examples of suspicious characteristics include:

- use of `-EncodedCommand`
- hidden execution
- bypass execution policy
- download-and-execute behavior
- abnormal parent process relationship

This scenario helps demonstrate how PowerShell, although legitimate, can be abused for malicious activity.

---

# Threat Context

PowerShell is a native administrative tool in Windows environments.

Because it is legitimate and widely available, attackers often use it for:

- initial execution
- payload download
- privilege escalation support
- persistence
- lateral movement
- in-memory execution

This makes PowerShell abuse an important detection use case for blue team operations.

---

# Simulated Attack Pattern

## Suspicious behavior examples

- `powershell.exe -EncodedCommand ...`
- `powershell.exe -ExecutionPolicy Bypass ...`
- PowerShell launched from unexpected process
- PowerShell spawning network connections
- PowerShell followed by scheduled task creation or user creation

## Why it matters

These patterns are often associated with:

- malware delivery
- command and control activity
- malicious administration
- fileless attacks
- LOLBins / Living Off the Land techniques

---

# Log Analysis

Relevant telemetry for this scenario may include:

- PowerShell process execution events
- Windows Security logs
- PowerShell Operational logs
- Sysmon logs (if enabled)
- Wazuh alerts and correlation

## Important events and indicators

### Process-related indicators
- execution of `powershell.exe`
- suspicious command-line arguments
- hidden or obfuscated commands
- unexpected parent-child process relationships

### Security indicators
- encoded commands
- use of `IEX` (Invoke-Expression)
- execution policy bypass
- download functions such as `Invoke-WebRequest` or `Net.WebClient`
- PowerShell activity followed by persistence behavior

---

# Detection Logic

This scenario can be identified through SIEM logic such as:

- detecting `powershell.exe` with `-EncodedCommand`
- matching suspicious keywords in command line
- detecting execution policy bypass attempts
- correlating PowerShell with outbound network connections
- correlating PowerShell with persistence artifacts

This supports detection of malicious or high-risk PowerShell activity.

---

# Investigation Approach

A structured investigation should include:

### 1. Validate the process execution
Confirm whether PowerShell was launched with suspicious parameters.

### 2. Review the command line
Look for indicators such as:

- `-EncodedCommand`
- `-nop`
- `-w hidden`
- `-ExecutionPolicy Bypass`
- `IEX`
- remote URL access

### 3. Identify the parent process
Determine what launched PowerShell.

Examples:
- `explorer.exe` → user-driven
- `winword.exe` → suspicious if tied to malicious macro
- `wscript.exe` or `cmd.exe` → suspicious depending on context

### 4. Check for follow-up behavior
Look for:

- network connections
- file creation
- scheduled tasks
- registry modifications
- new user creation
- privilege escalation attempts

### 5. Assess impact
Determine whether the event is:

- legitimate administrative activity
- suspicious but inconclusive
- clearly malicious

---

# Incident Response

The response should be evidence-driven and proportional to risk.

## 1. Identification
Suspicious PowerShell execution detected through logs or SIEM alerts.

## 2. Containment
Depending on severity:

- isolate the host if active compromise is suspected
- restrict suspicious network communication
- suspend malicious process if necessary and safe
- protect affected accounts if credentials may have been exposed

## 3. Analysis
- decode the encoded command if present
- review related logs and timeline
- correlate with persistence or network indicators
- identify whether this was user action, admin action or attacker activity

## 4. Preservation
- preserve logs and process details
- avoid rebooting the machine prematurely
- document command lines, timestamps and affected users

## 5. Documentation
- record findings and actions taken
- classify the event
- document if it was malicious, benign admin activity or false positive

---

# Analyst Decision-Making

This scenario reinforces a key analyst principle:

PowerShell is not malicious by itself.

The analyst must evaluate:

- context
- command line
- parent process
- related events
- timing
- business justification

Strong decisions come from evidence, not assumptions.

---

# Example Findings

Possible conclusions from this scenario:

- legitimate administrative script execution
- suspicious obfuscated PowerShell requiring escalation
- malicious encoded command with network communication
- PowerShell abuse followed by persistence mechanism
- probable fileless attack activity

---

# Evidence

Suggested evidence to attach in this folder or in the `evidence/` area:

- Wazuh alert screenshots
- PowerShell execution logs
- command-line capture
- screenshots showing encoded command detection
- notes about source host, affected user and timeline

---

# Skills Demonstrated

This scenario demonstrates practical experience with:

- suspicious PowerShell detection
- Windows log analysis
- SIEM correlation
- investigation of encoded commands
- process relationship analysis
- incident response workflow
- analyst reasoning in endpoint security context

---

# Use Cases

This scenario is useful for practicing:

- SOC monitoring
- endpoint investigation
- PowerShell abuse detection
- log-based triage
- suspicious execution analysis
- blue team incident response

---

# Recommended Next Steps

After completing this scenario, the next recommended scenarios are:

- anomalous login investigation
- unauthorized user creation
- persistence via scheduled tasks
- lateral movement analysis

---

# PrimeOps Mindset

> Think before acting  
> Understand before changing  
> Document to evolve
