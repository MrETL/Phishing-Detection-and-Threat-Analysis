# Phishing Email Detection & Awareness System

**Cyber Security Assessment**  
**Author:** Dilnessa Aemro  
**Date:** March 2026

---

## Project Overview

This repository contains a comprehensive phishing email analysis and awareness report created as part of the . The project demonstrates how to identify, analyze, and classify phishing emails while creating educational materials for organizational security awareness.

---

## What is Phishing?

Phishing is a cyber attack where malicious actors impersonate legitimate entities to:
- Steal login credentials
- Install malware
- Trick users into revealing sensitive information
- Conduct financial fraud

---

## Repository Structure

```
FUTURE_CS_02/
├── emails/
│   ├── samples/          # Raw phishing email samples (.eml, .txt, .json)
│   └── analysis/         # Analysis documentation for each sample
├── images/               # Screenshots of analysis process
│   ├── headers/          # Email header analysis screenshots
│   ├── links/            # URL/link inspection screenshots
│   └── content/          # Email content red flags
└── report/               # Final deliverables
    └── PHISHING_DETECTION_REPORT.md
```

---

## Tools Used

| Tool | URL | Purpose |
|------|-----|---------|
| Google Email Header Analyzer | https://toolbox.googleapps.com/apps/messageheader/ | Parse email headers |
| MxToolbox Email Headers | https://mxtoolbox.com/EmailHeaders.aspx | SPF/DKIM/DMARC check |
| VirusTotal | https://www.virustotal.com | URL/domain reputation |
| WHOIS Lookup | https://whois.domaintools.com | Domain registration info |
| URLScan.io | https://urlscan.io | Safe URL analysis |

---

## Phishing Samples Sources

Samples obtained from verified public security repositories:

1. **Phishing Pot** - https://github.com/rf-peixoto/phishing_pot
2. **Phishing Mail Examples** - https://github.com/autinerd/phishing-mail-examples
3. **Phishing Email Dataset** - https://github.com/sadat1971/Phishing_Email
4. **Phishing Database** - https://github.com/Phishing-Database/Phishing.Database

*All samples used for educational purposes only.*

---

## Key Phishing Indicators

### Email Header Red Flags
- SPF/DKIM/DMARC authentication failures
- Sender domain mismatch
- Suspicious routing (multiple hops, unusual countries)
- Missing or forged headers

### Domain Red Flags
- Recently registered domains
- Lookalike domains (amaz0n.com vs amazon.com)
- Free email services (gmail.com, yahoo.com) claiming to be official
- HTTP instead of HTTPS

### Content Red Flags
- Urgency and fear tactics
- Generic greetings
- Spelling and grammar errors
- Requests for sensitive information
- Unexpected attachments
- Too-good-to-be-true offers

---

## Risk Classification

| Level | Description | Action |
|-------|-------------|--------|
| **PHISHING** | Confirmed malicious | DELETE & REPORT |
| **SUSPICIOUS** | Multiple red flags | VERIFY before action |
| **SAFE** | Legitimate email | NORMAL PROCESSING |

---

## Prevention Guidelines

### For Users
- ✅ Verify sender email addresses carefully
- ✅ Hover over links before clicking
- ✅ Be skeptical of urgent requests
- ✅ Contact organizations directly via official websites
- ❌ Don't click links in unsolicited emails
- ❌ Don't download unexpected attachments
- ❌ Don't share credentials via email
- ❌ Don't trust display names alone

### For Organizations
- Implement SPF, DKIM, and DMARC email authentication
- Deploy email security filtering
- Enable multi-factor authentication (MFA)
- Conduct regular phishing awareness training
- Create easy reporting mechanisms

---

## Report Contents

The full report (`report/PHISHING_DETECTION_REPORT.md`) includes:

1. **Executive Summary** - Key findings overview
2. **Methodology** - Tools and approach used
3. **Sample Analysis** - Detailed review of each phishing email
4. **Indicator Analysis** - Technical and content-based red flags
5. **Risk Classification** - Categorized results
6. **Prevention Guidelines** - Do's and Don'ts for users
7. **Recommendations** - For organizations

---

## How to Use This Repository

1. **Review the Report** - Start with `report/PHISHING_DETECTION_REPORT.md`
2. **Examine Samples** - Check `emails/samples/` for raw email data
3. **View Analysis** - See `emails/analysis/` for detailed breakdowns
4. **Use as Training** - Share with teams for security awareness

---

## Disclaimer

This repository is for **educational purposes only**. All phishing samples are from publicly available security datasets. 

**DO NOT:**
- Use these techniques to create phishing emails
- Send test phishing emails without authorization
- Access private email accounts without permission

---

## Contact

**Author:** Dilnessa Aemro  
**Program:**   
**Date:** March 2026

---

*This project demonstrates security analysis skills for educational and professional development purposes.*
