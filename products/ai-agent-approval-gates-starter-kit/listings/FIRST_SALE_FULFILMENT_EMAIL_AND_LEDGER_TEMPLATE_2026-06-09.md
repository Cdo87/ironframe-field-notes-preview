# First-sale fulfilment email and redacted ledger template — Approval Gates Starter Kit

Date: 2026-06-09  
Status: local Product Forge readiness artefact; do not send, publish, or activate until a verified checkout route exists  
Owner lens: Feyre / Gwyn / Rhysand  
Product: `AI Agent Approval Gates Starter Kit v0.2`  
Route preference: Stripe Managed Payments + Payment Links first; Polar fallback if Stripe Managed Payments is unavailable

## Purpose

This file turns the prepared first-10-sales fulfilment checklist into copy/paste-ready buyer-support assets for the first verified Product Forge sale.

It exists so that, after Mark completes the seller-side Stripe/Polar gate and provides a verified checkout URL, Rhysand can patch the public preview and fulfil a paid digital download without inventing support wording under pressure.

No checkout, product listing, buyer email, ledger, payment link, download hosting, public launch, analytics, email capture, or external seller-platform action was created by this file.

## Preconditions before using any template

All must be true first:

- Mark has personally handled any platform password, 2FA, KYC, banking, payout, tax/liability, terms, live-payment activation, and API-key/secret handling.
- The seller route is IronFrame-controlled and not Mark Hale's personal Google/payment identity unless Mark explicitly approves otherwise.
- The buyer payment is visible as successful/paid for `AI Agent Approval Gates Starter Kit` at the approved price.
- Product zip hash is rechecked on the same day before fulfilment.
- The fulfilment route is chosen: platform-hosted file delivery, success-page download, or manual first-10-sales email.
- The support boundary and disclaimer below are not weakened.
- No buyer personal data is committed to Git.

## Package reference

Zip:

`content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`

Known SHA256:

`01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`

Recheck command:

```bash
cd /Users/edi/IronFrame
shasum -a 256 content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip
```

## Seller-platform confirmation snippet

Use this as internal checklist text before sending fulfilment:

```text
FULFILMENT PREFLIGHT — AI Agent Approval Gates Starter Kit
- Platform: [Stripe Managed Payments / Stripe / Polar]
- Product visible as: AI Agent Approval Gates Starter Kit
- Price visible as: £9.00 GBP one-time [or Mark-approved override]
- Payment status: paid/succeeded
- Fraud/refund/chargeback flag: none visible
- Buyer contact route: available through platform receipt/customer email
- Package hash rechecked today: yes/no
- Fulfilment route: platform download / success-page download / manual email
- Support boundary included: yes/no
- Disclaimer included: yes/no
```

Do not paste buyer names, buyer emails, transaction IDs, receipt URLs, checkout URLs with private identifiers, or support messages into Git.

## Manual fulfilment email — download route placeholder

Do not send until Mark confirms the approved sending route and the payment is verified.

```text
Subject: Your AI Agent Approval Gates Starter Kit

Thanks for buying the AI Agent Approval Gates Starter Kit.

Download/access:
[INSERT APPROVED DOWNLOAD LINK OR ATTACHMENT ROUTE]

Start here:
1. Open START_HERE.md.
2. Use the approval-gate checklist to classify one agent task as green, amber, or red.
3. Fill one task card before widening agent permissions.
4. Add stop rules for money, publishing, messaging, credentials, customer data, deletion, deployments, trading, or other high-liability actions.

Support boundary:
This is a self-serve digital template pack. File/access help is included. Custom implementation, account setup, legal/compliance review, cybersecurity certification, financial/tax/trading advice, agent deployment, and guaranteed outcomes are not included.

Disclaimer:
Operational templates only. Not legal, financial, tax, cybersecurity, compliance, investment, employment, or trading advice. No revenue, safety, compliance, or agent-performance guarantee.

If the download/access route fails, reply through the purchase support route with your payment receipt ID and I’ll help with file access.
```

## Platform-hosted delivery copy

If Stripe/Polar can attach the file directly, use this as product delivery text where the platform allows a post-purchase note:

```text
Your download is the AI Agent Approval Gates Starter Kit v0.2.

Open START_HERE.md first, then use the checklist and permission matrix to classify your next agent task before widening autonomy.

This is a self-serve operational template pack only. It does not include custom implementation, account setup, legal/compliance/cybersecurity/financial/tax/trading advice, agent deployment, or guaranteed outcomes.
```

## Redacted fulfilment ledger template

If a ledger is needed, keep buyer-identifiable details outside Git. A Git-safe redacted entry may look like this only:

```markdown
| Sale # | Date | Platform | Product | Price | Payment verified | Fulfilment route | Package hash checked | Support issue class | Notes |
|---:|---|---|---|---|---|---|---|---|---|
| 1 | YYYY-MM-DD | Stripe/Polar | Approval Gates Starter Kit v0.2 | £9 GBP | yes/no | platform/manual | yes/no | none/file-access/refund/other | no buyer PII |
```

Allowed ledger content:

- sale number;
- date;
- platform name;
- product name/version;
- price/currency;
- payment verified yes/no;
- fulfilment route;
- package hash checked yes/no;
- support issue class without buyer details.

Forbidden in Git:

- buyer names;
- buyer emails;
- receipt or transaction IDs;
- Stripe/Polar customer IDs;
- private checkout/session URLs;
- support message bodies;
- refund/private payment notes;
- screenshots of customer or payment-platform personal data.

## Gates preserved

APPROVAL REQUIRED: create or activate Stripe/Polar products, prices, payment links, live checkout, download hosting, API keys, test/live purchases, payout/bank/tax/KYC settings, or seller terms | payment, identity, and legal/tax boundary | Mark must complete the seller-side route personally and provide/verify the final non-secret checkout URL.

APPROVAL REQUIRED: send buyer emails, attach files to a platform, create a support mailbox/process, store buyer data, publish checkout links, remove `noindex,nofollow`, add analytics/email capture/affiliates/ads, or run outreach/launch posts | customer-data and public-exposure boundary | execute only after the route is verified and the action is within IronFrame scope.

## Definition of done for this readiness asset

- Email copy exists for manual fulfilment.
- Platform-hosted delivery copy exists.
- A Git-safe redacted ledger shape exists.
- Buyer PII and secrets are explicitly excluded.
- The package hash and checkout acceptance steps remain the controlling verification path.
