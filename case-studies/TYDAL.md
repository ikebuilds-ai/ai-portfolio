# TYDAL / "Brain Portal" — Multi-Tenant AI Agent Platform

**The flagship.** A multi-tenant, cross-organisation AI system built from scratch and shipped to production — in about 10 weeks, alongside a full-time day job.

## What it is

Not a chatbot demo. It's an AI **agent platform** where the assistant exists as its own accountable member of an organisation:

- The AI has **durable memory** and an **agent identity** — it's revocable, and it's answerable to the human who owns the space.
- Data lives in integrity-checked "jars" with provenance tracking — the record is **verifiable and tamper-evident**. This is the "the machine never chews the words" principle: what was said and stored stays exactly as it was.
- **Multi-tenant with per-request security re-scoping** — one organisation can never see another's data, and a real cross-org access leak was found and sealed.

## Screenshots

| What | Capture |
|---|---|
| Dashboard — the assistant saves to an immutable, provenance-tracked store | [`tydal-dashboard-save-memory.png`](../portfolio-assets/tydal-dashboard-save-memory.png) |
| A "jar" (data space) with integrity-checked provenance | [`tydal-jar-provenance-prestine.png`](../portfolio-assets/tydal-jar-provenance-prestine.png) |

## Engineering depth

- **788/789 automated tests passing** — a real test suite, not a demo.
- **Real debugging** — diagnosed and closed a subtle **4-surface file-disposition bug** (a browser download silently failed across four separate code paths) by auditing actual code, not guessing.
- **Cross-org save-routing fix** — when a save landed in the wrong organisation, the routing predicate was fixed at the root so one reusable rule governs all rescoping.
- **Real user verified end-to-end** — a tradesperson's family member (non-technical) was onboarded with her own secure space and verified a download landed in Finder **the same day** ("the download button worked, it landed in Downloads"). This is the hardest test there is: a real, non-technical human using it in anger.

## The idea

**Data Presents. Human Decides.** The assistant surfaces truth and options; the human owns the space and can revoke the assistant. Immutable stores mean the record can't quietly change underneath anyone.
