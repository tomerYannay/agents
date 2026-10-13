# Business Opportunity Research: Final Report, Phases 1–10

**Date:** 2026-10-13
**Branch:** `local-research-phase6-10`. This is the local continuation, kept separate from the cloud Routines `research` branch. Nothing from that branch was used.

**Phase reports:**
- `business-opportunity-report-2026-10-12.md` (Phase 1)
- `business-opportunity-report-phase{2..5}-2026-10-12.md`
- `business-opportunity-report-phase{6..10}-2026-10-13.md`

**Working files** in `research-notes/`:
- `research-methodology.md`
- `opportunity-ledger.md` (every scored idea and every exclusion)
- `cumulative-leaderboard.md`
- `checkpoint.md`
- `search-log.txt`
- one folder per phase (`phase6/` … `phase10/`), holding agent reports, audits, red-team reports and shortlists

**How to read this report.** Every claim carries one of these evidence labels:
- **[Verified]:** a primary source or dataset was re-opened.
- **[Secondary]:** a reputable second-hand source.
- **[Vendor]:** a self-interested source.
- **[Hypothesis]:** a model output or inference.
- **[Unknown]:** not established.

Scores use the frozen Phase 3 rubric. Differences under about 5 points are noise. No customer was contacted, no money was spent, nothing was built or deployed, and every test below is **described, not run**.

---

## 1. Executive summary

**1. Ten phases did not produce a clear winner. They produced a flat top cluster and a set of measured base rates that matter more than any single idea.**
- The top ten ideas sit at 49.6–55.4 Adjusted. That is about one noise band, so the ranking within the cluster cannot be relied on. The final red team recommended presenting the cluster as a tie, and this report does so.
- No idea in the cluster has verified evidence that a newcomer without an audience reaches $2–5k/month through its proposed channel.

**2. What newcomers actually get is the decisive fact, and it is low everywhere.** Measured in Phases 5–10:

| Dataset | Typical newcomer outcome |
|---|---|
| TrustMRR, 2024–26 cohort (69% random sample of ~11.4k profiles) | 3.9% reach $3k+ MRR [Verified; upper bound, self-selected] |
| App Store (19,614 new non-game apps) | Median 2 ratings; individual developers reach 1k ratings 4.9% of the time [Verified] |
| Superhive (Blender add-ons), 2026 | Median 2–2.5 sales in the first 3 months; 1–5.6% reach 100+ [Verified] |
| Apify Store, 2026 | Median 1 user in the last 30 days, at every age up to 9.5 months [Verified] |
| Hebrew business apps released since 2024 | Median 0 Israeli ratings [Verified] |
| First-time Texas DIR software contract holders | Median $19.7k/year; 43% sold $0 [Verified] |
| New EU medical-device authorised representatives (2023–26) | Median 1 client [Verified] |
| Local marketplaces, 7 small markets | Best entrant has 0–11 ratings vs incumbents at 400–42,661 [Verified] |

Treat any single attempt as roughly a **4–6% shot** at Track A. With a price of $300+/month per account, the rate is about 10–15% (§6).

**3. Copies arrive in about 6 months, and moats a $2k founder can buy don't stop them.** Every visible gap was entered within that window:
- 3 QuickBooks Desktop API clones;
- 4 WooCommerce Merchant Center monitors;
- 100+ padel apps per storefront;
- 141–151 wedding photo apps.

Licences, certifications and contracts obtainable in 3–9 months for about $2k are obtainable by followers on the same timeline (Phase 9).

**4. The traits of winners without an audience were measured and then corrected.**
- **Price:** charging $300+/month per account lifts the odds about **3×**, not 5×. About 90% of such launches still miss $3k MRR. Much of the lift is arithmetic: about 10 customers clears $3k.
- **Channel:** high-price winners sell through **outbound, LinkedIn, calls and partners**. The paid-ads lift is mostly a **low-ticket consumer-app** effect.
- **Team:** small teams of 2–5 outperform solo founders (4.4× vs 0.8×).
- **Paid traffic:** businesses built on it run at much lower margins (Empire Flippers median 28–42% vs 82–95%). Copying erodes them, since each new bidder raises everyone's cost per click.

