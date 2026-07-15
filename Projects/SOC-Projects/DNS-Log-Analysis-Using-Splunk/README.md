# DNS Log Analysis Using Splunk

## Project Overview

This project demonstrates DNS log analysis using Splunk Enterprise. The objective was to investigate DNS traffic, identify failed DNS lookups (NXDOMAIN), analyze source IP activity, and detect suspicious domain queries.

## Objectives

- Import DNS log dataset into Splunk
- Analyze DNS events
- Identify failed DNS lookups
- Investigate suspicious domains
- Analyze source IP activity
- Understand DNS query types
- Practice Splunk SPL queries

## Environment

- SIEM: Splunk Enterprise 10.4.1
- Dataset: Beginner DNS Logs
- Index: dns_project

## Skills Demonstrated

- Splunk Search Processing Language (SPL)
- DNS Log Analysis
- Security Event Investigation
- Source IP Analysis
- Response Code Analysis
- Threat Hunting
- Basic SOC Investigation

## Investigation Summary

- Total Events: **12**
- Successful DNS Responses (NOERROR): **8**
- Failed DNS Responses (NXDOMAIN): **4**
- Most Queried Suspicious Domain: **abcxyz123fake.com**
- Suspicious Source IP: **192.168.1.30**

## Screenshots

### Dataset Imported

![Dataset](01_Dataset_Imported.png)

---

### Important Fields

![Fields](02_Important_Fields.png)

---

### Total Events

![Events](03_Total_Events.png)

---

### Source IP Analysis

![Source IP](04_Source_IP_Analysis.png)

---

### Response Code Analysis

![Response Code](05_Response_Code_Analysis.png)

---

### Failed DNS Requests

![NXDOMAIN](06_Failed_DNS_Requests.png)

---

### Top Queried Domains

![Top Query](07_Top_Queried_Domains.png)

---

### Repeated Domains

![Repeated](08_Repeated_Domains.png)

---

### Source IP Investigation

![Source Investigation](09_Source_IP_Investigation.png)

---

### Domain Investigation

![Domain Investigation](10_Domain_Investigation.png)

---

### Query Type Analysis

![Query Type](11_Query_Type_Analysis.png)

---

## Conclusion

This project demonstrates the use of Splunk Enterprise for DNS log investigation. The analysis identified normal DNS activity, failed DNS requests (NXDOMAIN), repeated domain queries, and suspicious domains that could indicate malicious activity. This project helped strengthen practical SOC Analyst skills using Splunk SPL.
