# Credentials AI — A Live, Revenue-Generating Business-Trust Product

**A separate, commercial product that is live and selling.** The funnel: **free AI Profile → verified lead engine → paid.** Real payments (Stripe) are hooked up. This is not a demo — it's a product in front of real local businesses, built end-to-end: front end, backend, payments, deployment, marketing.

> **The one-line pitch:** Give every local business a **hosted, AI-readable profile** — one AI tools and search engines can actually read — then prove they're real with a **verified trust badge**, and count every enquiry that comes through it.

## What it is

- **Free AI-search profile** — a hosted business profile (not a brochure) that AI tools, search engines and AI assistants can read and cite. What's your address, services, suburbs you cover, working hours, what you're verified for — structured, machine-readable, always current.
- **Verified lead engine** — a "get in touch" path (tap-to-call, request a quote) that captures interest as a **tracked enquiry**, so the owner sees exactly how many calls, emails and quote requests each profile produces.
- **Paid tier via Stripe** — a real monetised funnel, live.
- **Live at credentialsai.com.au** (company: erosium.com.au).

## The trust layer — ABN-verified TrustBadge

This is the part that separates it from a "business card website": credentials you can *prove*, not claim.

- **Verification against official data.** The system calls the **Australian Business Register (ABR) API** using a **registered ABR web-services GUID**. It validates the ABN's checksum locally, then queries the ABR live to confirm the ABN is **active and registered** to the business claiming it.
- **A stored verification snapshot.** The badge is rendered from a snapshot of what the ABR actually returned, so the verification page shows *what was checked and when* — it doesn't re-claim trust it can't back.
- **A TrustBadge with a live verification page.** When verified, the profile displays a **TrustBadge** ("ABN Verified by Credentials AI") that one click opens onto a **public verification page** — the source, the status, the timestamp. No "trust us"; proof people can check themselves.
- **Independent, honest framing.** Credentials AI is an **independent verification service, not a government body.** A TrustBadge is a record of checks, not an endorsement. That honesty is part of the build.

## AI-readable + shareable

- **AI-readable profile** — structured so machine agents (not just human eyeballs) can consume it. This is the "be read by AI search" positioning that's rare in a local-business product.
- **QR code kit** — owners get a QR they can put on the truck, the window, the job quote, so customers scan straight to the verified profile.
- **Embeddable badge** — the TrustBadge can be embedded on the business's own site showing the verification.
- **Profile theming** — the hosted profile supports branding (e.g. changing the profile colour) so it feels like the business's own page, not a generic template.

## Engineering depth

- **Real payments** — Stripe checkout wired and live; proves I can ship something people pay for.
- **ABR API integration** — live call to the official Australian Business Register using a registered GUID; ABN checksum validation + ABR status check; snapshot stored so the public page renders without hammering ABR.
- **Scanner-safe auth** — magic-link login that routes through a confirmation step so automated email scanners can't silently redeem a session.
- **Verified lead funnel** — free profile → ABN verification → tracked enquiry → conversion, with a live dashboard of leads.
- **First-party transactional email lane** — owns its own server email (dashboard access, order notifications, lead alerts) rather than depending on a third party.

## Screenshots

| What | Capture |
|---|---|
| Home page — live at credentialsai.com.au | [`credentialsai-com-au-homepage.png`](../portfolio-assets/credentialsai-com-au-homepage.png) |
| Magic-link (scanner-safe) authentication | [`credentialsai-1-magic-link-login.png`](../portfolio-assets/credentialsai-1-magic-link-login.png) |
| Auth handoff — protected dashboard entry | [`credentialsai-2-continue-dashboard.png`](../portfolio-assets/credentialsai-2-continue-dashboard.png) |
| Dashboard — lead view (top) | [`credentialsai-3-dashboard-top.png`](../portfolio-assets/credentialsai-3-dashboard-top.png) |
| Dashboard — lead view (bottom) | [`credentialsai-4-dashboard-bottom.png`](../portfolio-assets/credentialsai-4-dashboard-bottom.png) |

## The idea

**Data Presents. Human Decides.** It presents a verified profile and tracked enquiries; a human founder decides the next move. It's built to make a real business decision easy and honest — and to prove, in public, that a business is what it says it is.
