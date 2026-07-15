# Windows Event Log Investigation

## Project Overview

This project demonstrates a practical investigation of Windows Security Event Logs and Sysmon logs using Windows Event Viewer. The investigation focuses on analyzing authentication events, account management activities, and process lifecycle events to understand how Windows records security-related activity.

During this project, multiple Windows Security Event IDs were generated manually and investigated using Event Viewer. Additionally, Sysmon was used to monitor process creation and termination events, providing enhanced endpoint visibility commonly used in Security Operations Centers (SOCs).

---

# Objectives

- Learn Windows Event Viewer navigation.
- Investigate Windows Security Event Logs.
- Analyze successful and failed logon events.
- Monitor user account creation and deletion.
- Investigate Sysmon Process Creation and Process Termination events.
- Develop practical Windows log analysis skills for a SOC Analyst role.

---

# Lab Environment

| Component | Details |
|-----------|---------|
| Operating System | Windows 10 |
| Log Source | Windows Security Logs |
| Additional Tool | Sysmon |
| Investigation Tool | Event Viewer |

---

# Tools Used

- Windows Event Viewer
- Windows Security Logs
- Sysmon

---

# Event IDs Investigated

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4720 | User Account Created |
| 4726 | User Account Deleted |
| Sysmon Event ID 1 | Process Creation |
| Sysmon Event ID 5 | Process Termination |

---

# Investigation Process

1. Opened Windows Event Viewer.
2. Navigated to Windows Security Logs.
3. Filtered logs using specific Event IDs.
4. Generated authentication events through normal and failed logins.
5. Created and deleted a local Windows user account.
6. Installed and used Sysmon.
7. Generated Process Creation events.
8. Generated Process Termination events.
9. Reviewed event details.
10. Documented findings.

---

# Key Findings

- Successfully investigated Windows authentication events.
- Identified successful user logons.
- Investigated failed authentication attempts.
- Verified local user account creation.
- Verified local user account deletion.
- Investigated Sysmon Process Creation logs.
- Investigated Sysmon Process Termination logs.
- Improved understanding of Windows endpoint monitoring.

---

# Skills Demonstrated

- Windows Event Log Analysis
- Event Viewer Investigation
- Windows Authentication Analysis
- User Account Monitoring
- Sysmon Investigation
- Process Monitoring
- Security Documentation
- Incident Investigation
- SOC Analyst Workflow

---

# Screenshots

## 1. Event Viewer Home

The Event Viewer interface used during the investigation.

![Event Viewer](Screenshots/01-Event-Viewer.png)

---

## 2. Windows Security Logs

Security logs containing authentication and account management events.

![Security Logs](Screenshots/02-Security-Logs.png)

---

## 3. Event ID 4624 – Successful Logon

Verified successful authentication and analyzed logon information.

![Event ID 4624](Screenshots/03-EventID-4624.png)

---

## 4. Event ID 4625 – Failed Logon

Investigated failed authentication attempts and reviewed the failure reason.

![Event ID 4625](Screenshots/04-EventID-4625.png)

---

## 5. Event ID 4720 – User Account Created

Generated and investigated a local user account creation event.

![Event ID 4720](Screenshots/05-EventID-4720.png)

---

## 6. Event ID 4726 – User Account Deleted

Generated and investigated a local user account deletion event.

![Event ID 4726](Screenshots/06-EventID-4726.png)

---

## 7. Sysmon Event ID 1 – Process Creation

Investigated Sysmon Process Creation events to analyze executable name, command line, process ID, and execution time.

![Sysmon Event ID 1](Screenshots/07-Sysmon-EventID-1.png)

---

## 8. Sysmon Event ID 5 – Process Termination

Investigated Sysmon Process Termination events to analyze terminated processes and process lifecycle.

![Sysmon Event ID 5](Screenshots/08-Sysmon-EventID-5.png)

---

# What I Learned

This project provided hands-on experience investigating Windows Security Event Logs and Sysmon telemetry. I learned how Windows records authentication events, account management activities, and process execution information. I also gained practical experience using Event Viewer to investigate Windows events and document findings similar to those performed by entry-level SOC Analysts.

---

# Conclusion

Windows Event Logs are one of the primary data sources used by Security Operations Centers (SOCs) to detect suspicious activity and investigate security incidents. Through this project, I developed practical experience generating, investigating, and documenting Windows Security Events and Sysmon logs. These skills are directly applicable to entry-level SOC Analyst responsibilities such as security monitoring, log analysis, and incident investigation.

---

# Project Files

```
SOC-Project-02-Windows-Event-Log-Investigation/
│
├── README.md
├── Investigation_Queries.md
├── Incident_Report.md
└── Screenshots/
    ├── 01-Event-Viewer.png
    ├── 02-Security-Logs.png
    ├── 03-EventID-4624.png
    ├── 04-EventID-4625.png
    ├── 05-EventID-4720.png
    ├── 06-EventID-4726.png
    ├── 07-Sysmon-EventID-1.png
    └── 08-Sysmon-EventID-5.png
```
