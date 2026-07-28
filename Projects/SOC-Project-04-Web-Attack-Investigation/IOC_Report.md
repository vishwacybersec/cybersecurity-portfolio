# Indicators of Compromise (IOC) Report

## Project

Web Attack Investigation using Apache Access Logs

---

# Source IP Address

- 192.168.4.25

---

# Web Reconnaissance Indicators

- /administrator/index.php
- /index.php/component/search/
- Administrative application endpoints

---

# SQL Injection Indicators

- ' OR
- waitfor delay
- SQL keywords
- Encoded SQL payloads

---

# Cross-Site Scripting (XSS) Indicators

- <script>
- ScRiPt
- onload=
- Expression(
- JavaScript payloads

---

# HTTP Status Codes Observed

- 200 OK
- 301 Moved Permanently
- 302 Found
- 303 See Other
- 404 Not Found
- 500 Internal Server Error

---

# Analyst Notes

The Apache access logs contain multiple indicators associated with Web Reconnaissance, SQL Injection, and Cross-Site Scripting (XSS). These indicators can be used to develop detection rules and improve monitoring capabilities.
