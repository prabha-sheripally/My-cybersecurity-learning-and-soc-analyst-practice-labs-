# 🔐 Suspicious Logon Investigation - Lab 5
Threat Type: Potential Brute Force or Unauthorized Access Attempt
## 🧪 File Details:
- Log Source: Windows Security Logs (Event Viewer)
- Event ID: `4625` (Failed Logon), followed by `4624` (Successful Logon)
- Username: `john-admin`
- Host: `DC01.internal.local`
- Logon Type: `10` (Remote Interactive / RDP)
- Time of Activity: Late night (non-business hours)
## 🔍 Investigation Steps:
1. Opened Event Viewer → Security Logs
2. Noticed multiple `4625` failed logon attempts from same IP address
3. Eventually saw a `4624` successful logon from same IP (possible brute-force)
4. Checked geolocation of source IP → Found it was from foreign country
5. Correlated with VPN/firewall logs to confirm unauthorized access
6. ## 🛠️ Tools Used:
- Windows Event Viewer
- SIEM (e.g., Splunk or Wazuh)
- GeoIP Lookup tools
- Firewall or VPN logs
## ✅ Outcome:
- Confirmed unauthorized access attempt via brute-force RDP
- Account `john-admin` credentials were reset
- Source IP was blocked at firewall
- Incident reported to management and ticket raised for full investigation
## 🧠 Summary:
This lab demonstrates how to identify suspicious remote logons using Windows Event IDs and investigate potential brute-force attacks.
## 🏷️ Tags: event log, brute force, failed logon, 4625, lateral movement, rdp
