# Concierge operating procedure

How Revuna actually delivers value to the first customers — **today, with zero infrastructure, zero accounts beyond what already exists.** No Google OAuth, no dashboard, no Stripe required to serve the first handful of customers. This is deliberate: prove people will pay before building the automation (STRATEGY.md's business model stress test flagged automation as the one check still open pre-launch — this is how it stays open on purpose).

## The loop

1. **A lead says "yes, send me my free replies"** (from a call or the Ludwig email in `outreach/batch-1-real-leads.md`).
2. **Jordan gets their Google Business Profile link** — ask for it directly, or if they don't know it, search "[business name] [city] google maps" and confirm with them.
3. **Jordan (or the customer directly) copies the text of up to 3 unanswered reviews** and sends them to Jordan — text message, email, whatever's easiest for them.
4. **Jordan pastes the review text into a Claude Code session** (this one, or any future one) and asks for a drafted reply — reference `outreach/sample-responses.md` for the tone bar: specific, warm, under 80 words, never defensive, always invites offline resolution for complaints.
5. **Claude drafts the reply. Jordan sends it back to the customer.**
6. **The customer copies it into their own Google Business Profile reply box and posts it themselves** — Revuna doesn't have posting access yet (that needs the Google OAuth verification in ROADMAP.md Phase 5, deliberately deferred).
7. **After 3 free replies, ask if they want to continue at $19/mo.** Payment collection is manual at this stage too — see below.

## Payment, without Stripe (yet)

Stripe requires Jordan's identity/bank details — that's real, can't be skipped, but it also **doesn't need to happen before the first "yes."** Two honest options once someone wants to pay:

- **Simplest**: Venmo/Cash App/Zelle — Jordan already has one of these for personal use, no new account needed, works for a handful of customers at $19/mo.
- **When it's worth the setup**: once there are enough paying customers that manual payment collection is actually annoying, that's the signal to create the Stripe account (ROADMAP.md Phase 4) — not before.

## Why this is the whole business right now, not a workaround

Every piece of infrastructure this session got stuck on — hosting, OAuth, Stripe, a separate repo — is genuinely optional for finding out whether 7 real dental practices will pay $19/mo for this. The loop above is the entire product until that's proven. Building the dashboard before that signal exists would be solving a problem that might not exist.

## What triggers building the real thing

Once **3+ customers** are paying via the manual loop above, that's the signal to:
1. Create the Stripe account (Phase 4)
2. Start the Google OAuth consent screen verification (Phase 5 — this takes 1-4 weeks, start it the moment signal appears, don't wait for it to be "needed")
3. Build the self-serve dashboard so the manual relay in steps 3-6 above becomes automatic

Until then, this SOP *is* the product.
