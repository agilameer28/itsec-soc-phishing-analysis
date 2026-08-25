# Phishing Incident: IoC Extraction Report

| Data Point | Extracted Value | Analysis / Threat Intel |
| :--- | :--- | :--- |
| **Spoofed Sender (From)** | `billing@trustedvendor.com` | Displayed to the victim to build false trust. |
| **True Sender (Return-Path)** | `admin@evil-attacker-infra.net` | The actual email account used to dispatch the payload. |
| **Attacker Source IP** | `198.51.100.22` | The origin server. Action: **Block at edge firewall.** |
| **SPF / DMARC Status** | `FAIL` | Confirms the origin IP is not authorized to send mail for trustedvendor.com. |
| **Payload Delivery** | `invoice_9842_overdue.zip` | Suspicious archive likely containing a malicious executable. |
