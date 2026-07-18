# Attack Commands

The following commands were executed from the Kali Linux attacker machine.

---

## Nmap Service Scan

```bash
nmap -sV 192.168.81.130
```

Purpose:

Identify open ports and services.

---

## HTTP Header Fingerprinting

```bash
curl -I http://192.168.81.130
```

Purpose:

Collect HTTP response headers.

---

## Directory Enumeration

```bash
gobuster dir \
-u http://192.168.81.130 \
-w /usr/share/wordlists/dirb/common.txt
```

Purpose:

Discover hidden files and directories.

---

## Manual Page Verification

```bash
curl http://192.168.81.130/admin.php
```

```bash
curl http://192.168.81.130/login.php
```

```bash
curl http://192.168.81.130/upload.php
```

```bash
curl http://192.168.81.130/backup.zip
```

Purpose:

Verify discovered resources.

---

## Sensitive Path Discovery

```bash
curl http://192.168.81.130/.env
```

```bash
curl http://192.168.81.130/phpmyadmin
```

```bash
curl http://192.168.81.130/config
```

```bash
curl http://192.168.81.130/test
```

```bash
curl http://192.168.81.130/admin
```

---

## SQL Injection Test

```bash
curl "http://192.168.81.130/login.php?id=1'"
```

```bash
curl "http://192.168.81.130/login.php?id=1%20OR%201=1"
```

Purpose:

Simulate SQL Injection testing.

---

## XSS Test

```bash
curl "http://192.168.81.130/<script>alert(1)</script>"
```

Purpose:

Generate XSS-related log entries.
