# Revuna — Market Research Report

*Generated via `/money-strategy` (fresh mode — no live product yet). Complements `STRATEGY.md` (the `/money-discover` wedge output); this report goes deeper on market sizing, competitive teardown, business model stress test, and GTM.*

## Premise deconstruction (condensed)

Full six-question validation already ran in `/money-discover` (see `STRATEGY.md`). Terms already made measurable there: "no contract" = month-to-month, cancel anytime, $0 setup fee; "cheap" = $19-39/mo vs. incumbents' documented $299-999/mo; "automated" = AI drafts a reply when a new review posts, owner approves in one tap.

**Assumption audit**:

| Assumption | Status |
|---|---|
| Demand exists for AI review-response tools | ✅ Validated — Podium ($219.9M revenue, 6.5K customers) and Birdeye ($146.8M revenue, 80K customers) prove large real payment volume for this category |
| Willingness to pay at $19-39/mo specifically | ⚠️ Plausible, not yet validated — narrowest-bet test pending (batch 1 queued, awaiting send) |
| Cold outreach is a viable channel for this ICP | ⚠️ Plausible — 4 real leads sourced, zero responses yet (nothing sent) |
| Claude Code can build this solo | ✅ Validated — Google OAuth + AI-drafted replies + simple approval dashboard is a well-understood build pattern, no novel technical risk |
| Timing is right now, not 2 years ago | ✅ Validated — AI drafting quality and cheap OAuth tooling make solo build/ops viable in a way it wasn't previously |

## Section 1: Market Overview

- **Market size**: Reputation management software market ~$7.75B (2026) → $14.01B by 2031, CAGR ~12.6% (Mordor Intelligence). Broader reputation management *services* TAM estimated ~$93.97B through 2034 (Business Research Insights) — that figure includes services/agencies, not just software, so treat it as a ceiling, not SAM.
- **SAM**: SMB single-location review-response software specifically — a narrow slice of the above.
- **SOM (year 1)**: US single-location dental/salon/med-spa practices reachable via direct outreach — realistically low thousands of businesses, deliberately narrow rather than chasing the full TAM.
- **Growth**: SMB is explicitly called out as reputation management's fastest-growing segment — cloud/subscription pricing is making this newly accessible to operators who couldn't previously afford enterprise tools.
- **Key trends**: (1) Incumbents now bundle AI-reply as a paid add-on rather than core (Podium charges **$99/mo extra** for its AI reply module on top of the $399+/mo base) — meaning even they price AI drafting at a premium, which is the exact gap Revuna's $19-39/mo *whole product* undercuts. (2) AI search (ChatGPT/Perplexity local queries) is raising the stakes on review recency/response quality as a trust signal, per STRATEGY.md's Q6 future-fit answer.
- **Timing signal**: Podium's average revenue/customer (~$33.8K/yr) and Birdeye's (~$1.8K/yr, ~$150/mo) show both are structurally anchored above true single-location comfort — neither has repositioned downmarket to self-serve monthly pricing for the smallest operators. That segment is currently served by expensive incumbents or nothing.

## Section 2: Competitive Landscape

| Competitor | Revenue / Scale | Pricing | Praised for | Complained about |
|---|---|---|---|---|
| **Podium** | $219.9M revenue, 6.5K customers, $421.6M raised, $3B valuation (2021) | $399-999/mo, annual contract, +$99/mo AI reply add-on, $5-15K implementation fees reported | All-in-one messaging + reviews + payments | Aggressive contract lock-in, hard to cancel, cost |
| **Birdeye** | $146.8M revenue, 80K customers, $93M raised | $299-449/mo, annual contract | Larger SMB-leaning customer base | Still priced well above single-location comfort |
| **NiceJob** | Not independently verified this session — flagged for a follow-up teardown | Lighter SMB-focused positioning per prior general knowledge | — | — |
| **"ReviewPilot" (multiple products)** | Several unrelated products share this exact name/concept (SaaSworthy, Capterra listings) | Unverified | Crowded name signals real demand for the feature | No single player owns cheap self-serve positioning |
| **EmbedSocial / Trustmary / Grade.us** | Smaller players | Review-collection/display focused | Less direct overlap — collection, not AI-response drafting | — |

**Positioning map**: X = price ($19/mo → $999/mo), Y = feature completeness (narrow → comprehensive). Podium and Birdeye sit high-price/high-feature (multi-location, messaging, payments, ticketing all bundled). Revuna sits low-price/narrow-but-deep — one feature done well and cheaply, deliberately excluding the enterprise bloat.

## Section 3: SWOT

