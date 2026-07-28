# MITRE ATT&CK Mapping

## Project

Web Attack Investigation using Apache Access Logs

---

## Purpose

This document maps the observed attack techniques from the investigation to the MITRE ATT&CK framework.

---

| Attack Observed | MITRE ATT&CK Tactic | Description |
|-----------------|---------------------|-------------|
| Web Reconnaissance | Reconnaissance | The attacker attempted to discover exposed administrative pages and application resources. |
| SQL Injection Attempt | Initial Access | The attacker attempted to exploit a public-facing web application using SQL Injection payloads. |
| Cross-Site Scripting (XSS) Attempt | Initial Access | The attacker attempted to exploit the application by injecting malicious JavaScript into user-supplied input. |

---

## Notes

- The Apache access logs showed evidence of attack attempts.
- No evidence confirmed successful exploitation.
- The mapping is based on observed attacker behavior within the available log data.

---

## References

- MITRE ATT&CK Framework
- Apache HTTP Access Logs
