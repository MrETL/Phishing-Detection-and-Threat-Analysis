# Email Analysis: EMAIL-003 - Solar Panel/Delivery Scam (Zonnepanelen)

---

## Basic Information
- **Sample ID:** EMAIL-003
- **Classification:** PHISHING / SPAM
- **Date Analyzed:** March 2026
- **Source:** rf-peixoto/phishing_pot GitHub Repository

---

## Email Details

**Subject:** =?UTF-8?B?8J+Uiw==?= Zonnepanelen voor een goede prijs 
(🔥 Solar panels for a good price)

**From:** "Zonnepanelen installateur" <zonnepaneel@appjj.serenitepure.fr>

**Reply-To:** "Zonnepanelen installateur" <news@aichakandisha.com>

**Sender:** zonnepaneel@appjj.serenitepure.fr

**Return-Path:** return@dturm.de

**To:** phishing@pot

**Date:** Thu, 3 Nov 2022 04:56:15 +0000

**Sender IP:** 57.128.69.202 (OVH, France)

**In-Reply-To:** References previous spam message

---

## Authentication Results

| Check | Result | Analysis |
|-------|--------|----------|
| **SPF** | none | No SPF policy configured |
| **DKIM** | none | Message not digitally signed |
| **DMARC** | none | No DMARC policy |
| **CompAuth** | fail | Composite authentication failed |

---

## Sender Analysis

**Claimed Identity:** Solar Panel Installer (Zonnepanelen installateur - Dutch/Flemish)

**Language:** Dutch (Netherlands/Belgium target)

**Domain Infrastructure:**
- **From:** appjj.serenitepure.fr
- **Sender:** serenitepure.fr
- **Reply-To:** aichakandisha.com
- **Return-Path:** dturm.de
- **Feedback-ID:** e.serenitepure.fr

**Domain Mismatch Analysis:**
| Component | Domain | Legitimate? |
|-----------|--------|-------------|
| From | serenitepure.fr | Suspicious |
| Reply-To | aichakandisha.com | Suspicious |
| Return-Path | dturm.de | Suspicious |
| X-Sender | e.serenitepure.fr | Suspicious |

**Multiple Domain Usage:** Four different domains in one email = spam/phishing infrastructure

---

## Content Analysis

### Subject Analysis
- Uses fire emoji (🔥) to grab attention
- Dutch language: "Zonnepanelen voor een goede prijs"
- Translation: "Solar panels for a good price"
- Appeal to green energy interest + financial savings

### Targeting
- **Geographic:** Netherlands/Belgium (Dutch language)
- **Demographic:** Homeowners interested in renewable energy
- **Psychological:** Eco-conscious + cost-conscious consumers

### Spam Characteristics
- X-mid header present (marketing platform identifier)
- Feedback-ID header (tracking identifier)
- List-Unsubscribe-Post (bulk email infrastructure)
- In-Reply-To (part of ongoing spam campaign)

---

## Red Flags Checklist

- [x] **Suspicious sender domain** - serenitepure.fr unrelated to solar business
- [x] **Multiple domain mismatches** - Four different domains used
- [x] **SPF/DKIM/DMARC missing** - No email authentication
- [x] **Reply-to mismatch** - Different domain for replies
- [x] **Marketing platform indicators** - X-mid, Feedback-ID headers
- [x] **Emoji manipulation** - Fire emoji to create urgency/attraction
- [x] **Spam campaign** - In-Reply-To references previous spam

---

## Risk Assessment

**Risk Level:** **PHISHING / SPAM - MEDIUM**

**Primary Threats:**
1. **Lead Generation Scam:** Harvesting contact info for resale
2. **Advance Fee Fraud:** Requesting payment for non-existent solar installation
3. **Malicious Links:** Potential malware or credential harvesting

**Secondary Risk:** Privacy violation (email harvested for spam lists)

---

## Technical Indicators

### Header Analysis
```
From: "Zonnepanelen installateur" <zonnepaneel@appjj.serenitepure.fr>
Sender: "Zonnepanelen installateur" <zonnepaneel@appjj.serenitepure.fr>
Reply-To: "Zonnepanelen installateur" <news@aichakandisha.com>
Return-Path: return@dturm.de
X-mid: YmlnYnVnMUBob3RtYWlsLmZy...
X-Sender: <news@e.serenitepure.fr>
Feedback-ID: e.serenitepure.fr
Authentication-Results: spf=none; dkim=none; dmarc=none
```

### Infrastructure Analysis
- **Primary Domain:** serenitepure.fr (French domain)
- **Hosting:** OVHcloud (France) - 57.128.69.202
- **Platform:** Appears to be bulk email/marketing platform
- **Age:** Likely recently registered domains

---

## Prevention Guidance

### For Users
1. **Verify Installer:** Contact local solar companies directly, never through unsolicited emails
2. **Check Credentials:** Legitimate installers have local business registration
3. **Domain Check:** Real Dutch solar companies use .nl domains, not .fr
4. **Too Good To Be True:** Unsolicited cheap offers are usually scams

### For Organizations
1. **Language Filtering:** Block emails with mismatched language/geography
2. **Emoji Filtering:** Consider filtering emails with manipulation emojis in subject
3. **Bulk Email Detection:** Flag emails with Feedback-ID and List-Unsubscribe headers
4. **Geographic Filtering:** Block emails from suspicious foreign IPs

---

## Recommended Action

**DELETE & BLOCK**

This is a spam/phishing email using solar panel offers as bait.

- Do not reply
- Do not click links
- Block sender domain
- Report as spam

---

*Analysis completed by Dilnessa Aemro*
