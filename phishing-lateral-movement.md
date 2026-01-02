# Phishing with Lateral Movement

## Incident Overview
A targeted phishing attack leading to credential compromise, followed by unauthorized lateral movement across internal enterprise systems.
The incident impacts identity security, endpoint integrity, and potentially sensitive organizational assets.

## Initial Detection
- User-reported suspicious email or automated email security alerts
- Authentication anomalies such as excessive failed logins, impossible travel, or logins from unfamiliar locations
- Endpoint alerts indicating abnormal process execution or credential access
- Network traffic anomalies suggesting lateral movement activity

## Investigation & Analysis
- Analyze the phishing email, including headers, sender reputation, and payload or embedded URLs
- Review endpoint telemetry for malicious execution, credential dumping, or persistence mechanisms
- Examine authentication logs for compromised accounts and access patterns
- Correlate network traffic logs to identify lateral movement techniques and affected systems
- Identify the scope of the incident, including additional compromised users or assets

## Containment Actions
- Immediately isolate affected endpoints from the network
- Disable or restrict compromised user accounts and enforce credential resets
- Block malicious domains, IP addresses, and file hashes across security controls
- Apply temporary network segmentation to limit further lateral movement
- Notify relevant stakeholders and escalate according to incident severity

## Eradication Steps
- Remove malicious files, scripts, or persistence mechanisms from affected systems
- Reset credentials for all impacted accounts and review privileged access
- Patch exploited vulnerabilities and harden authentication mechanisms
- Validate that no unauthorized access remains within the environment

## Recovery
- Gradually restore systems to production following validation and approval
- Increase monitoring on previously affected assets and accounts
- Confirm normal business operations and service availability
- Conduct post-incident verification to ensure full remediation

## Lessons Learned
- Identify gaps in email security, user awareness, or detection capabilities
- Assess response effectiveness and decision-making during the incident
- Update detection rules, playbooks, and security controls based on findings
- Provide targeted security awareness training to reduce future phishing risk
