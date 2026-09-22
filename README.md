# azure-iam-soc-lab
Hybrid cloud security lab: Identity and Access Management (IAM) and Microsoft Sentinel detection engineering using Microsoft Azure

## Project goals
- Configure Entra ID identity controls (RBAC, Conditional Access, MFA)
- Detect simulated attacks using Microsoft Sentinel and KQL

## Status
- Entra ID identity structure — 5 users, 3 groups
- Conditional Access — MFA enforced, tested
- RBAC — Contributor/Reader roles assigned, tested
- Azure Arc — local VM onboarded as Arc-enabled server
- Sentinel — enabled, Entra ID + Syslog data connectors live

## Structure
- 'identity/` — Entra ID, RBAC, and Conditional Access configuration
- 'sentinel/' — KQL detection rules
- 'vm/' - Virtual Machine configuration
- 'screenshots/' — supporting screenshots
