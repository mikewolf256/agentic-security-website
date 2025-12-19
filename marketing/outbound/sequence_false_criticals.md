# Outbound Sequence: "False Criticals Cost Engineering Time"

**Target:** CTO / VP Engineering at B2B SaaS (10-200 employees)  
**Trigger Signals:** SOC2 page, security hiring, public APIs, recent funding  
**Goal:** Book 15-min triage call → 72-hour Critical Triage

---

## Email 1: The Problem

**Subject Lines (A/B test):**
- "Your scanner's 'critical' findings—are they real?"
- "60% of 'critical' vulns are false positives"
- "Is your team chasing security ghosts?"

**Body:**

```
Hi {{FIRST_NAME}},

Quick question: how much engineering time does {{COMPANY}} spend investigating scanner "critical" findings that turn out to be nothing?

For most teams, it's 40+ hours/month chasing false positives.

We just wrapped an engagement where a client's scanner flagged 4 "Critical" auth bypass vulnerabilities. After validation: 0 were real. The endpoints just returned the homepage for every request—scanner confused "200 OK" with "successful attack."

If your team is drowning in scanner noise, I'd love to share how we're helping companies like {{SIMILAR_COMPANY}} get clarity fast.

Worth a 15-minute chat?

{{SIGNATURE}}

P.S. We offer a 72-hour Critical Triage—send your top "criticals," we validate and tell you what's real. No commitment needed.
```

---

## Email 2: The Evidence (Day 3)

**Subject Lines:**
- "Re: Your scanner's 'critical' findings—are they real?"
- "4 Critical → 0 Confirmed (the case study)"

**Body:**

```
Hi {{FIRST_NAME}},

Following up on my last note about scanner false positives.

Here's what the validation process looks like in practice:

Scanner says: "Critical - NoSQL Injection Auth Bypass"
We test: 6 payload variants + control requests
Result: Endpoint returns identical response for everything → Not vulnerable

That's 8+ hours of engineering investigation avoided per false positive.

We recently published a quick case study on this: [link to validation-in-action]

If {{COMPANY}} is dealing with scanner noise, I can walk you through how we'd approach your specific stack.

15 minutes—interested?

{{SIGNATURE}}
```

---

## Email 3: The Offer (Day 7)

**Subject Lines:**
- "72 hours to clarity"
- "Let's validate your top 3 criticals"

**Body:**

```
Hi {{FIRST_NAME}},

Last note on this—

We're offering a 72-Hour Critical Triage for teams drowning in scanner output:

→ Send us your top 3-5 "critical" findings
→ We validate each one (multi-stage testing, response analysis)
→ You get clear verdicts: Confirmed or False Positive
→ Evidence attached for both

No long engagement, no big commitment. Just answers.

If your next board meeting or SOC2 audit needs clarity on what's actually vulnerable, this might help.

Reply with "interested" and I'll send details.

{{SIGNATURE}}
```

---

## LinkedIn Touch 1: Connection Request (Day 0)

**Note:**

```
Hi {{FIRST_NAME}}—saw {{COMPANY}} is growing fast. I work with B2B SaaS security teams on validating scanner findings (the "is this actually exploitable?" question). Would love to connect.
```

---

## LinkedIn Touch 2: Follow-Up (Day 4, if connected)

**Message:**

```
Thanks for connecting, {{FIRST_NAME}}.

Quick question—is {{COMPANY}} using any automated security scanners? Curious because most teams I talk to are spending 30-40% of their security cycles chasing false positives.

We've been helping companies validate their "critical" findings before engineering gets involved. Happy to share what we're seeing if useful.
```

---

## LinkedIn Touch 3: Value Drop (Day 10)

**Message:**

```
{{FIRST_NAME}}—thought you might find this interesting.

We just published a breakdown of why most React2Shell "critical" findings are false positives (and how to validate them): [link]

Relevant if {{COMPANY}} is on Next.js or any SSR React framework.
```

---

## Cadence Summary

| Day | Channel | Touch |
|-----|---------|-------|
| 0 | Email | Email 1: The Problem |
| 0 | LinkedIn | Connection Request |
| 3 | Email | Email 2: The Evidence |
| 4 | LinkedIn | Follow-up (if connected) |
| 7 | Email | Email 3: The Offer |
| 10 | LinkedIn | Value Drop |
| 14 | Email | Break-up email (optional) |

---

## Personalization Variables

| Variable | Source | Example |
|----------|--------|---------|
| `{{FIRST_NAME}}` | LinkedIn/company page | "Sarah" |
| `{{COMPANY}}` | Target list | "Acme SaaS" |
| `{{SIMILAR_COMPANY}}` | Similar company in their space | "companies like Stripe" |
| `{{SIGNATURE}}` | Your signature block | Name, title, email |

---

## Response Handling

**Positive response ("interested"):**
→ Send Calendly for 15-min triage call
→ Prep: Review their public attack surface before call

**Objection: "We have a scanner already":**
→ "Great—we validate scanner output. We're the layer that tells you what's real."

**Objection: "We just did a pentest":**
→ "When was it? Attack surfaces change. We can run a delta validation on new endpoints."

**Objection: "Too expensive":**
→ "What's the cost of 40 hours chasing false positives? Our triage starts at $2.5k."

**No response after Day 14:**
→ Add to nurture list, re-engage in 60 days with new content

