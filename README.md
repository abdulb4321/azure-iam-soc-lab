# azure-iam-soc-lab
Hybrid cloud security lab: Identity and Access Management (IAM) and Microsoft Sentinel detection engineering using Microsoft Azure

## Project goals
- Configure Entra ID identity controls (RBAC, Conditional Access, MFA, PIM)
- Detect simulated attacks using Microsoft Sentinel and KQL

## Status

**Identity and Access Management**
- Entra ID identity structure - 5 users, 3 groups (IT-Admins, HR, Finance)
- Conditional Access - MFA enforced, tested via non-admin sign in
- RBAC - Contributor/Reader roles assigned, tested
- PIM - IT-Admins' Contributor access converted to eligible/just-in-time
- Access Reviews - quarterly recurring review for IT-Admins

**Hybrid Infrastructure and Detection**
- Azure Arc - local VirtualBox VM onboarded as Arc-enabled server
- Microsoft Sentinel - enabled, with Entra ID (sign-in/audit logs) and Syslog data connectors live
- Attack simulation - SSH brute-force tested against local VM (real and fake usernames)
- KQL detection rule - custom scheduled analytics rules detecting brute-force SSH login attempts and failed Entra ID sign-ins
- Incident investigation - simulated attack triggered a Sentinel incident, investigated and classified as benign positive (security testing)

## Structure
- `identity/` - Entra ID, Conditional Access, RBAC, PIM and Access Reviews configuration
- `sentinel/` - Data Connectors, KQL detection rules, incident investigation
- `vm/` - Virtual Machine configuration with Azure Arc onboarded and Azure Monitor Agent installed
- `screenshots/` - supporting screenshots
