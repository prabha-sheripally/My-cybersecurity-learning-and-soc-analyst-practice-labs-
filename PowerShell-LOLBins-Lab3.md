# 🧪 PowerShell LOLBins Investigation - Lab 3

## 🚨 Alert Summary:
- EDR Alert: Suspicious PowerShell Execution
- Source Process: `powershell.exe`
- Detected Command:
  ```powershell
  powershell -nop -w hidden -enc aQBmACg...
  ## 🔍 Investigation Steps:
1. Reviewed alert details in SIEM (e.g., command-line arguments, user, host)
2. Noticed use of `-nop`, `-w hidden`, and `-enc` → Common LOLBins pattern
3. Decoded base64 string using CyberChef to reveal the actual script
4. Identified script was attempting to download remote payload
5. Checked MITRE ATT&CK mapping: T1059 (Command and Scripting Interpreter)
## 🛠️ Tools Used:
- CrowdStrike Falcon
- CyberChef (for decoding)
- PowerShell logs from Sysmon
- MITRE ATT&CK knowledge base
- ## ✅ Outcome:
- Blocked the hash of the script via endpoint tool
- Reported IP/domain to Threat Intel team
- Reset account that ran the script
- Added YARA rule for similar encoded PowerShell patterns
- ## 🧠 Summary:
This lab covered how to detect and decode suspicious PowerShell commands often used in LOLBins-style attacks, including response and mitigation steps.## 🧠 Summary:
This lab covered how to detect and decode suspicious PowerShell commands often used in LOLBins-style attacks, including response and mitigation steps.
## 🏷️ Tags: powershell, lolbins, base64, cyberchef, MITRe##
