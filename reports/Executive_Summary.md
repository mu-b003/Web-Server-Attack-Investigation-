# Executive Summary

## Overview

This investigation analyzed suspicious activity against an Apache web server hosted on an Ubuntu Server within an isolated virtual laboratory.

The objective was to identify attacker behavior, reconstruct the attack timeline, and determine whether any successful compromise occurred.

---

## Key Observations

- Reconnaissance activity was performed using Nmap.
- Directory brute-force enumeration was conducted using Gobuster.
- Manual verification was performed using Curl.
- An exposed backup file (backup.zip) was successfully downloaded.
- SQL Injection and XSS payloads were tested.
- No evidence of successful server compromise was identified.

---

## Impact

The exposed administrative resources and downloadable backup file increased the attack surface and demonstrated poor web server security practices.

---

## Conclusion

The investigation successfully reconstructed the attack sequence and identified the techniques used by the attacker. All activities were performed within a controlled laboratory for educational purposes.
