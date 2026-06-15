# First-purchase buyer journey QA — Approval Gates Starter Kit

Date: 2026-06-09  
Owner lens: Feyre / Rhysand  
Status: local Product Forge sprint artefact; no listing, checkout, publication, analytics, email capture, or payment activation

## Decision re-ground

Current Product Forge ordering remains:

1. **Sell first:** `AI Agent Approval Gates Starter Kit v0.2`.
2. **Second product / bundle leg:** `AI OS Rung Zero Kit v0.2`.
3. **Do not package yet:** `AI Autonomy Starter Bundle`.

Reason: the Starter Kit is the only product with the right combination of buyer urgency, low-support delivery, low-liability promise, existing package/hash, public preview, seller handoffs, checkout acceptance test, and manual-fulfilment fallback. AI OS Rung Zero is useful, but still invites setup questions. The bundle should wait until the first product has a verified checkout route or first-sale evidence.

## First-purchase path being tested

A stranger should be able to understand this path without Mark or Rhysand on a call:

1. They see the problem: agents can quietly cross money, publishing, customer, credential, deletion, or commitment lines.
2. They preview the free checklist.
3. They understand the paid pack: matrix, autonomy policy, task card, risk register, first-week playbook, and printable checklist.
4. They see the support boundary: digital templates only; no implementation, legal/compliance/security/tax/financial/trading advice, custom setup, or guaranteed outcome.
5. When Mark provides a verified checkout URL, Rhysand patches exactly one buy link and runs the checkout acceptance script before any public-preview update.

## Buyer-facing QA verdict

| Surface | Current state | Verdict | Next safe move |
|---|---|---|---|
| Product comparison | `PRODUCT_COMPARISON.md` chooses Starter Kit first and defers AIOS/bundle. | Pass | Do not create another product before seller route is live. |
| Public preview / sales page | Preview contains free checklist, FAQ, agent-readable fit/non-fit, disabled checkout, noindex. | Pass | Patch only after verified Stripe/Polar URL. |
| Listing handoffs | Stripe/Polar, checkout preflight, manual first-10-sales fulfilment, and acceptance test exist. | Pass | Mark-side seller setup remains the bottleneck. |
| Package | v0.2 zip/hash/manifest exist. | Pass with caution | Recheck hash on listing day; avoid unnecessary v0.3 hash churn before checkout. |
| Buyer support expectation | Support boundary exists but must be repeated in seller checkout copy. | Needs exact reuse | Use the copy block below. |
| Bundle | Commercially coherent but premature. | Defer | Revisit only after checkout route or sale evidence. |

## Exact seller-checkout copy block

Use this wording if Mark creates or verifies a Stripe/Polar checkout page.

**Product name**

`AI Agent Approval Gates Starter Kit`

**Short checkout description**

`A self-serve template pack for setting safe approval boundaries around AI-agent work: money, publishing, messaging, credentials, customer data, deletion, production changes, and high-liability commitments.`

**What is included**

- AI Agent Approval Gate Checklist.
- Agent Permission Matrix.
- Founder AI Autonomy Policy.
- Agent Task Card Template.
- Risk Register Template.
- First 7 Days of Agent Delegation playbook.
- Printable PDF checklist.
- Start-here, changelog, and licence/use notes.

**Support / delivery boundary**

`Digital download only. Includes self-serve templates and quickstart docs. Does not include custom implementation, account setup, legal/compliance review, cybersecurity certification, financial/tax/trading advice, or agent deployment.`

**Disclaimer**

`Operational templates only. Not legal, financial, tax, cybersecurity, compliance, investment, employment, or trading advice. No revenue, safety, compliance, or agent-performance guarantee.`

## Patch acceptance rules after Mark provides a checkout URL

Before Rhysand patches the public preview:

- Mark has personally completed password, 2FA, KYC, banking, tax, terms, live-payment activation, and any seller-side secret/API-key handling.
- The route is IronFrame-controlled and not Mark Hale personal Google/payment identity unless explicitly approved.
- The payment URL is a verified Stripe/Polar URL for the exact product and price Mark approved.
- Package hash is rechecked on the same day.
- Fulfilment path is explicit: platform download, success-page download, or manual first-10-sales fulfilment.

After patching:

```bash
cd /Users/edi/IronFrame
python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --expected-payment-url 'PASTE_VERIFIED_STRIPE_OR_POLAR_URL_HERE'
```

Pass condition:

- exact payment URL appears exactly once;
- no other payment-like URL appears;
- no scripts/forms/analytics/email-capture have been introduced;
- `noindex,nofollow` remains unless Mark separately approves public launch state.

## Explicit non-actions this sprint

No product listing was created. No checkout/payment URL was activated. No public launch, email capture, analytics, affiliate link, ad, outreach, paid tool, account creation, seller-platform change, private-detail release, or package hash change was made.

## Next recommended Product Forge action

If no verified checkout URL exists next run, do **not** build the bundle. Run one of these safe local actions instead:

1. Recheck the disabled-checkout public-preview acceptance script and package hash.
2. Create a one-page `START_HERE` v0.3 draft only if it materially improves the buyer’s first 10 minutes without requiring a package rebuild yet.
3. Prepare a minimal fulfilment email template that points to the package after a verified purchase route exists, without sending it.
