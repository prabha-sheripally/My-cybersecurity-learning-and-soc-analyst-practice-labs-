# 🌐 DNS Tunneling Detection - Lab 10
> Threat Type: Command and Control (C2) via DNS Tunneling
- Alert Source: SIEM (Suricata/Zeek/Splunk)
- Device: `ENG-WORKSTATION02`
- Domain Queried: `abc.def.maliciousdomain.com`
- DNS Query Volume: 500+ queries in 15 minutes
- Detection: Unusual DNS request patterns with random subdomains
## 🔍 Investigation Steps:
1. SIEM raised alert for excessive DNS queries from a single host
2. Investigated domain patterns → detected use of random, encoded subdomains
3. Compared with known indicators from threat intelligence feeds
4. Used Wireshark to capture DNS traffic and review query lengths and frequency
5. Detected base64-encoded data inside DNS queries (common in DNS tunneling)
6. Correlated with EDR logs to check for suspicious PowerShell or background processes
## 🛠️ Tools Used:
- Suricata or Zeek (for DNS traffic monitoring)
- Splunk (SIEM alerting)
- Wireshark (packet capture)
- Threat intelligence platforms
- CrowdStrike/EDR
## ✅ Outcome:
- Host isolated from the network
- Malicious domain blocked at DNS firewall
- IOC added to detection rules
- Root cause traced to infected browser extension
## 🧠 Summary:
DNS Tunneling is a stealthy C2 technique. This lab demonstrates detection via traffic analysis, pattern recognition, and SIEM correlation.
