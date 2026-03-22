# Email Analysis: EMAIL-006 - Microsoft Account Tax/Financial Scam

---

## Basic Information
- **Sample ID:** EMAIL-006
- **Classification:** PHISHING
- **Date Analyzed:** March 2026
- **Source:** rf-peixoto/phishing_pot GitHub Repository

---

## Email Details

**Subject:** Microsoft account unusual signin activity

**From (Display):** Microsoft account team <no-reply@access-accsecurity.com>

**Reply-To:** solutionteamrecognizd02@gmail.com

**Return-Path:** bounce@thcultarfdes.co.uk

**To:** phishing@pot

**Date:** Wed, 26 Jul 2023 21:13:36 +0000

**Sender IP:** 89.144.44.2

**Message Size:** Large (22MB+ indicated)

---

## Authentication Results

| Check | Result | Analysis |
|-------|--------|----------|
| **SPF** | none | No SPF record for thcultarfdes.co.uk |
| **DKIM** | none | Message not digitally signed |
| **DMARC** | permerror | DMARC processing error |
| **CompAuth** | fail | Failed authentication |

---

## Sender Analysis

**Claimed Identity:** Microsoft Account Team

**Actual Infrastructure:**
- **From:** access-accsecurity.com
- **Return-Path:** thcultarfdes.co.uk (same as EMAIL-002)
- **Reply-To:** solutionteamrecognizd02@gmail.com (same as EMAIL-005)
- **Sending IP:** 89.144.44.2 (same as EMAIL-002 - same server)

**Campaign Connection:**
This email shares infrastructure with:
- EMAIL-002 (same sending IP and bounce domain)
- EMAIL-005 (same reply-to Gmail address)

**Shared Infrastructure = Coordinated Campaign**

---

## Campaign Analysis

### Infrastructure Sharing
| Component | EMAIL-002 | EMAIL-006 | Match |
|-----------|-----------|-----------|-------|
| Return-Path | thcultarfdes.co.uk | thcultarfdes.co.uk | ✅ |
| Reply-To | sotrecognizd@gmail.com | solutionteamrecognizd02@gmail.com | Similar |
| Sending IP | 89.144.44.2 | 89.144.44.2 | ✅ |
| From Domain | access-accsecurity.com | access-accsecurity.com | ✅ |

**Conclusion:** Same threat actor using consistent infrastructure

### Campaign Pattern
1. **Domain:** access-accsecurity.com (compromised or created for phishing)
2. **Bounce:** thcultarfdes.co.uk (dedicated bounce infrastructure)
3. **Replies:** Gmail accounts (disposable, easily created)
4. **Target:** Microsoft account holders
5. **Subject:** "unusual signin activity" (consistent social engineering)

---

## Content Analysis

### Subject Line
"Microsoft account unusual signin activity"

**Same Pattern:** Exactly matches EMAIL-002 and EMAIL-005

### Impersonation Tactics
- Claims to be "Microsoft account team"
- Spelling error: "signin" instead of "sign-in"
- Creates security urgency
- Professional formatting to appear legitimate

### Reply-To Analysis
**solutionteamrecognizd02@gmail.com**
- Same Gmail account as EMAIL-005
- Pattern: "solutionteamrecognizd" + number
- Consumer Gmail for "enterprise security team"
- Clear authentication red flag

---

## Red Flags Checklist

- [x] **Suspicious sender domain** - access-accsecurity.com not microsoft.com
- [x] **SPF/DKIM/DMARC failures** - Complete authentication failure
- [x] **Reply-to mismatch** - Gmail for Microsoft team
- [x] **Return-path mismatch** - Different bounce domain
- [x] **Campaign infrastructure** - Same IP/domain as other phishing
- [x] **Spelling error** - "signin" vs proper "sign-in"
- [x] **Large message** - 22MB+ suggests malicious attachment or tracking

---

## Risk Assessment

**Risk Level:** **PHISHING - HIGH**

**Primary Threat:** Account takeover via credential harvesting

**Campaign Risk:**
- Multiple emails using same infrastructure
- Coordinated attack on Microsoft users
- Consistent social engineering approach
- Likely automated or kit-based phishing

**Attack Vector:**
1. Security alert creates panic
2. Victim clicks "secure account" link
3. Fake Microsoft login page
4. Credentials harvested
5. Account compromised for:
   - Email access
   - Document theft
   - Cloud service access
   - Further phishing from compromised account

---

## Technical Indicators

### Header Analysis
```
From: Microsoft account team ,_<no-reply@access-accsecurity.com>
Reply-To: solutionteamrecognizd02@gmail.com
Return-Path: bounce@thcultarfdes.co.uk
Authentication-Results:
  spf=none (sender IP is 89.144.44.2)
  smtp.mailfrom=thcultarfdes.co.uk
  dkim=none
  dmarc=permerror
X-Sender-IP: 89.144.44.2
Content-Length: 22448528  (22MB - suspicious size)
```

### Infrastructure Analysis
- **IP:** 89.144.44.2 (UK - same as EMAIL-002)
- **Primary Domain:** access-accsecurity.com
- **Bounce Domain:** thcultarfdes.co.uk
- **Reply Domain:** gmail.com
- **Size:** 22MB suggests attachment or heavy obfuscation

---

## Campaign Tracking

### Indicators of Compromise (IOCs)

**Domains:**
- access-accsecurity.com (phishing domain)
- thcultarfdes.co.uk (bounce infrastructure)

**IP Addresses:**
- 89.144.44.2 (phishing server)

**Email Addresses:**
- solutionteamrecognizd02@gmail.com
- sotrecognizd@gmail.com

**Subject Patterns:**
- "Microsoft account unusual signin activity"

---

## Prevention Guidance

### For Users
1. **Recognize Campaigns:** Multiple similar emails = coordinated attack
2. **Check Consistency:** Same reply-to across emails = red flag
3. **Verify Independently:** Check account.microsoft.com directly
4. **Report Patterns:** Report all suspicious Microsoft emails

### For Organizations
1. **IOC Blocking:** Block domains access-accsecurity.com and thcultarfdes.co.uk
2. **IP Blocking:** Block 89.144.44.2 at firewall
3. **Pattern Detection:** Flag emails with "unusual signin" from non-Microsoft domains
4. **Campaign Alerts:** Notify users of active Microsoft phishing campaigns

---

## Recommended Action

**DELETE & REPORT**

Part of coordinated phishing campaign targeting Microsoft users.

**Report To:**
- Microsoft: https://www.microsoft.com/en-us/wdsi/support/report-unsafe-site
- Abuse: abuse@registrar of access-accsecurity.com
- Share IOCs with security community

---

*Analysis completed by Dilnessa Aemro*
