# Revuna

The actual business being built with the `/money-*` skills in this repo. Working name — not yet trademark/domain-checked (see ROADMAP.md Phase 1).

**What it is**: AI review-response agent for single-location local service businesses (dental clinics, med spas, salons). Drafts a reply to every new Google review in the owner's voice; owner approves in one tap. $19-39/mo, no contract — undercutting incumbents like Podium ($399-599/mo) and Birdeye ($299-449/mo) who sell to multi-location accounts via annual contracts and price out the single-location owner.

## Structure

- `STRATEGY.md` — the wedge, six-question validation, competitive intel, differentiation, 30-day plan, narrowest-bet statement
- `ROADMAP.md` — phased build plan with clear "you" vs "Claude" action items
- `site/` — static landing page (deploy free via Vercel, see ROADMAP.md Phase 1)
- `outreach/` — cold email template (CAN-SPAM checklist included) + sample AI-drafted review replies for demos

## Status

Phase 0 (strategy + landing page + outreach assets) complete. Next: Phase 1 — get the landing page live (needs a free Formspree + Vercel signup from Jordan), then Phase 2 — send the narrowest-bet outreach batch by 2026-07-16.

See `ROADMAP.md` for the full plan.

## Why this lives inside show-me-the-money

This repo's GitHub integration is scoped to a single repository and can't create new repos directly, so the venture lives in this subfolder for now. It's a self-contained folder — nothing here depends on the `skills/` tooling above it — so it can be extracted to its own repo anytime by copying this directory.
