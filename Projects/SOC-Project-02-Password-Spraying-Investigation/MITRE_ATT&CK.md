# MITRE ATT&CK Mapping

## Overview

This document maps the observed attacker behavior during the Password Spraying investigation to the MITRE ATT&CK Framework.

---

# MITRE ATT&CK Techniques

| Tactic | Technique | Technique ID | Evidence |
|---------|-----------|--------------|----------|
| Credential Access | Password Spraying | T1110.003 | Multiple failed logons (4625) against different user accounts from the same IP address |
| Defense Evasion / Persistence | Valid Accounts | T1078 | Successful authentication using a valid account (4624) |
| Execution | PowerShell | T1059.001 | PowerShell (Event ID 4688) executed after successful authentication |
| Persistence | Create Account | T1136 | New account (svc_update) created (Event ID 4720) |
| Privilege Escalation / Persistence | Account Manipulation | T1098 | svc_update added to the Domain Admins group (Event ID 4728) |

---

# Attack Flow

1. Password Spraying attack attempted against multiple user accounts.
2. Successful authentication achieved using valid credentials.
3. PowerShell executed after successful login.
4. Administrative privileges assigned.
5. New account (svc_update) created.
6. Account added to Domain Admins for persistence and elevated privileges.

---

# Summary

The attacker used password spraying to gain initial access, executed PowerShell, escalated privileges, created a new account, and modified Domain Admin group membership. These actions align with several MITRE ATT&CK techniques commonly observed during Active Directory compromises.
