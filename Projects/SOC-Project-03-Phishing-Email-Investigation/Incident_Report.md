# Incident Report

## Incident ID
PH-2026-001

## Incident Type
Credential Phishing

## Severity
High

## Executive Summary

A phishing email impersonating Microsoft Security attempted to trick users into verifying their Microsoft 365 account through a fake login page.

## Investigation Findings

- Lookalike Microsoft domain detected.
- SPF authentication failed.
- DKIM signature missing.
- DMARC validation failed.
- Reply-To domain differed from sender domain.
- The email used urgency and fear tactics.
- The embedded URL was designed to impersonate a Microsoft login page.

## Recommended Actions

- Quarantine the email.
- Block the sender domain.
- Block the phishing URL.
- Notify affected users.
- Reset passwords if credentials were submitted.
- Monitor sign-in logs for suspicious activity.

## Final Verdict

The email is classified as a **High Severity Credential Phishing Attack**.
