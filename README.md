# Isaac "Ike" Anasson — Proof of Work, Not a CV

**Self-taught AI systems builder.** 20 years in precision trade — stainless fabrication and TIG welding — taught me that *quality is a system, not a feeling*. I inspect. I verify. I certify. I don't guess.

In the last ~10 weeks, alongside a full-time job, I applied that same discipline to an entirely new domain: I **designed, built, and shipped** a multi-tenant AI platform from scratch, plus a separate commercial product with real payment processing. Real users. Real security. A real test suite (788/789 passing). **No CS degree — a builder who ships.**

> **The one idea that runs through everything I build:**
> **"Data Presents. Human Decides."**
>
> Machines should surface truth and options clearly. A human keeps the final decision. That's not just good design — it's the only honest way to put AI in front of real users.

---

## What this repo is

- **Screenshots and case studies** of systems I built and shipped — the live reality, not mockups.
- **Source code is intentionally private** — but these are real running systems, so you can see the actual result.
- Each system below has a case study (`case-studies/`) and a screenshot table.

---

## The systems

### 1. TYDAL — Multi-Tenant AI Agent Platform That Runs a Business *(flagship)*

Built from scratch and live. **You hand it your whole business** — customers, jobs, pricing, files, inbox. A **state machine** turns raw signals into a ranked "what needs the founder" view (approval queue, revenue/invoice tracking, time-based resurfacing) · **immutable data with provenance** (pristine, transportable, compounding, pre/post-reasoned, tamper-quarantining) · **shared jars** (cross-org, per-request re-scoping) · **AI CTO operator** (self-healing + calm founder surface). The assistant is an accountable member of the org — not a stateless chatbot. **Live Gmail: it ingests real email, drafts replies in your personality against your actual pricing/rules, and a human approves every send — right from your phone via a Telegram approval card.** Two products in one: a business brain that reasons over *your* memory jars, and a space where your *external* agents (OpenClaw, Hermes, anything) get their own ID, their own persistent memory box, and share jars with you cross-org. 788/789 tests green.

| What | Capture |
|---|---|
| Dashboard — the assistant saves to an immutable, provenance-tracked store | [`tydal-dashboard-save-memory.png`](portfolio-assets/tydal-dashboard-save-memory.png) |
| A "jar" (data space) with integrity-checked provenance | [`tydal-jar-provenance-prestine.png`](portfolio-assets/tydal-jar-provenance-prestine.png) |

**[Full case study →](case-studies/TYDAL.md)**

---

### 2. Credentials AI — Commercial Lead-Generation AI Product *(live, monetised)*

A revenue-oriented product: **free AI Profile → verified lead engine → paid**, with **Stripe checkout live**. Free AI-search profiles that verify a business exists, then convert interest into tracked enquiries.

| What | Capture |
|---|---|
| Home page — live at credentialsai.com.au | [`credentialsai-com-au-homepage.png`](portfolio-assets/credentialsai-com-au-homepage.png) |
| Magic-link (scanner-safe) authentication | [`credentialsai-1-magic-link-login.png`](portfolio-assets/credentialsai-1-magic-link-login.png) |
| Auth handoff — protected dashboard entry | [`credentialsai-2-continue-dashboard.png`](portfolio-assets/credentialsai-2-continue-dashboard.png) |
| Dashboard — lead view (top) | [`credentialsai-3-dashboard-top.png`](portfolio-assets/credentialsai-3-dashboard-top.png) |
| Dashboard — lead view (bottom) | [`credentialsai-4-dashboard-bottom.png`](portfolio-assets/credentialsai-4-dashboard-bottom.png) |

**[Full case study →](case-studies/CREDENTIALS-AI.md)**

---

### 3. RFQ OS — Request-for-Quote Workflow Engine

Turns voice/structure into a pre-screened, QC-checked, order-ready workflow. It's honest about what it doesn't know — it flags unknowns rather than guessing — and it never advances past a human founder gate.

