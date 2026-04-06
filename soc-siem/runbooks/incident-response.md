# Incident Response Runbook

## Objective

Provide a structured approach to handle security incidents.

---

# Severity Levels

- SEV1 → Critical (active compromise)
- SEV2 → High (strong indicators of attack)
- SEV3 → Medium (suspicious activity)
- SEV4 → Low (informational)

---

# Incident Workflow

## 1. Detection
- alert from SIEM
- abnormal logs
- suspicious behavior

## 2. Validation
- confirm if event is real
- rule out false positive

## 3. Classification
- brute force
- execution
- persistence
- lateral movement

## 4. Containment
- isolate host if necessary
- block suspicious access
- protect accounts

## 5. Investigation
- analyze logs
- correlate events
- build timeline

## 6. Recovery
- remove malicious artifacts
- restore systems

## 7. Documentation
- record incident
- actions taken
- lessons learned

---

# Key Principles

- do not destroy evidence
- prioritize containment
- act based on evidence
- maintain service availability when possible

---

# Analyst Checklist

- what happened?
- when did it start?
- who is affected?
- what is the impact?
- is it contained?
- what evidence exists?

---

# PrimeOps Standard

- structured thinking
- evidence-based decisions
- clear documentation
