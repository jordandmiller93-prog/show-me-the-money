# Revuna — Strategy Brief

*Generated via the `/money-discover` methodology in this repo. Working name, not yet trademark/domain-checked — see ROADMAP.md.*

## One-liner

AI drafts on-brand replies to every new Google review for single-location local businesses, owner approves in one tap. $19–39/mo, no contract.

## Five-Filter Score: 5/5

| Filter | Verdict |
|---|---|
| 1. Profitability | Pass — incumbents (Podium, Birdeye) charge $299–999/mo and prove the category pays. We undercut on price, not on proof of demand. |
| 2. Comprehension | Pass — "reads your new reviews, drafts a reply in your voice, you approve, it posts." Two sentences. |
| 3. Replicability | Pass — buildable solo with AI assistance in 2–4 weeks: Google Business Profile OAuth + Claude API for drafting + a thin dashboard. |
| 4. Automation potential | 9/10 — once connected, drafting runs unattended; only the approve-tap is manual by design (trust/liability). |
| 5. Speed to first dollar | Pass — first dollar doesn't require the product to exist yet. See "First dollar path" below. |

## Target customer

Single-location owner-operator local service business — dental clinics, med spas, hair/nail salons, boutique fitness studios. Filter: 4.0–4.7 star Google rating, 50+ total reviews, **3+ unanswered reviews in the last 90 days**. That last criterion is the entire targeting mechanism: it's visible for free on Google Maps before we ever contact them, so every prospect is pre-qualified by their own public behavior.

## Revenue model

- Starter: $19/mo — Google Business Profile only
- Pro: $39/mo — + Yelp + Facebook
- Self-serve, monthly, cancel anytime, no setup fee. This pricing and no-contract term *is* the differentiation (see below), not an afterthought.

## First dollar path (doesn't require the product built yet)

1. Build a list of ~50 businesses matching the targeting filter above (manual Google Maps research, zero API cost).
2. Email each owner a **screenshot of their own unanswered review** + a free AI-drafted reply for it (see `outreach/sample-responses.md` for the drafting quality bar) + a link to the landing page.
3. Offer: "reply free to your next 3 reviews, no card required." Convert to paid after that — this is a concierge MVP (I draft manually via Claude for the first handful of customers) before the self-serve dashboard exists.

## Competitive intelligence

**Incumbents**: Podium ($399–599/mo) and Birdeye ($299–449/mo) dominate the category but sell to multi-location/enterprise accounts via annual contracts with a 30–60 day cancellation window and $5–15K implementation fees on top. Documented complaints: businesses locked into contracts they can't exit, cost far exceeding value for a 1–5 location operator.

**Direct clones already exist**: "ReviewPilot" (multiple unrelated products using this exact name), "ReplyGuard" (adjacent — client email replies, not reviews), "RepliQ"/"Repliq" (cold outreach / email writing, different category). The *name* space is crowded; the *cheap, no-contract, single-location-first* positioning is not — none of the researched incumbents or clones lead with "$19/mo, no contract" as the headline.

**The gap**: incumbents' sales-led motion makes a single-location owner too small a deal to be worth their time. That's exactly the segment we serve.

### Blue Ocean grid

| Action | What |
|---|---|
| **Eliminate** | Sales calls, annual contracts, implementation fees, multi-location/enterprise features (SSO, call tracking, ticketing) |
| **Reduce** | Platform coverage at launch — Google Business Profile only first, add Yelp/Facebook once paying customers ask |
| **Raise** | Setup speed (under 5 minutes, no call required), pricing transparency (public price, no "contact sales") |
| **Create** | "Free until you love it" per-review trial (not a time-limited trial) + drafts tuned to the owner's actual voice from a 60-second onboarding survey |

## Six Questions (validation)

1. **Demand reality** — Businesses already pay $300–900/mo for this category (Podium/Birdeye revenue is the proof). We're not creating demand, we're serving the segment priced out of it.
2. **Status quo** — Owner either ignores reviews (most common) or replies manually, ~15–30 min per response, often weeks late. That delay itself is visible and provable per-business.
3. **Desperate specificity** — e.g. "Dr. [Name] at [Dental Practice], 4.3★, 6 unanswered 1–3★ reviews sitting 60+ days" — a real, findable business on Google Maps today, not a persona.
4. **Narrowest wedge** — One feature only: connect Google Business Profile → auto-draft reply to every new review → owner taps approve/edit/send.
5. **Observation test** — Owner gets stuck at the connection step if it's anything more than "Sign in with Google." One-click OAuth or the product is dead on arrival for this ICP.
6. **Future-fit** — As AI search (ChatGPT/Perplexity "best dentist near me") grows, review recency and response quality become a trust signal that matters *more* over time, not a temporary hype wave.

## Narrowest-bet statement

> By **2026-07-16**, I will send a personalized email containing a free AI-drafted reply to one of their real unanswered Google reviews to **20 named local business owners** with unanswered reviews, to test whether they'll pay **$19/mo** for **Revuna**. If no reply/signal by **2026-07-23**, the wedge is wrong.

## First 30 days

- **Week 1**: Landing page live, list of 50 target businesses built, first 20 outreach emails sent (narrowest-bet test).
- **Week 2**: Concierge-deliver replies manually (via Claude) for any business that responds positively — prove willingness to pay before building the dashboard.
- **Week 3**: Wire up Stripe for the businesses that convert; start building the self-serve dashboard (Google OAuth + review pull + draft + approve UI) in parallel.
- **Week 4**: Expand outreach to 100 more businesses; move first concierge customers onto self-serve.

## Risks / what would kill this

- Google's OAuth verification process for reading Business Profile reviews can take 1–4 weeks for a new app — this is the single biggest timeline risk. Mitigation: start the verification request in Week 1, run concierge-by-hand in the meantime.
- Cold email deliverability/response rates for unsolicited outreach to small business owners are typically low (2–5% reply rate is normal, not a failure signal) — 20 emails is a signal-finding batch, not a sufficient sample to judge the wedge on its own.
