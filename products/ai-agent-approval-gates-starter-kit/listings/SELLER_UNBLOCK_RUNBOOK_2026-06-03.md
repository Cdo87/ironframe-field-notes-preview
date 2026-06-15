# Seller Unblock Runbook — Approval Gates Starter Kit v0.2

Status: hard-gate handoff; no seller listing/payment link created  
Date: 2026-06-03  
Owner: Rhysand / Feyre / Gwyn  
Selected TODO: `TODO-006 — Execute Product Forge seller-platform checkout when an IronFrame seller session is available`

## Why this exists

`TODO-006` is still the highest-priority Product Forge/first-cash item, but it is blocked by seller-platform session/legal-payment setup rather than by approval. Mark has already approved IronFrame seller-platform activation and listing/payment-link management where the account is IronFrame-controlled and no hard gate is hit.

This runbook is the minimum unblock packet for the next browser-side session. It keeps Mark's required secret/tax/banking/identity actions on Mark's side and leaves Rhysand with a clean continuation point.

## Current verified product artefact

- Product: `AI Agent Approval Gates Starter Kit v0.2`.
- Zip: `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`.
- SHA256 re-verified on 2026-06-03: `01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`.
- Zip contents re-verified on 2026-06-03: 11 files, matching `build/v0.2/PACKAGE_MANIFEST.md`.
- Public preview remains checkout-disabled: `https://cdo87.github.io/ironframe-field-notes-preview/products/ai-agent-approval-gates-starter-kit/`.

## Best next platform order

Research updates 2026-06-04:

- `AGENT_FRIENDLY_CHECKOUT_PLATFORM_RESEARCH_2026-06-04.md` superseded the old `Lemon Squeezy first / Gumroad fallback` order.
- `STRIPE_VS_POLAR_TRIPLE_CHECK_2026-06-04.md` further corrects the recommendation after Mark challenged the Polar-first call. Stripe should not be dismissed; separate **Stripe Managed Payments** from ordinary **standard Stripe Payment Links/Checkout**.

Current platform order:

1. **Stripe Managed Payments preflight first** if Mark can personally verify IronFrame seller eligibility, MoR/tax coverage, digital-product fit, UK/GBP support, acceptable setup burden, and any file-delivery gap. This is the strongest serious-business route if available because Stripe has the best buyer trust, mature checkout, API/webhook surface, and official MCP/agent tooling.
2. **Polar.sh second / immediate MoR-file-delivery fallback** if Stripe Managed Payments is unavailable, too heavy, or does not solve simple digital file delivery. Polar has the strongest current blend of official MCP, API/webhooks, hosted checkout, Merchant-of-Record posture, and native file-download benefits, but weaker buyer recognition than Stripe.
3. **Paddle third** if a mature Merchant-of-Record route is preferred and heavier SaaS/software-style onboarding is acceptable.
4. **Dodo Payments fourth** as a promising newer AI/MCP-native route; verify buyer trust, UK seller flow, payout/KYC, and support maturity before making it primary.
5. **Creem fifth** if low-friction MoR digital-product sale matters more than mature MCP; verify UK/GBP/KYC and file-download flow.
6. **Standard Stripe Payment Links/Checkout only by explicit choice** if Mark accepts seller-managed tax/compliance and custom/manual file fulfilment in exchange for trusted Stripe checkout and fast setup.
7. **Lemon Squeezy fallback** only if the country/currency/store activation issue is corrected and the session is verified as IronFrame-controlled.
8. **Gumroad emergency fallback** only if speed beats agent-native automation/brand positioning.
9. **Do not add a checkout link** to the public preview until a seller listing URL exists and resolves correctly from a non-authenticated/private context.

## Mark-side 5-minute unblock checklist

Mark should complete these manually in the browser without sharing secrets:

1. Open the intended IronFrame-controlled seller dashboard: Lemon Squeezy or Gumroad.
2. Complete any password, 2FA, passkey, tax, banking, payout, identity, legal-entity, or account-selection screens personally.
3. Confirm the visible seller/store identity is `IronFrame` or another approved IronFrame seller identity.
4. Confirm the platform is not using Mark Hale's personal Google account as the operating route.
5. Confirm the pricing/currency route supports a £9 digital product without paid upgrades, boosts, ads, affiliate automation, analytics/pixels, forced email capture, or marketplace settings that cannot be disabled.
6. Stop before making high-liability tax/legal commitments if unsure.

When ready, give Rhysand one of these exact continuation phrases:

- Lemon Squeezy: `Continue TODO-006 from the authenticated IronFrame Lemon Squeezy dashboard; run the seller preflight first and keep optional growth settings closed.`
- Gumroad: `Continue TODO-006 from the authenticated IronFrame Gumroad dashboard; run the seller preflight first and keep optional growth settings closed.`

## Rhysand continuation sequence

After the authenticated seller session is available:

1. Run `SELLER_SESSION_PREFLIGHT_2026-05-31.md` before creating or publishing anything.
2. Re-check the zip hash:
   - `shasum -a 256 content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`
3. Use the relevant platform handoff:
   - `LEMON_SQUEEZY_ACTIVATION_HANDOFF.md`
   - `GUMROAD_ACTIVATION_HANDOFF.md`
4. Create/save draft first where possible; publish only when required for a checkout URL and all gates pass.
5. Keep disabled: analytics, pixels, email capture/newsletter automation, affiliates, marketplace/Discover/boost, coupons, upsells, subscriptions, paid ads, webhooks, guarantees.
6. Verify the listing URL from a private/non-authenticated context.
7. Record a dated activation log before touching the public preview.
8. Apply `PAYMENT_LINK_UPDATE_PATCH_TEMPLATE.md` only after URL verification.
9. Deploy/update the public preview and crawl it to prove the buy link resolves to the verified seller listing.
10. Update `SYSTEM_TODO.md`, `TASKS.md`, and `DECISIONS.md` only after evidence exists.

## Hard stop language

If any hard gate appears, record it exactly and stop with this format:

`APPROVAL REQUIRED: seller-platform unblock — [specific gate encountered] | this requires Mark-side secret/tax/banking/identity/legal/payment action or separate spend approval | Mark should complete the browser-side setup personally, then return with the matching continuation phrase above.`

## TODO-006 completion evidence checklist

`TODO-006` is done only when all are true:

- seller listing/checkout URL verified;
- seller identity, price/currency, file attachment, support/refund/disclaimer copy verified;
- dated activation log exists;
- public preview payment-link patch is deployed;
- post-deploy crawl proves the buy link resolves correctly;
- no hard gate was crossed and no optional growth/analytics/email/affiliate setting was enabled.