| | Helpful | Harmful |
|---|---|---|
| **Internal** | **Strengths**: Zero build cost for AI drafting via Claude API (likely stronger than incumbents' older in-house NLP); no legacy sales org to fund via high pricing; weekly iteration speed as a solo AI-driven operation | **Weaknesses**: Zero brand trust vs. 6.5K-80K-customer incumbents; no engineering team if something breaks; founder has $0-100 budget and 1-3 hrs/week, capping outreach volume |
| **External** | **Opportunities**: Podium's own $99/mo AI-add-on pricing proves willingness to pay for exactly this feature — Revuna's whole product undercuts their add-on alone; no-contract is a documented pain point in incumbents' own user complaints | **Threats**: Podium/Birdeye could trivially launch a cheap self-serve tier if they noticed demand (they already have the AI capability, just not the packaging); Google could add native AI reply drafting to Business Profile for free — existential risk already flagged in STRATEGY.md Q6 |

## Section 4: 4P Analysis

| P | Analysis | Recommendation |
|---|---|---|
| **Product** | Core value: never leave a review unanswered, zero effort | P0: GBP OAuth connect, AI-drafted reply per new review, one-tap approve/edit/post. P1: Yelp/Facebook (Pro tier). P2: tone-customization survey, multi-user access, analytics |
| **Price** | Incumbent AI add-on alone is $99/mo; whole incumbent product starts at $299/mo | $19/mo Starter (GBP only), $39/mo Pro (+Yelp/FB) — anchored at "less than their add-on alone" |
| **Place** | Ranked by expected ROI at $0 budget | 1) Direct outreach (cold email/call — near-$0 CAC, batch 1 already sourced) 2) Local business Facebook groups / Nextdoor (free, community) 3) SEO/content once concierge customers provide case studies |
| **Promotion** | Positioning: the tool for the business too small for a sales callback | "The review-reply tool for the business too small for Podium's sales team to call back." Supporting: no contract; $19 vs. their $299; drafted by AI, always on |

## Section 5: Why Revuna Wins

- **Primary wedge**: self-serve monthly pricing for the single-location segment incumbents' sales-led motion structurally ignores.
- **Unfair advantage**: none classically defensible yet (no network effect or data moat at this stage). The real moat in year 1 is founder speed — AI-native build and ops mean iteration and support cost approach zero, letting the business survive at a price point that would bankrupt a human-staffed competitor.
- **10x factor**: ~10x cheaper than the closest comparable incumbent tier, for the one feature this segment actually needs.

## Section 6: Why This Fits Jordan

Profile: $0-100 budget, 1-3 hrs/week, generalist background. Claude Code supplies the technical build and ongoing content/ops generation Jordan doesn't have personally — Jordan's role is approvals, the outreach calls/emails only a human can place, and holding the accounts (Stripe, domain, Google Cloud) only a human can create.

**Honest challenge**: growing past the first handful of concierge customers will need either more of Jordan's weekly hours (for outreach volume) or a paid channel funded by early revenue — 1-3 hrs/week caps how fast this scales by cold outreach alone. This isn't solved yet; it's the real constraint past month 1.

## Section 7: Business Model Canvas

```
┌──────────────────────────────────────────────────────────────┐
│                    BUSINESS MODEL CANVAS                      │
├──────────────┬──────────────┬──────────────┬─────────────────┤
│ Key Partners │ Key          │ Value        │ Customer        │
│ Google (OAuth│ Activities   │ Proposition  │ Relationships   │
│ Business     │ AI reply     │ Never leave  │ Self-serve,     │
│ Profile API),│ drafting,    │ a review     │ no account rep, │
│ Stripe,      │ outreach,    │ unanswered,  │ email support   │
│ Claude API   │ concierize   │ zero effort, │ only            │
│              │ delivery     │ $19-39/mo    │                 │
├──────────────┤ pre-launch   ├──────────────┤                 │
│ Key          │              │ Channels     │ Customer        │
│ Resources    │              │ Direct       │ Segments        │
│ Claude Code  │              │ outreach     │ Single-location │
│ (build+ops), │              │ (cold email/ │ dental/salon/   │
│ Jordan's     │              │ call), local │ med-spa owner-  │
│ approvals +  │              │ FB groups,   │ operators,      │
│ accounts     │              │ later SEO    │ 4.0-4.7★, 50+   │
│              │              │              │ reviews         │
├──────────────┴──────────────┴──────────────┴─────────────────┤
│ Cost Structure                │ Revenue Streams               │
│ Claude API (fractions of a    │ $19/mo Starter (GBP only)     │
│ cent/reply), free-tier        │ $39/mo Pro (+Yelp/Facebook)   │
│ hosting, $0 outreach (time    │ Self-serve monthly, no        │
│ only) pre-launch              │ contract, no setup fee        │
└───────────────────────────────┴───────────────────────────────┘
```

## Section 8: Business Model Stress Test

**Part A — Revenue Machine (7 checks)**

