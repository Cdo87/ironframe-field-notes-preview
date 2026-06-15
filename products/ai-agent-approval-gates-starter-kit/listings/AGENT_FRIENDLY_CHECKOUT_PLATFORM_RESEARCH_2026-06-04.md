# Agent-Friendly Checkout Platform Research — Approval Gates Starter Kit

Status: research / platform-selection recommendation; no checkout account action taken  
Date: 2026-06-04  
Owner: Rhysand / Feyre / Gwyn  
Product: `AI Agent Approval Gates Starter Kit v0.2`  
Current launch hypothesis: `£9` digital download/template pack

## User question

Mark asked whether Gumroad is too old-school and Lemon Squeezy is not well-known, and whether any checkout platforms integrate better with Hermes and AI agents.

## Operating gates

This research does **not** authorize password, 2FA, tax, banking, payout, identity/KYC, legal-entity, paid feature, production webhook, customer email, refund, or public checkout action by an agent.

Rhysand/Hermes may prepare copy, platform comparisons, webhook architecture, test plans, local ledgers, and handoff docs. Mark must personally handle secrets, identity, tax, banking, payout, and high-liability setup.

## Short answer

Yes: there are more agent-native choices than Gumroad or Lemon Squeezy.

Best shortlist for IronFrame:

1. **Polar.sh** — best current fit for Hermes/AI-agent compatibility plus Merchant-of-Record and digital file delivery.
2. **Dodo Payments** — strongest newer agent/MCP-native contender; worth trialing if account/KYC friction is low.
3. **Creem** — low-cost MoR digital-products option with good API/webhook/file-download posture; MCP docs appear less mature.
4. **Paddle** — established MoR with official MCP, but likely heavier and less ideal for a £9 downloadable template.
5. **Stripe** — strongest API/MCP ecosystem, but not MoR by default and needs separate digital delivery/tax responsibility.
6. **Lemon Squeezy** — still a good simple MoR digital-download route, but less agent-native and the current IronFrame route has country/currency/store-activation friction.
7. **Gumroad** — viable fallback for creator-style digital download, but high fee and weakest agent/API story.

## Decision lens

For this product, we need:

- hosted checkout / payment link;
- GBP/UK seller support;
- digital file delivery or easy fulfillment;
- Merchant of Record / tax handling preferred;
- webhooks for Hermes notifications and audit ledgers;
- API or MCP support for future agent operations;
- credible buyer-facing checkout;
- low setup friction for a £9 template product;
- no mandatory paid subscription before first sale.

## Ranked platform notes

### 1. Polar.sh — recommended first investigation

**Verdict:** best balance of agent-native architecture and simple digital product sale.

Why it fits:

- Official MCP/server documentation for agent workflows.
- Broad API for checkouts, products, orders, refunds, benefits, files, customer portal, and webhooks.
- Signed webhooks.
- Hosted checkout / checkout links.
- File-download benefits for digital delivery.
- Merchant of Record posture for sales tax/VAT handling.
- UK supported through payout/KYC flow.

Risks / gates:

- Newer and more developer-oriented than Stripe/Paddle; buyer trust should be checked with a live preview before public launch.
- Requires Mark-side KYC/identity/payout setup.
- Fees reported in docs as around `5% + $0.50` on starter-style pricing; verify at signup.

Sources checked:

- `https://polar.sh/docs/integrate/mcp`
- `https://polar.sh/docs/api-reference/introduction`
- `https://polar.sh/docs/integrate/webhooks/endpoints`
- `https://polar.sh/docs/features/benefits/file-downloads`
- `https://polar.sh/docs/merchant-of-record/introduction`
- `https://polar.sh/docs/merchant-of-record/supported-countries`
- `https://polar.sh/docs/merchant-of-record/fees`

### 2. Dodo Payments — strongest newer MCP-native challenger

**Verdict:** serious candidate if Mark wants the most agent-native route, but it needs buyer-trust and onboarding checks.

Why it fits:

- Docs position it for SaaS, AI, and digital products.
- API, webhooks, checkout sessions, storefronts, one-time payments, and MCP server documentation.
- Merchant-of-Record positioning.
- GBP/EUR/USD ledger/payout support surfaced in docs.

Risks / gates:

- Newer brand; unknown buyer trust compared with Stripe/Paddle.
- Need to verify UK seller/KYC/payout flow and whether a £9 digital-template product is accepted quickly.
- Agent should not configure live keys or production webhooks until Mark completes account setup.

