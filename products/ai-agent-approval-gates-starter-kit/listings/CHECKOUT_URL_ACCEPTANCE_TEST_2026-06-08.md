# Checkout URL acceptance test — Approval Gates Starter Kit

Date: 2026-06-08
Status: local readiness artefact; no checkout/payment action created
Owner lens: Feyre / Gwyn / Rhysand
Product: `AI Agent Approval Gates Starter Kit v0.2`

## Why this exists

Today's AI-income intelligence run selected three plausible revenue videos, but all three selected teardown targets had transcript capture failures. Because there is no transcript-backed mechanism, IronFrame should not create another creator-derived worksheet from title metadata.

The useful movement object is to reduce the friction between Mark completing the Stripe/Polar payment gate and Rhysand safely patching the Starter Kit preview. This acceptance test defines what must be true before a verified checkout URL is allowed onto the public preview.

## New local verifier

Script:

`/Users/edi/IronFrame/scripts/product_forge_checkout_acceptance.py`

Current disabled-checkout check:

```bash
cd /Users/edi/IronFrame
python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --allow-no-checkout
```

Expected result while checkout is disabled:

- `status: PASS`
- no script tags;
- no form tags;
- robots meta retains `noindex,nofollow`;
- no payment-like external checkout hrefs;
- no analytics/email-capture markers.

Post-payment-link check after Mark provides a verified URL:

```bash
cd /Users/edi/IronFrame
python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --expected-payment-url 'PASTE_VERIFIED_STRIPE_OR_POLAR_URL_HERE'
```

Pass condition after patch:

- expected payment URL itself is a full `https://` URL on an approved payment host (`buy.stripe.com`, Stripe, Polar, Lemon Squeezy, Gumroad, PayPal, or Payhip);
- expected payment URL contains no username/password component and no sensitive/private query keys such as email, token, key, code, client secret, or API key;
- exact payment URL appears exactly once;
- no other payment-like URLs appear;
- no scripts/forms/analytics/email-capture have been introduced;
- `noindex,nofollow` remains until a separate public-launch decision changes it.

## Acceptance checklist before patching public preview

- [ ] Mark has handled Stripe/Polar password, 2FA, KYC, banking, tax/liability, terms, live activation, and any API keys personally.
- [ ] Platform route is IronFrame-controlled and not Mark Hale personal Google/payment identity unless explicitly approved.
- [ ] Product title is exactly `AI Agent Approval Gates Starter Kit`.
- [ ] Price is exactly `£9.00 GBP` one-time unless Mark changes it.
- [ ] Product/package hash is rechecked on listing day.
- [ ] Fulfilment path is chosen: direct platform download, success-page download, or manual first-10-sales fulfilment.
- [ ] Checkout copy includes the operational-template disclaimer.
- [ ] The page patch uses `listings/PAYMENT_LINK_UPDATE_PATCH_TEMPLATE.md`.
- [ ] The acceptance script passes after patching.
- [ ] Live preview crawl confirms HTTP 200, correct buy link, free checklist still available, and no analytics/email capture.

## Gates preserved

APPROVAL REQUIRED: activate Stripe/Polar, create live product/payment link, accept terms, provide KYC/banking/tax/identity, use API keys, run cash test payments, publish checkout, or send buyer fulfilment email | payment/customer-data/legal boundary | Mark must complete the seller-side action and Rhysand may only patch after verified URL acceptance.

APPROVAL REQUIRED: remove `noindex,nofollow`, add analytics/email capture, run launch posts, run outreach, enable affiliates/ads, or make public income/safety/compliance guarantees | public exposure and claims risk | keep the preview controlled until Mark approves public launch state.
