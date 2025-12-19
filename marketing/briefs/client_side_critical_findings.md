# Executive Brief: Handling Client-Side "Critical" Findings

**Audience:** CTO, VP Engineering, Security Leadership  
**Reading Time:** 3 minutes

---

## The Problem

Your security scanner just flagged 12 "Critical" vulnerabilities. Your team is panicking. The board presentation is next week.

**Before you mobilize engineering, read this.**

Most client-side "critical" findings from automated scanners are **false positives**. Scanners use heuristics that detect *potential* issues, not *exploitable* vulnerabilities.

---

## The Decision Framework

### Step 1: Categorize the Finding

| Category | Examples | Typical FP Rate |
|----------|----------|-----------------|
| Client-Side Injection | XSS, Prototype Pollution, DOM-based attacks | 40-60% |
| Auth/Session Issues | JWT problems, session fixation | 50-70% |
| Configuration | Missing headers, CORS, CSP | 30-50% |
| Business Logic | IDOR, access control | 20-40% |

**Rule of thumb:** The more the scanner relies on response heuristics (vs. actual exploitation), the higher the false positive rate.

### Step 2: Ask Three Questions

1. **Can we reproduce it?** — Not "does the scanner say so," but can a human demonstrate the attack?

2. **What's the actual impact?** — "XSS in admin panel" ≠ "XSS on public 404 page"

3. **What's the exploitation path?** — Does the attack require auth? Social engineering? Unlikely conditions?

### Step 3: Validate Before Remediating

**Do not** assign engineering resources based on scanner severity alone.

**Do** validate critical findings before prioritizing remediation.

---

## Real-World Example

**Scanner Output:**
> 4 Critical: NoSQL/LDAP Injection Auth Bypass (CVSS 9.1)

**After Validation:**
> 0 Confirmed. All endpoints return homepage for any request. Scanner confused "200 OK" with "successful auth bypass."

**Engineering Hours Saved:** 40+

---

## When to Escalate Immediately

Some findings warrant immediate action:

- ✅ RCE/Command Injection with PoC
- ✅ SQL Injection with data extraction proof
- ✅ Auth bypass on production endpoints
- ✅ Exposed secrets/credentials
- ✅ Active exploitation indicators

**Key differentiator:** These have *proof*, not just scanner alerts.

---

## When to Validate First

Most "critical" findings should be validated before engineering sprint allocation:

- ⏸️ Client-side attacks (XSS, Prototype Pollution)
- ⏸️ Configuration issues (headers, CORS)
- ⏸️ Session/auth findings without PoC
- ⏸️ Anything where scanner says "potentially vulnerable"

---

## The Cost of False Positives

| Metric | Impact |
|--------|--------|
| Engineering hours per false positive | 4-8 hours |
| Typical false positive rate | 60-80% |
| Monthly cost (10 "criticals"/month) | 24-64 wasted hours |
| Annual cost | 288-768 hours (~$30k-$80k) |

**Plus:** Eroded trust, delayed features, security fatigue.

---

## Our Recommendation

1. **Don't panic** — Scanner severity ≠ actual risk
2. **Validate first** — 72-hour triage before sprint allocation
3. **Demand evidence** — No PoC = no priority
4. **Track validation rate** — Measure scanner accuracy over time

---

## Get Clarity in 72 Hours

We offer a **72-Hour Critical Triage**:

- Submit your scanner's "critical" findings
- We validate each one (control testing, payload variation, response analysis)
- You get clear verdicts: **Confirmed** or **False Positive**
- Evidence attached for both

**Result:** Engineering focuses on real issues. You present facts, not scanner noise.

[Request Critical Triage →](mailto:hello@agenticsec.team?subject=72-Hour%20Critical%20Triage)

---

*Agentic Security Partners — AI-Powered Discovery. Human-Verified Findings.*