Sources checked:

- `https://docs.dodopayments.com/`
- `https://docs.dodopayments.com/api-reference/introduction`
- `https://docs.dodopayments.com/developer-resources/webhooks`
- `https://docs.dodopayments.com/developer-resources/mcp-server`
- `https://dodopayments.com/pricing`

### 3. Creem — good MoR / file-download option, less mature MCP

**Verdict:** strong practical option if low fee and quick MoR digital-product setup matter more than official mature MCP.

Why it fits:

- Built for SaaS, digital products, and AI tools.
- Merchant-of-Record positioning.
- API/webhooks.
- File downloads.
- One-time payments and storefronts.
- Public docs mention `3.9% + 40¢` style pricing; verify at signup.

Risks / gates:

- MCP docs exist but appear less mature / “coming soon” in places.
- Newer brand; buyer trust needs evaluation.
- Mark-side KYC/payout/tax handling still required.

Sources checked:

- `https://docs.creem.io/getting-started/introduction`
- `https://docs.creem.io/code/webhooks`
- `https://docs.creem.io/code/mcp`
- `https://docs.creem.io/features/addons/file-downloads`
- `https://docs.creem.io/merchant-of-record/what-is`

### 4. Paddle — trusted MoR with official MCP, but heavier

**Verdict:** best established MoR / compliance platform if IronFrame moves toward SaaS, not the fastest £9 template launch.

Why it fits:

- Established Merchant-of-Record platform.
- Mature API and webhooks.
- Official Paddle MCP server.
- Hosted checkout and default payment links.
- Strong SaaS/software buyer trust.

Risks / gates:

- More SaaS/app/subscription-shaped than creator download-shaped.
- Digital file delivery may need external fulfillment rather than native simple file upload.
- Business/domain/live approval can take longer.
- Likely overkill for the first low-ticket template.

Sources checked:

- `https://developer.paddle.com/api-reference/`
- `https://developer.paddle.com/webhooks/`
- `https://developer.paddle.com/sdks/ai/paddle-mcp/`
- `https://developer.paddle.com/build/transactions/default-payment-link`
- `https://www.paddle.com/pricing`

### 5. Stripe — best API/MCP ecosystem, weaker first-product MoR fit

**Verdict:** excellent later infrastructure route; not the cleanest first-cash route for a simple digital download unless Mark wants to own tax/fulfillment complexity.

Why it fits:

- Best-known checkout brand.
- Mature API, SDKs, Payment Links, Checkout, webhooks.
- Official Stripe MCP and agent docs.
- Lower visible UK card processing rates than MoR platforms.

Risks / gates:

- Standard Stripe is a payment processor, not Merchant of Record.
- Stripe Tax helps calculate/collect/report but does not remove merchant responsibility.
- No native Gumroad-style file delivery; would need webhook-driven fulfillment/storage/email/customer portal.
- More custom engineering and more legal/tax responsibility.

Sources checked:

- `https://docs.stripe.com/api`
- `https://docs.stripe.com/webhooks`
- `https://docs.stripe.com/mcp`
- `https://docs.stripe.com/agents`
- `https://docs.stripe.com/payment-links`
- `https://docs.stripe.com/payments/checkout`
- `https://docs.stripe.com/tax`
- `https://stripe.com/gb/pricing`

### 6. Lemon Squeezy — still practical, but not the best agent-native route

**Verdict:** remains a good simple MoR/digital-download checkout route if the store/country/currency issue is fixed, but it is not the best answer to “integrates with Hermes and AI agents”.

Why it fits:

- Merchant of Record.
- Hosted checkout and API-created checkout URLs.
- Digital file upload/download.
- Webhooks with signing and simulations.
- UK supported.

Risks / gates:

- No official MCP found; third-party/community MCP only.
- Current IronFrame route showed country/currency/store activation friction.
- Brand is known in indie/dev circles but less well-known than Stripe/Paddle.

Sources checked:

- `https://docs.lemonsqueezy.com/api`
- `https://docs.lemonsqueezy.com/help/webhooks`
- `https://docs.lemonsqueezy.com/api/checkouts/create-checkout`
- `https://docs.lemonsqueezy.com/help/products/adding-products`
- `https://docs.lemonsqueezy.com/help/getting-started/supported-countries`
- `https://www.lemonsqueezy.com/pricing`

