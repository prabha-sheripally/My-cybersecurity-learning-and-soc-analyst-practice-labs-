# 🔄 Suspicious Scheduled Task - Lab 7
> Threat Type: Attacker Persistence using Scheduled Task
- Alert Triggered by: EDR (e.g., CrowdStrike or Defender for Endpoint)
- Device: `WIN-SERVER01`
- Task Name: `WinUpdateCheck`
- Command: `powershell.exe -nop -w hidden -enc <Base64Payload>`
- Created by user: `svc_backup`
- Log Source: Windows Event ID `4698` (Scheduled Task Created)
## 🔍 Investigation Steps:
1. EDR triggered alert for suspicious task creation with encoded PowerShell
2. Investigated `Event ID 4698` to confirm task details (creator, command, schedule)
3. Noted that task ran under a **non-admin service account**, possibly compromised
4. Decoded base64 command using CyberChef → Found C2 beaconing script
5. Checked system startup and registry for persistence indicators
6. Verified if lateral movement occurred post task execution
## 🛠️ Tools Used:
- CrowdStrike / Defender EDR
- Windows Event Viewer (4698 logs)
- CyberChef (for decoding)
- Sysinternals Autoruns
- SIEM (Splunk/Wazuh) for correlation
## ✅ Outcome:
- Task deleted and blocked via EDR policy
- `svc_backup` credentials reset
- IOC shared with threat intel team
- Full system scan completed and clean
## 🧠 Summary:
This lab showcases how attackers use scheduled tasks for persistence and how to detect and respond using log analysis and EDR tools.
## 🏷️ Tags: scheduled task, persistence, event logs, powershell, base64, edr
