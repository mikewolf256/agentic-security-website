# Sample Validation Report (Example)

This is an example structure of what “validated” looks like — concise, reproducible, and evidence-first.

## Finding

- **Title:** Potential Authentication Bypass via Injection Payloads
- **Status:** Not confirmed (false positive)
- **Confidence:** High
- **Impact:** None (candidate disproven)

## Evidence (high level)

- Control request and candidate payloads returned identical content markers
- Response size and status code were consistent across payload and control requests
- Endpoint behavior indicates it does not perform authentication logic

## Reproduction steps (example)

1. Send baseline request
2. Send candidate payload request
3. Compare markers and response body

## What we deliver

- A short “why it’s real” *or* “why it’s not” paragraph
- Request/response snippets (redacted if needed)
- Concrete remediation steps for confirmed findings


