# Buyer-Panel Copy Tournament — Approval Gates Starter Kit

Date: 2026-06-13  
Owner: Rhysand / Feyre / Gwyn  
Status: local product-page/listing proof; no public patch, checkout change, outreach, account action, analytics, or payment action executed

## Source signal

Greg Isenberg's `You are using Claude Fable 5 wrong` transcript at `briefs/x_ai_automation/transcripts/20260613_080020/vjdHAWvVCP4.txt` adds one buyer-facing mechanism worth adopting locally:

> Generate multiple copy variants, have distinct buyer/skeptic personas score and object to them, kill weak versions, then merge the strongest objections and promises into one safer final page.

This is not a reason to use paid model credits, hosted agents, Figma MCP, private customer data, or public claims. For IronFrame it becomes a no-spend **buyer-panel copy tournament** for the existing Starter Kit sales/listing surface.

## Product under review

- Product: AI Agent Approval Gates Starter Kit v0.2.
- Current commercial state: first product remains checkout target; checkout is disabled until a verified Stripe/Polar URL is available.
- Current source page: `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html`.
- Current approved promise: help operators let agents work without uncontrolled spending, publishing, deletion, private-data exposure, or commitments.
- Support boundary: digital templates only; no custom implementation, account setup, live AIOS build, legal/compliance/cybersecurity certification, financial/tax/trading advice, or agent deployment.

## Judges for the tournament

Use these judges before any public CTA/listing copy patch:

1. **Time-poor founder** — wants to know whether this saves setup time this week.
2. **Skeptical operator/CFO** — wants clear price, no inflated ROI, and no hidden support obligation.
3. **AI consultant/adopter** — wants client-ready boundaries without pretending the pack is legal/security advice.
4. **Risk owner** — looks for private-data, publishing, spend, deletion, and account-access safeguards.
5. **Buyer-agent / procurement bot** — needs fit, non-fit, deliverables, price hypothesis, support boundary, refund/disclaimer language, and receipt/fulfilment clarity in structured text.

## Candidate copy variants

### Variant A — Control / permission boundary

**Hook:** `Let agents work without letting them spend, publish, delete, or expose private data.`

- Fit: teams already testing agents in real workflows.
- Strongest promise: practical approval gates and risk registers.
- Weakness: may sound internal-process-heavy rather than purchase-ready.
- Verdict: keep as the core promise.

### Variant B — First 10 minutes / operator utility

**Hook:** `In ten minutes, map what your agent can do, what it must ask for, and what it must never touch.`

- Fit: solo founders/operators with little time.
- Strongest promise: fast self-serve utility without live setup.
- Weakness: must not imply complete compliance or custom implementation.
- Verdict: strong listing-page subhead candidate.

### Variant C — AI-consultant client pack

**Hook:** `A client-safe approval-gate pack for consultants before agent automations go live.`

- Fit: AI consultants and agency operators.
- Strongest promise: client-facing structure and reduced scope creep.
- Weakness: can accidentally imply professional compliance review or consultancy deliverable guarantee.
- Verdict: use as a secondary use case, not the main headline.

### Variant D — Buyer-agent structured surface

**Hook:** `A static, agent-readable operating pack: permissions, examples, risks, receipts, and escalation rules in one download.`

- Fit: procurement/buyer agents and technical evaluators.
- Strongest promise: structured evaluation surface.
- Weakness: too abstract for human cold visitors if used alone.
- Verdict: keep in the agent-readable section, not hero copy.

## Qualitative scoreboard

| Judge | A: permission boundary | B: first 10 minutes | C: consultant pack | D: buyer-agent surface |
|---|---|---|---|---|
| Time-poor founder | Pass, but slightly dry | Strong pass | Hold | Hold |
| Skeptical operator/CFO | Strong pass | Pass if no guarantee language | Hold for support-risk | Pass for clarity |
| AI consultant/adopter | Pass | Pass | Strong pass with caveat | Pass |
| Risk owner | Strong pass | Pass | Hold unless disclaimers are visible | Strong pass |
| Buyer-agent / procurement bot | Pass | Pass | Hold | Strong pass |

## Winner and merged safe copy

Winner: **Variant B as the next human-facing subhead**, anchored by Variant A's permission boundary and Variant D's structured buyer surface.

Safe merged copy candidate:

> `In ten minutes, map what your agent can do, what it must ask for, and what it must never touch — before you give it spend, publish, deletion, or private-data access.`

Use this only as a candidate for a future local/public page patch after the existing disabled-checkout verifier passes. It does not change the v0.2 package/hash and does not open checkout.

## Objections to answer before public patching

- `Is this legal/security advice?` — No. It is an operator template pack, not professional legal/compliance/cybersecurity advice.
- `Does it deploy or configure agents for me?` — No. Digital download/templates only.
- `Does it guarantee safer AI or revenue?` — No guarantees; it provides a practical control surface.
- `Can I buy it now?` — Not until an IronFrame-controlled Stripe/Polar checkout URL is verified; current page must remain checkout-disabled.
- `What do I receive?` — v0.2 zip with 11 manifest-listed files; fulfilment is manual/controlled until seller route is verified.

## Patch recommendation

When a public/local copy patch is next appropriate, update only one low-risk line first:

1. Add the merged safe copy candidate as a subhead or listing sentence.
2. Keep checkout disabled unless a verified Stripe/Polar URL exists.
3. Run:

```bash
python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --allow-no-checkout
```

4. If a verified payment URL exists later, run the same script with `--expected-payment-url` and patch exactly one CTA.

## Approval gates / non-actions

No public patch, payment link, seller-platform action, buyer email, analytics/email capture, account creation, paid model/tool credits, outreach, public income/security/legal claim, customer/private data, Mark personal Google use, or external publication was executed in this tournament.

APPROVAL REQUIRED: verified IronFrame-controlled Stripe/Polar checkout URL plus Mark-side seller setup | payment, tax, banking, identity, terms, fulfilment, and live-payment boundary | Mark completes/verifies seller setup and provides the non-secret checkout URL before Rhysand patches the public CTA or fulfils paid orders.
