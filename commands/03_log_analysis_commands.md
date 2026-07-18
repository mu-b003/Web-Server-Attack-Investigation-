# Apache Log Analysis Commands

Location:

```bash
/var/log/apache2/access.log
```

---

## Set Log Variable

```bash
LOG=/var/log/apache2/access.log
```

---

## Count Requests per IP

```bash
awk '{print $1}' $LOG | sort | uniq -c | sort -nr
```

---

## View Timeline

```bash
awk '{print $4,$1,$6,$7,$9}' $LOG
```

---

## First Request

```bash
grep "192.168.81.129" $LOG | head -1
```

---

## Last Request

```bash
grep "192.168.81.129" $LOG | tail -1
```

---

## Count Requested URLs

```bash
awk '{print $7}' $LOG | sort | uniq -c | sort -nr
```

---

## HTTP Status Codes

```bash
awk '{print $9}' $LOG | sort | uniq -c
```

---

## Search Sensitive Files

```bash
grep -Ei 'admin|login|upload|backup|config|\.env|phpmyadmin' $LOG
```

---

## Search SQL Injection

```bash
grep -Ei "union|select|or 1=1|%27|'|information_schema" $LOG
```

---

## Search XSS

```bash
grep "<script>" $LOG
```

---

## Search Backup Files

```bash
grep -Ei 'backup|\.zip|\.tar|\.gz|\.bak' $LOG
```

---

## Count Unique URLs

```bash
awk '{print $7}' $LOG | sort | uniq | wc -l
```

---

## User-Agent Analysis

```bash
awk -F\" '{print $6}' $LOG | sort | uniq -c | sort -nr
```

---

## Gobuster Requests

```bash
grep -i gobuster $LOG
```

---

## Curl Requests

```bash
grep -i curl $LOG
```
