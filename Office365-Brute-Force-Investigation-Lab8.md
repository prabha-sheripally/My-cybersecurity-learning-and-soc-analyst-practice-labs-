# Office 365 Brute Force Attack - Lab 8
> Threat Type:Cloud Account Compromise Attempt via Brute Force
- Alert Source: Microsoft Defender for Cloud Apps / Azure AD Identity Protection
- Affected User: `john.hr@company.com`
- IP Address: `103.45.66.77` (Unusual location - China)
- Sign-in Result: Multiple failures followed by success
- Detection Method: Impossible Travel / Sign-in from unfamiliar location
## 🔍 Investigation Steps:
1. Received alert from Defender for Cloud Apps for suspicious login pattern
2. Checked Azure AD sign-in logs → Noted multiple failed login attempts
3. Identified login from IP `103.45.66.77` not matching user's usual geolocation
4. Enabled MFA logs → No MFA used at the time of login
5. Investigated token activities and mail-forwarding rules for post-compromise actions
6. Verified mailbox access and login timestamps
## 🛠️ Tools Used:
- Microsoft Defender for Cloud Apps
- Azure AD Sign-in Logs
- Microsoft 365 Security Center
- GeoIP tools
- Conditional Access policies
## ✅ Outcome:
- User account temporarily disabled
- Password reset and MFA enforced
- Conditional Access rules updated to block risky IPs
- Security awareness training triggered for user
## 🧠 Summary:
This lab demonstrates a real-world scenario of brute force login attempts targeting Office 365 accounts. It shows how cloud security tools help identify and respond to identity-based attacks.
## 🏷️ Tags: brute force, o365, cloud security, azure ad, m365 defender, identity protection
