# TYDAL — Multi-Tenant AI Agent Platform That Runs a Business

**The flagship.** A multi-tenant, cross-organisation AI system built from scratch and shipped to production — in about 10 weeks, alongside a full-time day job.

TYDAL isn't a chatbot demo. It's an **agent platform you hand your whole business to** — customers, jobs, pricing, files, inbox — where the AI is an accountable member of your organisation, data is immutable and provenance-checked, and **a human approves every decision that matters.**

## ⚙️ It runs a business: customers, jobs, pricing

The deepest layer is an **operational state machine** that turns raw business signals into a ranked, actionable founder view. Throw your files and conversations in, and it works out what kind of business you are and what actually needs you.

- **It reads the room.** Put your files in and it reasons out what business you're in — *"you're a plumbing business, four staff, these are your customers, this is your sales pipeline"* — and assigns everything to the right object (customer / job / opportunity / invoice).
- **A state machine under the hood.** A 10-transition state machine with **8 enforced invariants** and append-only, idempotent events — the database itself **refuses illegal state changes**. 18/18 engine tests green, plus a full priority-engine test suite on top.
- **The "what needs me right now?" engine.** A priority router that scores every open item. It's got real business logic baked in:
  - **Customers outrank tech-tinkering.**
  - **Money on the table lifts a conversation.**
  - A fade guard lets stale junk age out so the queue stays truthful, not noisy.
- **Approval queue / "waiting on you."** Every action that needs a founder decision surfaces in a ranked queue, with **time-based resurfacing** — things you've let slip come back so nothing dies quietly.
- **Revenue, invoices and pricing wired in.** The business's own pricing rules feed the engine, and `invoice.paid` events flow straight in and move the state.
- **Email woven underneath.** Drafts, send, and invoice awareness all live under the same state model — the email rail is one worker in the machine, not a separate app.

## 🧬 Immutable data with provenance (the "machine never chews your words")

The data layer is built so the record **can't quietly change underneath you**:

- **Pristine** — exact text is never truncated, enforced at ingest so what you said is what's stored.
- **Transportable** — exports carry a fingerprint so a receiver can prove what they actually got.
- **Compounding** — a reasoned conclusion keeps a chain of custody back to every source it was built from.
- **Pre- and post-reasoned** — export, reason elsewhere, then re-import is verified before it lands, still marked untrusted.
- **WITH PROVENANCE** — a sealed, re-verified envelope; any drift is caught and quarantined on return.

Live receipts: 65/65 records in one canonical format · 0 drifted · the store **refuses illegal state changes** · tamper a sealed export and it fails · cite a source you never wrote and you're quarantined.

## 🤝 Shared jars — separate orgs, deliberate sharing

- **Cross-org, multi-tenant.** Each organisation keeps its own secure space with **per-request re-scoping** — one org can never see another's data.
- **You share what you choose.** Cross-org sharing is scoped and deliberate — a member sees exactly what they've been granted, nothing else.
- **Real user verified end-to-end.** A non-technical family member was onboarded with her own secure space and verified a download landed in Finder the same day — *"the download button worked, it landed in Downloads."* A real human using a real product, verified first-hand.

## 🧠 Two products, one platform — your business brain, and your agents

**1. The business brain.** You get an LLM inside TYDAL you talk to every day. It runs the business: it ingests your email, reasons over **your** jars — your memories, your documents, your saved words — drives the state machine, drafts replies, and acts as your AI CTO. The memory is **yours, not the brain's**: the jars are your durable record, so swap the model (DeepSeek today, Claude tomorrow) and nothing is lost.

**2. The agents' own space.** TYDAL can give **other agents — outside TYDAL entirely** — their own identity and their own space inside the team. That agent (an OpenClaw agent, a Hermes agent, anything) gets its own jars: **a persistent memory box it writes into**, that the platform it actually runs on points back to. You and that agent share memories across organisations.

**The point of it.** This isn't a document store — it's a store of *lived memory shared between humans and their agents*, permissioned, durable, portable across any platform. Your business brain runs your business; your agents carry a memory that outlives any runtime.

## 🛡️ The AI CTO operator — self-healing + a calm founder surface

- A **founder attention surface** — the answer, in five seconds, to: *is it healthy? what needs me? what changed? what next?*
- **Self-healing infrastructure** — endpoints are watched, hiccups are auto-healed, and the founder gets a calm notification, not a fire drill. Live System Health endpoint responding.
- **Human owns every gate** — nothing irreversible happens without approval. The machine presents; a human decides.

## 📲 It reaches you — Telegram alerts for the things that need you

This is the bit nobody else builds: the AI doesn't sit waiting in a dashboard — **it comes to you.**

