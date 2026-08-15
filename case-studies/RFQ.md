# RFQ OS — A Supplier-Aware Request-for-Quote Engine (Two Operating Modes)

**A Request-for-Quote (RFQ) workflow engine** — real business-process automation, not a chatbot. It turns spoken/loose input into a **structured, pre-screened, QC-checked, order-ready** workflow that is honest about what it doesn't know and **never contacts a supplier or fires an order without a human approving first.**

## What it is

- **Voice → structured** — captures a requirement the way a person naturally describes it and turns it into a structured request.
- **PreScreen → QC → order draft** — validates and shapes the request, quality-checks it, then produces the draft ready for the next human gate.
- **Honest about unknowns** — it flags gaps and uncertainties rather than quietly guessing. That's the discipline real supply chains depend on.
- **Supplier-respectful by design** — it's *research-only* by default: it can prescreen suppliers but does **not** contact them, and no order ever goes out without the founder's sign-off.

## Two operating modes

The platform runs the same core engine in two delivery modes, so it fits different customers' comfort levels:

1. **Bring-Your-Own-Key (BYOK) mode** — the customer supplies their own AI/search credentials into an **encrypted vault** (AES-GCM). The platform charges a **platform subscription** rather than riding the customer's key spend, and it never mounts its own company keys on the tenant's path. That's a hard security boundary enforced at boot: if the service detects company keys in a BYOK tenant environment, it refuses to run. *(The billing lifecycle is engineered in, but this lane is not yet a live payment rail — see engineering depth.)*
2. **Managed AI mode** — the supplier of the platform provides the AI on the customer's behalf, so the customer gets the same pre-screen / QC / order-draft pipeline without needing to wire up their own keys.

Same workflow engine underneath; the trust model (whose keys, who pays for inference) is what changes between the two.

## Engineering depth

- **AES-GCM encrypted BYOK vault** — the customer's search/AI keys are encrypted at rest; vault supports list / put / revoke / test / resolve-check.
- **Zero-vendor-key offline path** — a requirement can be pre-screened **offline with no vendor keys mounted at all**, with a live BYOK upgrade path only when the user's vault key, an active platform subscription, and a budget arm are all in place.
- **Env-class security boundary** — `internal_demo` (company keys, dogfood only) vs `test_mock` (unit tests, no keys) vs `pilot_product` (tenant path, company keys forbidden) are enforced, not aspirational.
- **Platform billing logic** — a subscription lifecycle (activate / past-due / cancel) with budget arms and caps is engineered into the product so usage can't run away. **To be clear: this is the billing *model*, not a live payment rail** — no live card-charging is wired to real customers yet.
- **Operator UI** — vault, subscription and budget are managed through a product shell, not raw config.
- **Data portability + audit** — export and full org delete are first-class API endpoints, so a customer can leave cleanly with their data.
- **Real test + secret hygiene** — 64/64 tests plus an automated secret-scanner gate before any pilot runs.
- **State-machine gates, not a single prompt** — a real business process encoded as steps; a human founder approves before any order.

## Screenshots

| What | Capture |
|---|---|
| Voice → structured input | [`rfq-demo-1-voice-talk.png`](../portfolio-assets/rfq-demo-1-voice-talk.png) |
| Generated, pre-screened form | [`rfq-demo-2-generated-form.png`](../portfolio-assets/rfq-demo-2-generated-form.png) |
| Supplier pre-solve | [`rfq-demo-3-supplier-presolve.png`](../portfolio-assets/rfq-demo-3-supplier-presolve.png) |

## The idea

**Data Presents. Human Decides.** RFQ OS flags what it doesn't know rather than guessing, respects suppliers by default, keeps the customer's keys their own, and stops at the founder gate before anything is sent or ordered. That's the difference between automation that's trustworthy and automation that's just fast.
