# Cloud Credential Compromise

## Incident Overview
Unauthorized access to cloud resources resulting from compromised cloud credentials such as API keys, access tokens, or IAM user credentials.
This incident poses a high risk to data confidentiality, service availability, and cloud account integrity.

## Initial Detection
- Alerts from cloud-native security services indicating anomalous API or management activity
- Authentication events from unfamiliar geolocations or untrusted IP addresses
- Unusual access to sensitive cloud services or data stores
- Unexpected creation, modification, or deletion of cloud resources

## Investigation & Analysis
- Review cloud audit logs (e.g. CloudTrail, Azure Activity Logs) to identify suspicious actions
- Identify compromised identities, roles, and associated permissions
- Analyze accessed services, modified resources, and potential data exposure
- Determine the attack timeline and assess lateral movement within the cloud environment
- Evaluate potential impact on connected systems or on-prem integrations

## Containment Actions
- Immediately disable or rotate compromised credentials (Credential rotation allows us to cut attacker access while maintaining service continuity. We generate new credentials, update dependent services, and only then revoke the compromised ones)
- Revoke active sessions and invalidate access tokens
- Apply restrictive IAM policies to affected identities
- Temporarily limit access to sensitive cloud resources
- Notify relevant stakeholders and escalate based on incident severity

## Eradication Steps
- Remove unauthorized cloud resources or malicious configurations
- Reset all affected credentials and enforce multi-factor authentication
- Review and tighten IAM policies following the principle of least privilege
- Validate that no persistence mechanisms remain in the cloud environment

## Recovery
- Gradually restore normal cloud operations following validation
- Increase monitoring for previously affected identities and services
- Confirm that logging, alerting, and access controls are fully operational
- Obtain management approval before returning to steady-state operations

## Lessons Learned
- Identify gaps in cloud credential management and access controls
- Improve visibility and alerting for cloud management activities
- Update cloud incident response procedures and playbooks
- Conduct targeted training on secure credential handling and cloud security awareness
