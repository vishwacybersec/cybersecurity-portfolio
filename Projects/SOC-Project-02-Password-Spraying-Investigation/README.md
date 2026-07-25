# SOC Project 02 – Password Spraying Attack Investigation Using Splunk

## Project Overview

This project demonstrates the investigation of a simulated Windows Active Directory Password Spraying attack using Splunk Enterprise.

The investigation focuses on identifying suspicious authentication attempts, analyzing Windows Security Event Logs, reconstructing the attack timeline, identifying Indicators of Compromise (IOCs), mapping attacker techniques to the MITRE ATT&CK framework, and documenting the incident from a SOC Analyst perspective.

This project showcases practical SOC Analyst skills including log analysis, SIEM investigation, incident response, Windows Event Log analysis, and threat detection.

---

# Objectives

- Detect suspicious authentication activity.
- Identify password spraying behavior.
- Analyze Windows Security Event Logs.
- Identify compromised accounts.
- Investigate PowerShell execution.
- Detect privilege escalation.
- Investigate account creation.
- Identify Domain Admin group modifications.
- Build an attack timeline.
- Map attacker techniques to MITRE ATT&CK.
- Document the investigation.

---

# Lab Environment

| Component | Details |
|-----------|---------|
| SIEM | Splunk Enterprise 10.4.1 |
| Operating System | Windows |
| Data Source | Windows Security Event Logs |
| Dataset | 01_soc-lab.csv |
| Investigation Type | Password Spraying |
| Log Source | Windows Security Logs |

---

# Attack Scenario

An attacker performed a Password Spraying attack against multiple Active Directory user accounts.

After obtaining valid credentials, the attacker authenticated successfully, executed PowerShell commands, obtained administrative privileges, created a new account named **svc_update**, and added that account to the **Domain Admins** group.

The objective of the investigation was to reconstruct the attack using Windows Security Event Logs in Splunk.

---

# Investigation Process

The investigation followed the following workflow:

1. Authentication Analysis
2. Failed Login Analysis
3. Successful Login Identification
4. Source IP Investigation
5. Target User Analysis
6. Timeline Reconstruction
7. PowerShell Execution Analysis
8. Privilege Escalation Investigation
9. Account Creation Investigation
10. Domain Admin Group Modification Investigation
11. IOC Identification
12. MITRE ATT&CK Mapping

---

# Windows Event IDs Investigated

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4672 | Special Privileges Assigned |
| 4688 | Process Creation |
| 4720 | User Account Created |
| 4728 | User Added to Security Group |

---

# Splunk Reports Created

The following reports were created during the investigation:

- Authentication Success vs Failure
- Event ID Distribution
- Top Source IP Addresses
- Targeted User Accounts
- Attack Timeline
- PowerShell Process Execution
- Privilege Escalation Events
- Account Creation and Domain Admin Changes

---

# Attack Timeline

1. Multiple failed authentication attempts were detected.

2. Multiple usernames were targeted from the same IP address.

3. Password Spraying activity was identified.

4. A successful authentication occurred.

5. PowerShell execution was observed.

6. Administrative privileges were assigned.

7. A new account (**svc_update**) was created.

8. The newly created account was added to the **Domain Admins** group.

---

# Indicators of Compromise (IOCs)

| IOC | Value |
|------|-------|
| Attack Type | Password Spraying |
| Suspicious Account | akumar |
| New Account | svc_update |
| PowerShell | powershell.exe |
| Privilege Escalation | Event ID 4672 |
| Account Creation | Event ID 4720 |
| Domain Admin Modification | Event ID 4728 |

---

# MITRE ATT&CK Mapping

| Technique | MITRE ID |
|------------|-----------|
| Password Spraying | T1110.003 |
| Valid Accounts | T1078 |
| PowerShell | T1059.001 |
| Create Account | T1136 |
| Account Manipulation | T1098 |

---

# Investigation Findings

The investigation identified evidence of a Password Spraying attack targeting multiple Active Directory accounts.

Following successful authentication, PowerShell activity was observed. Administrative privileges were assigned, after which a new user account (**svc_update**) was created and added to the Domain Admins group.

The sequence of events indicates a successful compromise followed by privilege escalation and persistence.

---

# Recommendations

- Enforce Multi-Factor Authentication (MFA).
- Implement strong password policies.
- Enable account lockout policies.
- Monitor repeated failed authentication attempts.
- Monitor PowerShell execution.
- Review privileged account usage.
- Audit Domain Admin group modifications.
- Regularly review Windows Security Logs.
- Configure SIEM alerts for authentication anomalies.
- Continuously monitor administrative account activity.

---

# Skills Demonstrated

- Windows Event Log Analysis
- Splunk Enterprise
- SPL Query Development
- Authentication Log Analysis
- Password Spraying Detection
- Windows Security Monitoring
- IOC Identification
- Incident Investigation
- Timeline Reconstruction
- Threat Hunting
- MITRE ATT&CK Mapping
- Incident Reporting
- SOC Investigation Methodology

---

# Screenshots

The `Screenshots` directory contains evidence collected during the investigation:

- Authentication Success vs Failure
- Event ID Distribution
- Top Source IP Addresses
- Targeted User Accounts
- Attack Timeline
- PowerShell Process Execution
- Privilege Escalation Events
- Account Creation and Domain Admin Changes

---

# Project Structure

```
SOC-Project-02-Password-Spraying-Investigation
│
├── README.md
├── Dataset
│   └── 01_soc-lab.csv
│
├── Reports
│
└── Screenshots
    ├── 01_Authentication_Success_vs_Failure.png
    ├── 02_Event_ID_Distribution.png
    ├── 03_Top_Source_IPs.png
    ├── 04_Targeted_User_Accounts.png
    ├── 05_Attack_Timeline.png
    ├── 06_PowerShell_Process_Execution.png
    ├── 07_Privilege_Escalation_Events.png
    └── 08_Account_Creation_Domain_Admin_Changes.png
```

---

# Conclusion

This project demonstrates a complete SOC investigation of a simulated Password Spraying attack using Splunk Enterprise and Windows Security Event Logs.

The investigation successfully reconstructed the attack timeline, identified attacker behavior, mapped techniques to the MITRE ATT&CK framework, and documented the findings using industry-standard SOC investigation methodology.

The project highlights practical skills required for an entry-level SOC Analyst, including SIEM investigation, log analysis, incident response, IOC identification, and threat detection.
