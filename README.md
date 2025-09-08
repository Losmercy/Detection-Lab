# Email Phishing - Simulation, Detection and Threat Hunting - Microsoft Defender (Cloud)

## Project Overview:
This project aims to simulate a phishing attack via email to detect employees who click on the embedded URL, which in this case is assumed to be malicious.

### Skills Learned

- Create a SafeLink Policy for users within the organization
- Create and Anti-Phishing Policy to detect whether an email is malicious emails before deciding the course of action based on preset Rules
- Simulate a phishing email attack from two sources - Newly created email address on a different domain, and pre-built Microsoft phishing email simulation.
- Detect URL clicks by users, and recommend appropriate training for users affected


### Tools Used

- Outlook office
- ProtonMail
- Microsoft Defender


## Steps
- Setup SafeLink and Anti-Phishing Policies to prevent users from clicking hidden links within an email and scan emails before delivering to users or quarantining.
<img width="1920" height="1080" alt="Screenshot (41)" src="https://github.com/user-attachments/assets/e022537e-a308-4c2d-9ebb-3d6e869d6ca9" />
Ref 1: SafeLink Policy overview (Microsoft Defender>Policies & Rules>Threat Policies>Safe Links.


<img width="1920" height="1080" alt="Screenshot (43)" src="https://github.com/user-attachments/assets/93d968f3-2202-4ef9-8d49-5cee9d38bdb3" />
Ref 2: Anit-Phishing Policy OverviewPolicy overview (Microsoft Defender>Policies & Rules>Threat Policies>Anti-Phishing.


- Sent an email with an embedded link using ProtonMail domain from a newly created account -Email Delivered to the intended receiver.
- Simulated an email phishing simulation using a pre-built simulator on Microsoft defender. The MITRE ATT&CK technique being exploited here is “credential access” to know which users will provide their credentials to the supposedly malicious URL page. The URL page requests the user to enter their login credentials which in a real world scenario, would be forwarded to the attackers.
<img width="1920" height="1080" alt="Screenshot (46)" src="https://github.com/user-attachments/assets/8001bd0c-53d1-45de-9abe-baa87621f760" />
Ref 3: Phishing email simulator sent to intended user with the aim of obtaining their login credentials


<img width="1920" height="1080" alt="Screenshot (49)" src="https://github.com/user-attachments/assets/b20fe27e-52d5-4baa-9430-3d3c0ffa4519" />
Ref 4: Phishing email received and opened by User


<img width="1920" height="1080" alt="Screenshot (51)" src="https://github.com/user-attachments/assets/a90a118b-ae54-4371-97dc-f3d21b703f52" />
Ref 5: Phishing notification


<img width="1920" height="1080" alt="Screenshot (52)" src="https://github.com/user-attachments/assets/9ae8a8d4-81d9-4e0e-9a9e-7cf65845477b" />
Ref 6: New training recommended for user (Automated mail as set up in the Anit-Phishing Policy)


- Conducted further investigation to determine the legitimacy of the embedded URL within the phishing emails. Microsoft Defender>Investigation and Response> Hunting> Advanced Hunting>Email and Collaborations. Queried EmailUrlInfo and UrlClickEvents to see the fields available which would help with threat hunting if this were a real world scenario.
  
<img width="1920" height="1080" alt="Screenshot (66)" src="https://github.com/user-attachments/assets/9cd75fbd-0b43-409a-b3f5-60ee963ee3f1" />
Ref 7: Advanced hunting for legitimacy of the embedded link.



## Lesson Learned

Email phishing is one of the most common ways malicious actors gain initial access to a system and users should be trained regularly on what to look out for when they receive an email. In the event that a malicious link has been clicked, users are advised to report to the security team to investigate in a bid to prevent further compromise. Such users should be placed on appropriate training after the incident.

