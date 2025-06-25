# 🛡️ Phishing Email Analysis – Cyber Security Internship (Task 2)


---

## 🎯 Task Overview

- **Task:** Analyze a suspicious email for phishing indicators  
- **Tools Used:**  
  - [EML Analyzer](https://eml-analyzer.herokuapp.com)  
  - Kali Linux  
  - VirusTotal, urlscan.io, header inspection tools  
- **Deliverable:** Report listing phishing indicators found

---

## 🔍 Email Sample Details

- **From Address:** `sac@bradesco.com.br` *(spoofed)*  
- **Subject Line:** _"Seus pontos Livelo expiram em breve - PROTOCOLO: 57949307"_  
- **Date:** 26 July 2023 (UTC)

---

## 🚨 Phishing Traits Identified

| Trait                      | Description                                                                 |
|---------------------------|-----------------------------------------------------------------------------|
| **Sender Spoofing**       | Email appears from a bank, but real sending IP (`147.182.193.196`) is DigitalOcean (not official) |
| **Urgent Language**       | Subject creates urgency about expiring points to trigger emotional action |
| **Fake Domain Links**     | Links direct to suspicious `.run.app` cloud pages and tracking beacons     |
| **No SPF/DKIM Evidence**  | Missing or failed verification of email authenticity                       |
| **Mass Targeting Pattern**| Sent to generic inbox (`phishing@pot`) — likely bulk phishing              |

---

## 🔗 Extracted URLs & Domains

| URL / Domain                                                | Type           | Verdict        |
|-------------------------------------------------------------|----------------|----------------|
| `http://sstatic1.histats.com/0.gif?4787682&101`             | Tracking pixel | ⚠️ Suspicious  |
| `https://function-9-xka7zvb73a-rj.a.run.app`                | Payload page   | 🚨 Phishing risk |
| `rodrigo-f-p@hotmail.com`                                   | Bait email     | ⚠️ Unknown use |
| Domains: `histats.com`, `run.app`, `hotmail.com`            | Mixed usage    | Used in phish  |

👉 **See** `Suspicious_Links_Analysis.md` for full link analysis.

---

## 📁 Files in This Repo

```bash
phishing-email-analysis/
├── README.md
├── Phishing_Email_Analysis_Report.md
├── Suspicious_Links_Analysis.md
├── phishing_sample.eml       # (if permitted)
├── header_analysis.txt
└── screenshots/
    ├── email_header.png
    └── eml_analyzer_links.png
