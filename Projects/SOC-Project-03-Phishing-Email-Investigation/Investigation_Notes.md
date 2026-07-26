# Investigation Notes

## Incident Overview

A user reported a suspicious email claiming to be from Microsoft Security. The email warned about an unusual sign-in attempt and instructed the recipient to verify their account through a provided link.

---

## Email Analysis

**Sender**
- security-noreply@microsoftonline-security.com

**Subject**
- Unusual Sign-in Activity Detected

### Observed Phishing Indicators

- Lookalike Microsoft domain
- Generic greeting ("Dear User")
- Urgent language ("Verify immediately")
- Time pressure ("within 12 hours")
- Suspicious login URL
- Different Reply-To address
- SPF = Fail
- DKIM = None
- DMARC = Fail

---

## Social Engineering Techniques

- Urgency
- Fear
- Authority (Impersonating Microsoft Security)

---

## Initial Assessment

The email is highly suspicious and appears to be a credential phishing attempt.