- **"What needs you?" right now.** Instead of you checking a screen, the system pushes the founder a heads-up on what actually needs a decision.
- **"Draft ready — your call."** When an email reply is drafted, an approval card lands in the founder's **Telegram** with approve / deny wired to the real approval record — you can run the whole approval gate off your phone.
- **Health alerts, not fire drills.** If something in the infrastructure hiccups, you get a calm alert — including the security lane (a planted honeypot being touched fires a red alert to the same channel). You hear about the real things, and only the real things.
- **You arm it, not the machine.** The whole alert lane is a founder-flipped switch — the system is silent until *you* turn it on.

## 📧 Email that knows your business — live Gmail, human-approved

The strongest proof it's real: TYDAL is connected to a live Gmail inbox and works it like a member of the team.

- **Ingests real email.** It polls the connected Gmail inbox (Google Gmail API), reads the full message body — not the truncated preview — and turns every new message into a tracked item in the business state machine. Senders are auto-labelled by domain and matched against your CRM.
- **It drafts in your personality, against your rules.** Every reply is drafted in the founder's own plain-English style, driven by a business knowledge base: pricing, signup, and discount policy — "don't quote a discount, keep the decision with the founder." It ignores signature blocks, flags spam and notifications as no-reply, and recalls what it already knows about that contact from memory.
- **Then a human approves every send.** The mail never goes out on its own — "AI drafted a reply · edit or send as-is · you approve every send." Approve / Deny / Hold is structural, not a suggestion.
- **Approve from your phone.** When a draft is ready, the founder gets a **"Draft ready — your call"** card pushed straight to Telegram — see the *It reaches you* section below. The gate travels with you, and it's founder-flipped, not machine-flipped.
- **Attachments work both ways.** Files land in the system with a real download path (a non-technical user verified an upload landed in her Finder the same day), and you can add files to a reply and send them out with it — approved, like everything else.

## Engineering depth

**This is a shipped platform with a running engineering log, not a marketing page.** Highlights from what's actually built and verified — described by capability, not mechanism:

- **Multi-tenant isolation, enforced not assumed.** Every tenant's access is re-scoped to their authenticated organisation across the whole system — one org can never read another's data. A non-technical real user was onboarded into her own fully-separated org and verified a file landing in her local Downloads — the hardest test there is.
- **Cross-org shared spaces with a permission matrix.** Shared data spaces carry per-member roles (view / edit) enforced by a live read-gate: a member sees shared-and-granted spaces only, private spaces stay dark, only the owner removes, and every grant is deliberate. Identity comes from the real authenticated session, not a hardcoded user.
- **Immutability with provenance, law-enforced.** The system refuses illegal state changes and keeps an append-only event log. Verbatim text is pinned at ingest so the original words are never truncated or rewritten; exports carry a fingerprint; reasoned conclusions keep chain-of-custody back to their sources; a tampered sealed export is detected and quarantined on return. **Nothing is ever silently destroyed** — retiring a record de-activates it while its history is preserved.
- **A consent system that treats memory-writes as external actions.** A durable record of what a human says is captured into a scratchpad, but **requires an explicit ask** before it enters a shared/contact space. The guard is deterministic at the single write path, so an inbound email saying "remember this" cannot silently steer a save — intent can't be written around.
- **A knowledge base with a controlled edit door.** The rules that steer live customer email (pricing, discount policy, signup wording) are governed, not hardcoded: one controlled way to change them, changes carry a recorded reason, staleness is measured, and every change is auditable. The founder's exact words steer any customer reply.
- **State machine with enforced integrity.** Transitions are governed by invariants the system refuses to violate; a priority engine scores what needs the founder (customers outrank tinkering, money lifts a conversation, stale junk ages out); revenue and invoice events move state directly.
- **Email rail as one worker in the machine.** Full send and read-back of emails with real attachments, a duplicate-send guard, a retry that never drops the file, mark-as-read on the chat card, and archive enforcement across every surface so nothing resurrects.
- **Active security posture.** Planted trap credentials trigger a red alert if ever touched; checks that catch accidental secrets run before deploys; environment classes keep the way you run it yourself separate from the way it runs for tenants.
- **Systems thinking end to end** — state machine, priority engine, provenance layer, consent system, multi-tenant isolation, operator surface, and email all working as one governed system.
- **788/789 automated tests passing** — a rigorous, continuously maintained suite. A real platform, not a demo.

## The idea

**Data Presents. Human Decides.** The assistant surfaces truth and options; the human owns the space, can revoke the assistant, and approves every decision that matters. "The machine never chews your words" is the law underneath it — for customers, for jobs, and for the agent itself.
