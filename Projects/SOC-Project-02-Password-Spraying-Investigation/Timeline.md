# Attack Timeline

## Overview

This timeline reconstructs the sequence of attacker activity observed during the Password Spraying investigation.

---

| Time | Event ID | Activity |
|------|----------|----------|
| Initial Phase | 4625 | Multiple failed logon attempts detected against different user accounts from the same source IP. |
| Authentication | 4624 | Successful authentication observed after repeated failed logons. |
| Post-Authentication | 4688 | PowerShell executed following successful authentication. |
| Privilege Assignment | 4672 | Special privileges assigned to the logged-on account. |
| Account Creation | 4720 | New account **svc_update** created by **akumar**. |
| Privilege Modification | 4728 | **svc_update** added to the **Domain Admins** group. |

---

## Attack Flow

Password Spraying

↓

Successful Authentication

↓

PowerShell Execution

↓

Privilege Escalation

↓

Account Creation

↓

Added to Domain Admins

---

## Summary

The sequence of Windows Security Events indicates a successful compromise that progressed from credential attacks to privilege escalation and persistence.
