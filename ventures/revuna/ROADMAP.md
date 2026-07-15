# Revuna — Roadmap

Phased build plan. Each item is marked who does it — **[You]** needs Jordan's own account/identity/payment, **[Claude]** is something that gets done in a Claude Code session (this one or a future one).

## Phase 0 — Foundations (this session)

- [x] **[Claude]** Wedge, six-question validation, differentiation grid → `STRATEGY.md`
- [x] **[Claude]** Landing page → `site/index.html`, `site/styles.css`
- [x] **[Claude]** Cold email template + CAN-SPAM checklist → `outreach/cold-email-template.md`
- [x] **[Claude]** Sample AI-drafted replies (demo/proof asset) → `outreach/sample-responses.md`

## Phase 1 — Get the landing page live (free)

- [ ] **[You]** Create a free Formspree account (formspree.io), get a form ID, replace `YOUR_FORM_ID` in `site/index.html`.
- [ ] **[You]** Deploy `site/` for free — easiest path: [Vercel](https://vercel.com) free tier, "Import Git Repository," point it at this repo with **root directory set to `ventures/revuna/site`**. No build step needed, it's static HTML. Takes about 3 minutes, no card required.
- [ ] **[You]** (Optional, costs money) Buy a domain once the wedge is validated — don't spend on this before the narrowest-bet test resolves.

## Phase 2 — Narrowest-bet test (target: send by 2026-07-16)

**Update (2026-07-15): plan changed mid-flight.** The original plan assumed I could browse Google Maps/Yelp to pull real unanswered-review text. Both blocked automated fetches (Yelp returned `403 Forbidden`), and working around that would mean scraping against their terms of service — not doing that, and not fabricating review quotes to put in emails to real businesses either. Decision: use Google's official Places API instead (also groundwork Revuna needs later for the real product).

- [ ] **[You]** Set up Google Places API access:
  1. Go to [console.cloud.google.com](https://console.cloud.google.com), create a new project (e.g. "revuna-prospecting").
  2. APIs & Services → Library → enable **"Places API (New)"**.
  3. APIs & Services → Credentials → Create Credentials → API key. Restrict it to Places API only (Credentials → edit key → API restrictions).
  4. **Set a budget alert before doing anything else** (Billing → Budgets & alerts → create a budget, e.g. $5) — Places API has a free monthly usage credit but a card is required on file, and a budget alert protects your $0-100 budget from surprise charges if usage patterns change.
  5. Share the API key in chat so I can use it this session (I won't commit it to the repo — it'll go in a local, gitignored `.env` file only).
- [ ] **[Claude]** Using the API key: query Places for ~50 candidate businesses matching the targeting filter in STRATEGY.md (category + rating + review count), pull real recent review text via Place Details, identify ones without an owner response.
- [ ] **[Claude]** Draft 20 personalized outreach emails using `outreach/cold-email-template.md`, each with a real, accurately-quoted review.
- [ ] **[You]** Review and actually send the 20 emails from an email address you control (sending needs your mailbox — I can't send email on your behalf without access to an account). I'll hand you a ready-to-send batch.
- [ ] **[You/Claude]** Track replies. Check the kill-switch signal by 2026-07-23 per STRATEGY.md.

## Phase 3 — Concierge MVP (for anyone who says yes)

- [ ] **[Claude]** For each interested business: manually pull their new reviews weekly and draft replies (no product yet — you're proving willingness to pay before building the automation).
- [ ] **[You]** Collect payment manually at first (Stripe Payment Link, see Phase 4) once someone's ready to pay past the free 3 replies.

## Phase 4 — Payments

- [ ] **[You]** Create a Stripe account (requires your identity/bank details — I cannot do this step). https://stripe.com
- [ ] **[Claude]** Once you share the Stripe publishable key (never share the secret key in chat), wire up a Payment Link or Checkout session for the $19/$39 plans.

## Phase 5 — Self-serve dashboard (build once concierge proves demand)

- [ ] **[You]** Set up a Google Cloud project and start the OAuth consent screen verification for Business Profile API access — this can take 1-4 weeks for Google's review, so start it as soon as Phase 2 shows signal, in parallel with concierge delivery.
- [ ] **[Claude]** Build the dashboard: Google sign-in, pull new reviews, draft via Claude API, one-tap approve/edit/post, basic auth + hosting (Vercel + a free-tier Postgres like Neon or Supabase).
- [ ] **[Claude]** Move concierge customers onto self-serve.

## Phase 6 — Expand

- [ ] Add Yelp + Facebook (Pro tier).
- [ ] Expand outreach volume once the wedge and message are proven at small scale.
- [ ] Consider `/money-ops` (in this repo's tool suite) for scheduling recurring outreach/content once there's a live product to operate.

---

**Where we are right now**: Phase 0 done. Next concrete action is Phase 1 — get the landing page live, which only needs your Formspree + Vercel signups (both free, no card). Then Phase 2's outreach batch is ready for me to draft as soon as you confirm you're ready to send.
