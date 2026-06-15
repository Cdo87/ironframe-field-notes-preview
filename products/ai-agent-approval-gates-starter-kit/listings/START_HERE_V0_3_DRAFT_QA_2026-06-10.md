# START_HERE v0.3 draft QA — Approval Gates Starter Kit

Date: 2026-06-10  
Owner lens: Feyre / Gwyn / Rhysand  
Status: local QA note; no package rebuild, checkout change, seller-platform action, public update, email capture, analytics, or buyer/customer-data action

## Selected movement

`SYSTEM_TODO.md` TODO-009 remains the highest-priority unblocked Product Forge movement while TODO-006 is seller-side blocked by Stripe/Polar account, KYC, tax, banking, payout, and live-payment setup.

Today's AI-income run already converted repeated AIOS/agent-loop/creative-agency signals into a no-rebuild `START_HERE` v0.3 draft. This QA note is the bounded daily processor movement: decide whether the draft is safe to keep as a future package candidate without disturbing the sellable v0.2 package/hash.

## Files inspected

- `SYSTEM_TODO.md`
- `APPROVALS.md`
- `TASKS.md`
- `DECISIONS.md`
- `CRON_REGISTER.md`
- `revenue_streams/ai-income-intelligence/adoptions/2026-06-10/MORNING_AI_INCOME_TEARDOWN_AND_ACTIONS.md`
- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/listings/START_HERE_V0_3_DRAFT_2026-06-10.md`
- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/PACKAGE_MANIFEST.md`
- `content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2/START_HERE.md`

## QA verdict

Verdict: **keep as v0.3 candidate; do not rebuild yet.**

Reason:

- It improves the buyer's first 10 minutes by making the Green / Amber / Red permission setup more explicit.
- It repeats the support and disclaimer boundary instead of widening the promise.
- It does not introduce checkout links, public URLs, email capture, analytics, seller-platform dependencies, private details, or external calls to action.
- It explicitly says not to copy into the v0.2 build folder and not to change the v0.2 package hash yet.
- It should only become packaged content after Mark's seller route is unblocked or after a deliberate v0.3 rebuild decision.

## Verification run

```bash
cd /Users/edi/IronFrame
python3 scripts/product_forge_checkout_acceptance.py \
  --html content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/sales-page.html \
  --allow-no-checkout

shasum -a 256 \
  content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/build/v0.2/ironframe-ai-agent-approval-gates-starter-kit-v0.2.zip

python3 - <<'PY'
from pathlib import Path
p=Path('content/ironframe-field-notes/products/ai-agent-approval-gates-starter-kit/listings/START_HERE_V0_3_DRAFT_2026-06-10.md')
s=p.read_text()
checks={
 'has_no_http_url': 'http://' not in s and 'https://' not in s,
 'has_no_email_marker': '@' not in s,
 'states_no_rebuild': 'do **not** rebuild package' in s,
 'keeps_v02_hash_stable': 'Do not copy it into the v0.2 build folder yet' in s,
 'includes_support_boundary': 'does not include custom implementation' in s,
 'includes_external_exposure_stop_rules': 'External exposure includes' in s,
}
print('START_HERE_V0_3_DRAFT_QA')
for k,v in checks.items():
    print(f'{k}: {"PASS" if v else "FAIL"}')
print('chars:', len(s))
if not all(checks.values()):
    raise SystemExit(1)
PY
```

Observed result:

- Checkout acceptance: `PASS` with `allow_no_checkout: true`, `form_tag_count: 0`, `script_tag_count: 0`, `payment_like_hrefs: []`, and `robots: ["noindex,nofollow"]`.
- v0.2 zip SHA256: `01c29fa10b5eb9e76157a4663850b0adbfc4e7d9241195776a1fbc07b5f9e0ef`.
- Draft QA checks: all `PASS`; character count `5554`.

## Next safe Product Forge action

If no verified Stripe/Polar checkout URL exists next run, do **not** rebuild v0.3 or create the AI Autonomy Starter Bundle. Re-run the package hash + checkout acceptance checks, or prepare the exact post-checkout public-preview patch only after Mark provides a verified non-secret checkout URL.

## Gates preserved

No seller-platform listing, checkout URL, payment link, public update, email capture, analytics, outreach, buyer email, customer data, paid tool, account creation, secret handling, tax/banking/payout/KYC action, or package hash change occurred.
