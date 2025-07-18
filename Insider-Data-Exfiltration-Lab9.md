# 🕵️‍♂️ Insider Data Exfiltration via Cloud Apps - Lab 9
> Threat Type: Insider Threat – Data Exfiltration via Personal Cloud Storage
- Alert Triggered by: Microsoft Defender for Cloud Apps / DLP Policy
- User: `sales.exec@company.com`
- Activity: Uploaded 30+ sensitive PDFs to `Google Drive` using web browser
- Triggered DLP Rule: "Confidential Data Uploaded to Unauthorized Cloud App"
- Severity: High
## 🔍 Investigation Steps:
1. Alert received from Defender for Cloud Apps (MCAS) for large data upload
2. Reviewed activity log: confirmed multiple files uploaded to `drive.google.com`
3. Matched files with DLP fingerprints (customer PII, pricing documents)
4. Checked user’s recent downloads from internal CRM via SIEM
5. Investigated proxy/web logs to validate upload behavior
6. Interviewed user — found intent to leave company soon
## 🛠️ Tools Used:
- Microsoft Defender for Cloud Apps (MCAS)
- DLP policies in Microsoft 365
- Web proxy logs (e.g., Zscaler, Bluecoat)
- SIEM (Splunk/Wazuh) for correlating CRM access
- Insider Threat Playbook
## ✅ Outcome:
- User account suspended
- HR and legal team notified
- Data access logs archived
- DLP policies tightened to block Google Drive uploads
## 🧠 Summary:
This lab highlights the importance of monitoring cloud app usage for insider threats. It shows how DLP and MCAS can detect when sensitive data leaves the organization through unapproved apps.
## 🏷️ Tags: insider threat, dlp, cloud apps, mcsa, data exfiltration, google drive
