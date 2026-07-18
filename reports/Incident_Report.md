# Incident Report

## Incident Information

**Incident Name:** Web Server Attack Investigation

**Incident Type:** Simulated Web Application Attack

**Environment:** Isolated Virtual Lab

**Victim:** Ubuntu Server (Apache2)

**Attacker:** Kali Linux

---

# Attack Summary

The attacker began with reconnaissance using Nmap to identify exposed services. The web server was then fingerprinted using Curl, followed by directory enumeration with Gobuster.

Several hidden pages were successfully discovered, including:

- admin.php
- login.php
- upload.php
- backup.zip

The attacker downloaded the exposed backup file and later attempted SQL Injection and Cross-Site Scripting (XSS) attacks.

---

# Evidence Collected

- Apache Access Log
- Apache Error Log
- Attacker Activity Log

---

# Indicators of Compromise

Attacker IP

```
192.168.81.129
```

User Agents

- Gobuster/3.8.2
- curl/8.20.0
- Nmap Scripting Engine

---

# Findings

- More than 4600 requests originated from the attacker.
- Most requests resulted in HTTP 404 responses.
- Hidden administrative pages were discovered.
- An exposed backup file was downloaded successfully.
- SQL Injection testing was observed.
- XSS testing was observed.

---

# Conclusion

The incident represented a realistic web reconnaissance and enumeration scenario followed by basic exploitation attempts. No evidence indicated successful remote code execution or privilege escalation.
