# Validation in Action (Case Study)

## Summary

Scanner output is not a vulnerability. This case study shows how a “critical” alert can be a false positive — and what “validated findings” actually means in practice.

**Headline result:** 4 scanner “Critical” auth-bypass findings → **0 confirmed vulnerabilities** after validation.

## What was flagged

The automated scan initially flagged:

- **NoSQL Injection Auth Bypass** — Critical (CVSS 9.1) (heuristic: “200 OK with homepage content instead of login form”)
- **LDAP Injection Auth Bypass (3 variants)** — Critical (CVSS 9.1) (heuristic: “200 OK with homepage content”)

## What validation did

Validation re-ran the candidate findings with:

- Multiple payload variants per class (NoSQL / LDAP)
- Control requests (normal payloads, empty body, GET/POST variations)
- Response comparison (status, size, key markers)
- Endpoint behavior checks (does this route actually process auth?)

## Outcome

- Root endpoint returned the same homepage response for **all** requests.
- Login endpoint returned a stable login page for all payloads.
- Several flagged API endpoints were not in scope or returned 404.

**Conclusion:** the “auth bypass” indicators were response-shape artifacts, not exploitability.

## Why this matters

Without validation, a report would include “4 critical vulnerabilities” that waste engineering time and erode trust.

With validation, the deliverable becomes:

> “4 candidates investigated. 0 confirmed vulnerabilities. Evidence attached.”

## What you should expect in our deliverables

- A clear label: **confirmed / unconfirmed / false positive**
- Evidence: request/response excerpts, reproduction notes
- “Why it’s not exploitable” explanation when we close out a candidate


