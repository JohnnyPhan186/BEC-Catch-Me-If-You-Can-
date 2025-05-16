# BEC-Catch-Me-If-You-Can (:

Simulated a real-world Business Email Compromise (BEC) attack targeting a corporate network. As part of the Blue Team, I analyzed network traffic (PCAP files) using Wireshark to:

- Identify malicious phishing emails masquerading as legitimate communications.

- Trace the attacker’s infrastructure (IPs, domains, email headers).

- Distinguish between fraudulent vs. legitimate emails to mitigate the threat.

## 🔐 BEC Attack Simulation - Wireshark Analysis  
**Scenario**: A threat actor impersonated executives via phishing emails.  
**My Role**: Blue Team analyst tasked with identifying malicious emails in PCAPs.  
**Key Findings**:  
- Attacker IP: `10.6.1.104`.  
- Spoofed Emails: Used `From: <YourLife40@0859.com>"`,`From: <YourLife26@5088"`, `From: <YourLife11@7040"` with fear-mongering phising emails.  
**Tools**: Wireshark

## 📝 Methodology
1. **Analyzed pcap files**:
   - Filtered SMTP packets: `smtp contains "FROM""`
   - This display filter searches for packets where SMTP protocol data such as email heards includes the string "FROM".
   - This filter revealed multiple emails with nearly identical headers and all email oringinating from the same source IP address!
   - ![smtp contains](https://github.com/user-attachments/assets/e9782614-da48-4a4a-88cc-2bc36047dd05)

2. **Identified Malicious Actor**:
   - Used `smtp.data.fragments` to view the content of the emails.
   - Identified attacker IP address: (`10.6.1.104`).
   - ![smtp](https://github.com/user-attachments/assets/74360889-79fa-48d8-ad40-7aace5ddd1cd)
3. **Exported IOCs**:
   - Extracted phishing email content via `File → Export Objects → IMF`.


Source of the malcious **pcap** file: https://www.malware-traffic-analysis.net/
