# Incident Report – Network Traffic Analysis Using Wireshark

## Incident Information

| Field | Value |
|-------|-------|
| Project | Network Traffic Analysis Using Wireshark |
| Analyst | Vishwa Shankar |
| Investigation Type | Network Traffic Analysis |
| Tool Used | Wireshark |
| Operating System | Kali Linux |
| Investigation Status | Completed |
| Severity | Informational |
| Risk Level | Low |

---

# Executive Summary

A live network traffic capture was generated on a Kali Linux virtual machine using Wireshark. Normal web browsing activity was performed to create realistic network traffic for analysis. The captured packets were examined to understand network communications, identify protocols, analyze DNS queries, inspect TCP and TLS sessions, and review network endpoints and conversations.

No evidence of malicious activity or indicators of compromise (IOCs) were identified during the investigation.

---

# Investigation Scope

The investigation focused on:

- Packet Capture Overview
- Protocol Hierarchy Analysis
- DNS Analysis
- TCP Connection Analysis
- TLS Handshake Analysis
- Endpoint Analysis
- Network Conversation Analysis

---

# Investigation Findings

## Capture Overview

- Total Packets Captured: **18,971**
- Capture Duration: **394.690 Seconds**
- Capture Size: **21 MB**

The capture contained sufficient network traffic to perform protocol and communication analysis.

---

## Protocol Analysis

The following protocols were observed:

- Ethernet II
- IPv4
- TCP
- UDP
- DNS
- TLS 1.2
- TLS 1.3
- QUIC
- ARP

Modern encrypted web traffic (TLS and QUIC) represented the majority of the captured communication.

---

## DNS Analysis

Observed DNS queries included legitimate domains such as:

- example.org
- cloudflare-dns.com
- ipv4only.arpa
- content-signature-2.cdn.mozilla.net
- ads.mozilla.org

No suspicious or malicious domains were identified.

---

## TCP Analysis

The investigation confirmed successful TCP three-way handshakes between the client and multiple remote servers.

No abnormal TCP behavior such as excessive retransmissions or repeated connection failures was observed.

---

## TLS Analysis

Encrypted HTTPS communication was successfully established using TLS 1.2 and TLS 1.3.

The TLS handshake included:

- Client Hello
- Server Hello
- Certificate Exchange
- Key Exchange
- Change Cipher Spec
- Encrypted Application Data

The observed encrypted sessions appeared legitimate.

---

## Endpoint Analysis

The local system communicated with multiple public web servers during normal browsing activity.

The endpoint statistics reflected expected client-server communication patterns.

---

## Conversation Analysis

Network conversations showed successful communication between the local machine and multiple external web servers.

Traffic volume and communication behavior were consistent with standard web browsing.

---

# Indicators of Compromise (IOCs)

No indicators of compromise were identified during this investigation.

- Malicious Domains: None
- Malicious IP Addresses: None
- Suspicious DNS Requests: None
- Suspicious TLS Sessions: None
- Malicious File Downloads: None

---

# Conclusion

The captured network traffic represents normal user web browsing activity.

DNS requests, TCP connections, and TLS handshakes completed successfully, and no evidence of malicious behavior was identified.

This investigation demonstrates practical experience in network traffic analysis using Wireshark and reinforces fundamental SOC Analyst skills in packet inspection, protocol analysis, and incident documentation.
