# Stripe vs Polar Triple-Check — Approval Gates Starter Kit

Status: skeptical re-check after Mark challenged the Polar-first recommendation  
Date: 2026-06-04  
Owner: Rhysand / Feyre / Gwyn  
Product: `AI Agent Approval Gates Starter Kit v0.2`  
Launch hypothesis: `£9` digital download/template pack

## Question

Mark challenged the prior recommendation:

> Why not Stripe? Lots of people recommend it. Triple-check and justify.

## Corrected position

The prior recommendation was directionally right about **plain Stripe** being a worse first fit than a Merchant-of-Record digital-download platform, but it underweighted Stripe’s strengths and did not separate **standard Stripe** from **Stripe Managed Payments** clearly enough.

Revised decision:

1. **Check Stripe Managed Payments first if Mark wants maximum buyer trust and Stripe-native agent tooling.** If IronFrame is eligible and it supports this product cleanly, Stripe becomes the best long-term/default checkout route.
2. **Use Polar first if the immediate requirement is MoR + native file delivery + agent/MCP integration with minimum custom fulfilment.**
3. **Do not use standard/plain Stripe Payment Links as the first live route unless IronFrame deliberately accepts seller-managed tax/compliance and custom file fulfilment.**

## Why people recommend Stripe

They are right to recommend it for most serious internet businesses.

Stripe strengths:

- strongest buyer trust and checkout familiarity;
- mature UK/GBP support;
- excellent dashboard, test mode, APIs, SDKs, webhooks, refunds, dispute tooling;
- official Stripe MCP / agent docs;
- Payment Links can be created quickly;
- lower visible payment-processing fees than most MoR platforms;
- scales better if IronFrame later builds subscriptions, bundles, business invoices, licensing, or a custom storefront.

Sources checked:

- `https://docs.stripe.com/payment-links`
- `https://docs.stripe.com/checkout/fulfillment`
- `https://docs.stripe.com/mcp`
- `https://docs.stripe.com/agents`
- `https://docs.stripe.com/tax`
- `https://docs.stripe.com/payments/managed-payments`
- `https://docs.stripe.com/payments/managed-payments/tax-compliance`

## Why plain Stripe may still be wrong for the first £9 file download

Plain Stripe Checkout / Payment Links is a payment rail, not a Gumroad-style digital delivery platform.

For the Starter Kit, plain Stripe would require:

- digital file delivery layer;
- post-payment fulfilment webhook;
- signed/expiring download link or manual email delivery;
- idempotent sales/fulfilment ledger;
- refund/revocation handling;
- customer support/access-resend process;
- tax/VAT/GST compliance judgement if selling globally;
- Stripe Tax configuration or external accounting workflow.

Stripe’s own fulfilment docs emphasize that successful redirect is not reliable enough for fulfilment; webhooks should drive fulfilment after payment events.

For a `£9` validation product, building and owning that custom commerce stack may be disproportionate unless we intentionally want Stripe as long-term infrastructure.

## Important nuance: Stripe Managed Payments

Stripe now has a Managed Payments / Merchant-of-Record-style product for digital products. This changes the old simplistic critique that “Stripe is never MoR.”

If IronFrame is eligible and Stripe Managed Payments supports the Starter Kit cleanly, the platform order should become:

1. **Stripe Managed Payments** — best buyer trust + Stripe-native agent tooling + potential MoR/tax coverage.
2. **Polar.sh** — best current native-file-delivery + MoR + MCP fallback if Stripe Managed Payments is unavailable/too heavy.
3. **Paddle** — established MoR if Stripe/Polar onboarding blocks and stronger brand/compliance is desired.
4. **Dodo Payments** — promising agent-native challenger, but newer/trust needs testing.
5. **Lemon Squeezy** — simple MoR digital-download fallback if existing country/currency issue is fixed.
6. **Gumroad** — emergency fallback only.

## Polar critique

Polar remains attractive, but it is not risk-free.

Strengths:

- official MCP docs;
- API/webhooks;
- Merchant-of-Record posture;
- native file-download benefits;
- developer/AI-product audience fit;
- simple hosted checkout for digital products.

Risks:

- less buyer-recognised than Stripe;
- younger checkout product;
- account/KYC/payout review uncertainty;
- first payout review may delay cash availability;
- platform may intervene on refunds/disputes/chargebacks;
- fixed fee is relatively material on a £9 product;
- buyer receipt/card-descriptor trust must be tested.

Polar is best when we prioritise **MoR + file delivery + agent operations**. Stripe is best when we prioritise **buyer trust + mature payments + long-term infrastructure**.

## Practical recommendation

### If Mark wants the best serious business recommendation

Use **Stripe first**, but specifically investigate **Stripe Managed Payments** rather than plain Payment Links.

Why:

- Stripe is the trusted default.
- Stripe’s MCP/API/agent story is excellent.
- It scales into future IronFrame products better than Polar/Gumroad-style platforms.
- If Managed Payments is available, it may close the main MoR/tax gap.

### If Mark wants fastest safe first sale with minimal custom infrastructure

Use **Polar first**.

Why:

- Native digital file delivery.
- MoR posture.
- Official MCP.
- Less custom fulfilment work.
- Good fit for an AI-agent/digital-template buyer audience.

### If Mark wants fastest possible checkout regardless of agent elegance

Use **standard Stripe Payment Links** only with a deliberately simple fulfilment compromise:

- no global launch claim;
- manual fulfilment or simple private download page at first;
- Stripe Tax/tax position reviewed separately;
- webhook ledger built before any scale;
- public page makes refund/support/access boundaries explicit.

This would be fast but creates more operational/tax ownership for IronFrame.

## Final ranked decision for now

For Product Forge, replace the previous overconfident `Polar first` with:

1. **Stripe Managed Payments preflight first** — check eligibility, MoR coverage, digital-product fit, file-delivery options/gaps, UK/GBP, and setup burden.
2. **Polar activation handoff second** — ready if Stripe Managed Payments is not available or is too heavy.
3. **Paddle as serious MoR fallback** — stronger maturity than Polar, weaker simple file delivery.
4. **Standard Stripe Payment Links only as an intentional non-MoR route** — acceptable if Mark chooses buyer trust and speed over built-in delivery/MoR simplicity.

## Next safe action

Prepare two handoffs, with no account action:

- `STRIPE_MANAGED_PAYMENTS_PREFLIGHT.md` — what Mark must personally verify in Stripe before any live route.
- `POLAR_ACTIVATION_HANDOFF.md` — fallback route if Stripe Managed Payments is unavailable or too heavy.

No payment link, API key, webhook, product, tax/banking/KYC action, or public checkout should be created until Mark performs the platform-side identity/payout setup personally and confirms the seller route is IronFrame-controlled.
