# Fundwell — operating procedure

Mirrors Revuna's `CONCIERGE-SOP.md` pattern: zero infrastructure needed to serve the first clients. Claude does the actual grant-writing work directly in a Claude Code session.

## The loop

1. **A lead says yes to the $450 Breva Thrive application** (or another grant, once sourced).
2. **Jordan collects the basics from the client**: business name, what they do, revenue (approximate is fine), how long operating, their community-impact story (who they serve, what gap they fill, any jobs created).
3. **Jordan brings that info into a Claude Code session** (this one or a future one) along with the specific grant's exact application fields (for Breva Thrive: business demographics, ownership info, revenue range, impact narrative — pull the current form fields from breva.com/thrive-grant before writing, in case they've changed).
4. **Claude drafts the full application** — every narrative field, tailored to the client's real facts and the funder's stated priorities (for Breva: underserved ZIP codes, job creation, service gaps).
5. **Jordan relays the draft to the client for review.** Client flags anything inaccurate or missing; Claude revises.
6. **Client submits it themselves** through their own account on the funder's site — Fundwell doesn't have login access to file on their behalf.
7. **Payment**: $450 flat fee via Venmo/Zelle, due on delivery of the final draft (not contingent on winning).

## Why flat fee, due on delivery — not contingent on winning

Stated in STRATEGY.md: contingency (percentage-of-award) fees are viewed as an ethics concern in the grant-writing profession, and they misalign incentives — the deliverable is a complete, well-written application, not a guaranteed outcome nobody controls.

## What triggers building more infrastructure

Same principle as Revuna: don't build anything until paid signal justifies it. If 3+ clients pay for one-off applications, that's the signal to consider:
- A lightweight intake form (so clients submit their basics without a live call)
- A small library of pre-researched funder profiles beyond Breva Thrive, to speed up matching new clients to real open grants
- Possibly Stripe once it's actually usable in whatever environment is running this
