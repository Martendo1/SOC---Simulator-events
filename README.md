# SOC---Simulator-events

# 🛡️ SOC Analyst Portfolio – Security Incident Investigations

## 👨‍💻 Author  
**Austin Martins**  
Aspiring SOC Analyst | Cybersecurity Enthusiast  

---

## 📖 Overview  
This project presents multiple security investigations carried out in a SOC (Security Operations Center) simulation environment. The objective is to analyze alerts, determine their legitimacy, and recommend appropriate remediation actions.

The cases include phishing emails, suspicious links, and firewall detections. Each alert was investigated using real-world SOC techniques such as log analysis, domain verification, and threat identification.

---

## 🧾 Introduction  
As a cybersecurity student, this project simulates real-world SOC responsibilities. I analyzed multiple alerts generated from different systems and determined whether they were malicious or legitimate.

During the investigation, I worked with:
- Email content and sender analysis  
- URL and domain verification  
- Firewall and proxy logs  
- Indicators of Compromise (IOCs)  

This project strengthened my ability to identify threats and make accurate security decisions.

---

## 📊 TOTAL NUMBER OF ALERTS  
<img width="1102" height="401" alt="image" src="https://github.com/user-attachments/assets/3cf90dc3-602d-4ed0-89ba-2523338f9836" />

---

## 🚨 ASSIGNED ALERTS  
**8816 – Access to Blacklisted External URL Blocked by Firewall (High)**  

I chose this as the **top priority** due to its **high severity and potential impact**.

---

# 🚨 INCIDENT N01

## 📌 Case ID: 8816  
**Alert Name:** Access To Blacklisted External URL Blocked By Firewall  
- **Severity:** High  
- **Category:** Firewall  
- **Date:** 24 March 2026  

## 📄 Description  
A firewall detected and blocked an outbound request to a URL classified as malicious or blacklisted. This may indicate user interaction with a phishing link or malware attempting communication with an external command-and-control server.

- **Source IP:** 10.20.2.17  
- **Action:** Blocked  
- **Timestamp:** 03/24/2026 12:35:27.900  

<img width="647" height="311" src="https://github.com/user-attachments/assets/a9a9031d-d00a-45cf-a2b0-fbc3ca24565a" />

---

### 🔍 Threat Validation  
**URL response via TryHackMe:**  
<img width="862" height="481" src="https://github.com/user-attachments/assets/617d521c-d457-4d5e-9a00-48b4a4f271f4" />

✔️ Confirmed malicious  

---

### 📸 Additional Evidence  
<img width="565" height="391" src="https://github.com/user-attachments/assets/2803f2d7-1a16-45a3-ab74-10013092aaad" />
<img width="566" height="425" src="https://github.com/user-attachments/assets/d399236a-74e0-44fa-95e7-37178656560a" />
<img width="543" height="238" src="https://github.com/user-attachments/assets/b9734eec-3158-4cdf-8fdb-f48ba92c939b" />

---

## ✅ Conclusion  
**True Positive – Threat Blocked Successfully**

---

# 📧 INCIDENT N02

## 📌 Case ID: 8815  
**Alert Name:** Inbound Email Containing Suspicious External Link  

<img width="1042" height="672" src="https://github.com/user-attachments/assets/093d9905-15a0-477d-ab97-abd3eb96c353" />

---

## ⏰ Time of Activity  
**24 March 2026, 12:34:13 PM**

---

## 👥 Affected Entities  
- Recipient: h.harris@thetrydaily.thm  
- Sender: urgents@amazon.biz  

---

## 📄 Incident Summary  
Phishing email impersonating Amazon, attempting to trick the user into clicking a malicious delivery link.

---

## 🚨 Indicators of Compromise  
- Fake domain: amazon.biz  
- Shortened URL (bit.ly)  
- Urgent phishing message  

---

## 🛠️ Remediation Actions  
- Block domain and URL  
- Scan for similar emails  
- Reset credentials if needed  

---

## ✅ Verdict  
**True Positive – Phishing Attempt**

---

# 📧 INCIDENT N03

## 📌 Case ID: 8814  

## 📄 Description  
Onboarding email flagged due to embedded link.

---

## 🔍 Analysis  
- Sender: onboarding@hrconnex.thm  
- Link: https://hrconnex.thm/onboarding/...  

✔️ Domain aligns with organization  

---

## 📸 Evidence  
<img width="1079" height="345" src="https://github.com/user-attachments/assets/448ddf02-9d38-4f54-82f9-7de064ba8771" />
<img width="860" height="514" src="https://github.com/user-attachments/assets/545aef9b-028b-411b-bee3-e15d76ae3f70" />
<img width="546" height="494" src="https://github.com/user-attachments/assets/684c4bc4-a404-4291-93be-593c25082b37" />
<img width="545" height="143" src="https://github.com/user-attachments/assets/8ea67406-b0eb-4209-91ab-1e7b1802323c" />

---

## ⚠️ Conclusion  
**Suspicious – Needs Validation (Likely False Positive)**

---

# 📧 INCIDENT N04

## 📌 Case ID: 8817  

## 📄 Description  
Phishing email impersonating Microsoft using a fake domain.

---

## 🔍 Analysis  
- Sender: no-reply@m1crosoftsupport.co  
- Malicious URL: https://m1crosoftsupport.co/login  

---

## 🚨 Indicators  
- Typosquatting domain  
- Fake login page  
- Urgent message  

---

## 📸 Evidence  
<img width="1062" height="351" src="https://github.com/user-attachments/assets/615b4a21-cac0-416f-a57d-86f620ddde26" />
<img width="845" height="470" src="https://github.com/user-attachments/assets/894450df-e147-4a76-84e7-4a6ec6de752a" />
<img width="435" height="456" src="https://github.com/user-attachments/assets/e41599b9-0021-4f63-867d-91f57d22a973" />

---

## ✅ Verdict  
**True Positive – Phishing Attack**

---

# 📧 INCIDENT N05

## 📌 Case ID: 8818  

## 📄 Description  
This alert involved an onboarding email with an embedded link. The investigation focused on verifying whether the email was malicious or legitimate.

---

## 🔍 Analysis  
- Sender: onboarding@hrconnex.thm  
- Domain: hrconnex.thm  
- No spoofing or malicious indicators  

---

## 📊 Observations  
- Legitimate internal domain  
- No phishing indicators  
- Normal onboarding process  

---

## ✅ Verdict  
**False Positive – Legitimate Email**

---

# 🏁 Final Conclusion  

This project demonstrates my ability to:
- Analyze SOC alerts  
- Identify phishing attacks  
- Investigate logs and domains  
- Differentiate between real threats and false positives  

---

## 🎯 Key Takeaways  
- Phishing attacks rely on **social engineering and fake domains**  
- Not all alerts are malicious (**false positives exist**)  
- Firewall logs help prevent real threats  
- Proper investigation is critical in SOC operations  

---

## 🚀 Future Improvements  
- Add MITRE ATT&CK mapping  
- Include Splunk queries  
- Expand to endpoint security cases  

---

## ⭐ Final Note  
This project reflects my hands-on SOC analysis skills and readiness for an entry-level cybersecurity role.
