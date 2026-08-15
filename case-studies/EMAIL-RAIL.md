# AI Email System — Human-Approval Send + Inbox, Production-Proven

**A controlled send + inbox system** with a hard, non-negotiable rule: **the model proposes, a human approves before anything goes out.** This is the safety-critical agent design enterprise AI teams specifically look for — and it's been **used for Ike's real daily email**, not a mockup.

## What it is

- **Live Gmail ingestion** — it reads real inbound email (accounts configured through the platform).
- **Drafting with structured context** — the model composes from the right source material: your actual pricing, rules, and personality, not a generic bot voice.
- **A controlled send rail** — nothing is auto-sent, ever. Every outbound message lands on an **Approval card**.
- **Approve / Deny / Hold** — the human founder makes the final call on every single send.
- **Remote approval** — the approval card reaches Ike **on his phone via Telegram**, so he can approve a real send from anywhere, not just at a desk.
- **Provenance labels** — the approver sees *where* the content came from before deciding, so a decision is informed, not blind.

## Production-hardening (the "it actually works under real use" layer)

- **Attachments end-to-end.** Full compose + read with real attachments (photo, PDF, document) — they ride the same approval lane, and Gmail registers them as genuine attachments. Verified live: sent a real email with a photo attached and confirmed it on the receiving side. Also reads attachments back: a received email with a file lands a card with a 📎 that **opens in two clicks**.
- **Duplicate-send guard.** A confirmed-send dedupe stops the same message firing twice on a flaky connection — a genuine reliability bug that was found and killed, not swept under the rug.
- **Retry keeps the file.** If a send fails on a blip, the retry **doesn't drop the attachment** or ghost the draft — it steers back to the safe approval card where the file is preserved.
- **Mark-as-read from the chat card.** Open an inbound email from the rail → **📖 Mark as read** right on the card → it settles as Resolved and stops re-surfacing. No hunting through a decisions queue.
- **Attachment snapshot after send.** Each sent email records exactly what was attached (filename, type, size) — evidence written *after* Gmail confirms, so the record matches reality.
- **Multi-lane archive enforcement.** Deleted/archived items are excluded consistently across every surface (home rail, chat rail, decision view, search) — no "phantom" resurfacing.

## Engineering depth

- **Human in the loop by design** — the approval gate is structural, baked into the send lane, not a suggestion.
- **Provenance-aware** — the approver reviews not just the message but its source and attachments, so decisions are informed.
- **Safety-first agent design** — the pattern that matters when AI touches real outbound communication.
- **Test-backed** — a real suite guards the send lane (dedupe, attachment integrity, mark-as-read), not hand-waving.

## Screenshots

| What | Capture |
|---|---|
| Draft step — composing with structured context | [`email-rail-1-draft-type.png`](../portfolio-assets/email-rail-1-draft-type.png) |
| Structured input | [`email-rail-2-structured-input.png`](../portfolio-assets/email-rail-2-structured-input.png) |
| The approval gate — Approve / Deny / Hold | [`email-rail-3-approval-gate.png`](../portfolio-assets/email-rail-3-approval-gate.png) |
| Approver review screen with provenance | [`email-rail-4-approver-review-screen.png`](../portfolio-assets/email-rail-4-approver-review-screen.png) |

## The idea

**Data Presents. Human Decides.** The AI Email system never sends on its own — a human approves every send. That's the responsible-agent principle applied to one of the highest-consequence surfaces there is, and it's had real emails through it.