**5. Best ideas by track.** Details are in §3–§5.
- **Track A ($2–5k/month), best risk-adjusted:**
  - College-baseball data API (H6, 52.2)
  - Blender/VRChat add-ons run as a portfolio (H7, 55.4)
  - AI live translation for small US public bodies (Q1, 47.0, outside the cluster but software-native with verified spending)
  - UK MTD prep (50.2)
  - Hebrew tender intelligence (K13, 50.6)
- **Track B ($10–30k+/month):** no idea has credible newcomer evidence for Track B. The routes with a stated Track B upside all depend on a hit or an unverified assumption:
  - Sage 50 integration API (M1, 49.6)
  - Spanish Holy Land box (H8, 49.4)
  - Pay-per-call emergency lead sites (L6, 48.8)
  - Backflow tester-pay platform (L7, 45.0)
- **The recipe the evidence best supports** (a template, not a scored idea): a B2B vertical tool at $300+/month, delivered the same way for every account, sold by founder outbound plus one partner channel, with paid search only as support.

**6. The single most important next step is not more desk research.** It is the cheap behavioural tests in §11, which can falsify the decisive assumptions for about $0–1,000 each. Desk research hit diminishing returns around Phase 8.

---

## 2. What was done

**Scale (approximate):**
- About 470 distinct ideas were logged across ten phases.
- 107 were scored on the frozen rubric.
- About 360 were investigated and excluded, with reasons (see `opportunity-ledger.md`).

| Phase | Theme | New-idea leader (Adjusted at the time) |
|---|---|---|
| 1 | Open discovery | Atlassian Forge migration contracting (F4-S); later rescored 44.8 |
| 2 | Expansion | UK MTD white-label prep (56 under the Phase 2 formula; 52.6 under the frozen rubric) |
| 3 | Unexplored areas; rubric frozen | Blender add-ons (59.4), college-baseball API (57.2), Meshtastic kits (54.6) |
| 4 | Continued | Apify Actors (55.4) |
| 5 | Continued; first newcomer measurements | Hebrew tender intelligence (53.6), Framer kit (53.2) |
| 6 | Owned and direct distribution | Pay-per-call lead sites (48.8) |
| 7 | Borrowed, contracted and inherited distribution | Sage 50 API (52.0) |
| 8 | Reverse-engineering verified newcomer winners | WooCommerce Merchant Center monitor (48.0) |
| 9 | Copy-resistant positions | Boater-safety course (44.7) |
| 10 | High-ticket with paid acquisition | AI translation for public bodies (47.0) |

**Process in every phase:**
1. Six discovery agents (Consumer, Physical, Traditional, Software, Distribution, Contrarian).
2. A shared search log.
3. A 12–15 item shortlist.
4. An independent evidence auditor and an independent red team.
5. About five finalist deep dives with downside, base and upside scenarios.
6. A leader re-check against newcomer evidence.

**Search effort in Phases 6–10:** 301 logged WebSearches (69, 73, 52, 53 and 54), plus extensive direct fetching of primary pages and public APIs.

**Rubric and scoring:**
- The rubric was frozen in Phase 3 and never changed.
- From Phase 6, scores were published at criterion level.
- From Phase 8, new ideas take the mean of the auditor's and red team's criterion scores.
- Leader corrections were applied only as named criterion steps, and penalties were raised only on direct contradiction.

---

## 3. Cumulative top opportunities (final scores)

