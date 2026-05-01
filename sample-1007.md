# sample-1007

## Overview
- Date Analyzed: 2026-05-01
- Disposition: Phishing confirmed
- Techniques: Brand Impersonation via Legitimate Sending Infrastructure, DMARC Absence Exploitation, Lookalike From Domain, Urgency Fabrication

## Header Analysis
- Display Name: Binance
- From: no-reply-supportbinancewallet[.]irs@auswestbc[.]com[.]au
- Return-Path: 1070189a93c67a5-2d72e19a-1525-41c6-92cb-347e9e7f27a5-000000@eu-central-1[.]amazonses[.]com
- Reply-To: N/A
- Sender IP: 69[.]169[.]224[.]12
- Subject: [Binance] Withdraw Successful - 2023-07-30 51:51:51(UTC)
- AuthAs: N/A - email arrived via authenticated Amazon SES, no anonymous relay flag
- Routing: Amazon SES EU-Central-1 (Frankfurt) -> Microsoft Exchange Online Protection (MW2NAM12FT067) - legitimate sending infrastructure abused by attacker-registered SES account

## Authentication
| Record | Result | Notes |
| --- | --- | --- |
| SPF | Pass| 69[.]169[.]224[.]12 authorized sender for eu-central-1[.]amazonses[.]com - validates infrastructure only, not sender identity |
| DKIM | Pass | Valid Amazon SES signature - confirms infrastructure, not identity |
| DMARC | None | No policy published for auswestbc[.]com[.]au - absence exploited to bypass alignment enforcement |

## External OSINT
| Indicator | Tool | Finding |
| --- | --- | --- |
| 69[.]169[.]224[.]12 | ASN lookup | Confirmed Amazon SES infrastructure - legitimate service abused |
| auswestbc[.]com[.]au | WHOIS | Domain unregistered - From domain is nonexistent |
| shylshom[.]com | WHOIS | Domain unregistered - expired since 2023 campaign |
| shylshow[.]com | VirusTotal | Flagged malicious - confirmed phishing payload destination |
| auswestbc[.]com[.]au | VirusTotal | Flagged malicious |

## Technique Classification
- Brand Impoersonation via Legitimate Sending Infrastructure - attacker registered Amazon SES account to send through verified insfrastructure, causing SPF and DKIM to pass despite fraudulent sender activity
- DMARC Absence Exploitation - no DMARC policy on From domain auswestbc[.]com[.]au allows authentication bypass without enforcement
- Lookalike From Domain - auswestbc[.]com[.]au constructued to obscure non-Binance origin while display name presents as legitimate Binance sender
- Urgency Fabrication - fake withdrawal notification with invalid timestamp `51:51:51 UTC` - phishing kit artifact confirming automated template generation

## URLs
Legitimate Binance brand URLs included to add visual legitimacy — low analytical value:
- hxxps://www[.]binance[.]com/en/my/security/anti-phishing-code
- hxxps://twitter[.]com/binance
- hxxps://telegram[.]me/BinanceExchange
- hxxps://www[.]facebook[.]com/binance
- hxxps://www[.]youtube[.]com/c/BinanceYoutube/featured
- hxxps://instagram[.]com/binance
- hxxps://www[.]reddit[.]com/r/binance/
- hxxps://www[.]linkedin[.]com/company/binance
- hxxps://www[.]reddit[.]com/r/binance/

Primary payload URL:
hxxps://shylshom[.]com/ — VirusTotal confirmed malicious — likely phishing landing page

## Attachments
- None

## IOCs
| Type | Indicator | Notes |
| --- | --- | --- |
| Domain | auswestbc[.]com[.]au | From domain - unregistered - VirusTotal flagged |
| Domain | shylshom[.]com | Payload domain - unregistered - VirusTotal flagged |
| Email | no-reply-supportbinancewallet[.]irs@auswestbc[.]com[.]au | Sender address |
| IP | 69[.]169[.]224[.]12 | Amazon SES EU-Central-1 - legitimate infrastructure abused |

<img width="1920" height="1602" alt="1-ipinfo-main" src="https://github.com/user-attachments/assets/c2ce0094-4d7d-4865-84a8-cb790a179fad" />

---

<img width="1920" height="610" alt="auswest-virustotal-main" src="https://github.com/user-attachments/assets/f13ee87f-ffdd-45f3-bdd3-b25b7eb2c04f" />

---

<img width="1326" height="807" alt="impossible-utc-main" src="https://github.com/user-attachments/assets/1b377a30-f6b7-45d7-8cf9-84b8ca30d4d5" />

---

<img width="1920" height="652" alt="shylshom-virustotal-main" src="https://github.com/user-attachments/assets/46f444a9-297e-49a5-927e-462f9a508045" />

---

<img width="1920" height="323" alt="shylshom-whois-main" src="https://github.com/user-attachments/assets/a4f66d41-6cc4-46c6-b227-ced77f7faf7d" />

