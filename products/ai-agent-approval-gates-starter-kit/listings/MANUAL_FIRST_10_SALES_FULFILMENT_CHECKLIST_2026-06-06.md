# Manual first-10-sales fulfilment checklist — Approval Gates Starter Kit

Date: 2026-06-06  
Status: local operating checklist; no checkout/payment action created  
Owner lens: Feyre / Gwyn / Rhysand  
Product: `AI Agent Approval Gates Starter Kit v0.2`  
Route preference: Stripe Managed Payments + Payment Links first; Polar fallback if Stripe Managed Payments is unavailable

## Purpose

Today's AI-income intelligence run had no usable transcript evidence, so no new creator mechanism should be adopted. The useful movement object is checkout readiness for the first Product Forge sale: define the manual fulfilment path before Mark creates or provides a verified payment link.

This checklist is for the **first 10 verified sales only**. It keeps the first-cash route simple, reversible, and non-automated while the seller platform, buyer support, refund, and tax/liability posture are still being proven.

## Hard prerequisites before any buyer can purchase

- [ ] Mark has completed Stripe/Polar account, password, 2FA, KYC, banking, tax/liability, terms, and live-payment activation personally.
- [ ] A verified IronFrame-controlled checkout URL exists.
- [ ] Product name is exactly `AI Agent Approval Gates Starter Kit`.
- [ ] Price is exactly `£9.00 GBP` one-time payment unless Mark explicitly changes it.
- [ ] Checkout copy includes the operational-template disclaimer.
- [ ] Customer email collection is enabled by the payment platform for receipt/fulfilment only.
- [ ] Product zip hash is rechecked on the listing day.
- [ ] Success/thank-you route is chosen: manual fulfilment, direct download, or simple download page.
- [ ] Public preview CTA is patched only after the checkout URL is verified.

## Package to fulfil

Zip:

`content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`

Known SHA256:

`01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`

Recheck command before listing or fulfilling:

```bash
cd /Users/edi/IronFrame
shasum -a 256 content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip
```

## Manual fulfilment sequence

Use this if the first payment link cannot attach/deliver the file automatically.

1. Payment platform records successful payment.
2. Mark/Rhysand verifies:
   - platform name;
   - payment status is successful/paid;
   - product name and price match;
   - buyer email is available;
   - no chargeback/refund/fraud flag is visible.
3. Recheck product zip hash.
4. Send fulfilment from the approved platform/email route only after Mark confirms the route is appropriate.
5. Include only:
   - thank-you line;
   - download/access instruction;
   - support boundary;
   - refund boundary if Mark has approved wording;
   - disclaimer.
6. Record sale fulfilment in a private local ledger **only if it does not expose buyer personal data into Git**.

## Buyer email copy draft

Do not send until the platform/account/email route is approved.

Use the expanded copy/paste fulfilment asset here:

`FIRST_SALE_FULFILMENT_EMAIL_AND_LEDGER_TEMPLATE_2026-06-09.md`

It includes:

- manual buyer email copy;
- platform-hosted delivery copy;
- seller-platform confirmation snippet;
- Git-safe redacted fulfilment ledger shape;
- explicit buyer PII / transaction-data exclusions.

## First-10-sales support boundary

Allowed:

- file access help;
- clarify where a template lives inside the zip;
- correct broken download/receipt issues;
- issue a refund if Mark/platform policy says to.

Not included:

- custom implementation;
- legal/compliance/security advice;
- reviewing secrets, customer data, contracts, codebases, trading systems, or private workflows;
- setting up agents/accounts/SaaS/platforms for the buyer;
- guaranteed safety, compliance, income, or performance claims.

## Privacy and record boundary

Do not commit buyer names, emails, receipts, transaction IDs, Stripe/Polar URLs containing private identifiers, refund notes, or support messages to Git.

If a fulfilment ledger is needed, create it outside the repo or use redacted local entries only.

## Approval gates preserved

APPROVAL REQUIRED: create/activate Stripe, Polar, standard Stripe Checkout, live Payment Links, products/prices, payout/bank/tax/KYC setup, API keys, or test/live payments | payment and identity obligations | Mark must handle seller-platform setup and verify the live URL before Rhysand patches public CTAs.

APPROVAL REQUIRED: send buyer emails, publish checkout links, attach hosted downloads, collect email beyond payment receipt needs, or create a support mailbox/process | external buyer/customer-data action | keep this checklist local until Mark chooses the live fulfilment route.
