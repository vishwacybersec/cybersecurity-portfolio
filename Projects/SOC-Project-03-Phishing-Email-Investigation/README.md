# SOC Project 03 – Phishing Email Investigation

## Objective

Investigate a suspicious Microsoft-themed phishing email by analyzing its content, headers, authentication results, and embedded URL to determine whether it represents a credential phishing attack.

---

## Scenario

An employee reported receiving an email claiming there was an unusual sign-in attempt on their Microsoft 365 account. The email instructed the user to verify their identity through a provided login link.

The objective of this investigation was to determine whether the email was legitimate or a phishing attempt.

---

## Investigation Workflow

1. Email Content Analysis
2. Email Header Analysis
3. SPF Verification
4. DKIM Verification
5. DMARC Verification
6. Return-Path Analysis
7. Reply-To Analysis
8. URL Analysis
9. IOC Extraction
10. Incident Classification
11. Remediation Recommendations

---

## Tools Used

- VS Code
- VirusTotal (conceptually)
- URLScan (conceptually)
- WHOIS Lookup
- GitHub

---

## Key Findings

- Lookalike Microsoft domain
- Generic greeting
- Urgent language
- Fear-based social engineering
- Suspicious login URL
- SPF = Fail
- DKIM = None
- DMARC = Fail
- Different Reply-To address

---

## Indicators of Compromise (IOCs)

- Sender Email
- Reply-To Address
- Sender Domain
- URL
- URL Domain
- Message-ID
- Received IP Address
- X-Mailer

---

## Final Verdict

The email was classified as a **High Severity Credential Phishing Attack**.

The attack attempted to steal Microsoft 365 credentials using social engineering techniques and a fake Microsoft login page.

---

## Skills Demonstrated

- Phishing Email Investigation
- Email Header Analysis
- SPF / DKIM / DMARC Analysis
- IOC Extraction
- Social Engineering Detection
- Threat Analysis
- Incident Documentation

- ## Disclaimer

This project uses a synthetic phishing email created for cybersecurity education and SOC analyst training. It does not contain real user data or active malicious infrastructure.
