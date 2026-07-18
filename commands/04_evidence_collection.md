# Evidence Collection

The following commands were used to extract forensic evidence from the Apache access log.

---

## Create Evidence File

```bash
touch attacker_activity.log
```

---

## Extract Attacker Activity

```bash
grep "192.168.81.129" $LOG > attacker_activity.log
```

---

## Verify Evidence

```bash
cat attacker_activity.log
```

---

## Analyze the Evidence

```bash
awk '{print $4,$1,$6,$7,$9}' attacker_activity.log
```

---

## Evidence Collected

- Attacker IP Address
- Request Timeline
- HTTP Methods
- Requested URLs
- HTTP Status Codes
- User-Agent Values
- SQL Injection Attempts
- XSS Attempts
- Directory Enumeration Activity
- Backup File Access

---

## Investigation Outcome

The investigation confirmed that the attacker performed:

- Reconnaissance using Nmap
- Directory brute-force using Gobuster
- Manual verification using Curl
- SQL Injection testing
- XSS testing
- Backup file download

The extracted evidence was preserved in a separate log file for further forensic analysis.
