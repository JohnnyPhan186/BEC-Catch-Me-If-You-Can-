# BEC-Catch-Me-If-You-Can-

Simulated a real-world Business Email Compromise (BEC) attack targeting a corporate network. As part of the Blue Team, I analyzed network traffic (PCAP files) using Wireshark to:

- Identify malicious phishing emails masquerading as legitimate communications.

- Trace the attacker’s infrastructure (IPs, domains, email headers).

- Distinguish between fraudulent vs. legitimate emails to mitigate the threat.

## 🔐 BEC Attack Simulation - Wireshark Analysis  
**Scenario**: A threat actor impersonated executives via phishing emails.  
**My Role**: Blue Team analyst tasked with identifying malicious emails in PCAPs.  
**Key Findings**:  
- Attacker IP: `203.0.113.22` (linked to known BEC campaigns).  
- Spoofed Emails: Used `MAIL FROM: CEO@company.com` with malicious PDF attachments.  
**Tools**: Wireshark, TShark, VirusTotal.  
