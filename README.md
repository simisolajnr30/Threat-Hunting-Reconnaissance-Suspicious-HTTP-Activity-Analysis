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

2 . Focused on HTTP traffic

- To analyze web traffic

```splunk
index=botsv2 sourcetype=stream:http
```

3 . Targeted a Specific Website

- Narrowed it down to a specific website

```splunk
index=botsv2 sourcetype=stream:http site="www.froth.ly"
```

4 . Analyze User Agent

- To identify unusual clients

```splunk
index=botsv2 sourcetype=stream:http site="www.froth.ly"
| stats count by http_user_agent
| sort +count
```
- I noticed a strange user agent named "Naenara Browser" which look unusual.

---

































