# Stripe-first checkout preflight — AI Agent Approval Gates Starter Kit

Date: 2026-06-05  
Owner: Feyre / Rhysand  
Product: AI Agent Approval Gates Starter Kit v0.2  
Proposed first price: £9 GBP one-time digital download  
Status: ready for Mark-side Stripe account/Managed Payments preflight; no live payment link created

## Recommendation

Use **Stripe Managed Payments + Payment Links** first if Mark's Stripe Dashboard exposes Managed Payments and Mark can complete Stripe activation, KYC/business verification, bank payout setup, and Managed Payments terms.

Why this is now the preferred route:

- Mark has selected Stripe as the likely cash app/payment route.
- Stripe has the highest buyer trust and the best long-term commerce infrastructure.
- Stripe docs describe Managed Payments as a merchant-of-record solution for digital products, including software and digital content/downloads.
- Managed Payments can reduce the immediate VAT/GST/sales-tax, fraud, dispute, and transaction-support burden that made plain Stripe less attractive for a £9 digital download.
- Payment Links can give us a no-code first-cash route once Mark completes gated account setup.

If Managed Payments is unavailable or not eligible, use **Polar** as the first fallback. Use standard Stripe Payment Links/Checkout only if Mark explicitly accepts seller-managed tax/compliance and fulfilment.

## Immediate route order

### 1. Stripe Managed Payments + Payment Links — preferred

Best fit when:

- Stripe account is IronFrame/Mark-controlled;
- Managed Payments is available in the Dashboard;
- product category is eligible as a digital/software/template product;
- Mark completes KYC, bank, tax/liability, and terms steps personally;
- we have a simple post-payment fulfilment path.

Catches:

- Mark must complete all identity, banking, tax, ToS, and live activation steps.
- First Stripe payout may not be immediate; Stripe docs describe initial payout timing as often 7–14 days after the first successful payment depending on country/industry/risk.
- Managed Payments handles transaction-side obligations; product fulfilment/download still needs a configured redirect, manual fulfilment, or later webhook automation.

### 2. Polar — fallback MoR

Best fit if Stripe Managed Payments is unavailable/blocked.

Reasons:

- Merchant-of-record posture.
- Strong developer/digital-product fit.
- File downloads and automated benefits are natively aligned with template packs.
- Better first-cash fit than building fulfilment/tax stack ourselves.

### 3. Standard Stripe Payment Links / Checkout — explicit-choice fallback

Use only if Mark deliberately chooses speed and Stripe buyer trust while accepting:

- seller-managed tax/compliance;
- custom/manual fulfilment;
- refund/support process ownership;
- later automation work for delivery/webhooks.

## Mark-side gated actions

These remain Mark-side and must not be handled by Hermes/agents:

1. Stripe sign-in/account creation.
2. Password, 2FA, recovery, and account security.
3. Business verification/KYC/legal identity.
4. Banking and payout setup.
5. Tax/liability choice.
6. Managed Payments activation and terms acceptance.
7. Live product/price/payment link creation.
8. Any API key creation or secret handling.
9. Real payment/self-purchase/testing with cash.
10. Refund/legal/support policy final approval.

## Agent-side actions now authorised

Within the non-spend approval boundary, agents may prepare:

- checkout copy;
- product title/description/feature bullets;
- refund/support/licence drafts;
- static landing CTA placeholder;
- post-payment fulfilment plan;
- manual first-10-sales operating checklist;
- webhook architecture and test-mode pseudocode;
- public preview patch **after** Mark provides a verified live checkout URL.

## Product facts to use

Product name:

- `AI Agent Approval Gates Starter Kit`

Price:

- `£9.00 GBP`, one-time payment.

Package:

- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`

Known SHA256 from existing repo records:

- `01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`

Short checkout description:

> Practical approval-gate templates for AI-agent workflows: spend gates, credential gates, live-publish gates, safety checks, and operator handoff prompts.

Buyer promise:

> A self-serve template pack to help founders/operators decide what AI agents can do automatically, what needs approval, and what must never be delegated.

Non-promise:

> Not legal, financial, security, compliance, employment, or investment advice. Does not guarantee revenue, safety, compliance, or agent performance.

## Preflight checklist

### Product readiness

- [ ] Final product title approved.
- [ ] v0.2 zip verified.
- [ ] Package manifest/hash rechecked on the day of listing.
- [ ] Checkout description approved.
- [ ] Refund/support/licence text approved.
- [ ] Thank-you/download route chosen.

### Stripe Managed Payments

- [ ] Mark confirms Stripe account is IronFrame-controlled.
- [ ] Mark confirms Managed Payments availability.
- [ ] Mark activates Managed Payments if available.
- [ ] Mark accepts Managed Payments terms.
- [ ] Product mapped to eligible digital/software/template category.
- [ ] Mark confirms tax/liability route.

### Payment Link setup — Mark live action

- [ ] Product: AI Agent Approval Gates Starter Kit.
- [ ] Price: £9 GBP one-time.
- [ ] Customer email collected.
- [ ] Success behaviour set: redirect/download/thank-you instructions.
- [ ] Receipt text checked.
- [ ] Link copied for Rhysand only after Mark verifies it.

### Fulfilment

- [ ] Manual first-sales fulfilment path chosen, or download page ready.
- [ ] If manual: sale notification → verify payment → send download link/email.
- [ ] If redirect: success page contains download and support boundary.
- [ ] If automated later: webhook test-mode plan first.

## Sources checked

Stripe:

- Managed Payments overview: https://docs.stripe.com/payments/managed-payments
- Managed Payments eligibility: https://docs.stripe.com/payments/managed-payments/eligibility
- Managed Payments tax compliance: https://docs.stripe.com/payments/managed-payments/tax-compliance
- How Managed Payments works: https://docs.stripe.com/payments/managed-payments/how-it-works
- Build Checkout integration with Managed Payments: https://docs.stripe.com/payments/managed-payments/set-up
- Use Payment Links with Managed Payments: https://docs.stripe.com/payments/managed-payments/use-payment-links
- Payment Links overview: https://docs.stripe.com/payment-links
- After Payment Link payment / fulfilment: https://docs.stripe.com/payment-links/post-payment
- Checkout fulfilment/webhooks: https://docs.stripe.com/payments/checkout/fulfill-orders
- Checkout tax collection / Managed Payments tax-liability note: https://docs.stripe.com/payments/checkout/taxes
- Stripe Tax: https://docs.stripe.com/tax
- Stripe account activation: https://docs.stripe.com/get-started/account/activate
- Stripe payouts: https://docs.stripe.com/payouts
- UK pricing: https://stripe.com/gb/pricing

Fallback MoR:

- Polar docs: https://polar.sh/docs
- Lemon Squeezy pricing/platform: https://www.lemonsqueezy.com/pricing

## Decision

Move Product Forge TODO-006 from Lemon/Gumroad-first to **Stripe-first**. Keep Polar as fallback. No live checkout/payment action occurs until Mark completes the gated Stripe-side setup and provides/approves the verified live route.
