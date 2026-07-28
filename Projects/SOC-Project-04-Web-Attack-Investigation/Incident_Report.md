# Incident Report

## Incident Information

**Project:** Web Attack Investigation using Apache Access Logs

**Analyst:** Vishwa Shankar

**Severity:** High

**Status:** Closed (Attack attempts detected, no confirmed compromise)

---

# Executive Summary

An investigation was conducted on Apache access logs after suspicious HTTP requests were detected. The analysis identified multiple web attack attempts, including Web Reconnaissance, SQL Injection, and Cross-Site Scripting (XSS).

The investigation focused on identifying malicious requests, analyzing attack patterns, assessing the impact, and recommending mitigation strategies.

No evidence from the available Apache access logs confirmed successful exploitation.

---

# Investigation Scope

- Apache Access Log Analysis
- Normal Web Requests
- Web Reconnaissance
- SQL Injection
- Cross-Site Scripting (XSS)

---

# Investigation Findings

## Web Reconnaissance

Multiple requests targeted administrative pages and application resources, indicating reconnaissance activity.

---

## SQL Injection

SQL Injection payloads attempting authentication bypass and database enumeration were identified.

---

## Cross-Site Scripting (XSS)

Multiple requests contained JavaScript payloads attempting to inject malicious scripts into web application parameters.

---

# Impact Assessment

- Multiple web attack attempts observed.
- No confirmed evidence of successful compromise.
- Continued monitoring recommended.

---

# Recommendations

- Deploy a Web Application Firewall (WAF).
- Validate and sanitize user input.
- Restrict access to administrative interfaces.
- Monitor Apache access logs using a SIEM.
- Regularly update and patch web applications.

---

# Conclusion

The investigation successfully identified Web Reconnaissance, SQL Injection, and Cross-Site Scripting (XSS) attempts within the Apache access logs. While no successful compromise was confirmed, the observed activity indicates active probing of the web application. Appropriate security controls and continuous monitoring are recommended.