| Rank | ID | Opportunity | Phase | CF | Scal | Dist | Pen | **Adjusted** | Track | Score history |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | H7 | Blender/VRChat pipeline add-ons (Superhive, Gumroad) | 3 | 80 | 58 | 61 | 12 | **55.4** | A (B only with a hit) | 59.4 → 56.6 → 55.4 |
| 2 | H6 | College-baseball/softball hobbyist data API | 3 | 75 | 59 | 58 | 13 | **52.2** | A (single-sport ceiling) | 57.2 → 52.2 |
| 3 | H1 | Ready-to-run Meshtastic family/neighbourhood kits | 3 | 61 | 49 | 71 | 7 | **51.2** (majority dissent 49.2) | A | 54.6 → 51.2 |
| 4= | — | monday.com Israeli invoicing app | 1 | 74 | 64 | 48 | 14 | **50.8** | A | 52.0 → 50.8 |
| 4= | J7 | Niche Apify Actors | 4 | 75 | 58 | 48 | 12 | **50.8** (dissent 49.2) | A (B with a hit) | 55.4 → 50.8 |
| 6 | K13 | Hebrew tender + receivership-sale intelligence | 5 | 74 | 60 | 55 | 14 | **50.6** | A | 53.6 → 50.6 |
| 7 | K8 | Framer vertical kit (plugins + templates) | 5 | 80 | 56 | 45 | 13 | **50.4** | A | 53.2 → 52.0 → 50.4 |
| 8 | — | UK MTD white-label prep for accountants | 2 | 61 | 63 | 53 | 10 | **50.2** | A, possible B | 52.6 → 50.2 |
| 9 | — | Israeli allocation-number verification | 1 | 72 | 53 | 59 | 12 | **49.8** | A | — |
| 10 | M1 | Sage 50 US/CA integration API (Conductor model) | 7 | 68 | 60 | 52 | 12 | **49.6** | A; B upside | 52.0 → 49.6 |
| 11= | H10 | Israeli-artist ketubot | 3 | 76 | 47 | 61 | 12 | 49.4 | A (small) | 50.6 → 49.4 |
| 11= | H8 | Spanish-language Holy Land subscription box | 3 | 53 | 62 | 67 | 10 | 49.4 | B (clearest stated) | — |
| 11= | H5 | Non-US sold-out availability alerts | 3 | 79 | 44 | 51 | 10 | 49.4 | A | — |
| 14 | L6 | Pay-per-call emergency home-service lead sites | 6 | 68 | 59 | 55 | 13 | 48.8 | A; B upside | — |
| 15 | J1 | Hebrew/Russian voice-memoir books | 4 | 68 | 52 | 58 | 11 | 48.6 | A | 51.0 → 48.6 |
| 16= | J2 | Hebrew personalised children's books | 4 | 67 | 49 | 64 | 11 | 48.2 | A | — |
| 16= | H4 | Judaica STL studio | 3 | 64 | 53 | 57 | 10 | 48.2 | A | — |
| 18= | N12 | WooCommerce Merchant Center policy monitor | 8 | 76.5 | 53 | 46 | 13 | 48.0 | A | — |
| 18= | J9 | MT5 prop-rule utility | 4 | 75 | 48 | 54 | 12 | 48.0 | A | — |
| 20 | H9 | Remote b'nai mitzvah prep | 3 | 70 | 42 | 55 | 8 | 47.8 | A | — |
| … | | K12 47.6 · **Q1 47.0** · L2 46.6 · L10 46.2 · N1 45.9 · L9 45.4 · N9 45.0 · L7 45.0 · P1 44.7 | | | | | | | | |

**What the scores mean, and do not mean:**
- **Within the cluster, scores reflect test cost and observability more than profit odds.** The rubric's Cash-Flow score rewards cheap, fast starts. H7, J7, K8 and N12 score well partly because they cost almost nothing to try.
- Under the base rates in §1, each of them is a **2–5% shot per product**. H7's #1 is "not meaningful" (red team), because its lead over #2 is 3.2 points.
- **Israel-domestic leaders** may be overstated by 1–3 points (Phase 9, Agent F): the monday.com app, K13, allocation verification, J1 and J2. Audits kept finding Israeli incumbents late, partly because our search tools are US-centric. This caution is noted, not applied.

---

## 4. Best ideas for Track A ($2–5k/month owner profit)

The ranking below weighs score, the cost of the decisive test, founder fit, and how much of the case is known rather than assumed.

