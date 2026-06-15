# Seller Session Preflight — Approval Gates Starter Kit v0.2

Status: unblock handoff for TODO-006; no seller listing/payment link created  
Date: 2026-05-31  
Owner: Rhysand / Feyre / Gwyn  
Selected TODO: `TODO-006 — Execute Product Forge seller-platform checkout when an IronFrame seller session is available`

## Purpose

This is the exact preflight Rhysand should run when an IronFrame-controlled Lemon Squeezy or Gumroad seller route is available. Mark has approved IronFrame seller-platform activation and payment-link/listing management under standing authority, but the session still must pass the hard gates below before any product is published or linked.

## Current state

- Product: `AI Agent Approval Gates Starter Kit v0.2`.
- Package path: `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`.
- SHA256 verified on 2026-05-31: `01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`.
- Zip contents verified on 2026-05-31: 11 expected files; no live payment link, analytics, email capture, affiliate code, or seller-platform dependency included.
- Public preview is live with checkout disabled: `https://cdo87.github.io/ironframe-field-notes-preview/products/ai-agent-approval-gates-starter-kit/`.
- Preferred platform: Lemon Squeezy, only if country/currency/live-payment/test-mode/public seller identity are clean.
- Fallback platform: Gumroad, only if the account/session is clearly IronFrame-controlled and optional growth/marketplace/email/analytics features remain closed.

## Hard-stop gates

Stop and report a precise blocker if any appears:

- password, 2FA, passkey, recovery-code, API-key, banking, payout, tax, identity, legal-entity, payment-card, or secret entry;
- Mark Hale personal Google/account selection;
- wrong seller identity, wrong public brand, or non-IronFrame account;
- wrong legal country/currency for the intended seller route;
- paid feature/subscription/boost/advertising prompt;
- platform requires high-liability legal/tax/accounting commitment Rhysand cannot make;
- checkout requires a real-money self-purchase for verification without Mark separately approving that spend;
- analytics/pixels/cookies/email capture/affiliates/marketplace/discover/webhooks are forced on and cannot be disabled;
- any prompt to expose Mark/family/private details or make legal/compliance/security/income guarantees.

## Safe preflight sequence

1. Confirm the dashboard/session is already authenticated and clearly belongs to `IronFrame` or an approved IronFrame seller identity.
2. Confirm platform context:
   - seller/store name;
   - country/legal route visible without entering identity/tax/bank details;
   - displayed currency supports the intended £9 launch price or a clearly equivalent approved GBP route;
   - live/test mode state;
   - whether draft product creation is possible without publishing.
3. Re-check local package hash before upload:
   - `shasum -a 256 content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`
4. Create the listing from the platform handoff:
   - Lemon Squeezy: `LEMON_SQUEEZY_ACTIVATION_HANDOFF.md`.
   - Gumroad: `GUMROAD_ACTIVATION_HANDOFF.md`.
5. Keep closed: analytics, pixels, email capture, affiliates, marketplace discovery/boost, coupons, upsells, subscriptions, memberships, webhooks, paid ads, guarantees.
6. Save draft first if possible. Publish only if the platform requires publish for a checkout URL and all hard gates are clean.
7. Verify the public checkout/product URL in a private/non-authenticated context.
8. Record a dated activation log with:
   - platform;
   - listing URL;
   - seller identity observed;
   - price/currency;
   - package hash;
   - file attachment status;
   - optional settings disabled;
   - verification result;
   - remaining gates.
9. Only after URL verification, apply `PAYMENT_LINK_UPDATE_PATCH_TEMPLATE.md` to the local product page and public preview route, then crawl the live page and verify the buy link resolves to the approved listing.

## Mark-side unblock sentence if session requires browser setup

If Mark is present and wants to unblock the route without sharing secrets, the useful instruction is:

`I have opened the IronFrame-controlled [Lemon Squeezy/Gumroad] seller dashboard and completed any password/2FA/tax/banking/identity screens myself. Continue with the Approval Gates Starter Kit seller preflight; do not enable optional growth settings.`

## Definition of done for TODO-006

TODO-006 can be marked done only when all exist:

- verified seller listing/checkout URL;
- dated activation log;
- public preview payment-link patch applied and deployed;
- post-deploy crawl verifies the buy link resolves correctly;
- no hard gate crossed and no optional growth/analytics/email/affiliate settings enabled.
