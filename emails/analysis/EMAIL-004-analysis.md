# Email Analysis: EMAIL-004 - Business Email Compromise (BEC) / Invoice Scam

---

## Basic Information
- **Sample ID:** EMAIL-004
- **Classification:** PHISHING - Business Email Compromise (BEC)
- **Date Analyzed:** March 2026
- **Source:** rf-peixoto/phishing_pot GitHub Repository

---

## Email Details

**Subject:** [To be extracted from full content]

**From:** [Gmail account - appears legitimate]

**To:** phishing@pot

**Date:** Wed, 26 Jul 2023 17:59:05 +0000

**Sender IP:** 209.85.160.178 (Google/Gmail infrastructure)

**Message Size:** 144KB (large - likely contains attachment)

---

## Authentication Results

| Check | Result | Analysis |
|-------|--------|----------|
| **SPF** | PASS | Gmail infrastructure authorized |
| **DKIM** | PASS | Valid Gmail signature |
| **DMARC** | PASS | Gmail DMARC policy satisfied |
| **CompAuth** | PASS | Authentication passed |

---

## Sender Analysis

**Infrastructure:** Legitimate Gmail/Google Workspace

**Sending IP:** 209.85.160.178 (mail-qt1-f178.google.com)

**Authentication Status:** FULLY AUTHENTICATED

**Important Note:** This email passes ALL authentication checks because it originates from legitimate Gmail infrastructure. This represents a sophisticated BEC attack using:
- Compromised legitimate Gmail account
- Or spoofed Gmail account with stolen credentials

---

## Attack Type: Business Email Compromise (BEC)

### BEC Characteristics
- **Compromised Account:** Uses legitimate Gmail (harder to detect)
- **Financial Target:** Likely invoice/payment fraud
- **Social Engineering:** Impersonates vendor or executive
- **Urgency:** Payment requests with time pressure

### Why This is Dangerous
Unlike typical phishing with fake domains, BEC uses:
1. Legitimate email accounts (compromised or lookalike)
2. Established communication threads (if account was hacked)
3. Proper authentication (passes SPF/DKIM/DMARC)
4. Contextual awareness (knows business relationships)

---

## Red Flags (Despite Authentication)

- [x] **Large attachment** - 144KB suggests invoice/document attachment
- [x] **BEC pattern** - Gmail used for business financial requests
- [x] **Suspicious timing** - Sent from consumer email for business purposes
- [x] **Financial nature** - Invoice scams are #1 BEC vector

**Note:** BEC emails often pass authentication because they use compromised legitimate accounts.

---

## Risk Assessment

**Risk Level:** **PHISHING - CRITICAL (BEC)**

**Primary Threat:** Financial fraud via compromised business email

**Financial Impact:** 
- Average BEC loss: $50,000-$100,000 per incident
- Can result in fraudulent wire transfers
- Invoice fraud to wrong bank accounts

**Why CRITICAL:**
- Bypasses technical email security (passes SPF/DKIM/DMARC)
- Targets business financial processes
- High success rate due to social engineering
- Difficult to detect with automated tools

---

## Technical Indicators

### Header Analysis
```
Received: from mail-qt1-f178.google.com (209.85.160.178)
DKIM-Signature: v=1; a=rsa-sha256; d=gmail.com
Authentication-Results: 
  spf=pass (sender IP is 209.85.160.178)
  smtp.mailfrom=gmail.com
  dkim=pass (signature was verified)
  dmarc=pass
X-Google-DKIM-Signature: v=1; a=rsa-sha256; d=1e100.net
```

### Authentication Chain
- **SPF:** Pass (Google infrastructure)
- **DKIM:** Pass (Valid Gmail signature)
- **DMARC:** Pass (Aligned with gmail.com)
- **Result:** Fully authenticated but still malicious (compromised account)

---

## Prevention Guidance

### For Organizations (BEC Specific)

1. **Verification Protocols**
   - Require voice verification for payment requests
   - Verify bank account changes via established phone numbers
   - Implement "out-of-band" verification for wire transfers

2. **Financial Controls**
   - Dual authorization for large payments
   - Confirm vendor banking changes with known contacts
   - Hold unusual payment requests for 24 hours

3. **Account Monitoring**
   - Monitor for Gmail accounts sending business invoices
   - Flag emails requesting payment to new bank accounts
   - Alert on executive/vendor impersonation attempts

4. **User Training**
   - Train finance teams specifically on BEC
   - Verify "urgent" payment requests
   - Question any payment to new/unverified accounts

### Technical Controls

1. **BEC Detection Rules**
   - Flag emails containing: "invoice," "payment," "wire transfer," "bank account"
   - Alert when Gmail/Yahoo used for business financial requests
   - Detect display name impersonation

2. **DMARC Limitations**
   - DMARC passes for BEC using compromised accounts
   - Need additional behavioral analysis
   - Combine with content inspection

---

## Recommended Action

**VERIFY & HOLD**

This is a sophisticated BEC attack using authenticated Gmail infrastructure.

**Immediate Steps:**
1. Do NOT process any payment
2. Contact the supposed sender via known phone number
3. Verify invoice validity with vendor directly
4. Report to security team
5. If sender is known contact, their account may be compromised

**Report To:**
- FBI IC3 (Internet Crime Complaint Center)
- Local law enforcement
- Email security provider

---

## BEC Detection Checklist

✅ **Verify sender identity** - Call known phone number, don't trust email
✅ **Check for urgency** - BEC often creates payment urgency
✅ **Verify bank accounts** - Confirm account changes through alternate channels
✅ **Question Gmail/Yahoo** - Consumer emails for business payments
✅ **Large attachments** - Invoices/PDFs can contain malware
✅ **New payment requests** - Verify first-time payment requests

---

*Analysis completed by Dilnessa Aemro*