| # | Idea | Why it is here | Decisive assumption | Known vs assumed |
|---|---|---|---|---|
| 1 | **H6 College-baseball/softball data API** (52.2) | Strong founder fit (backend and data). Under $2k. A paying niche exists: CFBD has 3,684 paid members, about $6–29k/month [Verified: Graphtreon]. | Enough paying users at $5–30/month despite NCAA/SIDEARM noncommercial terms. Comparable creators have 8–447 patrons, i.e. about $40–3,500/month. | **Known:** a paid niche exists; terms are noncommercial; paid APIs operate openly. **Assumed:** this founder's API gets past about 150 paying users; terms are not enforced. |
| 2 | **H7 Blender/VRChat add-ons, run as a portfolio** (55.4) | Highest score; cheapest test; proven marketplace with visible sales. | A portfolio of 5–10 add-ons gets at least one into the top 1–5%. | **Known:** median newcomer 2 sales in 3 months; 1–5.6% reach 100+; supply rising about 390–490/month. **Assumed:** this founder's products land in the tail. |
| 3 | **UK MTD prep for accountants** (50.2) | Mandated, recurring quarterly demand; about 3M taxpayers by 2028 [Secondary]. | A practice pays for AI-prepared submissions that offshore preparers (Outbooks, QX) and Sage's MTD agent don't already provide cheaper. | **Known:** mandate and incumbents. **Assumed:** a differentiated entry. |
| 4 | **K13 Hebrew tender + receivership intelligence** (50.6) | Local language and data. Kones charges ₪249/month [Verified]. | Users switch from Ifat and kones.co.il for better AI summaries. | **Known:** incumbents and prices. **Assumed:** switching; Israel-incumbent caution applies. |
| 5 | **Q1 AI live translation for small US public bodies** (47.0) | Software-native; under $2k; verified spending (Mountain View $43,750 for 300 hours; Gilroy about $300 per meeting). The adjacent comparable Glossa grew $4.1k → $31.8k/month. | Small bodies buy at $300–600/month from a non-US newcomer within about 60 days without a tender. | **Known:** spending; Wordly is self-serve; Teams and Zoom bundle captions. **Assumed:** purchase speed; night-hours support is workable. |

**Honourable mentions (Track A):**
- **L6 pay-per-call lead sites (48.8):** a cheap test, but no newcomer ranking data exists.
- **N12 WooCommerce Merchant Center monitor (48.0):** four 2025–26 entrants have 0–30 installs.
- **M1 Sage 50 API (49.6):** see Track B.

## 5. Best ideas for Track B ($10–30k+/month owner profit)

**No idea has verified newcomer evidence of a route to Track B.** Every candidate below needs either a hit or a currently unverified assumption to hold. They are listed in order of how cheaply that assumption can be tested.

| # | Idea | Upside mechanism | Blocking unknown | Cheapest falsifier |
|---|---|---|---|---|
| 1 | **M1 Sage 50 US/CA integration API** (49.6) | Recurring per-file pricing on the Conductor model (Conductor: $42,133 MRR, solo founder [Verified]). Can extend to a desktop-accounting API portfolio. | Sage's partner terms: the only archived agreement text bars use for third parties' benefit and allows termination on 90 days' notice. Demand is thin: 0.12 Sage-to-QuickBooks ratio on vertical-SaaS integration pages. Three QuickBooks Desktop clones appeared in 2026. | Obtain the current Sage 50 developer agreement and read the resale clause. Kill if a hosted third-party API is barred. |
| 2 | **H8 Spanish Holy Land subscription box** (49.4) | Subscription with a fulfilment partner. Comparables: Artza claims 85k customers [Vendor]; Lev Haolam has 341 Trustpilot reviews in 12 months [Verified]. | Spanish Meta CAC; inventory capital ($3–4k, over budget). | A Spanish landing page plus a $300–500 Meta test. Kill if cost per pre-order exceeds 50% of the first box's margin. |
| 3 | **L6 Pay-per-call emergency lead sites** (48.8) | Selling exclusive calls direct to contractors in 8–10 metros: $12–18k/month [Hypothesis]. | Can a new organic-only site rank in 2026 despite AI Overviews and Local Services Ads? | Build 5–8 sites for under $1.5k. Kill if none ranks top 5 for a metro emergency query within 9 months. |
| 4 | **L7 Backflow-test platform paid by testers** (45.0) | 40 utilities ≈ $25k/month [Hypothesis]. | Utilities adopting a foreign solo vendor; BSI's patent scope. | A patent claim read and 20 utility outreach emails (not executed). |
| 5 | **Template: B2B vertical tool at $300+/month via outbound plus one partner** | The only recipe consistent with all Phase 8–10 measurements. | Can this founder, part-time from Israel, sustain outbound and convert ≥1%? | 300 outbound touches over 4 weeks (about $100–300). Kill at under 3 qualified calls per 100, or no paid pilot. |

## 6. Best risk-adjusted ideas

"Risk-adjusted" here means:
- a high Adjusted score;
- capital under about $2k;
- a decisive assumption that can be **falsified for under about $1k**;
- no drift into services or staffing;
- strong founder fit.

