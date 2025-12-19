# Outbound Sequence: "React2Shell Validation Offer"

**Target:** CTO / VP Engineering at companies using React SSR (Next.js, Remix, Nuxt)  
**Trigger Signals:** Next.js/Remix in tech stack, recent React upgrade, SSR-related blog posts  
**Goal:** Book 15-min triage call → 72-hour Critical Triage

---

## Email 1: The Hook

**Subject Lines (A/B test):**
- "React2Shell: validate vs panic"
- "Your Next.js app flagged for React2Shell?"
- "Is React2Shell actually exploitable in your app?"

**Body:**

```
Hi {{FIRST_NAME}},

If you're running Next.js (or any React SSR framework), you've probably seen scanners flag "React2Shell" or "Prototype Pollution → RCE" as Critical.

Here's the thing: most of those findings are wrong.

React2Shell is real—but it requires a very specific chain: client-side prototype pollution + SSR + vulnerable render path + no mitigations. Miss one link, and it's not exploitable.

Scanners don't check for all four. They see "prototype pollution gadget" and scream Critical.

If {{COMPANY}} is dealing with React2Shell alerts, I can walk you through how to validate them in 15 minutes—or we can do it for you in 72 hours.

Worth a quick chat?

{{SIGNATURE}}

P.S. We just published a validation checklist for React2Shell: [link to blog post]. Might save your team some time.
```

---

## Email 2: The Checklist (Day 3)

**Subject Lines:**
- "Re: React2Shell: validate vs panic"
- "The React2Shell validation checklist"

**Body:**

```
Hi {{FIRST_NAME}},

Following up—here's the quick checklist we use to validate React2Shell findings:

1. Is there actually a prototype pollution gadget? (Can you demo Object.prototype.polluted = true?)
2. Is SSR in use? (Check for __NEXT_DATA__ or similar markers)
3. Can you reach a vulnerable render path? (Does SSR evaluate the polluted property?)
4. Are mitigations in place? (Object.freeze, sanitization, etc.)

If you can't check all four boxes, it's not exploitable.

Most scanner findings fail at step 1 or 2. The scanner sees "Next.js" and assumes SSR is processing attacker input—usually wrong.

If {{COMPANY}} wants us to run through this on your actual findings, happy to help.

{{SIGNATURE}}
```

---

## Email 3: The Offer (Day 7)

**Subject Lines:**
- "72-hour React2Shell verdict"
- "Validate your SSR stack in 72 hours"

**Body:**

```
Hi {{FIRST_NAME}},

Last note on React2Shell—

We're running 72-Hour Critical Triages for teams with SSR security concerns:

→ You send your scanner's "critical" findings (React2Shell, prototype pollution, etc.)
→ We validate each one against the full exploitation chain
→ You get clear verdicts: Confirmed (with PoC) or False Positive (with evidence)

No more guessing. No more engineering hours on ghosts.

If {{COMPANY}}'s next release or audit needs clarity on what's actually vulnerable, reply "interested" and I'll send details.

{{SIGNATURE}}
```

---

## LinkedIn Touch 1: Connection Request (Day 0)

**Note:**

```
Hi {{FIRST_NAME}}—noticed {{COMPANY}} is using Next.js. I've been helping teams validate React2Shell/prototype pollution findings (lots of scanner false positives lately). Would love to connect.
```

---

## LinkedIn Touch 2: Value Share (Day 5, if connected)

**Message:**

```
{{FIRST_NAME}}—quick heads up.

We just published a breakdown of React2Shell: what's real vs noise, plus a validation checklist for SSR apps.

Might be useful if {{COMPANY}}'s scanner is flagging prototype pollution issues: [link]

Happy to chat if you want to walk through any specific findings.
```

---

## Cadence Summary

| Day | Channel | Touch |
|-----|---------|-------|
| 0 | Email | Email 1: The Hook |
| 0 | LinkedIn | Connection Request |
| 3 | Email | Email 2: The Checklist |
| 5 | LinkedIn | Value Share (if connected) |
| 7 | Email | Email 3: The Offer |
| 10 | LinkedIn | Direct offer (if engaged) |

---

## Tech Stack Detection

**How to identify Next.js/SSR targets:**

1. **BuiltWith/Wappalyzer:** Filter for Next.js, Remix, Nuxt
2. **Job postings:** "React SSR," "Next.js developer"
3. **View source:** Look for `__NEXT_DATA__` script tag
4. **GitHub:** Public repos using Next.js
5. **Blog posts:** Company posts about SSR, React optimization

---

## Personalization Variables

| Variable | Source | Example |
|----------|--------|---------|
| `{{FIRST_NAME}}` | LinkedIn | "Alex" |
| `{{COMPANY}}` | Target list | "CloudApp" |
| `{{FRAMEWORK}}` | Tech detection | "Next.js" / "Remix" |
| `{{SIGNATURE}}` | Your signature | Name, title, email |

---

## Response Handling

**Positive response:**
→ Send Calendly for 15-min call
→ Before call: Check their public app for SSR markers

**"We're not using SSR":**
→ "Good to know! React2Shell isn't relevant then. Are you dealing with other scanner noise we could help with?"

**"We already validated it internally":**
→ "Great! What did you find? Happy to share what we're seeing across other Next.js apps if useful."

**"Our scanner vendor says it's real":**
→ "Scanner vendors have incentives to flag. We have incentives to validate. Want a second opinion?"

---

## Content to Reference

- Blog: `react2shell_validation.md`
- Exec brief: `client_side_critical_findings.md`
- Case study: `validation-in-action.html`

