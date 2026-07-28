# Investigation Findings

## Investigation Objective

Analyze Apache access logs to identify suspicious web activity and investigate common web attacks.

---

# Investigation Scope

- Normal Web Requests
- Web Reconnaissance
- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)

---

# Evidence 1 – Normal Web Requests

### Observation

Normal requests were identified for the home page, images, CSS, and other application resources.

### Sample Evidence

```http
GET / HTTP/1.1                         200
GET /images/joomla_black.gif HTTP/1.1  200
POST /index.php HTTP/1.1               200
```

### Analysis

These requests indicate legitimate user activity. The HTTP 200 status code shows that the requested resources were successfully served by the web server.

---

# Evidence 2 – Web Reconnaissance

### Observation

The attacker attempted to access administrative resources.

### Sample Evidence

```http
POST /administrator/index.php HTTP/1.1 303
POST /administrator/index.php HTTP/1.1 500
```

### Analysis

Repeated requests to administrative pages indicate reconnaissance activity. Attackers commonly probe these locations to identify exposed administration interfaces.

---

# Evidence 3 – SQL Injection

### Observation

The logs contain SQL Injection payloads.

### Sample Evidence

```http
GET ... OR ...
GET ... waitfor delay '0:0:6'
```

### Analysis

The requests contain classic SQL Injection techniques such as logical conditions and time-based payloads used to test database behavior.

---

# Evidence 4 – Cross-Site Scripting (XSS)

### Observation

JavaScript payloads were identified in URL parameters.

### Sample Evidence

```http
<script>
ScRiPt
onload=
```

### Analysis

These payloads indicate attempts to execute malicious JavaScript within the web application, consistent with Cross-Site Scripting (XSS) attacks.

---

# Summary of Findings

| Attack Type | Status |
|-------------|--------|
| Normal Requests | Observed |
| Web Reconnaissance | Detected |
| SQL Injection | Detected |
| Cross-Site Scripting (XSS) | Detected |

---

# Severity

**High**

### Reason

- Multiple web attack techniques observed.
- Reconnaissance followed by exploitation attempts.
- No confirmed successful compromise based on the available Apache access logs.

---

# Recommendations

1. Deploy a Web Application Firewall (WAF).
2. Validate and sanitize user input.
3. Restrict access to administrative interfaces.
4. Monitor Apache logs using a SIEM.
5. Keep the web application updated.

---

# Conclusion

The investigation identified multiple web attack attempts, including Web Reconnaissance, SQL Injection, and Cross-Site Scripting (XSS). While no successful compromise was confirmed, the attack patterns demonstrate active probing of the web application and highlight the need for continuous monitoring and stronger security controls.
