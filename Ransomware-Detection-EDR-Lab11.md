# Ransomware Detection via EDR - Lab 11
> Threat Type: Ransomware Execution and Containment (Detected by EDR)
- Alert Source: CrowdStrike Falcon / SentinelOne
- Host: `FINANCE-PC01`
- Detected File: `invoice_update.exe`
- Behavior: File encryption activity, creation of `.locked` extensions
- Ransom Note Dropped: `README_RECOVER.txt`
- Severity: Critical
## 🔍 Investigation Steps:
1. Received alert from EDR tool for suspicious encryption activity
2. Observed parent process: `invoice_update.exe` executed via email attachment
3. Verified process tree – used PowerShell to drop files and disable shadow copies
4. EDR flagged behavior: mass file rename, registry changes, backup deletion
5. Located dropped ransom note with instructions and bitcoin address
6. Checked network connections – found C2 beacon attempts
7. Isolated the host from the network to contain the spread
## 🛠️ Tools Used:
- CrowdStrike Falcon / SentinelOne
- EDR Process Tree Analysis
- File Integrity Monitoring (FIM)
- VirusTotal for hash analysis
- SIEM to check lateral movement
## ✅ Outcome:
- Host isolated and re-imaged
- IOC hashes added to threat feed
- Email attachment source blocked at email gateway
- User retrained on phishing awareness
## 🧠 Summary:
This lab shows how EDR tools help detect and contain ransomware by analyzing file behavior, process tree, and system-level changes. It highlights the importance of early detection and quick response.
## 🏷️ Tags: ransomware, edr, crowdstrike, process tree, encryption, phishing attachment, response
