# Splunk Alert Analysis – Suspicious Login Activity

## Alert Summary
- Alert source: Splunk (lab environment)
- Alert type: Repeated failed authentication attempts
- Time detected: Simulated lab timeframe
- Severity: Medium

## Initial Assessment
The alert triggered due to multiple failed login attempts against a single user account over a short period of time, followed by a successful authentication. This pattern warranted further investigation to determine whether the activity was malicious or benign.

## Investigation Steps
- Reviewed Windows authentication logs in Splunk
- Examined source IP addresses and login frequency
- Analyzed timestamps to identify attack patterns
- Checked for successful authentication following failures

## Findings
Log analysis showed repeated failed login attempts originating from a single external IP address, followed by a successful login using the same account. The activity was inconsistent with normal user behavior and indicated potential credential guessing.

## Root Cause
The most likely cause was weak or reused credentials that allowed an attacker to successfully authenticate after multiple attempts.

## Remediation Actions
- Reset credentials for the affected account
- Block the source IP address
- Enable or enforce multi-factor authentication (MFA)
- Monitor the account for additional suspicious activity

## Lessons Learned
Improved alerting for authentication anomalies and stronger access controls would reduce the risk of similar activity in the future.