| What | Capture |
|---|---|
| Voice → structured input | [`rfq-demo-1-voice-talk.png`](portfolio-assets/rfq-demo-1-voice-talk.png) |
| Generated, pre-screened form | [`rfq-demo-2-generated-form.png`](portfolio-assets/rfq-demo-2-generated-form.png) |
| Supplier pre-solve | [`rfq-demo-3-supplier-presolve.png`](portfolio-assets/rfq-demo-3-supplier-presolve.png) |

**[Full case study →](case-studies/RFQ.md)**

---

### 4. AI Email / Send System — Human-Approval Gates

Controlled send + inbox with a hard rule: **the model proposes, a human approves before anything goes out.** Exactly the safety-conscious agent design enterprise AI teams want to see.

| What | Capture |
|---|---|
| Draft step — composing with structured context | [`email-rail-1-draft-type.png`](portfolio-assets/email-rail-1-draft-type.png) |
| Structured input | [`email-rail-2-structured-input.png`](portfolio-assets/email-rail-2-structured-input.png) |
| The approval gate — Approve / Deny / Hold | [`email-rail-3-approval-gate.png`](portfolio-assets/email-rail-3-approval-gate.png) |
| Approver review screen with provenance | [`email-rail-4-approver-review-screen.png`](portfolio-assets/email-rail-4-approver-review-screen.png) |

**[Full case study →](case-studies/EMAIL-RAIL.md)**

---

### 5. Rubik Resilience — Disaster-Risk Evidence System

Suburb-level risk scoring that backs every conclusion with an "evidence ladder" — sources you can climb, not a black box. Flags MONITOR / INVESTIGATE / ESCALATE.

| What | Capture |
|---|---|
| Triage dashboard — risk view | [`rubik-resilience-triage-dashboard.png`](portfolio-assets/rubik-resilience-triage-dashboard.png) |
| Evidence ladder — every claim traceable to a source | [`rubik-resilience-evidence-ladder.png`](portfolio-assets/rubik-resilience-evidence-ladder.png) |

**[Full case study →](case-studies/RUBIK.md)**

---

### 6. Recognition — Gold Coast Innovation Hub Open Data Challenge (disaster resilience)

Built under the "Data Presents. Human Decides." philosophy. **Recognised at the Gold Coast Innovation Hub Open Data Challenge (disaster resilience); pitched live on stage.** To be fully honest: the hosts never publicly announced formal rankings, so I describe this as *recognised* — not "winner."

| What | Capture |
|---|---|
| Live stage pitch — decision gates | [`odc-stage-pitch-decision-gates.jpg`](portfolio-assets/odc-stage-pitch-decision-gates.jpg) |
| Stage pitch — hero | [`odc-stage-pitch-hero.jpg`](portfolio-assets/odc-stage-pitch-hero.jpg) |
| On-stage with a Gold Coast City Council representative (a council disaster-management judge voted for the entry) | [`odc-prize-with-councillor-1.jpg`](portfolio-assets/odc-prize-with-councillor-1.jpg) |

**[Full case study →](case-studies/ODC-OPEN-DATA-CHALLENGE.md)**

---

## The through-line: "Data Presents. Human Decides."

- **TYDAL** — the assistant surfaces truth and options; the human owns the space and can revoke the assistant. Immutable stores mean the record can't quietly change.
- **Credentials AI** — presents verified business profiles and tracked enquiries; a human founder decides the next move.
- **RFQ OS** — flags what it doesn't know rather than guessing, and stops at the founder gate.
- **AI Email** — never sends on its own; a human approves every send.
- **Rubik Resilience** — every risk score is backed by an evidence ladder; a person reads it and decides to monitor, investigate, or escalate.

Machines present. Humans decide. Everywhere.

---

## About me

- **Location:** Gold Coast QLD — train-reachable to Brisbane.
- **Background:** 20 years precision trade (stainless fabrication, TIG welding) + NDT Level 2 (AINDT). Same discipline — inspect, verify, certify — now applied to building AI systems.
- **What I'm looking for:** hands-on AI / software-adjacent roles where I can ship real systems to production.
- **Contact:** isaac@erosium.com.au

---

*All captures above are from real, live deployed systems. Source code is intentionally kept private — see the individual case studies for the engineering depth.*
