# Indicators of Compromise (IOC) Report

## Incident Overview

This document lists the Indicators of Compromise (IOCs) identified during the Password Spraying investigation.

---

# Attack Type

Password Spraying

---

# Indicators of Compromise

| IOC Type | Value | Description |
|----------|-------|-------------|
| Attack Technique | Password Spraying | Multiple failed logins against different accounts |
| Source IP | 192.168.1.150 | Primary suspicious IP observed during failed logons |
| Event ID | 4625 | Failed Logon |
| Event ID | 4624 | Successful Logon |
| Event ID | 4688 | Process Creation |
| Event ID | 4672 | Special Privileges Assigned |
| Event ID | 4720 | User Account Created |
| Event ID | 4728 | User Added to Domain Admins |
| Suspicious User | akumar | Account involved in administrative activity |
| Created Account | svc_update | Newly created account |
| Process | powershell.exe | Executed after successful authentication |
| Target Group | Domain Admins | Group modified during the attack |

---

# IOC Analysis

The investigation identified multiple failed authentication attempts originating from the same source IP address against different user accounts. This behavior is consistent with a Password Spraying attack.

Following successful authentication, PowerShell execution, privilege assignment, creation of the **svc_update** account, and addition of that account to the **Domain Admins** group indicate successful compromise and privilege escalation.

---

# Recommendation

Immediately investigate authentication activity from suspicious source IPs, monitor privileged account changes, review PowerShell execution, and enable SIEM alerts for abnormal authentication patterns.
