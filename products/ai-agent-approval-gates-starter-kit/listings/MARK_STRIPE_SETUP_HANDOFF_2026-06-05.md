# Mark-side Stripe setup handoff — Approval Gates Starter Kit

Date: 2026-06-05
Status: waiting for Mark-side Stripe access/setup
Agent boundary: Rhysand can prepare copy and patch after a verified URL; Rhysand must not handle password, 2FA, KYC, banking, tax, API keys, or live payment creation.

## Goal

Create a Stripe-first route for first cash flow on:

- Product: `AI Agent Approval Gates Starter Kit`
- Price: `£9.00 GBP`
- Type: one-time digital download/template pack

Preferred route:

1. Stripe Managed Payments + Payment Links.
2. Polar if Stripe Managed Payments is unavailable.
3. Standard Stripe only if Mark accepts tax/fulfilment responsibility.

## Mark-side steps

1. Open Stripe Dashboard under the intended IronFrame/Mark-controlled account.
2. Check whether **Managed Payments** is available.
3. If available:
   - activate Managed Payments;
   - accept terms;
   - select eligible digital/software/template product category;
   - complete all Stripe account activation requirements.
4. Complete personally if prompted:
   - password/2FA;
   - KYC/business verification;
   - tax/liability choices;
   - bank/payout details;
   - statement descriptor;
   - terms and compliance prompts.
5. Create or prepare live Payment Link only when comfortable with:
   - product name;
   - £9 GBP one-time price;
   - customer email collection;
   - success/thank-you/download route;
   - refund/support wording.
6. Send Rhysand the verified checkout URL only after opening/checking it yourself.
7. Send only non-secret listing facts: checkout URL, platform name, product name, price/currency, fulfilment route, and support/refund/disclaimer text. Do **not** send API keys, account IDs, dashboard-private URLs, customer emails, bank/tax/KYC details, or URLs containing prefilled email/token/key/code/client-secret query parameters.

## Copy to use

Product name:

`AI Agent Approval Gates Starter Kit`

Short description:

`Practical approval-gate templates for AI-agent workflows: spend gates, credential gates, live-publish gates, safety checks, and operator handoff prompts.`

Longer buyer copy:

`A self-serve template pack to help founders/operators decide what AI agents can do automatically, what needs approval, and what must never be delegated. Includes editable checklists, task-card templates, policy examples, risk-register prompts, and a quickstart guide.`

Disclaimer:

`Operational templates only. Not legal, financial, tax, cybersecurity, compliance, investment, employment, or trading advice. No revenue, safety, compliance, or agent-performance guarantee.`

Support boundary:

`Digital download only. Includes self-serve templates and quickstart docs. Does not include custom implementation, account setup, legal/compliance review, or agent deployment.`

## Package reference

Zip:

`content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip`

SHA256:

`01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`

## When Mark sends the URL

Rhysand will:

1. Verify URL format and product copy from browser view where accessible.
2. Patch the public preview CTA.
3. Preserve noindex/no analytics/no email capture unless separately approved.
4. Deploy/update preview if appropriate.
5. Record activation log and verification evidence.
