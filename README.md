# BEC-Catch-Me-If-You-Can-

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
   - ![smtp](https://github.com/user-attachments/assets/cfe84c07-8561-4fe4-9ac2-3bb1b1b9f3a9)
2. **Identified Malicious Actor**:
   - Used `smtp.data.fragments` to view the content of the emails.
   - ![smtp](https://github.com/user-attachments/assets/ae46ad37-a511-471f-ba85-d9a18150d131)
   - Identified attacker IP address: (`10.6.1.104`).
3. **Exported IOCs**:
   - Extracted phishing email content via `File → Export Objects → IMF`.


