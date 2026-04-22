# sample-1002
```
## Report
Overview:
Date Analyzed: 2026-04-21
Disposition: Phishing Confirmed
Technique: Display Name Spoofing, Lookalike Domain, Reply-To Hijack, Pre-Staged Social Engineering Action Links

Header Analysis:
Display Name: Microsoft account team
From: no-reply@access-accsecurity[.]com
Return-Path: bounce@thcultarfdes[.]co[.]uk
Reply-To: solutionteamrecognizd02@gmail[.]com
Sender IP: 89[.]144[.]44[.]2
Subject: Microsoft account unusual signin activity
AuthAs: Anonymous
Routing: Unauthenticated relay via Microsoft EOP (VI1EUR05FT062[.]eop-eur05) - originated from 89[.]144[.]44[.]2,
traversed three Exchange Online hops before delivery

Authentication:
SPF: None - thcultarfdes[.]co[.]uk designates no permitted senders
DKIM: None - No signature present
DMARC: permerror - Permanent error, policy misconfigured or absent

External OSINT:
WHOIS: 89[.]144[.]44[.]2
- MSCode PL, provisioned 2026-02-14, GhostNet upstream, dual ASN AS201132/AS214762

MXToolbox: thcultarfdes[.]co[.]uk
- DNS record not found. No DMARC record found

WHOIS + MXToolbox: access-accsecurity[.]com
- (WHOIS) Domain not registered
- (MXToolbox) DNS record not found. No DMARC record found

Technique Classification:
Display Name Spoofing: "Microsoft account team" with no authentication backing
Lookalike Domain: access-accsecurity[.]com engineered to imply account security
Reply-To Hijack: Replies routed to solutionteamrecognizd02@gmail[.]com
Pre-Staged Social Engineering Action Links: Three mailto links routing victim responses to attacker-controlled Gmail

Embedded Action URLs
Pre-constructed mailto links designed to route victim responses to attacker-controlled address:

mailto[:]solutionteamrecognizd02@gmail[.]com?&cc=solutionteamrecognizd02@gmail[.]com&Subject=Unsubscribe+me
mailto[:]solutionteamrecognizd02@gmail[.]com?&cc=solutionteamrecognizd02@gmail[.]com&Subject=Report+The+User
mailto[:]solutionteamrecognizd02@gmail[.]com?&cc=solutionteamrecognizd02@gmail[.]com&Subject=unusual signin activity&body=Report The User

All three confirm Reply-To hijack destination.
Social engineering vectors designed to elicit victim email confirmation and engagement.

Attachments:
None.

-- IOCs --
Domains:
- thcultarfdes[.]co[.]uk
- access-accsecurity[.]com

Email Addresses:
- no-reply@access-accsecurity[.]com
- bounce@thcultarfdes[.]co[.]uk
- solutionteamrecognizd02@gmail[.]com

IPs:
- 89[.]144[.]44[.]2 - ASN AS201132/AS214762 - MSCode PL - GhostNet upstream

URLs:
- mailto:solutionteamrecognizd02@gmail[.]com?&cc=solutionteamrecognizd02@gmail[.]com&Subject=Unsubscribe+me
- mailto:solutionteamrecognizd02@gmail[.]com?&cc=solutionteamrecognizd02@gmail[.]com&Subject=Report+The+User
- mailto:solutionteamrecognizd02@gmail[.]com?&cc=solutionteamrecognizd02@gmail[.]com&Subject=unusual+signin+activity&body=Report+The+User
```
<img width="1612" height="497" alt="MXToolbox" src="https://github.com/user-attachments/assets/ef074449-291e-48c7-804a-fa72ce0c5ff2" />

---

<img width="1619" height="470" alt="MXToolbox2" src="https://github.com/user-attachments/assets/c1951ed3-ffdb-4b8b-9935-2e2d5dda5341" />

---

<img width="799" height="936" alt="whois" src="https://github.com/user-attachments/assets/9c4af35c-1cc3-4d20-ae70-55ed02033a78" />
