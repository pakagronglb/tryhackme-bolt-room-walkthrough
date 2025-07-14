# Bolt CMS Security Assessment – TryHackMe Room

Welcome to the repository for the **Bolt CMS Security Assessment** performed against the [TryHackMe "Bolt" room](https://tryhackme.com/room/bolt). This repository contains the official penetration test report and supporting materials for a black-box assessment of a Bolt CMS environment.

---

## 📄 Report

The complete, detailed report is available here: [[THM-Bolt-Report.pdf](https://github.com/user-attachments/files/21213771/THM-Bolt-Report.pdf)
])

---

## Project Overview

- **Target:** Bolt CMS (version 3.7.0) at `10.10.101.223:8000` (TryHackMe "Bolt" room)
- **Assessment Dates:** 10/06/2025 – 22/06/2025
- **Methodology:** [OWASP Web Security Testing Guide (WSTG) v4.2](https://owasp.org/www-project-web-security-testing-guide/) and [NIST SP 800-115](https://csrc.nist.gov/publications/detail/sp/800-115/final)
- **Analyst:** Pakagrong Lebel
- **Lab Creator:** 0x9747

---

## Summary of Findings

This assessment identified several critical and high-risk vulnerabilities, including:

- **Authenticated Remote Code Execution** (CVE-2020-12256) via template processing and weak credentials (`bolt:boltadmin123`)
- **Weak Authentication Controls** (default credentials, lack of brute-force protection)
- **Sensitive Data Exposure** (admin credentials in public content)
- **Missing Security Headers** (CSP, HSTS, X-Frame-Options)
- **Outdated Software Components** (Bolt CMS 3.7.0, old OpenSSH)

These issues collectively enabled complete system compromise and root-level access. For a full breakdown of vulnerabilities, risk ratings, and technical evidence, please refer to the [attached report](./THM-Bolt-Report-1.pdf)[1].

---

## Tools Utilized

- **Parrot OS 5.3 x64**
- **Nmap 7.80**
- **Metasploit Framework 6.4.59**
- **ExploitDB** ([EDB-ID 48296](https://www.exploit-db.com/exploits/48296))

---

## References

- [TryHackMe "Bolt" Room](https://tryhackme.com/room/bolt)
- [OWASP WSTG v4.2](https://owasp.org/www-project-web-security-testing-guide/)
- [NIST SP 800-115](https://csrc.nist.gov/publications/detail/sp/800-115/final)
- [Bolt CMS Official Site](https://bolt.cm/)
- [CVE-2020-12256](https://nvd.nist.gov/vuln/detail/CVE-2020-12256)
- [ExploitDB EDB-ID 48296](https://www.exploit-db.com/exploits/48296)

---

## Disclaimer

This repository is intended **solely for educational and research purposes**. All testing was performed on a purposely vulnerable environment provided by TryHackMe.  
**Do not attempt these techniques on any system without explicit authorisation.**

---
