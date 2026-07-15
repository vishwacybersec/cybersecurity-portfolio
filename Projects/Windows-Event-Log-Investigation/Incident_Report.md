# Incident Report

## Incident Summary

This investigation focused on analyzing Windows Security Event Logs and Sysmon logs using Windows Event Viewer. The objective was to identify authentication events, account management activities, and process creation events that are commonly monitored by Security Operations Center (SOC) analysts.

---

## Investigation Details

**Investigation Date:** *(Add your investigation date)*

**Operating System:** Windows 10

**Tools Used:**
- Windows Event Viewer
- Sysmon

**Log Sources:**
- Windows Security Logs
- Sysmon Operational Logs

---

## Events Investigated

| Event ID | Description | Status |
|----------|-------------|--------|
| 4624 | Successful Logon | Investigated |
| 4625 | Failed Logon | Investigated |
| 4720 | User Account Created | Investigated |
| 4726 | User Account Deleted | Investigated |
| 4740 | Account Locked | Investigated |
| Sysmon Event ID 1 | Process Creation | Investigated |

---

## Investigation Steps

1. Opened Windows Event Viewer.
2. Navigated to **Windows Logs → Security**.
3. Filtered logs using the required Event IDs.
4. Reviewed authentication events.
5. Investigated account creation, deletion, and lockout activities.
6. Opened Sysmon Operational logs.
7. Reviewed Process Creation (Event ID 1).
8. Documented observations and findings.

---

## Findings

### Successful Logon (4624)
- Verified successful user authentication events.
- Confirmed account names, logon types, and timestamps.

### Failed Logon (4625)
- Reviewed failed authentication attempts.
- Identified possible incorrect password attempts.

### User Account Created (4720)
- Verified account creation events.
- Identified the account responsible for creating new users.

### User Account Deleted (4726)
- Reviewed account deletion activities.
- Confirmed authorized account management actions.

### Account Locked (4740)
- Observed account lockout events.
- Reviewed possible repeated failed login attempts.

### Sysmon Event ID 1
- Investigated process creation events.
- Reviewed parent and child process relationships.
- Verified command-line execution details.

---

## Security Assessment

No malicious activity was identified during this investigation. The analyzed events represented normal Windows authentication, account management, and process execution activities. However, these event IDs are critical for detecting unauthorized access, brute-force attacks, privilege misuse, and suspicious process execution in real-world environments.

---

## Skills Demonstrated

- Windows Event Log Analysis
- Authentication Monitoring
- Windows Security Investigation
- Account Management Analysis
- Sysmon Log Analysis
- Process Creation Investigation
- Incident Documentation
- SOC Investigation Workflow

---

## Recommendations

- Continuously monitor Windows Security Event Logs.
- Enable Sysmon for enhanced endpoint visibility.
- Investigate repeated failed login attempts promptly.
- Review account management events regularly.
- Correlate Windows logs with SIEM alerts for faster incident detection.

---

## Conclusion

This project provided hands-on experience investigating Windows Security Event Logs and Sysmon telemetry. Understanding these events is essential for SOC Analysts to detect suspicious activity, investigate incidents, and strengthen endpoint security monitoring.
