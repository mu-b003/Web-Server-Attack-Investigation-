# Lessons Learned

## Technical Lessons

- Apache access logs provide valuable forensic evidence.
- Directory brute-force attacks generate a very high number of HTTP 404 responses.
- User-Agent analysis helps identify attacker tools.
- Timeline reconstruction simplifies incident investigations.
- Exposed backup files represent a significant security risk.

---

## Security Improvements

- Remove unnecessary backup files.
- Restrict access to administrative pages.
- Implement authentication for sensitive resources.
- Deploy a Web Application Firewall (WAF).
- Monitor Apache logs continuously.
- Enable automated alerting for suspicious activity.
- Perform regular vulnerability assessments.
- Apply operating system and Apache security updates.

---

## SOC Skills Practiced

- Web Server Investigation
- Log Analysis
- Threat Hunting
- IOC Extraction
- Incident Response
- Apache Security
- Linux Administration

---

## Final Note

This project was completed in a controlled virtual environment for educational purposes and demonstrates practical Blue Team investigation skills applicable to Security Operations Center (SOC) environments.