1. **H6 college-baseball data API.** Software-only, cheap, strong fit. The kill test is clear: a paid tier plus a public free tier for one season.
2. **H7 Blender add-ons as a portfolio.** Cheapest test, with directly observable sales data. It is a lottery per product, so its risk is managed through the portfolio, not the product.
3. **M1 Sage 50 API.** Only if a desk read of the agreement clears it. It is the only top-ten idea modelled on a verified solo success without an audience.
4. **Q1 AI translation for public bodies.** A desk check of 30 meeting agenda packets can kill or confirm it for $0.
5. **J7 Apify Actors.** Cheap and a strong fit, but newcomers' median is 1 user. Use it only as a distribution add-on to another data product.

---

## 7. Material ranking changes and why

| Idea | First score | Final | What changed |
|---|---|---|---|
| H7 Blender add-ons | 59.4 (P3) | 55.4 | Newcomer sales measured (P5: under 10 in 2–3 months; P8: median 2.5; P10: median 2). Proven channel cut. |
| H6 College-baseball API | 57.2 (P3) | 52.2 | P6: CFBD is an outlier; peers have 8–447 patrons; NCAA terms are noncommercial. |
| J7 Apify Actors | 55.4 (P4) | 50.8 | P5: median new Actor has 1 monthly user; confirmed in P10 (n=1,500). |
| H1 Meshtastic kits | 54.6 (P3) | 51.2 | P6: 2-packs exist; branded $150+ nodes have 0–39 ratings. Amazon unreadable for 4 phases; majority dissent at 49.2. |
| K13 Tender intelligence | 53.6 (P5) | 50.6 | P6: Ifat already covers receivers with AI summaries. |
| K8 Framer kit | 53.2 (P5) | 50.4 | P6: payout totals no longer credited. P9: at most 9–13% of creators paid; 2026 creators' median is 43 followers. |
| UK MTD prep | 56 (P2 formula) / 52.6 (P3) | 50.2 | P7: offshore prep (Outbooks/QX), Sage MTD AI agent, NRLA statement upload. |
| M1 Sage 50 API | 52.0 (P7) | 49.6 | P8: vertical-SaaS ratio 0.12; Conductor is n=1 among about 7.9k TrustMRR profiles; three QuickBooks Desktop clones in 2026. |
| monday.com app | 52.0 | 50.8 | P6: Israeli invoicing apps on Shopify/Wix have 0–16 reviews. |
| J1 Memoir books | 51.0 (P4) | 48.6 | P7: MyHeritage MyStories offers voice, AI, QR and 10 languages. |
| H2 Revival boards | 38.6 (P3) | 41.2 | P8: MiciMike's $133k raise without an audience (raised); no orphaned target device. |
| Atlassian Forge contracting (Phase 1 winner) | Top of P1 | 44.8 | Rescored under the frozen rubric; it is contracting, not a business. |

**Pattern:** every leader re-checked against newcomer outcomes was lowered, and none was raised on newcomer evidence. The board compressed from a 7-point spread (P3) to a tie cluster.

---

## 8. Negative findings (what the evidence rules out)

1. **Marketplace-wide payouts do not show what a newcomer will earn.** This held on every open marketplace measured: Superhive, Apify, Gumroad, JetBrains, Wix, WooCommerce, the App Store, CodeCanyon, Framer and the Crowd Supply post-campaign tail.
2. **Launch sites don't produce revenue.** On TrustMRR, Hacker News gives a 0× lift, Product Hunt 0.14×, Reddit 0.39× and X 0.40×. Hacker News page base rate: 4.7%.
3. **"Borrowed distribution" mostly fails for newcomers** (Phase 7). About 20 partner channels were checked: perks portals, voucher marketplaces, insurer catalogues, HSA/FSA, Faire, co-ops, franchisor programmes, telecom-advisor distributors, Shopify/Odoo directories, Pax8 and AI-agent registries. Each one either builds the product itself, concentrates spend on giants, or offers newcomers an application form rather than sales. In the Shopify directory, 67% of post-2024 partners have 0 reviews.
4. **Public procurement favours incumbents.**
   - UK G-Cloud: 86% of suppliers earn nothing.
   - Israeli central tenders: single incumbent winners.
   - Texas DIR: first-time software holders have a median of $19.7k.
5. **Moats a $2k founder can buy are not moats** (Phase 9). Cheap approvals fill within years, from 64 to 149 providers in one case. Hard licences protect incumbents. Empire Flippers buyers pay no premium multiple for licensed or contracted businesses.
6. **Israel is a weaker edge than assumed.**
   - Israel-domestic ideas have the same median score as the rest (43.5 vs 43.8).
   - New Hebrew business apps have a median of 0 ratings.
   - Most regulatory gaps (allocation numbers, invoicing) were filled by local startups within months.
   - Israel's 2023–25 EU-alignment reforms removed most import-certification barriers.