### 7. Gumroad — fallback only

**Verdict:** not dead, but relatively old-school and least aligned with Hermes/agent automation.

Why it fits:

- Simple digital product pages.
- File delivery.
- Creator/buyer familiarity.
- Merchant-of-Record/tax handling now claimed publicly.

Risks / gates:

- High fee compared with alternatives; research found `10% + $0.50` direct-style pricing and higher marketplace cuts.
- Sparse/awkward API and webhook story compared with Stripe/Polar/Dodo/Paddle.
- No official MCP found.
- Brand feel is more creator-store than serious AI-ops product.

Sources checked:

- `https://gumroad.com/pricing`
- `https://gumroad.com/api`
- `https://help.gumroad.com/article/280-webhooks`

## Other options considered

- **Whop:** technically powerful with API, webhooks, entitlements, license keys, files, and AI/MCP docs, but buyer experience is community/access-product shaped. Better if IronFrame sells membership, community, or gated software access.
- **Payhip:** practical creator checkout with digital downloads and webhooks; less agent-native than Polar/Dodo/Creem. Could be fallback if MoR onboarding blocks first sale.
- **Shopify:** trusted and highly automatable, but monthly store overhead, digital-download app, and not MoR by default; overbuilt for the first £9 template.
- **Ko-fi / Buy Me a Coffee:** good support/donation channels, weaker professional product positioning.
- **RevenueCat:** excellent for app subscriptions/entitlements, poor fit for a one-off template download.
- **FastSpring / PayPro Global:** credible software MoR providers, likely overkill for first low-ticket product.

## Recommended IronFrame architecture

Preferred near-term architecture if using Polar/Dodo/Creem/Lemon Squeezy:

```text
Customer
  ↓
Verified hosted checkout/payment link
  ↓
MoR checkout platform
  ├─ handles payment/tax/receipt/file access where supported
  ├─ sends signed webhook events
  └─ remains system of record for payment/refund/dispute state
        ↓
Hermes webhook subscription
  ├─ Telegram notification to Mark/Rhysand
  ├─ local normalized sales/audit ledger in IronFrame repo
  ├─ daily cron reconciliation against platform export/API
  └─ LLM only drafts summaries/support responses/exceptions
```

Hermes should **not** be the source of truth for payment validity. The payment platform remains source of truth. Hermes records, reconciles, summarizes, and prepares next actions.

## Safe automation pattern for Hermes

Allowed after Mark completes account/KYC/secrets personally:

- create draft product/listing using least-privilege API token if platform supports it;
- update product copy/assets from checked-in handoff docs;
- create sandbox/test checkout links;
- receive signed webhooks through `hermes webhook subscribe` route;
- append local audit ledger rows;
- notify Telegram on sale/refund/dispute/license/download events;
- run daily reconciliation cron;
- draft support/refund responses for approval.

Human approval still required before:

- public checkout publication;
- price/refund/support/legal copy changes;
- customer emails;
- refunds/dispute responses;
- external CRM/list writes;
- production webhook exposure;
- OAuth/API key creation or rotation;
- tax/banking/payout/identity/legal setup.

## Recommendation

Change the platform order for Product Forge from `Lemon Squeezy first, Gumroad fallback` to:

1. **Polar.sh first** — because it is the best proven mix of official MCP, API/webhooks, hosted checkout, MoR, and native file downloads.
2. **Dodo Payments second** — because it is the most promising newer agent-native/MCP route, but needs trust/onboarding verification.
3. **Creem third** — because it looks commercially efficient and digital-product friendly, but MCP maturity is weaker.
4. **Paddle fourth** — if Mark wants established MoR/SaaS credibility and can tolerate heavier setup.
5. **Lemon Squeezy fallback** — only if the existing store/country/currency issue is corrected.
6. **Gumroad emergency fallback** — only if first-sale speed matters more than agent-native automation and brand positioning.

## Next safe action

Create a `POLAR_ACTIVATION_HANDOFF.md` for the Approval Gates Starter Kit, using the current v0.2 zip, listing copy, price, refund/support boundary, platform preflight, and webhook/test-plan gates. Do **not** create an account, API key, webhook, checkout link, or public payment URL until Mark completes Polar-side identity/payout setup personally and confirms the seller identity is IronFrame-controlled.
