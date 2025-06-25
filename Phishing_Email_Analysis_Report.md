# 📄 Phishing Email Analysis Report

**Internship Task**: Cyber Security Internship – Task 2  
**Analyzed By**: Yuvaraj S  
**Date of Analysis**: 25 June 2025  
**Tool Used**: [EML Analyzer](https://eml-analyzer.herokuapp.com/)

---

## 📌 1. Basic Email Details

- **Message ID**: `<20230726121746.6B02D4DDDB@ubuntu-s-1vcpu-512mb-10gb-sfo3-01>`
- **Subject**: *Seus pontos Livelo expiram em breve - PROTOCOLO: 57949307.*
- **Date (UTC)**: `2023-07-26T12:17:46Z`
- **From Address**: `sac@bradesco.com.br`
- **To Address**: `phishing@pot`

---

## 🕵️ 2. Phishing Indicators Found

### ✅ 2.1 Spoofed Sender Address
- The sender claims to be from `bradesco.com.br` (a known Brazilian bank).
- However, upon investigation, **email originated from IP `147.182.193.196`**, which is **not associated with Bradesco's official servers**.
- Spoofing technique likely used to fake legitimacy.

### ✅ 2.2 Suspicious Subject Line
- Subject line contains urgency: “Points expiring soon” + protocol number — a **common social engineering tactic**.

### ✅ 2.3 Multiple Unusual Hops
- The email passed through several suspicious relays:
