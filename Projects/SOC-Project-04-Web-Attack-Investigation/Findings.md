# Investigation Findings

## Investigation Objective

Analyze Apache access logs to identify suspicious web activity and investigate common web attacks.

---

# Investigation Scope

The investigation focused on identifying:

- Normal Web Requests
- Web Reconnaissance
- SQL Injection (SQLi)
- Cross-Site Scripting (XSS)

---

# Summary of Findings

## Normal Activity

Normal browsing activity was observed, including requests for application pages and standard web resources.

---

## Web Reconnaissance

Multiple requests targeted administrative pages and web application components, indicating reconnaissance activity.

---

## SQL Injection

Several requests contained SQL Injection payloads attempting authentication bypass and database-related attacks.

---

## Cross-Site Scripting (XSS)

Requests containing JavaScript injection payloads were identified, indicating attempted XSS attacks.

---

# Severity Assessment

**Severity:** High

**Reason:**

- Multiple attack techniques observed.
- Repeated malicious requests.
- Reconnaissance followed by exploitation attempts.
- No confirmed evidence of successful compromise based on the available logs.

---

# Recommendations

1. Deploy a Web Application Firewall (WAF).
2. Validate and sanitize all user input.
3. Restrict access to administrative interfaces.
4. Continuously monitor Apache logs using a SIEM.
5. Keep web applications updated and patched.

---

# Conclusion

The investigation identified Web Reconnaissance, SQL Injection, and Cross-Site Scripting (XSS) attempts within the Apache access logs. The available evidence did not confirm a successful compromise, but the observed attack patterns highlight the need for continuous monitoring and stronger web application security controls.
