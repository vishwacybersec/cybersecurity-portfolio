# Windows Event Log Investigation

## Project Overview

This project demonstrates the investigation of Windows Security Event Logs using Event Viewer and Sysmon. The investigation focuses on analyzing authentication events, account management activities, and process creation logs to identify normal and suspicious system behavior. The project simulates tasks commonly performed by a Security Operations Center (SOC) Analyst during security monitoring and incident response.

---

## Objectives

- Understand Windows Security Event Logs.
- Investigate common Windows Event IDs.
- Analyze successful and failed logon events.
- Monitor user account creation, deletion, and account lockout events.
- Investigate process creation using Sysmon.
- Develop practical Windows log analysis skills required for an entry-level SOC Analyst.

---

## Lab Environment

| Component | Details |
|----------|---------|
| Operating System | Windows 10 |
| Log Source | Windows Security Logs |
| Additional Tool | Sysmon |
| Investigation Tool | Event Viewer |

---

## Tools Used

- Windows Event Viewer
- Sysmon
- Windows Security Logs

---

## Event IDs Investigated

| Event ID | Description |
|----------|-------------|
| 4624 | Successful Logon |
| 4625 | Failed Logon |
| 4720 | User Account Created |
| 4726 | User Account Deleted |
| 4740 | User Account Locked |
| Sysmon Event ID 1 | Process Creation |

---

## Investigation Process

1. Opened Windows Event Viewer.
2. Navigated to **Windows Logs → Security**.
3. Filtered logs using specific Event IDs.
4. Examined event details such as:
   - Time Created
   - Account Name
   - Logon Type
   - Computer Name
   - Process Name
5. Investigated Sysmon Process Creation events.
6. Documented findings and security observations.

---

## Key Findings

- Successfully identified successful user logon events.
- Investigated failed authentication attempts.
- Verified user account creation and deletion events.
- Examined account lockout activities.
- Monitored process creation using Sysmon.
- Understood how Windows logs assist SOC analysts during incident investigations.

---

## Skills Demonstrated

- Windows Event Log Analysis
- Event Viewer Investigation
- Windows Authentication Analysis
- Account Management Monitoring
- Sysmon Log Analysis
- Security Monitoring
- Incident Investigation
- SOC Documentation

---

## Screenshots

The **Screenshots** folder contains images demonstrating:

- Windows Event Viewer
- Event ID 4624 Investigation
- Event ID 4625 Investigation
- Event ID 4720 Investigation
- Event ID 4726 Investigation
- Event ID 4740 Investigation
- Sysmon Event ID 1 Investigation

---

## What I Learned

Through this project, I gained practical experience investigating Windows Security Event Logs and understanding how authentication events, account management activities, and process creation logs are used during security monitoring. This hands-on exercise strengthened my log analysis skills and improved my ability to identify potential security incidents from Windows event data.

---

## Conclusion

Windows Event Logs are one of the primary data sources used by SOC analysts to detect suspicious activity and investigate security incidents. This project provided practical experience with Windows Security Logs and Sysmon, improving my ability to analyze authentication events, monitor user activity, and document findings in a professional incident investigation workflow.
