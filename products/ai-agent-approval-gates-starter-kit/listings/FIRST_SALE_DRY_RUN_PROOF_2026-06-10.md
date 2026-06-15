# First-sale dry-run proof — Approval Gates Starter Kit

Date: 2026-06-10  
Owner lens: Feyre / Gwyn / Rhysand  
Status: local Product Forge first-cash readiness proof; no seller-platform, payment, buyer email, listing, public launch, analytics, or customer-data action

## Why this was the selected sprint

`SYSTEM_TODO.md` still puts Product Forge first for safe commercial movement. `TODO-006` remains blocked on Mark-side seller setup and verified Stripe/Polar checkout, so the highest-value unblocked local action was to prove the first-sale fulfilment path with deterministic local checks rather than create another product, listing draft, or public surface.

This sprint converts the existing buyer journey, fulfilment template, package manifest, and disabled checkout state into one repeatable first-sale dry-run.

## Artefacts created

- Script: `scripts/product_forge_first_sale_dry_run.py`
- JSON proof output: `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/listings/first_sale_dry_run/2026-06-10_first_sale_dry_run_result.json`
- This proof note: `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/listings/FIRST_SALE_DRY_RUN_PROOF_2026-06-10.md`

## What the dry-run verifies

The script is local/no-network and checks:

1. v0.2 package zip exists.
2. Package SHA256 matches the manifest.
3. Zip contents match the 11-file manifest exactly.
4. The first-sale fulfilment template, first-10-sales checklist, and buyer journey QA contain the required fulfilment, support-boundary, disclaimer, no-PII, and approval-gate markers.
5. The templates and sales page contain no email-like markers, secret-like markers, or live payment URLs.
6. A dummy redacted ledger entry can be produced without buyer PII, receipt IDs, transaction IDs, checkout URLs, or customer messages.
7. A dry-run email stub exists but remains `not_sent_dry_run_only`.

## Verification run

Command run from `/Users/edi/IronFrame`:

```bash
python3 scripts/product_forge_first_sale_dry_run.py \
  --date 2026-06-10 \
  --output content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/listings/first_sale_dry_run/2026-06-10_first_sale_dry_run_result.json

python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --allow-no-checkout
```

Results:

- First-sale dry-run: `PASS`
- Package SHA256: `01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`
- Package file count: `11 / 11`
- Template scans: no email-like markers, no secret-like markers, no live payment URL markers
- Sales-page scan: no live payment URL markers
- Checkout acceptance: `PASS`
- Public checkout state preserved: no payment-like hrefs, no external anchor hrefs, no scripts, no forms, `noindex,nofollow` retained

## Commercial movement achieved

Before this sprint, the first-sale route had copy/checklists. After this sprint, it has a repeatable proof command that can be run on listing day before Mark or Rhysand patches a verified checkout URL.

The result is not a new public surface. It is a lower-risk path to first cash: once Mark completes seller-side Stripe/Polar setup, Rhysand can re-run the dry-run, re-run checkout acceptance, patch the verified URL, and fulfil the first sale without inventing process under pressure.

## Non-actions / gates preserved

No checkout link, seller listing, platform product, buyer email, public launch, analytics, email capture, customer/private data, paid API/model call, cash spend, secret handling, app-store action, outreach/DM, live trading/ad/email execution, or Mark personal Google use occurred.

Remaining blocker:

`APPROVAL REQUIRED: verified IronFrame-controlled Stripe/Polar checkout route plus Mark-side seller setup | payment, identity, banking, tax, terms, password/2FA, and live-payment activation boundary | Mark completes/verifies seller setup and provides the non-secret checkout URL before public CTA patching or any buyer fulfilment.`
