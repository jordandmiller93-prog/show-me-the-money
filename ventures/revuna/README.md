# Revuna

The actual business being built with the `/money-*` skills in this repo. Working name — not yet trademark/domain-checked (see ROADMAP.md Phase 1).

**What it is**: AI review-response agent for single-location local service businesses (dental clinics, med spas, salons). Drafts a reply to every new Google review in the owner's voice; owner approves in one tap. $19-39/mo, no contract — undercutting incumbents like Podium ($399-599/mo) and Birdeye ($299-449/mo) who sell to multi-location accounts via annual contracts and price out the single-location owner.

## Structure

- `STRATEGY.md` — the wedge, six-question validation, competitive intel, differentiation, 30-day plan, narrowest-bet statement (via `/money-discover`)
- `MARKET-RESEARCH.md` — full market sizing, competitor teardown, business model stress test, GTM plan (via `/money-strategy`)
- `CONCIERGE-SOP.md` — **how the business actually runs right now**, with zero infrastructure: manual reply drafting until paid signal justifies building automation
- `ROADMAP.md` — phased build plan with clear "you" vs "Claude" action items
- `site/` — static landing page (hosting deliberately on hold — not needed for concierge mode)
- `outreach/batch-1-real-leads.md` — 7 real, verified single-location dental practices, ready-to-read call scripts + 1 email

## Status

Operating in **concierge mode** (see `CONCIERGE-SOP.md`) — no dashboard, no OAuth, no Stripe needed yet. The only remaining step is mechanical: place the 7 calls / send the 1 email in `outreach/batch-1-real-leads.md`. Kill-switch check 2026-07-23 per STRATEGY.md.

Hosting and a standalone repo were both attempted and hit real external blockers this session (see ROADMAP.md) — deliberately deprioritized since neither is required to find out if this business works.

## Why this lives inside show-me-the-money

Multiple attempts to move this to its own `revuna` repo hit a stuck permission connector. Rather than keep fighting it, this stays here — a self-contained folder, easily copied out later if it ever matters.
