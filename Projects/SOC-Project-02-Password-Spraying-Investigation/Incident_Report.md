# Incident Report

## Incident Summary

A simulated Password Spraying attack was identified using Windows Security Event Logs analyzed in Splunk Enterprise.

Multiple failed authentication attempts originated from the same source IP against different user accounts. This behavior was identified as Password Spraying.

Following the failed logon attempts, a successful authentication was observed. The attacker then executed PowerShell, received administrative privileges, created a new user account (svc_update), and added the account to the Domain Admins group.

---

## Incident Details

**Attack Type**

Password Spraying

**Status**

Investigated

**Severity**

High

**SIEM**

Splunk Enterprise

**Log Source**

Windows Security Logs

---

## Investigation Steps

1. Identified repeated failed logon events (4625).
2. Correlated failed logons from the same source IP.
3. Observed successful authentication (4624).
4. Investigated PowerShell execution (4688).
5. Reviewed Special Privileges Assigned (4672).
6. Investigated User Account Creation (4720).
7. Investigated Domain Admin Group Modification (4728).
8. Reconstructed the attack timeline.
9. Mapped attacker techniques to MITRE ATT&CK.

---

## Findings

- Multiple user accounts were targeted.
- Password Spraying behavior identified.
- Successful authentication achieved.
- PowerShell executed after authentication.
- Administrative privileges assigned.
- svc_update account created.
- svc_update added to Domain Admins.

---

## Conclusion

The investigation confirmed evidence of a Password Spraying attack followed by privilege escalation and persistence through creation of a privileged account.
