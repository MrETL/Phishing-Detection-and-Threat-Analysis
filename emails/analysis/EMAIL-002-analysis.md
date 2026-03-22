# Email Analysis: EMAIL-002 - Microsoft Login Scam

---

## Basic Information
- **Sample ID:** EMAIL-002
- **Classification:** PHISHING
- **Date Analyzed:** March 2026
- **Source:** rf-peixoto/phishing_pot GitHub Repository

---

## Email Details

**Subject:** Microsoft account unusual signin activity

**From (Display):** Microsoft account team <no-reply@access-accsecurity.com>

**From (Actual):** no-reply@access-accsecurity.com

**Reply-To:** sotrecognizd@gmail.com

**Return-Path:** bounce@thcultarfdes.co.uk

**To:** phishing@pot

**Date:** Fri, 8 Sep 2023 05:47:04 +0000

**Sender IP:** 89.144.44.2

**Priority:** High (X-Priority: 1)

---

## Authentication Results

| Check | Result | Analysis |
|-------|--------|----------|
| **SPF** | none | No SPF record for sending domain |
| **DKIM** | none | Message not digitally signed |
| **DMARC** | permerror | Permanent error in DMARC processing |
| **Composite Auth** | fail | Failed authentication checks |

---

## Sender Analysis

**Claimed Identity:** Microsoft Account Team

**Actual Sending Infrastructure:**
- **Domain:** thcultarfdes.co.uk (suspicious, random characters)
- **Reply-To:** sotrecognizd@gmail.com (Gmail - consumer email)
- **Return-Path:** Different domain (bounce@thcultarfdes.co.uk)

**Domain Analysis:**
- **From Domain:** access-accsecurity.com
- **SMTP Domain:** thcultarfdes.co.uk  
- **Reply Domain:** gmail.com
- **Mismatch:** Three different domains used = high spoofing indicator

**Server Location:** UK-based infrastructure

---

## Content Analysis

### Subject Line
"Microsoft account unusual signin activity"

**Red Flags:**
- Creates urgency about account security
- Spelling error: "signin" instead of "sign-in" or "sign in"
- Common social engineering subject used in Microsoft phishing

### Visual Impersonation
- Claims to be from "Microsoft account team"
- Uses professional display name format
- High priority flag set (X-Priority: 1)

### Urgency Indicators
- X-Priority: 1 (Highest priority)
- X-Message-Flag: Flag
- Importance: high
- Forces immediate attention

### Reply-To Analysis
**sotrecognizd@gmail.com**
- Consumer Gmail account
- Not a Microsoft domain (@microsoft.com, @outlook.com, @office.com)
- Clear indicator of phishing - legitimate Microsoft never uses Gmail for replies

---

## Red Flags Checklist

- [x] **Suspicious sender domain** - access-accsecurity.com is not microsoft.com
- [x] **SPF/DKIM/DMARC failures** - No authentication passed
- [x] **Reply-to mismatch** - Replies go to Gmail instead of Microsoft
- [x] **Urgency language** - High priority flags set
- [x] **Return-path mismatch** - Different domain for bounces
- [x] **Spoofing attempt** - Claiming Microsoft identity

---

## Risk Assessment

**Risk Level:** **PHISHING - HIGH**

**Primary Threat:** Account takeover via credential harvesting

**Target Victims:** Microsoft account holders (Outlook, Office 365, Xbox, etc.)

**Attack Vector:**
1. User receives "urgent security alert"
2. Click link to "secure account"
3. Fake Microsoft login page steals credentials
4. Account compromised for data theft or business email compromise

---

## Technical Indicators

### Header Analysis
```
From: Microsoft account team ,_<no-reply@access-accsecurity.com>
Reply-To: sotrecognizd@gmail.com
Return-Path: bounce@thcultarfdes.co.uk
Authentication-Results: spf=none
  smtp.mailfrom=thcultarfdes.co.uk
  dkim=none (message not signed)
  dmarc=permerror
```

### IP Analysis
- **IP Address:** 89.144.44.2
- **Location:** United Kingdom
- **ISP:** Unknown hosting provider
- **Type:** Likely compromised or rented server

---

## Prevention Guidance

### For Users
1. **Check Reply-To:** Always verify reply address matches claimed sender
2. **Microsoft Domains:** Legitimate Microsoft uses @microsoft.com, @outlook.com, @office.com
3. **Gmail Red Flag:** Microsoft NEVER uses Gmail addresses
4. **Sign-in Activity:** Check actual account activity at account.microsoft.com directly

### For Organizations
1. **Microsoft Defender:** Enable Microsoft Defender for Office 365
2. **Conditional Access:** Implement location-based access policies
3. **MFA Enforcement:** Require multi-factor authentication for all Microsoft accounts
4. **User Training:** Educate about security alert phishing patterns

---

## Recommended Action

**DELETE & REPORT**

Confirmed phishing attempting to harvest Microsoft credentials. 

Report to:
- Report phishing to Microsoft: https://www.microsoft.com/en-us/wdsi/support/report-unsafe-site
- Forward to: abuse@outlook.com
- Gmail abuse: Report the reply-to address

---

*Analysis completed by Dilnessa Aemro*
