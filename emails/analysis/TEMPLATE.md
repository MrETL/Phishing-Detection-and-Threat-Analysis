# Email Analysis Template

## Sample #: [TYPE - e.g., Bank Phishing]

---

### Basic Information
- **Sample ID:** EMAIL-001
- **Classification:** PHISHING / SUSPICIOUS / SAFE
- **Date Analyzed:** [YYYY-MM-DD]
- **Source:** [GitHub repo / Public dataset]

### Email Headers

**From (Display):** [What user sees]
**From (Actual):** [Real sender address from headers]
**Reply-To:** [If different from sender]
**Subject:** [Subject line]
**Date:** [Timestamp]
**To:** [Recipient]

### Authentication Results

| Check | Result | Notes |
|-------|--------|-------|
| SPF | PASS / FAIL / NONE | |
| DKIM | VALID / INVALID / MISSING | |
| DMARC | PASS / FAIL / NO POLICY | |

### Sender Analysis

**Claimed Domain:** [e.g., bankofamerica.com]
**Actual Domain:** [e.g., bankofamerica-security.com]
**Domain Age:** [Check via WHOIS]
**Domain Similarity:** [Legitimate or lookalike?]

### URL/Link Analysis

| Link Text | Actual URL | Destination | Risk |
|-----------|------------|-------------|------|
| "Verify Account" | http://... | [IP/Domain] | HIGH |

### Content Analysis

**Greeting:** [Generic or personalized?]
**Tone:** [Urgent, threatening, friendly?]
**Grammar/Spelling:** [Errors present?]
**Requested Action:** [Click link, download, reply?]
**Threats Mentioned:** [Account lock, legal action?]

### Red Flags Checklist

- [ ] Suspicious sender domain
- [ ] Failed/missing SPF, DKIM, or DMARC
- [ ] Urgency language used
- [ ] Generic greeting (Dear Customer, Dear User)
- [ ] Suspicious/misleading links
- [ ] Spelling or grammar errors
- [ ] Requests sensitive information
- [ ] Threatening consequences
- [ ] Unexpected attachment
- [ ] Too-good-to-be-true offer

### Screenshots

- [ ] Header analysis screenshot
- [ ] Link hover screenshot
- [ ] Domain lookup screenshot

### Final Assessment

**Risk Level:** PHISHING / SUSPICIOUS / SAFE

**Primary Threat:** [Credential theft / Malware / Fraud / etc.]

**Recommended Action:** 
- DELETE / REPORT / VERIFY / SAFE

**Notes:**
[Additional observations]

---
