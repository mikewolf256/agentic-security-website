# Dashboard Demo Script

**Duration:** 3-5 minutes  
**Audience:** CTO/VP Eng evaluating validation service  
**Goal:** Show the candidate → confirmed workflow and evidence quality

---

## Pre-Demo Setup

- [ ] Dashboard loaded with sample engagement data
- [ ] At least 2 confirmed findings with evidence
- [ ] At least 3 false positives with explanations
- [ ] Executive summary populated
- [ ] Screen recording ready (1080p, clean desktop)

---

## Script

### Opening (15 seconds)

> "Let me show you what a validated security assessment looks like in practice. This is our dashboard—where you see exactly what we find, how we validate it, and what's actually real."

### Executive Summary (30 seconds)

*Navigate to Executive Summary view*

> "First, the executive summary. This is what you'd share with leadership or auditors.
>
> You can see: [X] findings submitted as candidates, [Y] confirmed as real vulnerabilities, and [Z] closed as false positives.
>
> That [Z/X]% false positive rate? That's engineering time you're not wasting. Most scanners would have reported all [X] as 'critical'—we validated them first."

### Candidate vs Confirmed Workflow (45 seconds)

*Navigate to Findings list*

> "Here's the core workflow. Every finding starts as a 'candidate'—something our automated discovery flagged as potentially interesting.
>
> *Click on a candidate*
>
> Before it reaches your team, we validate it. We test with multiple payloads, compare against control requests, and determine: is this actually exploitable?
>
> *Show status changing from Candidate → Confirmed or False Positive*
>
> Only confirmed findings make it to your report. False positives get closed with evidence explaining why they're not exploitable."

### Confirmed Finding Deep-Dive (60 seconds)

*Open a confirmed finding*

> "Let's look at a confirmed finding. This is [vulnerability type] on [endpoint].
>
> *Scroll through finding*
>
> You see the severity—this is [Critical/High/Medium] based on actual exploitability, not scanner heuristics.
>
> Here's the evidence: the actual HTTP request we sent, the response we got, and exactly how to reproduce it.
>
> *Highlight request/response*
>
> Your developers can copy this curl command and verify in 30 seconds. No ambiguity about whether it's real.
>
> *Scroll to remediation*
>
> And here's the fix—specific to your stack, not generic boilerplate."

### False Positive Example (45 seconds)

*Open a false positive finding*

> "Now let's look at what we *didn't* report. This was flagged by our scanner as [vulnerability type].
>
> *Show false positive evidence*
>
> But when we validated it—see here—the endpoint returns the same response for normal requests and attack payloads. It's not processing our input at all.
>
> Scanner saw a 200 OK and assumed success. We tested it and proved otherwise.
>
> *Highlight the 'Why Not Exploitable' section*
>
> This is the evidence. Your team doesn't need to investigate this. It's closed."

### Export and Reporting (30 seconds)

*Navigate to export options*

> "When you're ready, export as PDF for stakeholders, JSON for your ticketing system, or Markdown for docs.
>
> *Show PDF preview*
>
> The PDF includes the executive summary, all confirmed findings with evidence, and an attestation letter—signed by the engineer who validated your assessment."

### Closing (15 seconds)

> "That's the dashboard. Candidates go in, validated findings come out. Your team focuses on what's real—not chasing scanner noise.
>
> Ready to see what's actually vulnerable in your app? Let's set up a 72-hour triage."

---

## Key Points to Hit

1. **Candidate → Confirmed workflow** — The core value proposition
2. **False positive rate** — Quantify the noise reduction
3. **Evidence quality** — Request/response, reproduction steps
4. **Developer-ready** — Curl commands, copy-paste reproduction
5. **Exec-ready** — PDF export, attestation letter

---

## B-Roll Shots Needed

- Executive summary dashboard view
- Finding list with status filters
- Individual finding with evidence expanded
- False positive with "Why Not Exploitable" section
- PDF export preview
- JSON export (for DevOps buyers)

---

## Recording Notes

- Use consistent mouse movement (slow, deliberate)
- Pause on key evidence sections
- Highlight text when reading important parts
- Keep dashboard data realistic but anonymized
- Avoid showing any real client data

---

## Call-to-Action Overlay

End screen should include:
- "Get a 72-Hour Critical Triage"
- Email: hello@agenticsec.team
- Website: agenticsecurity.com

