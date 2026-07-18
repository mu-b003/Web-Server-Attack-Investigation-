# Findings

## Summary

The investigation confirmed malicious activity originating from a single attacker.

---

## Key Findings

- Attacker IP: 192.168.81.129
- Apache server successfully fingerprinted
- Hidden resources discovered
- backup.zip downloaded
- admin.php discovered
- SQL Injection attempt detected
- XSS attempt detected
- Large-scale Gobuster enumeration
- More than 4600 HTTP 404 responses

---

## Evidence

- Apache Access Log
- Apache Error Log
- Extracted attacker activity

---

## Conclusion

The attack consisted of reconnaissance, directory enumeration, manual verification of discovered pages, and basic web exploitation attempts.
