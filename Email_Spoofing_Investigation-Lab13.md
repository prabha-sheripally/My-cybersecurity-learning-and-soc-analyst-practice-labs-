# 🛡️ Scenario13#: Email Spoofing Investigation
## 🔐 Threat Type:Email Spoofing (Social Engineering / Identity Impersonation
## 📁 File Details / Artifacts:
- No attachments (text-only email)  
- Sender: `hr@company.com` (spoofed)  
- Return Path: suspicious external domain  
- No hash found — not a file-based threat
## 🕵️ Investigation Steps:
1. Verified sender's domain using WHOIS & DNS lookup  
2. Analyzed full email header in Outlook Message Header Analyzer  
3. Checked SPF, DKIM, DMARC results — SPF failed  
4. Searched SIEM/Email Gateway logs for similar messages to other users  
5. Confirmed no malware or phishing link was embedded
## ✅ Outcome / Actions Taken:
- Blocked spoofed domain in **Proofpoint / Email Gateway**  
- Reported domain to email security team  
- Verified no users interacted with the email  
- Trained user on identifying spoofed senders  
- Created detection rule for similar spoofed domain patterns
## 🛠️ Tools Used:
- Outlook Header Analyzer  
- VirusTotal  
- WHOIS Lookup  
- Proofpoint / Mimecast  
- SIEM (e.g., Splunk or Microsoft Sentinel)
## 🧵 Summary:
A user reported receiving an email appearing to be from HR. The sender name matched the internal HR department, but the email domain was not genuine. No links or attachments were present. The case was identified as **email spoofing**, likely for social engineering or reconnaissance.
