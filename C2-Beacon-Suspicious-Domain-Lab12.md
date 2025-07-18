# Command and Control Beacon via Suspicious Domain - Lab 12
>  Threat Type: Command and Control (C2) Communication via Suspicious Domain
- Alert Source: SIEM (DNS logs + Threat Intel)
- Endpoint: `ENG-WORKSTATION09`
- Domain Contacted: `beacon-stage.fakecdn.live`
- Query Pattern: Every 60 seconds (regular interval)
- Detection: Unusual domain with low reputation + known APT IOC
## 🔍 Investigation Steps:
1. Alert triggered from SIEM for repeated DNS queries to suspicious domain
2. Checked DNS logs → Queries every 60 seconds → Indicates beaconing behavior
3. Domain flagged by threat intelligence feed as APT-related
4. Correlated with EDR logs → Parent process was `svchost.exe` spawned from unknown binary
5. Found encoded payload in memory (used `strings` and `ProcessHacker`)
6. No user activity during beaconing → ruled out browser or software update
## 🛠️ Tools Used:
- SIEM (Splunk, Wazuh)
- DNS logs and Threat Intelligence (AlienVault, AbuseIPDB)
- EDR (CrowdStrike/SentinelOne)
- Wireshark / Sysmon / Process Explorer
- Memory forensics (optional)
## ✅ Outcome:
- Host quarantined from network
- IOC domain blocked via DNS firewall
- Binary uploaded to VirusTotal for further analysis
- Threat hunting initiated to check lateral movement
## 🧠 Summary:
This lab covers detecting beaconing behavior that’s often missed by traditional antivirus. Identifying patterns and using threat intel helps detect advanced threats early.
## 🏷️ Tags: c2, beaconing, threat hunting, siem, edr, dns, apt