7. **Paid acquisition does not survive copying for one-off high-ticket services.** At 3× cost per click, contribution turns negative for reverse recruiting, expat tax, pet relocation and equipment dealing.
8. **Physical goods within $2k are thin.**
   - Young dealer and dropship stores median 10.5% margin, and 8 of 14 had a loss month.
   - Paid-led stores run at 5–10%.
   - The cheapest young store for sale costs $32.9k.
9. **The Conductor pattern (a self-serve API for a closed legacy system) is real but rare (n=1) and copied fast.** No 2024–26 accounting or ERP integration on TrustMRR reached $1k MRR.
10. **Services drift into agencies.**
    - About 79% of young B2B service listings on Empire Flippers are marketing agencies.
    - There are no bookkeeping or compliance service comparables at all.
    - 41% of the $300+ TrustMRR group are services or agencies.

---

## 9. Market-wide patterns

1. **AI-built supply roughly tripled newcomer volume from 2024 to 2026** (App Store, Superhive). The tail stayed thin while the median fell toward zero.
2. **Winners without an audience exist and are the majority of winners**: 82% of $3k+ TrustMRR winners have under 2k X followers. But they are about 4% of attempts.
3. **Copy window of about 6 months.** Any visible newcomer win is cloned, often by studios (Next Vision) or AI-assisted solo developers.
4. **Price per account is the strongest controllable lever, at about 3×.** It works through B2B buyers, outbound and partners, not ads.
5. **Paid channels favour low-ticket consumer apps** (Meta, TikTok). For B2B they are a support channel, and they compress margins.
6. **Revenue tools for people who sell** (coaches, agencies, sales teams, Shopify brands) are over-represented among young software winners. So are local-language copies of US-proven categories and entries priced far below an enterprise incumbent.
7. **Regulatory deadlines create real spending, but obvious gaps are filled within months,** in Israel especially (allocation numbers, MTD, PPWR, Forge migration).
8. **Datasets are survivor-biased.** TrustMRR, Empire Flippers, Flippa and App Store search all contain few or no failures. Every comparable was n=1, and several were declining or unsold when re-checked.

---

## 10. Biggest uncertainties

1. **Founder-specific execution odds.** All base rates come from other founders. Whether this founder's software skill moves them from about 4% to about 15% is unknowable without trying.
2. **Customer acquisition cost.** No idea in ten phases has a measured newcomer CAC. Keyword-level CPCs are unpublished, and ad libraries could not be read at scale.
3. **Retention.** Every recurring idea's economics at 3× cost per click depend on retention nobody has measured.
4. **Terms and legal positions:**
   - Sage 50 developer agreement (M1)
   - NCAA/SIDEARM enforcement (H6)
   - CONTPAQi SDK (N3)
   - Meta automation rules (Q2)
   - Fresha/Booksy partner access
5. **Israeli market data.** gov.il and several Israeli registries blocked automated access, and our search engine is US-only. Israeli incumbents may be under-found, so Israel ideas carry an unpriced risk of 1–3 points.
6. **Channels that could not be measured:** Amazon (H1), Etsy (H10, H4), the monday marketplace, Meta Ad Library, Trustpilot history and Indie Hackers.
7. **Rubric bias.** The rubric rewards cheap, fast digital starts, so the cluster may over-represent "cheap lottery tickets" relative to slower businesses with higher odds.

---

## 11. Recommended next research and validation questions (not executed)

These are ordered by cost and information value. **None was run.** Each needs the user's approval before any contact, spend or build.

**A. Free desk checks (no contact, no spend)**

