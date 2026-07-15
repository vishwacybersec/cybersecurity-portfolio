# Investigation Queries

## Overview

This document contains the Windows Event IDs investigated during this project. Each event includes its purpose, where it can be found, important fields to examine, and the observations made during the investigation.

---

# Event ID 4624 – Successful Logon

## Purpose
Records a successful user logon to the Windows system.

## Location
Windows Logs → Security

## Important Fields
- Account Name
- Security ID
- Logon Type
- Source Network Address
- Logon Process
- Authentication Package
- Time Created

## Investigation
Verified successful user authentication and reviewed the logon details to determine who logged in, when the login occurred, and the logon method used.

---

# Event ID 4625 – Failed Logon

## Purpose
Records failed user authentication attempts.

## Location
Windows Logs → Security

## Important Fields
- Account Name
- Failure Reason
- Status Code
- Sub Status
- Source IP Address
- Logon Type
- Time Created

## Investigation
Reviewed failed authentication attempts to identify incorrect passwords, unknown usernames, or suspicious login activity.

---

# Event ID 4720 – User Account Created

## Purpose
Indicates that a new user account was created.

## Location
Windows Logs → Security

## Important Fields
- Target Account Name
- Subject Account
- Security ID
- Time Created

## Investigation
Verified when a new account was created and identified which administrator or user performed the action.

---

# Event ID 4726 – User Account Deleted

## Purpose
Indicates that a user account was deleted.

## Location
Windows Logs → Security

## Important Fields
- Target Account Name
- Subject Account
- Security ID
- Time Created

## Investigation
Reviewed account deletion events to ensure user accounts were removed by authorized administrators.

---

# Event ID 4740 – User Account Locked

## Purpose
Indicates that a user account was locked because of multiple failed login attempts.

## Location
Windows Logs → Security

## Important Fields
- Account Name
- Caller Computer Name
- Security ID
- Time Created

## Investigation
Analyzed account lockout events to identify possible brute-force attacks or repeated incorrect password attempts.

---

# Sysmon Event ID 1 – Process Creation

## Purpose
Records every new process created on the system.

## Location
Applications and Services Logs → Microsoft → Windows → Sysmon → Operational

## Important Fields
- Process Name
- Parent Process
- Command Line
- User
- Process ID
- Hashes
- Time Created

## Investigation
Reviewed newly created processes and their parent-child relationships to identify suspicious executions or potentially malicious activity.

---

## Summary

The investigation covered Windows authentication events, account management activities, account lockouts, and process creation logs. These event IDs are commonly monitored by SOC Analysts to detect unauthorized access attempts, account misuse, and suspicious process execution.
