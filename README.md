# Web Server Attack Investigation

## Overview

This project demonstrates a complete Web Server Attack Investigation performed inside an isolated virtual lab. The objective was to simulate common web attacks against an Apache web server and investigate the generated logs as a Security Operations Center (SOC) analyst.

---

# Objectives

- Deploy an Apache web server
- Build a vulnerable test website
- Simulate reconnaissance attacks
- Perform directory enumeration
- Generate web server logs
- Analyze Apache access logs
- Identify Indicators of Compromise (IOCs)
- Produce an incident investigation report

---

# Lab Environment

| Machine | Operating System |
|---------|------------------|
| Victim | Ubuntu Server |
| Attacker | Kali Linux |

### Services

- Apache2
- SSH

### Network

- Victim IP: 192.168.81.130
- Attacker IP: 192.168.81.129

---

# Tools Used

- Apache2
- Kali Linux
- Nmap
- Gobuster
- Curl
- grep
- awk
- sort
- uniq
- wc

---

# Attack Scenario

The following activities were simulated:

- Apache deployment
- Fake website creation
- Nmap reconnaissance
- Gobuster directory brute force
- Manual page discovery
- Backup file download
- SQL Injection attempt
- XSS attempt

---

# Investigation

The Apache access log was analyzed to identify:

- Attacker IP
- User-Agent
- Request timeline
- HTTP Status Codes
- Sensitive files accessed
- Directory brute force
- SQL Injection attempts
- XSS attempts

---

# Findings

- 4635 requests originated from the attacker
- 4618 HTTP 404 responses
- Successful access to backup.zip
- Successful discovery of admin.php
- SQL Injection attempt detected
- XSS attempt detected
- Massive Gobuster enumeration activity

---

# Skills Demonstrated

- Web Server Investigation
- Apache Log Analysis
- Incident Response
- Threat Hunting
- IOC Extraction
- Linux Log Analysis
- Blue Team Investigation

---

# Repository Structure

```
docs/
commands/
evidence/
reports/
screenshots/
assets/
```

---

# Author

Mubarak Bashr

Cybersecurity Student | SOC Analyst (Learning)
