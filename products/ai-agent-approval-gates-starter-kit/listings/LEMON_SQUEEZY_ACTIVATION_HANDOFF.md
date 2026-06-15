# Lemon Squeezy Activation Handoff — Approval Gates Starter Kit

Status: ready for authenticated seller-platform execution; no listing/payment activation completed
Date: 2026-05-20
Owner: Rhysand / IronFrame

## Current blocker

Lemon Squeezy still presents an unauthenticated sign-in page at:

`https://app.lemonsqueezy.com/products`

Rhysand must not type passwords, select personal accounts, create credentials, complete tax/payment setup, or improvise around sign-in. Continue only when an IronFrame-controlled authenticated Lemon Squeezy seller session or least-privilege API route is available.

Before creating or publishing anything, run `SELLER_SESSION_PREFLIGHT_2026-05-31.md`. Mark's standing IronFrame authority permits seller-platform activation/listing management when the route is IronFrame-controlled and no hard gate is hit; it does not permit password/2FA/tax/banking/identity handling, paid features, wrong-country/currency activation, or high-liability commitments.

## Product package to upload

Zip:

`content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`

SHA256:

`01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`

Manifest:

`content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/PACKAGE_MANIFEST.md`

## Public seller identity

Use public brand:

`IronFrame`

Do not expose Mark/family/private/defence details in listing copy, support copy, or product metadata.

## Listing fields

### Product name

AI Agent Approval Gates Starter Kit

### Product type

Digital download / template pack

### Launch price

£9

Normal price candidate after validation: £19.

Do not add discounts, coupons, affiliates, bundles, upsells, subscriptions, or order bumps unless separately approved.

### One-line promise

Give your AI agents clear permission boundaries before they touch publishing, money, customer messages, secrets, deletion, production systems, or trading.

### Short description

A practical template pack for founders and operators who want to delegate to AI agents without vague permission boundaries.

### Full description

AI agents are becoming useful enough to delegate research, drafting, coding, content preparation, and operations work. The danger is not that they become evil. The danger is that they are given vague permission and quietly cross a line.

This starter kit gives founders a simple local operating system for agent boundaries:

- Green actions the agent may usually perform locally.
- Amber actions that require explicit approval.
- Red actions prohibited by default.
- Evidence required before work is marked complete.
- Task card and risk register templates.

Included files:

- Printable Approval Gate Checklist PDF.
- Editable Markdown checklist.
- Founder AI autonomy policy template.
- Agent task card template.
- Risk register template.
- Start-here guide, changelog, and use/licence notes.

This product provides operational templates only. It is not legal, financial, tax, cybersecurity, compliance, investment, employment, or trading advice. You remain responsible for how you configure, supervise, and authorise AI tools.

### Tags / keywords

AI agents, automation, founder operations, Claude Code, Codex, AI governance, checklists, templates, approval gates, agent safety

## Preview assets

Use these seller-platform-ready PNG assets if Lemon Squeezy requests product images:

- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/assets/preview-product-cover.png`
- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/assets/preview-checklist.png`
- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/assets/preview-task-card.png`
- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/assets/preview-risk-register.png`

Source SVGs remain in the same asset folder. PNG export evidence and hashes are recorded in `assets/README.md` and `logs/2026-05-27-starter-kit-preview-png-assets.md`.

## Refund wording

Because this is a digital template pack, refunds are available for accidental duplicate purchases or clear technical access/download problems within 14 days. If the templates are materially not as described, contact support with the issue and we will either fix access, provide the corrected files, or refund the order.

## Support boundary

Included support is limited to download/access issues and corrections to the supplied files. It does not include custom implementation, legal/compliance review, agent setup, security audit, automation buildout, or personal/business consulting.

## Listing settings to keep closed

Do not enable unless Mark separately approves:

- affiliates;
- analytics/pixels/cookies;
- email capture/newsletter automation;
- paid ads;
- public posting/distribution campaign;
- coupons/discount codes;
- upsells/order bumps;
- subscriptions;
- paid credits or external generation;
- any claim of guaranteed legal/compliance/security/income outcome.

## Smoke test after listing creation

After listing exists:

1. Copy the checkout/product URL.
2. Open it in a private/non-authenticated browser context if possible.
3. Verify product name, price, refund/support/disclaimer copy, and file attachment.
4. If Lemon Squeezy offers test mode, run a test checkout and verify download access.
5. If no test mode is available without real payment, do not self-purchase unless Mark separately approves a real-money test.
6. Record the verified listing URL and test result in a dated log.

## Public preview update after verification only

Only after a verified Lemon Squeezy URL exists:

- update the private IronFrame product page and public preview repo with one `Buy the Starter Kit` CTA;
- keep the free checklist visible;
- keep `noindex` and `robots.txt Disallow: /` unless Mark approves broader distribution;
- do not add analytics, email capture, cookies, pixels, affiliate links, or public posting;
- crawl the public preview and verify the payment link resolves to the approved listing.

## Resume command for Rhysand

Once Mark has authenticated the IronFrame Lemon Squeezy seller dashboard, say:

`Continue from the Lemon Squeezy dashboard for the Approval Gates Starter Kit.`

Rhysand should then create/upload the listing from this handoff, verify the URL, update the preview only after verification, commit, push, and report gates still closed.
