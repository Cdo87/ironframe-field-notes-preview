# Payment Link Update Patch Template — Approval Gates Starter Kit

Status: template only; do not apply until verified checkout URL exists
Date: 2026-06-05
Route preference: Stripe Managed Payments + Payment Links first; Polar fallback; standard Stripe only by explicit tax/fulfilment choice

## Preconditions

Apply this patch only after all are true:

- Stripe Managed Payments + Payment Link is verified under Mark/IronFrame control, or Polar fallback is explicitly chosen.
- Product zip hash matches the manifest.
- Checkout/product URL has been opened and verified.
- Checkout/product URL is a full `https://` URL on an approved payment host and contains no username/password component, customer/private data, API key, token, code, client secret, or prefilled-email query parameter.
- Product name, price, refund/support boundary, disclaimer, and file attachment/fulfilment path are correct.
- Mark has personally handled any Stripe/Polar password, 2FA, KYC, tax, banking, payout, terms, and live activation steps.
- No analytics, email capture, affiliates, cookies/pixels, paid ads, or private-detail release has been enabled.

## Values to fill

- `PAYMENT_URL`: verified checkout/product URL.
- `PLATFORM_NAME`: Stripe Managed Payments, Stripe, or Polar.
- `VERIFIED_AT`: timestamp of verification.

## Product-page copy block

Use a single CTA block like this:

```html
<section class="card" id="buy">
  <p class="eyebrow">Digital starter kit · £9 launch price</p>
  <h2>Buy the Approval Gates Starter Kit</h2>
  <p>
    Get the editable checklist, founder autonomy policy, agent task card, risk register, and start-here guide as one downloadable template pack.
  </p>
  <p>
    <a class="button" href="PAYMENT_URL" rel="noopener">Buy the Starter Kit</a>
  </p>
  <p class="small">
    Checkout handled by PLATFORM_NAME. This is an operational template pack, not legal, financial, tax, cybersecurity, compliance, investment, employment, or trading advice.
  </p>
</section>
```

## Boundaries to preserve

Keep these unchanged unless separately approved:

- `robots.txt` should continue to block indexing.
- No analytics script.
- No email capture form.
- No affiliate link.
- No income/safety/compliance guarantee.
- No Mark/family/defence/private details.

## Verification before and after applying

Before patching, verify the current disabled-checkout page is still clean:

```bash
cd /Users/edi/IronFrame
python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --allow-no-checkout
```

After patching with a verified URL, run:

```bash
cd /Users/edi/IronFrame
python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --expected-payment-url 'PAYMENT_URL'
python3 scripts/status_check.py
git status --short --branch
```

Then crawl/verify the public preview after deployment/update:

- product page loads;
- free checklist remains accessible;
- buy button resolves to the exact verified checkout URL;
- no new external links appear except the approved payment URL;
- no analytics/cookies/email-capture scripts are present;
- `noindex,nofollow` remains unless Mark separately approves a public-launch/indexing change.
