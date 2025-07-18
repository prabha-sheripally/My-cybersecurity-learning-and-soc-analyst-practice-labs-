# 🛡️ DLP Alert Investigation - Lab 4
Threat Type: Data Exfiltration via Personal Email (Insider Threat)
- File: `customer_data.xlsx`
- Attempted upload to: `gmail.com` via browser
- User: `employee123`
- Triggered by: DLP endpoint agent
- Classification: Contains PII (names, emails, credit card info)
## 🔍 Investigation Steps:
1. Opened DLP console and reviewed alert metadata (user, device, file name)
2. Checked email browser logs and verified upload attempt
3. Used SIEM to trace user activity 30 mins before and after incident
4. Verified file content contained PII (names, emails, credit card numbers)
5. Notified HR and manager as part of insider threat protocol
6. Checked if similar alerts triggered on other endpoints
## 🛠️ Tools Used:
- Symantec DLP / Forcepoint DLP
- SIEM (like Splunk)
- Endpoint logs
- HR escalation procedure
- ## ✅ Outcome:
- Upload attempt was blocked by DLP
- Employee was given warning and educated on company policy
- No actual data breach occurred
- Added domain `gmail.com` to blocked upload list for sensitive files
- ## 🧠 Summary:
This lab showed how to handle a DLP alert for sensitive data upload, including triage, verification, and escalation processes.
## 🏷️ Tags: DLP, insider threat, sensitive data, PII, upload monitoring