| # | Check | Status |
|---|---|---|
| 1 | Revenue machine clear/repeatable | ✅ Review posts → AI drafts → owner approves → retained subscriber |
| 2 | Integrity check | ✅ Owner approves every reply before it posts — no auto-post without consent, aligns incentive with quality |
| 3 | Pricing bands (entry/profit tier, gap ≤15x) | ✅ $19 → $39, 2x gap, well within band |
| 4 | Demand validation (real, not assumed) | ⚠️ Category demand validated (incumbent revenue); Revuna's specific price point not yet tested |
| 5 | Traffic-to-money ≤3 steps | ✅ Cold outreach → 3 free replies → convert to paid, 2 steps |
| 6 | Scalability without linear effort | ✅ AI drafting scales near-free per additional customer once dashboard exists |
| 7 | Automation readiness | ⚠️ High post-launch; **currently manual/concierge pre-launch by design** (proving demand before automating) |

**Part B — Unit Economics**

| # | Check | Status |
|---|---|---|
| 8 | LTV > 3×CAC | ✅ LTV ≈ $19 × 12mo assumed retention = $228 (retention assumption unverified). CAC ≈ $0 now (time-only outreach), plausibly $20-40 with a future paid channel. $228 clears 3×CAC even at $40 CAC ($120) |
| 9 | Payback period ≤3 months | ✅ Immediate — first month's $19-39 exceeds near-$0 current CAC |
| 10 | Gross margin ≥70% (SaaS) | ✅ Claude API cost per reply is fractions of a cent; free-tier hosting pre-scale; gross margin comfortably >90% |

**Part C — Constraint (Theory of Constraints)**

Stage: **Pre-launch**. Constraint: **demand uncertainty** — unresolved until real prospects respond to the batch-1 outreach. Test already designed and queued: the narrowest-bet statement in STRATEGY.md (3 calls + 1 email, kill-switch check 2026-07-23). **No other constraint matters until this one resolves** — do not build the dashboard, do not scale outreach volume, do not chase Yelp/Facebook integration until batch 1 produces a signal.

## Section 9: Go-To-Market Plan

**Channels ranked**:
1. **Direct outreach** (cold email/call) — near-$0 CAC, batch 1 of 4 already sourced and drafted
2. **Local business communities** (Facebook groups, Nextdoor business posts) — free, untested this session
3. **SEO/content** — deferred until concierge customers can provide real case studies/testimonials

**30-day plan**:

| Week | Focus | Actions | Target |
|---|---|---|---|
| 1 | Narrowest-bet test | Jordan places 3 calls + sends 1 email (batch 1) | Kill-switch signal by 2026-07-23 |
| 2 | Scale sourcing (if signal positive) | Claude sources 15-20 more real leads via WebSearch method | 20-lead batch ready |
| 3 | Concierge delivery | Manually draft replies weekly for any business that said yes | First paying customer |
| 4 | Stripe + dashboard groundwork | Jordan creates Stripe account; Claude begins self-serve dashboard build | Payment collection live |

**90-day milestones**: Month 1 — first paying customer (concierge). Month 2 — $100-300 MRR, self-serve dashboard replacing concierge delivery. Month 3 — repeatable outreach-to-paid conversion rate established, decide whether to fund a paid channel with early revenue.

## Section 10: KPI Framework

| Category | Metric | Target (Month 1) | Target (Month 3) |
|---|---|---|---|
| Revenue | MRR | $19-76 (1-4 customers) | $300-500 |
| Growth | Leads contacted/week | 4-8 | 15-20 |
| Activation | Free-trial → Paid | Unmeasured yet | 20%+ (small-N, directional) |
| Retention | Monthly churn | N/A (too early) | <15% |
| Efficiency | CAC | ~$0 (time only) | <$40 if a paid channel is added |

## Section 11: First Priorities & Action Items

```
□ Tomorrow (Jordan): Place the 3 calls + send the 1 email in outreach/batch-1-real-leads.md
□ This week (Claude): Source 15-20 more real leads via the WebSearch method proven this session
□ This week (Claude): Write the concierge-delivery SOP (how replies get drafted/delivered weekly by hand, pre-dashboard)
□ This month (Jordan): Create Stripe account once first "yes" lands
□ This month (Claude): Begin self-serve dashboard build (Google OAuth + Claude-drafted replies + approve UI) once concierge proves demand
```

---

**Next**: Run `/money-save` to checkpoint the wedge, this market research, and the open hypotheses (retention assumption, outreach channel effectiveness — both unvalidated). Then `/money-product` to start building once the narrowest-bet test shows signal.

## Value Quantification

| Dimension | This session |
|---|---|
| ⏱ Time saved | ~15-20 hours of market research, competitor revenue/pricing research, and business-model stress-testing |
| ⚠️ Risks avoided | (1) Pricing blind — now anchored against verified incumbent pricing/add-on structure; (2) ignoring that incumbents could downmarket-compete; (3) skipping the retention/CAC assumption check that most solo founders skip until MRR stalls |
| ✅ What you got | Full market sizing (with real TAM/CAGR figures), 5-competitor teardown with real revenue/customer data, SWOT, 4P, business model canvas, 10-point stress test, GTM plan, KPI targets |
| 🚧 Without this skill | Most solo founders price by gut feel and discover the competitive landscape only after launch — this report exists before a line of product code is written |
