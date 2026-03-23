# Threat-Hunting-Reconnaissance-Suspicious-HTTP-Activity-Analysis

In this project, i performed threat hunting using splunk to analyze HTTP traffic within the botsv2 dataset. The objective was identify to suspicious behaviour, investigate anomalies, and determine whether malicious activity occurred.

---

## **Tools Used**
- Splunk
- OSINT (Google, AbuseIPDB, IPinfo)
- HTTP Log Analysis

  ---

  ## **What I Did**

  1 . Identified Available Data
     
- I started by checking available log in splunk using METADATA

```splunk
| metadata type=sourcetypes index=botsv2
```
