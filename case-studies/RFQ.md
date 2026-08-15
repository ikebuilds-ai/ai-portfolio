# RFQ OS — Request-for-Quote Workflow Engine

**A Request-for-Quote (RFQ) workflow engine** — business-process automation and data pipelines, not just a chatbot. It turns spoken/loose input into a **structured, pre-screened, QC-checked, order-ready** workflow.

## What it is

- **Voice → structured** — captures a requirement the way a person naturally describes it.
- **PreScreen** — validates and shapes it before it moves down the pipeline.
- **QC → order draft** — quality-checks the output, then produces the draft ready for the next gate.
- **Honest about unknowns** — it flags what it doesn't know rather than quietly guessing (see `OFFLINE_MOCK` and the "unknown-flagging" behaviour). That's the discipline real supply chains depend on.

## Screenshots

| What | Capture |
|---|---|
| Voice → structured input | [`rfq-demo-1-voice-talk.png`](../portfolio-assets/rfq-demo-1-voice-talk.png) |
| Generated, pre-screened form | [`rfq-demo-2-generated-form.png`](../portfolio-assets/rfq-demo-2-generated-form.png) |
| Supplier pre-solve | [`rfq-demo-3-supplier-presolve.png`](../portfolio-assets/rfq-demo-3-supplier-presolve.png) |

## Engineering depth

- **Workflow / state automation** — a real business process encoded as steps and gates, not a single prompt.
- **Unknown-flagging** — the system is built to surface gaps and uncertainties instead of papering over them.
- **Founder (human) gate** — nothing advances to an order without a human decision. The machine prepares; a person approves.

## The idea

**Data Presents. Human Decides.** RFQ OS flags what it doesn't know rather than guessing, and stops at the founder gate. That's the difference between automation that's trustworthy and automation that's just fast.
