# Splunk Alert Analysis – Authentication Anomaly

## Context 
This investigation was conducted using Splunk training and lab environments focused on SOC analyst workflows.

## Alert Summary 
- Alert Type: Repeated failed authentication attempts
- Data Source: Windows authentication logs (lab data)
- Severity: Medium

## Investigation Process (What I Did)
- Used SPL to identify failed and successful login events
- Applied field extraction to correlate user accounts and source IPs
- Reviewed timestamps and login frequency to identify anomalies (Human error vs bot)

## What I Found
Analysis revealed multiple failed login attempts from a single external IP address, followed by a successful authentication. The pattern was inconsistent with typical user behavior and suggested potential credential guessing.

## Conclusion
The activity was classified as suspicious and warranted remediation due to the risk of account compromise.

## Recommended Remediation
- Reset the affected user's credentials immediately
- Block or monitor the source IP to stop the malicious activity
- Enforce multi-factor authentication to increase login security
- Review authentication alert thresholds to catch these patterns faster next time

