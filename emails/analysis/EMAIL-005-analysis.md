# Email Analysis: EMAIL-005 - Microsoft Account Security Alert Phishing

---

## Basic Information
- **Sample ID:** EMAIL-005
- **Classification:** PHISHING
- **Date Analyzed:** March 2026
- **Source:** rf-peixoto/phishing_pot GitHub Repository

---

## Email Details

**Subject:** Microsoft account unusual signin activity

**From (Display):** Microsoft account team <no-reply@access-accsecurity.com>

**Reply-To:** solutionteamrecognizd02@gmail.com

**Return-Path:** bounce@nonkfrgr.co.uk

**To:** phishing@pot

**Date:** Thu, 27 Jul 2023 07:40:03 +0000

**Sender IP:** 89.144.9.87

---

## Authentication Results

| Check | Result | Analysis |
|-------|--------|----------|
| **SPF** | none | No SPF record for nonkfrgr.co.uk |
| **DKIM** | none | Message not digitally signed |
| **DMARC** | permerror | Permanent DMARC error |
| **CompAuth** | fail | Failed authentication |

---

## Sender Analysis

**Claimed Identity:** Microsoft Account Team

**Actual Infrastructure:**
- **From:** access-accsecurity.com
- **Return-Path:** nonkfrgr.co.uk (suspicious random name)
- **Reply-To:** solutionteamrecognizd02@gmail.com
- **Sending IP:** 89.144.9.87 (UK-based)

**Domain Mismatch Pattern:**
| Claimed | Actual | Status |
|---------|--------|--------|
| Microsoft | access-accsecurity.com | ❌ Fake |
| Microsoft | nonkfrgr.co.uk | ❌ Fake |
| Microsoft | gmail.com | ❌ Consumer email |

**Multiple Domain Usage:** 3 different domains = clear spoofing attempt

---

## Content Analysis

### Subject Line
"Microsoft account unusual signin activity"

**Social Engineering Tactics:**
- Creates security concern (account compromise fear)
- "unusual signin" implies unauthorized access
- Spelling error: "signin" (should be "sign-in")
- Same subject pattern as EMAIL-002 (campaign indicator)

### Impersonation Elements
- Claims to be "Microsoft account team"
- Uses professional display name format
- Spoofing Microsoft security notifications

### Reply-To Analysis
**solutionteamrecognizd02@gmail.com**
- Consumer Gmail account
- Random naming pattern ("recognizd" misspelled)
- Clear red flag: Microsoft doesn't use Gmail

---

## Red Flags Checklist

- [x] **Suspicious sender domain** - access-accsecurity.com is not microsoft.com
- [x] **SPF/DKIM/DMARC failures** - Complete authentication failure
- [x] **Reply-to mismatch** - Gmail reply address
- [x] **Return-path mismatch** - Different bounce domain
- [x] **Spelling error** - "signin" vs "sign-in"
- [x] **Same campaign** - Similar to EMAIL-002 (same subject pattern)
- [x] **Consumer email** - Gmail used for "enterprise security"

---

## Campaign Analysis

**Pattern Match:** This email shares characteristics with EMAIL-002:
- Same subject line pattern
- Similar "account team" impersonation
- Gmail reply-to addresses
- Same spoofing technique
- Likely same threat actor or phishing kit

**Campaign Indicators:**
- Reused subject templates
- Consistent Gmail reply-to pattern
- Similar domain naming (access-accsecurity)
- Same authentication failures

---

## Risk Assessment

**Risk Level:** **PHISHING - HIGH**

**Primary Threat:** Microsoft account credential harvesting

**Attack Vector:**
1. Security alert creates urgency
2. User clicks to "secure account"
3. Fake Microsoft login page
4. Credentials stolen
5. Account takeover (email, documents, cloud storage)

**Secondary Risks:**
- Office 365/Outlook account compromise
- Business email compromise if corporate account
- Access to Microsoft cloud services
- Password reuse attacks on other services

---

## Technical Indicators

### Header Analysis
```
From: Microsoft account team ,_<no-reply@access-accsecurity.com>
Subject: Microsoft account unusual signin activity
Reply-To: solutionteamrecognizd02@gmail.com
Return-Path: bounce@nonkfrgr.co.uk
Authentication-Results: 
  spf=none (sender IP is 89.144.9.87)
  smtp.mailfrom=nonkfrgr.co.uk
  dkim=none
  dmarc=permerror
X-Sender-IP: 89.144.9.87
```

### Infrastructure
- **IP:** 89.144.9.87 (UK)
- **From Domain:** access-accsecurity.com
- **Bounce Domain:** nonkfrgr.co.uk
- **Reply Domain:** gmail.com

---

## Prevention Guidance

### For Users
1. **Check Domain:** Microsoft only uses microsoft.com, outlook.com, office.com
2. **Verify Reply-To:** Never trust security emails with Gmail reply addresses
3. **Direct Login:** Go to account.microsoft.com directly, never through email links
4. **Sign-in History:** Check actual sign-ins in Microsoft account security settings

### For Organizations
1. **Microsoft Defender:** Enable Microsoft Defender for Office 365 protection
2. **Brand Impersonation:** Create rules to flag "Microsoft account" from non-Microsoft domains
3. **User Reports:** Encourage reporting suspicious Microsoft-branded emails
4. **Security Training:** Educate users on Microsoft security alert phishing

---

## Recommended Action

**DELETE & REPORT**

Confirmed phishing impersonating Microsoft security team.

**Report To:**
- Microsoft phishing report: https://www.microsoft.com/en-us/wdsi/support/report-unsafe-site
- Forward to: phishing@microsoft.com
- Gmail: Report the reply-to address

---

*Analysis completed by Dilnessa Aemro*
