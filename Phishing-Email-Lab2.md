# 📧 Phishing Email Investigation - Lab 2
Threat Type: Phishing Attack with Malicious Attachment
## 🚨 Alert Details:
- Source: Microsoft Defender for Office 365
- Alert Type: Suspicious Email with Malicious Link
- Subject: "Urgent: Payment Issue in Your Account"
- Sender: `finance@secure-payments.com`
## 🔍 Investigation Steps:
1. Checked email headers → Spoofed domain detected
2. Link analysis → Redirects to fake login page (`http://secure-payments-login.co`)
3. URL submitted to VirusTotal → Flagged as phishing by 35 engines
4. Attachment `.html` file opened in safe environment → Contains credential harvesting script
5. ## 🛠️ Tools Used:
- VirusTotal
- Email Header Analyzer (MxToolbox or built-in SOC tool)
- Browser sandbox for link testing (like Any.Run)
- Internal SIEM for related events

- ## 🎯 Outcome:
- Email confirmed as phishing
- Blocked sender in mail gateway
- Reported to Threat Intel team
- Affected user’s password reset
- ## 📝 Summary:
This lab demonstrates how to analyze a phishing email using header inspection and link/attachment analysis, and how to escalate based on indicators of compromise (IOCs).
