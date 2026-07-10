# DNS Log Analysis Using Splunk

## Project Overview

This project demonstrates how to analyze DNS logs using Splunk Enterprise. The objective is to identify normal and suspicious DNS activity by using Splunk Search Processing Language (SPL).

## Project Objectives

- Import DNS logs into Splunk
- Perform DNS log analysis
- Investigate failed DNS requests
- Identify suspicious domains
- Practice SPL queries
- Improve SOC Analyst investigation skills
  
## Tools Used

- Splunk Enterprise 10.4
- Windows 10
- Sample DNS Log Dataset (CSV)
- GitHub

## Dataset

The dataset contains sample DNS events used for learning Splunk SIEM.

Fields included:

- timestamp
- src_ip
- dest_ip
- protocol
- port
- query
- query_type
- response_code
- resolved_ip
- note

## Skills Demonstrated

- Log Ingestion into Splunk
- DNS Log Analysis
- SPL Query Writing
- Source IP Investigation
- DNS Response Code Analysis
- Suspicious Domain Investigation
- Basic Incident Investigation

## SPL Queries Used

### Display All Events

```spl
source="Beginner_DNS_Logs.csv"
```

### Display Selected Fields

```spl
source="Beginner_DNS_Logs.csv"
| table timestamp src_ip dest_ip protocol port query query_type response_code resolved_ip note
```

### Count Total Events

```spl
source="Beginner_DNS_Logs.csv"
| stats count
```

### Count by Source IP

```spl
source="Beginner_DNS_Logs.csv"
| stats count by src_ip
| sort -count
```

### Find Failed DNS Requests

```spl
source="Beginner_DNS_Logs.csv"
| search response_code="NXDOMAIN"
```

### Find Top Queried Domains

```spl
source="Beginner_DNS_Logs.csv"
| top query
```

### Find Rare Domains

```spl
source="Beginner_DNS_Logs.csv"
| rare query
```

### Remove Duplicate Queries

```spl
source="Beginner_DNS_Logs.csv"
| dedup query
```

## Investigation Findings

### Total DNS Events

- 12 DNS events analyzed

### DNS Response Summary

- NOERROR: 8
- NXDOMAIN: 4

### Source IP Analysis

The following source IPs generated multiple DNS requests:

- 192.168.1.10 (2 Requests)
- 192.168.1.30 (2 Requests)

### Suspicious Observations

- Repeated DNS requests to **abcxyz123fake.com**
- DNS lookup failed with **NXDOMAIN**
- Suspicious-looking domain:
  - xn--security-check-update123.com
- Possible malware domain:
  - random-malware-domain.biz

### Analyst Observation

Repeated failed DNS requests may indicate user error, application retry behavior, or potentially suspicious activity. Additional investigation is required before concluding the activity is malicious.

## Incident Report

### Incident Type

DNS Investigation

### Summary

A DNS log analysis was performed using Splunk Enterprise.

### Findings

- 12 DNS events analyzed
- 8 successful DNS lookups
- 4 failed DNS lookups (NXDOMAIN)

Repeated requests were identified for **abcxyz123fake.com**.

The domain **random-malware-domain.biz** appeared suspicious and should be investigated further.

### Recommendation

Review endpoint activity, verify the requested domains using threat intelligence, and correlate findings with other security logs before determining whether the activity is malicious.

## Conclusion

This project demonstrates practical DNS log analysis using Splunk SIEM.

Skills demonstrated include:

- DNS log investigation
- SPL query writing
- Source IP analysis
- DNS response analysis
- Suspicious domain identification
- Basic SOC incident investigation

This project was completed as part of my SOC Analyst learning journey.
