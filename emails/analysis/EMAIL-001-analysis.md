# Email Analysis: EMAIL-001 - Bank Phishing (Banco do Bradesco)

---

## Basic Information
- **Sample ID:** EMAIL-001
- **Classification:** PHISHING
- **Date Analyzed:** March 2026
- **Source:** rf-peixoto/phishing_pot GitHub Repository

---

## Email Details

**Subject:** CLIENTE PRIME - BRADESCO LIVELO: Seu cartão tem 92.990 pontos LIVELO expirando hoje!

**From (Display):** BANCO DO BRADESCO LIVELO <banco.bradesco@atendimento.com.br>

**From (Actual SMTP):** root@ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06

**Return-Path:** root@ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06

**To:** phishing@pot

**Date:** Tue, 19 Sep 2023 18:35:49 +0000

**Sender IP:** 137.184.34.4 (DigitalOcean, United States)

---

## Authentication Results

| Check | Result | Analysis |
|-------|--------|----------|
| **SPF** | temperror | SPF lookup failed - DNS timeout |
| **DKIM** | none | Message not digitally signed |
| **DMARC** | temperror | DMARC policy check failed |
| **Composite Auth** | fail | Failed authentication checks |

---

## Sender Analysis

**Claimed Identity:** Banco do Bradesco (Brazilian Bank)

**Actual Sending Domain:** ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06 (DigitalOcean VPS)

**Domain Mismatch:**
- Displayed: atendimento.com.br
- Actual: ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06
- Mail From: ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06

**Server Location:** San Francisco, US (DigitalOcean datacenter)

**Legitimacy:** The email claims to be from a Brazilian bank but originates from a US-based cloud VPS with no relation to the actual bank.

---

## Content Analysis

### Visual Deception
- Uses Banco do Bradesco branding and color scheme (red #FF0080)
- Mentions "Pontos Livelo" (legitimate Brazilian rewards program)
- Professional HTML formatting mimicking real bank communications

### Urgency Tactics
- "expirando HOJE" (expiring TODAY)
- Creates fear of losing rewards points
- Time-sensitive call to action

### Call to Action
**Malicious Link:** https://blog1seguimentmydomaine2bra.me/

**Red Flags:**
- Domain name is obfuscated and suspicious
- Uses URL shortening/obfuscation technique
- Domain registered recently (me TLD is commonly abused)
- No HTTPS security indicators mentioned

### Social Engineering Elements
1. **Reward Exploitation:** Promises 92,990 points (high value to attract clicks)
2. **Discount Incentive:** Claims 35% discount on credit card bill
3. **Brand Impersonation:** Uses legitimate bank name and loyalty program

---

## Red Flags Checklist

- [x] **Suspicious sender domain** - Email originates from VPS, not bank domain
- [x] **SPF/DKIM/DMARC failures** - Authentication completely failed
- [x] **Urgency language** - "expirando hoje" (expiring today)
- [x] **Suspicious links** - Obfuscated domain not related to Bradesco
- [x] **Sender spoofing** - Claims bank identity but sent from unrelated server
- [x] **Reward-based manipulation** - Unrealistic points offer

---

## Risk Assessment

**Risk Level:** **PHISHING - HIGH**

**Primary Threat:** Credential harvesting and potential financial fraud

**Target Victims:** Brazilian banking customers, specifically Banco do Bradesco clients

**Attack Vector:** 
1. User clicks malicious link
2. Directed to fake login page
3. Credentials stolen
4. Bank account compromised

---

## Technical Indicators

### Email Headers Excerpt
```
Received: from ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06 (137.184.34.4)
Authentication-Results: spf=temperror
  smtp.mailfrom=ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06
  dkim=none (message not signed)
  dmarc=temperror
Return-Path: root@ubuntu-s-1vcpu-1gb-35gb-intel-sfo3-06
From: BANCO DO BRADESCO LIVELO<banco.bradesco@atendimento.com.br>
```

### IP Analysis
- **IP Address:** 137.184.34.4
- **ISP:** DigitalOcean, LLC
- **Type:** Cloud VPS (easily rented by attackers)
- **Country:** United States
- **Reputation:** High-risk (VPS commonly used for phishing)

---

## Prevention Guidance

### For Users
1. **Verify Sender:** Banks never send reward notifications from personal VPS servers
2. **Check Links:** Hover to see actual URL before clicking
3. **Access Directly:** Log into bank account directly via official website, never through email links
4. **Enable Alerts:** Use bank's official mobile app for notifications

### For Organizations
1. **Implement DMARC:** Enforce strict DMARC policies to block spoofed emails
2. **User Training:** Educate customers about reward point scams
3. **Brand Protection:** Monitor for domain registrations similar to official domains
4. **Report Abuse:** Forward phishing attempts to abuse@digitalocean.com

---

## Recommended Action

**DELETE & REPORT**

This email is a confirmed phishing attempt targeting Brazilian banking customers. Do not click any links. Report to:
- Your bank's fraud department
- Local cybercrime authorities
- Email provider as phishing

---

*Analysis completed by Dilnessa Aemro*
