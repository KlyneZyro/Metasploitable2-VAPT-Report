# VAPT Report: Metasploitable 2 System Compromise 🛡️

## 📝 Project Overview
This repository contains a comprehensive Vulnerability Assessment and Penetration Testing (VAPT) report for the **Metasploitable 2** vulnerable environment. The assessment follows the standard 5-phase ethical hacking methodology, demonstrating a complete "Kill Chain"—from initial reconnaissance to unauthenticated root access and post-exploitation persistence.

## 🎯 Target Profile
- **Target OS:** Linux (Metasploitable 2)
- **Primary Attack Vector:** vsftpd 2.3.4 Backdoor (CVE-2011-2523)
- **Risk Severity:** 🔴 CRITICAL (CVSS 9.8)

## 🛡️ Executive Summary
Successfully achieved **unauthenticated remote root access** by exploiting a backdoor in the FTP service. Following initial access, I performed credential harvesting from `/etc/shadow` and established long-term persistence via SSH key injection and manual system hardening for "stealth" access. The engagement concluded with anti-forensic log wiping and a detailed remediation roadmap.



## 🛠️ Key Skills & Tools Demonstrated
- **Reconnaissance:** Service/Version detection and network mapping using `Nmap`.
- **Exploitation:** Leveraged `Metasploit` for unauthenticated Remote Code Execution (RCE).
- **Post-Exploitation:** Credential exfiltration and password cracking using `John the Ripper` with the `rockyou.txt` wordlist.
- **Persistence:** Injected SSH RSA keys into `authorized_keys` and modified `sshd_config` for backup access.
- **Troubleshooting:** Resolved legacy environment issues (e.g., `xterm-256color` errors) through manual environment variable manipulation.
- **Defense Evasion:** Simulated "anti-forensics" by wiping `auth.log` and clearing shell command histories.
- **Reporting:** Authored a professional audit report including Executive Summaries and Remediation strategies.

## 📂 Documentation
- **[Full Technical Report (PDF)](./Metasploitable%202_%20vsftpd%202.3.4%20Exploitation%20Lab.pdf)** - Detailed step-by-step walk-through and findings.

## 💡 Lessons Learned
- **Reconnaissance Foundation:** Extensive pre-exploitation research reduces "time-on-target" and detection risk.
- **Manual Verification:** Tools can fail; manually verifying active sessions with `sessions -l` is critical for operational success.
- **Stealth Strategy:** Pivoting from a noisy exploit to a "legitimate-looking" SSH login is superior for long-term persistence.

---
*Disclaimer: This project was conducted in a private, authorized lab environment for educational purposes. Unauthorized hacking is illegal and unethical.*
