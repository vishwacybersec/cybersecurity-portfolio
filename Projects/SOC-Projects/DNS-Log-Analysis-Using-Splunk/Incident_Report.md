# DNS Incident Investigation Report

## Incident Summary

A DNS log investigation was performed using Splunk Enterprise to analyze DNS traffic, identify suspicious activity, and investigate failed DNS requests.

---

# Investigation Details

**Date of Investigation:** July 2026

**Tool Used:** Splunk Enterprise 10.4.1

**Dataset:** Beginner DNS Logs

**Index:** dns_project

---

# Objectives

- Analyze DNS traffic
- Identify failed DNS lookups
- Investigate suspicious domains
- Examine source IP activity
- Detect repeated DNS queries

---

# Investigation Findings

## Total DNS Events

**12 Events**

---

## DNS Response Codes

| Response Code | Count |
|--------------|------:|
| NOERROR | 8 |
| NXDOMAIN | 4 |

---

## Suspicious Source IP

**192.168.1.30**

Reason:

- Generated multiple DNS requests.
- Requested the same suspicious domain multiple times.
- Returned NXDOMAIN responses.

---

## Suspicious Domain

**abcxyz123fake.com**

Observations:

- Queried multiple times.
- DNS resolution failed (NXDOMAIN).
- Repeated failed lookups may indicate suspicious or automated activity.

---

## Additional Domain Observed

**random-malware-domain.biz**

Observations:

- Appeared in the DNS logs.
- Marked in the dataset as a possible malware-related domain.
- Requires further investigation in a real SOC environment.

---

# Query Types Observed

- A
- AAAA
- MX
- PTR

---

# SPL Queries Used

- Display all events
- Display important fields
- Count total events
- Analyze source IP activity
- Analyze response codes
- Search NXDOMAIN events
- Find top queried domains
- Detect repeated domains
- Investigate suspicious IP
- Investigate suspicious domain
- Analyze query types

---

# Conclusion

The investigation identified multiple failed DNS lookups (NXDOMAIN), repeated queries to **abcxyz123fake.com**, and a suspicious source IP (**192.168.1.30**).

Although this dataset is intended for training, the investigation follows the same methodology used by SOC analysts to review DNS logs, identify anomalies, and investigate potentially malicious activity.

This project demonstrates practical experience with Splunk SPL, DNS log analysis, and basic threat hunting techniques.
