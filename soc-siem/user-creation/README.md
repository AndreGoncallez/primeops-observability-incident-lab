# Unauthorized User Creation Scenario

![Wazuh](https://img.shields.io/badge/Wazuh-SIEM-red)
![Windows Logs](https://img.shields.io/badge/Windows-Event_Logs-blue)
![Active Directory](https://img.shields.io/badge/AD-User_Management-purple)
![Incident Response](https://img.shields.io/badge/IR-Workflow-orange)

A hands-on security scenario focused on detecting and analyzing unauthorized user creation, a common persistence technique used by attackers after gaining access to a system.

---

# Overview

This scenario simulates the creation of a new user account in a system or domain environment.

The objective is to practice:

- detection of unauthorized account creation
- analysis of privileged actions
- investigation of persistence mechanisms
- incident response decision-making

---

# Scenario Description

A new user account is created on the system.

This action may be:

- legitimate (administrative activity)
- suspicious (unauthorized action)
- malicious (attacker persistence)

The analyst must determine the context and decide how to respond.

---

# Threat Context

Attackers often create new accounts after gaining access in order to:

- maintain persistence
- avoid detection
- regain access later
- escalate privileges
- establish backdoor access

This makes user creation a critical event to monitor in any environment.

---

# Log Analysis

Relevant Windows Security Events:

- **EventID 4720** → User account created
- **EventID 4722** → User account enabled
- **EventID 4723 / 4724** → Password change or reset
- **EventID 4732 / 4733** → User added or removed from group

---

# Key Indicators

During investigation, the analyst should evaluate:

- who created the user
- when the user was created
- whether the creator account is legitimate
- whether the new account has elevated privileges
- whether the action occurred during expected hours
- whether there is any related suspicious activity

---

# Detection Logic

This scenario can be identified through SIEM rules such as:

- detection of EventID 4720
- alert on user creation outside business hours
- alert on privileged user creation
- correlation with suspicious login activity
- correlation with brute force or PowerShell events

---

# Investigation Approach

A structured investigation should include:

### 1. Validate the event
Confirm that a user account was created.

### 2. Identify the creator
Check which account performed the action.

- is it an administrator?
- is it expected behavior?

### 3. Analyze the created account
- username pattern
- assigned groups
- privilege level

### 4. Check timeline correlation
Look for related events such as:

- brute force attempts
- suspicious logins
- PowerShell execution
- privilege escalation

### 5. Assess legitimacy
Determine whether the action is:

- authorized administrative task
- suspicious but explainable
- unauthorized / malicious

---

# Incident Response

## 1. Identification
User account creation detected via logs or SIEM alert.

## 2. Containment
If suspicious:

- disable or remove the created account
- remove privileges if already assigned
- isolate affected system if needed

## 3. Analysis
- investigate the account that created the user
- review logs before and after creation
- determine if attacker activity is present

## 4. Preservation
- preserve logs and timestamps
- avoid deleting evidence prematurely
- document all findings

## 5. Documentation
- record incident details
- classify the event (legitimate vs malicious)
- describe actions taken

---

# Analyst Decision-Making

User creation is not always malicious.

The analyst must evaluate:

- context of the action
- identity of the creator
- privilege level of the new account
- timing and correlation with other events

Good decisions rely on:

- evidence
- context
- business awareness

---

# Example Findings

Possible outcomes:

- legitimate admin-created account
- suspicious user creation outside normal pattern
- unauthorized account with elevated privileges
- persistence mechanism after initial compromise
- malicious activity requiring escalation

---

# Evidence

Suggested evidence to attach:

- Windows Security logs (EventID 4720)
- Wazuh alerts
- user account details
- group membership changes
- timeline of events

---

# Skills Demonstrated

This scenario demonstrates:

- Active Directory event analysis
- SIEM correlation
- detection of persistence techniques
- investigation of privileged actions
- incident response workflow
- security decision-making

---

# Use Cases

This scenario is useful for:

- SOC operations
- identity security monitoring
- AD security analysis
- incident response training
- persistence detection

---

# Recommended Next Steps

- privilege escalation scenario
- lateral movement detection
- anomalous login analysis
- persistence via scheduled tasks

---

# PrimeOps Mindset

> Think before acting  
> Understand before changing  
> Document to evolve
