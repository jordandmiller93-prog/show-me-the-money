# Revuna — Roadmap

Phased build plan. Each item is marked who does it — **[You]** needs Jordan's own account/identity/payment, **[Claude]** is something that gets done in a Claude Code. session (this one or a future one).

## Phase 0 — Foundations (this session)

- [x] **[Claude]** Wedge, six-question validation, differentiation grid → `STRATEGY.md`
- [x] **[Claude]** Landing page → `site/index.html`, `site/styles.css`
- [x] **[Claude]** Cold email template + CAN-SPAM checklist → `outreach/cold-email-template.md`
- [x] **[Claude]** Sample AI-drafted replies (demo/proof asset) → `outreach/sample-responses.md`

## Phase 1 — Get the landing page live (free)

- [x] **[You + Claude]** Formspree form created and wired into `site/index.html` (endpoint `xjgngwbd`).
- [x] **[Claude]** Deploy `site/` — done 2026-07-15 via the Vercel connector (this session has one; the old sandbox blocker is gone). Production deployment `dpl_9hfSShWNpdhLLg8qVHyY1Vfgndyj`, project `revuna`, URL `revuna-jordandmiller93-5423s-projects.vercel.app`. **One step left [You]:** the URL is behind Vercel's Deployment Protection auth wall — disable it in the dashboard (see HANDOFF.md #3). Loop will verify public reachability after.
- [ ] **[You]** (Optional, costs money) Buy a domain once the wedge is validated — don't spend on this before the narrowest-bet test resolves.

## Phase 2 — Narrowest-bet test (target: send by 2026-07-16)

**Update (2026-07-15): plan changed twice.** First attempt assumed browsing Google Maps/Yelp for real unanswered-review text — both blocked automated fetches (Yelp returned `403 Forbidden`), ruled out working around that (ToS) or fabricating quotes. Second attempt was going to use Google's Places API, but WebFetch itself turned out to be non-functional this whole session (403s on everything, even `example.com`) and the API key was never provided — rather than keep blocking on external setup, pivoted to sourcing real leads via WebSearch against practices' own websites/directories (not scraping gated platforms), with an honest general outreach hook instead of a fabricated review quote, and phone as the channel for leads without a verified email.

- [x] **[Claude]** Sourced first batch of 4 real, verified single-location dental practices → `outreach/batch-1-real-leads.md`. Star rating / unanswered-review-count criteria from STRATEGY.md's targeting filter are **not verified** for this batch (no Maps access this session) — treat as a first test batch, not fully-qualified.
- [x] **[Claude]** Drafted outreach: cold-call script (3 leads, no verified email) + 1 full email (1 lead with a verified address) in `outreach/batch-1-real-leads.md`.
- [x] **[Claude]** 2026-07-15: Gmail outreach drafts created for all 5 verified-email batch-1 leads (drafts only, nothing sent) — see HANDOFF.md #1. Batch-2 lead sourcing (target ~13 more) in progress via autonomous loop.
- [ ] **[You]** Add your real mailing address to the 5 drafts, review, send. Place the calls for the 12 phone-only leads. See HANDOFF.md.
- [ ] **[You/Claude]** Track replies/responses. Check the kill-switch signal by 2026-07-23 per STRATEGY.md.
- [ ] **[Optional, later]** Scale beyond this first batch of 4 — either continued manual WebSearch sourcing (slow, ~1-2 searches per lead) or the Google Places API (setup steps below, kept for reference) if this channel proves out and volume is worth the setup.

<details>
<summary>Original Places API setup steps (kept for reference, not currently blocking anything)</summary>

1. Go to [console.cloud.google.com](https://console.cloud.google.com), create a new project (e.g. "revuna-prospecting").
2. APIs & Services → Library → enable **"Places API (New)"**.
3. APIs & Services → Credentials → Create Credentials → API key. Restrict it to Places API only (Credentials → edit key → API restrictions).
4. **Set a budget alert before doing anything else** (Billing → Budgets & alerts → create a budget, e.g. $5) — Places API has a free monthly usage credit but a card is required on file.
5. Share the API key in chat if you want to revisit this path (I won't commit it to the repo — it'll go in a local, gitignored `.env` file only).

</details>

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

**Where we are right now (2026-07-15)**: Phase 0 done. Phase 1 (live landing page) is stuck — Vercel dashboard, GitHub Actions/Pages, and the Vercel CLI/API have all hit real walls (mobile UI issues, GitHub Actions not registering for reasons neither of us could see or fix, and this session's sandbox blocking outbound access to Vercel's API entirely). Parked for now, not blocking anything else — revisit whenever, ideally from a desktop. Phase 2 has a real first batch ready: 3 calls + 1 email in `outreach/batch-1-real-leads.md`, waiting on you to actually place/send them since I can't use your phone or inbox.