| # | Question | Kill or keep rule |
|---|---|---|
| 1 | Does the current Sage 50 US/CA developer agreement permit a hosted API used by third-party vendors? (M1) | Kill M1 if barred. |
| 2 | In 30 small-town or school-board agenda packets, how many show translation spend, and how many already name an AI vendor? (Q1) | Kill if fewer than 5 of 30 show spend, or more than a third name a vendor. |
| 3 | Of about 100 vertical-SaaS integration pages, how many list Sage 50 vs QuickBooks Desktop? (M1) | Keep if ≥0.2; kill if ≤0.08. Measured: 0.12, so borderline. |
| 4 | Backtest the gap between first scanner and first studio clone for three collecting booms (Labubu, Lorcana, One Piece) via the iTunes API. Should the founder ever enter trend-timed apps? | Kill the boom-entry strategy if the median gap is under 8 weeks. |
| 5 | Re-query the four WooCommerce Merchant Center plugins' installs in 60 days. (N12) | Kill if all stay under 50. |
| 6 | Read NCAA/SIDEARM terms against how CFBD and Highlightly operate. Is there any enforcement history? (H6) | Raise H6's penalty if enforcement exists. |
| 7 | List Superhive's 2025–26 add-ons that reached 100+ sales. What do they share (category, price, update cadence)? (H7) | Use as a product-selection filter, not a kill. |

**B. Cheap behavioural tests (each needs approval; about $0–1,000)**

| # | Test | Kill threshold |
|---|---|---|
| 1 | **H6:** ship a free plus paid ($5–15/month) college-baseball API for one season, listed where CFBD-type users look. | Fewer than 30 paid users by mid-season. |
| 2 | **H7:** release 3 add-ons in categories selected by desk check A7 within 8 weeks. | Fewer than 25 total sales in 90 days. |
| 3 | **Q1:** 200 targeted contacts plus $400 of ads offering 30-day pilots. | Fewer than 5 pilots, or fewer than 2 paid at $300+/month in 90 days. |
| 4 | **B2B outbound template:** 300 touches in one vertical over 4 weeks. | Under 3 qualified calls per 100, or no paid pilot. |
| 5 | **L6:** 5–8 organic-only emergency-trade sites. | No site ranks top 5 for a metro emergency query within 9 months. |
| 6 | **H8:** Spanish landing page plus a $300–500 Meta test. | Cost per pre-order over 50% of first-box margin. |

**C. Questions only real buyers can answer** (these require customer contact, which was not authorised):
- Would small US public bodies buy AI translation by card without a tender?
- Would vertical SaaS vendors pay $45+/month per Sage 50 company file?
- Would UK practices pay per MTD submission for AI-prepared filings?
- What CAC does this founder actually achieve on outbound in one vertical?

---

## 12. Known vs assumed (summary)

**Known (measured from primary data):**
- Newcomer base rates on TrustMRR, the App Store, Superhive, Apify, Hebrew business apps, Texas DIR, EU authorised representatives and local marketplaces (§1).
- The corrected price and channel effects (§1 item 4; Phase 10).
- Copy speed in ten niches (§1 item 3).
- Holder counts for about 25 licences and certifications (Phase 9).
- Comparables' monthly revenue trends (TrustMRR, Empire Flippers P&L): Conductor, Glossa, ai-dm-setter, LeadX, SoldComps, Alimentia, #94286 and others.
- Primary legal texts: §43 IfSG, NY GBL §171, 19 CFR 111.11, Israeli device regulations, NASBLA terms, and the Fresha partner terms (as read by the red team).

**Assumed (not established):**
- Any newcomer CAC.
- Retention for any recurring idea.
- Any keyword-level CPC.
- Whether any specific buyer would pay for *our* offer.
- Sage, CONTPAQi and Meta terms as they apply to the proposed use.
- All Track B scenarios.
- All owner-profit scenarios in the phase reports (labelled [Hypothesis]).

---

## 13. Process disclosures

- **Phase 7 incident:** one SEC EDGAR request by a sub-agent carried the user's email address in its User-Agent header. It was disclosed at the time. Briefs then banned personal identifiers in requests, and no further occurrence was found.
- **Phase 8 crawl:** the TrustMRR crawl was stopped at 7,866 of 11,435 sitemap pages (a 69% random sample) to bound runtime. All base rates from it are sample estimates.
- **Phase 7 search cap:** one agent exceeded its cap by one search (disclosed).
- **Phase 2–4 baselines:** leader criterion baselines were reconstructed to reproduce the published totals.
- **Reconciliation rule:** introduced in Phase 8 (mean of two reviewers for new ideas), stated before results were seen.
- **H1 penalty:** the Phase 10 majority of reviewers disagreed with holding its penalty at 7. The convention of raising a penalty only on direct contradiction was kept, and the dissent is recorded.
- **Blocked sources were never bypassed.** No browser automation, signed-in session or private account was used. No one was contacted, nothing was bought, built or deployed, and no ads were run.
