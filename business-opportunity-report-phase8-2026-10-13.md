# Phase 8: Reverse-Engineering Verified Newcomer Winners

**Date:** 2026-10-13
**Branch:** `local-research-phase6-10`
**Working files:** `research-notes/phase8/`
- Six discovery reports (`agent-A.md` … `agent-F.md`)
- Leader re-check (`audit-leaders.md`)
- Shortlist (`shortlist.md`)
- Evidence audit (`audit-shortlist.md`)
- Red-team report (`redteam.md`)

Scoring script: `scratchpad/p6plus/P8-score/score.py`. It is session scratch and is reproduced in §6.

---

## Bottom line

**No Phase 8 idea enters the top cluster.**
- The best new idea is N12, a recurring Google Merchant Center policy monitor for WooCommerce stores and agencies, at **48.0**. It ties for #18 on the cumulative board.
- The 14 shortlisted ideas score 30–48.
- Two were killed in their original form by primary-source blockers:
  - **German food-hygiene certificate (N1):** the job-seeker certificate can only come from the Gesundheitsamt under §43(1) IfSG.
  - **Fresha review add-on (N11):** Fresha's partner terms forbid credential sharing and hosted resale, and Fresha already ships "Google Rating Boost".

**What Phase 8 did produce is the first large measured base rate for newcomers without an audience.** It also shows how fast niches are copied.

| Dataset | Newcomer outcome |
|---|---|
| TrustMRR, 69% random sample (7,883 profiles; 2024–26 cohort n=5,965) | **3.9%** reach $3k+ MRR; 7.4% reach $1k+. Treat as upper bounds, since listing is self-selected. |
| App Store, 19,614 new non-game apps | Median 2 ratings. **5.8%** reach 1k ratings; individual developers 4.9%. |
| Superhive (H7 re-check) | Median paid add-on: 2.5 sales in first 3 months. 5.6% reach 100+ sales. |
| Crowd Supply 2024–26 | About 116 campaigns, about 92% funded, but over 75% of applications rejected. First-time median raised: $26k. |
| Empire Flippers young physical brands | Median $6.9k/month profit, but this is a listing floor, not a base rate. |

**What separates winners without an audience** (TrustMRR lift versus average):
- **Pricing:** monthly revenue per subscription of $300+ gives 5.1× lift, and $100–300 gives 2.9×. Under $10 gives 0.37×.
- **Team size:** teams of 2–5 people give 4.4× lift. Solo founders give 0.8×.
- **Channel:** paid and partner channels do best (TikTok Ads 6.3×, Meta Ads 4.3×, affiliates 3.7×, partnerships 3.1×). Launch sites do worst (Product Hunt 0.14×, Hacker News 0×, Reddit 0.39×, X 0.40×). Channel causation may run both ways.
- **Audience:** 82% of $3k+ winners have founders with under 2k X followers. Audience still roughly triples the hit rate.

**Copy speed is now measured, and it is about 6 months, not 18.**

| Niche | Entrants |
|---|---|
| QuickBooks Desktop APIs | Three priced clones in 2026 |
| WooCommerce Merchant Center tools | Four, with 0–10 installs each |
| Padel-americano apps | 111–132 new apps per storefront in 2026 |
| Wedding photo-sharing apps | 141–151 since 2024 |
| Prediction-market apps | About 90 per keyword since mid-2025 |

**Leader corrections:**

| Leader | Was | Now | Change |
|---|---|---|---|
| H7 Blender add-ons | 56.6 | **55.4** | Proven channel 3→2. Still #1, by 3.2 points, which is within noise. |
| M1 Sage 50 API | 52.0 | **49.6** | Depth 2→1 and proven channel 2→1. It is out of the podium group. |
| H2 revival boards | 38.6 | **41.2** | Spending +1 and first customers +1. Still no target device. |
| H6 college-baseball API | 52.2 | 52.2 | Held |
| M2 data API | 44.4 | 44.4 | Held. SoldComps is unlicensed eBay scraping. |

---

## 1. Methodology (unchanged)

**Rubric (frozen, criterion level).**

| Score | Criterion step values |
|---|---|
| Cash flow (CF) | Spending ×5 · Speed ×4 · Capital ×4 · Margin ×4 · Labour independence ×3 |
| Scalability (Scal) | Depth ×3 · Recurring ×4 · Acquisition ×4 · Leverage ×4 · Defensibility ×3 · Founder fit ×2 |
| Distribution (Dist) | Clarity ×4 · Discoverability ×4 · Proven channel ×6 · First customers ×3 · Beyond founder ×3 |

- Balanced = 0.4 CF + 0.4 Scal + 0.2 Dist.
- Adjusted = Balanced − penalty (0–15).
- Differences under about 5 points are noise.

**Process.**
1. Six discovery agents (A Consumer, B Physical, C Traditional, D Software, E Distribution, F Contrarian). Each mined a dataset of recent entrants with verifiable outcomes.
2. A leader auditor re-measured H7 and M1, and re-checked H6.
3. A 14-item shortlist.
4. An independent evidence auditor and an independent red team, working in parallel without seeing each other's output.

**Reconciliation rule (new in Phase 8, stated before seeing the result).** The two reviewers scored every idea at criterion level, independently. Each final score is the mean of the two reviewers' CF, Scal, Dist and penalty. With two reviewers this is the median. Half-steps are allowed, so no tie-break is needed. Every final score therefore lies between the two reviewers' scores. Leader corrections are applied only as named criterion steps.

**Searches.** 52 WebSearches, each logged in `research-notes/search-log.txt`:

| Agent | Searches |
|---|---|
| A | 6 |
| B | 6 |
| C | 5 |
| D | 6 |
| E | 6 |
| F | 7 |
| Auditors (leader + shortlist) | 8 |
| Red team | 8 |

Most evidence came from primary data:
- TrustMRR `.md` pages
- iTunes Search API
- Empire Flippers public listing API, with monthly P&L
- Crowd Supply project pages
- WordPress.org plugins API
- npm download API
- Superhive embedded JSON
- statute text at gesetze-im-internet.de
- platform help centres

**Crawl note.** Agent D's TrustMRR crawl was stopped by the orchestrator at 7,866 of 11,435 sitemap pages, after about 3 hours, to bound runtime.
- Slugs had been shuffled first (seed 8), so the collected pages are a 69% random sample.
- There were 3 HTTP 404 errors, no throttling and no truncated files.
- The base rates above are sample estimates.

**Boundaries kept.**
- No contact with anyone, no purchases, sign-ups or browser use, and no deployment.
- No personal identifiers were sent in requests; generic User-Agents only.
- Blocked sources were reported, not bypassed:
  - Kalshi developer agreement (HTTP 429)
  - Fresha integrations and Data Connector pages (JavaScript-only)
  - Shopify App Store search (login wall)
  - five Mexican SaaS sites (403)
  - Indie Hackers
  - Sage North America partner PDFs (403)

---

## 2. Research direction and why

Phases 5–7 measured newcomer outcomes on about 30 channels. Channels kept rewarding incumbents, audience owners and suppliers with references. The only verified newcomer success without an audience came from a pattern rather than a channel: Conductor, a missing-API product found by developers searching for it.

Phase 8 therefore worked backwards from verified recent winners. The question was which replicable traits let a newcomer without an audience reach $2k+/month, across both software and non-software.

---

## 3. Discovery: what each dataset showed

### Agent A: App Store (19,614 new non-game apps)

**Base rates:**
- Median 2 ratings per new app.
- 5.8% reach 1k ratings; 1.3% reach 10k.
- Individual developers aged 15+ months reach 1k ratings 4.9% of the time.
- RevenueCat: 17% of monetising apps reach $1k MRR within two years. RevenueCat counts only monetising apps, so this overstates the newcomer rate.

**Patterns among winners:**

| Pattern | Evidence |
|---|---|
| Enter a hobby or OS boom in its first 6–12 months | 15–30% hit rate early, versus 1–6% after studios clone it |
| Money-adjacent value at weekly prices | PropGPT: $82k MRR verified, 194 X followers, organic short video; the spike came at about video #70 |
| Portfolio studios | About 1 hit per 8–16 launches |

**Supply is accelerating.** AI-built apps roughly tripled newcomer volume from 2024 to 2026.

### Agent B: physical products

**Crowd Supply:** see the table in the bottom line. Manufacturer partner programmes, such as Elecrow Project Aviary and Soldered Inkubator, fund production.

**Empire Flippers physical businesses earning since 2022:**
- Median profit $6.9k/month.
- Non-English EU brands $9.4k versus US $5.7k (small n).
- **The auditor found the Czech comparable (#91698) averaged −$4.1k/month profit over Feb–May 2026, with the owner working 30 hours/week.**

**H2 rescore evidence:** MiciMike's Google Home Mini board raised $133k on Crowd Supply. It is undelivered and now ships January 2027.

### Agent C: Empire Flippers and Flippa young businesses

**Shape of the market:**
- About 4% of young listings are services.
- Young winners report a median of 5 owner hours/week, achieved through contractor teams of 8–35 people. The red team notes this is partly a sale-readiness artefact.

**Comparables:**

| Listing | What it is | Audit finding |
|---|---|---|
| #94286 | Healthcare certification study kits sold through Facebook ads: $2.1M revenue and $433k profit in 12 months | Co-broker listing. Profit fell from about $51k/month in H2 2025 to about $11.7k/month in Apr–Jun 2026, an 11% margin. |
| #86244 | French human-plus-AI guest-messaging desk: about 130 customers, $8.6k/month profit | Monthly profit swung between −$345 and $18.8k |

### Agent D: TrustMRR (7,883-profile random sample)

- Produced the base rates and traits in the bottom line.
- **Conductor is the only legacy-integration API in the sample.**
- No 2024–26 accounting or ERP integration reached $1k MRR.
- Developer tools and APIs as a whole underperform: 2.2% hit rate, 0.63× lift.

### Agent E: acquisition channels of 440 winners

**Share of startups on each channel page earning $2k+ in the last 30 days:**

| Channel | Share |
|---|---|
| Hacker News | 4.7% |
| Product Hunt | about 5% |
| Google Ads | ≥15% |
| TikTok Ads | 34% (lower bound) |
| YouTube Ads | 44% (lower bound) |

**Founders without an audience:**
- 116 of 157 winners founded 2023+ had founders with under 1k X followers; their median was $9k per 30 days.
- Among clean cases, organic short-form video accounted for 34% and search for 28%.

**Warning:** organic-video revenue decays when posting stops. AppAlchemy claimed $17k but verified at $5.5k.

### Agent F: does the Conductor pattern generalise?

**The original niche is already being copied.** Three priced QuickBooks Desktop APIs appeared in 2026: Nxus, TenkeyBridge, and Desktop Accounting API at $49/file. Monthly npm downloads:

| Package | Downloads last month |
|---|---|
| Conductor | 53,125 |
| Copies | about 3.3k, 1.3k and 282 |

**Remaining gaps:**
- CONTPAQi (Mexico): an existing $720/year API was found by the auditor.
- TallyPrime: crowded.
- Sage Pastel: Sage-gated.

**Killed:** DATEV; Hashavshevet, which has an official API (H-CONNECT); construction systems.

**Pattern:** newcomers win by pricing below an incumbent's minimum price.

---

## 4. Shortlist (14)

| ID | Idea | Source |
|---|---|---|
| N1 | German online food-hygiene certificate (Alimentia model) | E |
| N2 | Certification study kits via paid social, no personal brand | C |
| N3 | Self-serve CONTPAQi integration API (variants: TallyPrime, Sage Pastel) | F |
| N4 | German human-plus-AI guest-messaging desk for short-term-rental managers | C |
| N5 | Local-language Meta-ads store in a small EU market (variant: high-ticket dealer store) | B/C |
| N6 | Firmware-first field tool on Crowd Supply through a manufacturer partner | B |
| N7 | Trend-timed collectible value-scanner app micro-studio | A |
| N8 | Kalshi/Polymarket research and alert companion | A |
| N9 | QR guest photo-sharing for events in an under-served language | E |
| N10 | Hebrew copy of a proven AI consumer-app category | E |
| N11 | Review-and-rebooking add-on for Fresha/Booksy salons (with a Fresha integration API) | D |
| N12 | Recurring Google Merchant Center policy monitor for WooCommerce stores and agencies | D |
| N13 | Connector supplier to unified-API aggregators | F |
| N14 | Organiser apps for amateur padel, beach tennis or darts outside the US | A |

Not shortlisted, with reasons in `shortlist.md`:
- cruise price-drop monitor
- Slant 3D made-to-order tools
- niche paid-ads agency
- Spanish/Italian phone-prospecting data (GDPR)
- Agent D's kills: Thumbtack responders, Upwork proposal automation, business-owner lead data, file-downgrade tools, vending directories, OpenClaw wrappers, generic AI ads/SEO agents
- Agent F's kills

---

## 5. Adversarial review: what the auditor and red team established

**Kills and contradicted claims, all from primary sources:**

| ID | Finding |
|---|---|
| N1 | §43(1) IfSG: only the Gesundheitsamt or a doctor it commissions may give the initial briefing. Gesundheitsämter already sell it online for €28 (LRA Fürth, Nürnberger Land). The private remainder (LMHV training and the 2-yearly follow-up briefing) is an employer purchase with 20+ online sellers at €29–35 (IHK Frankfurt list, hygieneschulung.org, TÜV Nord). Alimentia reproduces ($167.8k all-time) but has plateaued since July. Its own site says no official Spanish card exists. **Killed as specified.** |
| N11 | Fresha ships "Google Rating Boost" natively. Its Partner Terms forbid sharing credentials and hosted resale; its Terms of Use ban scrapers and bots. Booksy's API is alpha and partner-gated. MyFrank is not a booking add-on. Coucou reproduces ($5.9k MRR) but took about 19 months to get there. **Fresha route killed; the Fresha integration API dies with it.** |
| N12 | "No WooCommerce monitor exists" is **false**. Four 2025–26 WordPress.org entrants target this, with 0–30 installs. The Shopify analogue reproduces ($14,745 MRR, 244 subscriptions) but was flat January–July and is listed for sale at 0.9× revenue. |
| N3 | AR Software already sells a cloud CONTPAQi API with a local sync agent at $720/year per RFC (Mexican tax ID, one per company). Bind ERP built its own connector. Thirty of 33 Mexican SaaS homepages don't mention CONTPAQi. |
| N2 | #94286 is a co-broker listing whose profit is falling (see §3). |
| N10 | The Hebrew calorie-app category already has three Hebrew-native apps plus a localised entrant (2,520–3,372 ratings). |
| N13 | No evidence that any aggregator licenses outside connectors. Chift builds its own local agents. |
| N8 | Kalshi's developer agreement was unreadable (HTTP 429). Of 224 companion apps released since 2025, only three have more than 100 ratings. |

**Cross-cutting attacks (red team):**
1. **Every comparable is n=1 from a survivor list.**
   - TrustMRR stealth listings hit 24%, and listings for sale 5.7%, versus 3.0% for the rest.
   - Empire Flippers has an intake floor.
   - App Store search caps at 200 relevance-ranked results.
2. **The copy flood arrives within about 6 months.**
3. **No idea has a measured newcomer CAC.** $2k buys one or two credible ad tests.
4. **Solo founders underperform** (0.8× versus 4.4× for small teams).
5. **Israel fit:** EU time zones are fine. Mexico and the US give 0–3 hours of overlap. German, Spanish, Czech and Swedish B2B selling needs hired native speakers.

---

## 6. Phase 8 scoring (frozen rubric, criterion level)

Each final score is the mean of the auditor's and the red team's scores (§1). Both sets of criterion steps are in the review files.

| ID | Auditor steps (CF / Scal / Dist, pen) | Red-team steps (CF / Scal / Dist, pen) | **CF** | **Scal** | **Dist** | Balanced | Pen | **Adjusted** | Aud / RT |
|---|---|---|---|---|---|---|---|---|---|
| N12 WooCommerce Merchant Center monitor | 3,3,5,5,4 / 2,3,2,4,0,5 / 4,3,1,2,2, 13 | 2,3,5,5,4 / 2,4,2,4,0,4 / 4,3,1,2,2, 13 | 76.5 | 53.0 | 46.0 | 61.0 | 13 | **48.0** | 48.6 / 47.4 |
| N1 Hygiene certificate (employer remainder) | 2,3,5,4,4 / 3,2,2,4,1,3 / 4,3,1,2,3, 13 | 3,3,4,4,4 / 2,2,3,4,1,2 / 3,4,2,2,3, 12 | 70.5 | 49.5 | 52.0 | 58.4 | 12.5 | **45.9** (original killed) | 44.8 / 47.0 |
| N9 QR event photos | 4,3,5,3,4 / 2,0,3,4,1,4 / 4,3,2,2,3, 13 | 3,3,4,3,4 / 2,1,3,4,1,3 / 4,3,2,2,3, 13 | 71.5 | 46.0 | 55.0 | 58.0 | 13 | **45.0** | 46.4 / 43.6 |
| N11 Salon add-on (Booksy remainder) | 3,2,4,4,3 / 2,5,2,4,0,4 / 4,2,1,2,2, 14 | 3,2,4,4,3 / 3,5,2,4,1,3 / 4,2,1,2,2, 14 | 64.0 | 60.0 | 42.0 | 58.0 | 14 | **44.0** (Fresha killed) | 43.2 / 44.8 |
| N3 CONTPAQi API | 2,2,4,5,3 / 2,5,2,4,1,4 / 3,3,1,2,3, 13 | 2,1,4,5,3 / 2,5,2,4,1,2 / 3,2,1,2,3, 13 | 61.0 | 59.0 | 43.0 | 56.6 | 13 | **43.6** | 45.6 / 41.6 |
| N7 Collectible-scanner studio | 3,3,4,4,2 / 3,4,2,3,0,4 / 3,3,2,2,2, 12 | 3,3,4,4,2 / 3,4,2,3,0,3 / 3,2,2,2,2, 13 | 65.0 | 52.0 | 46.0 | 56.0 | 12.5 | **43.5** | 44.8 / 42.2 |
| N8 Prediction-market companion | 3,3,5,4,2 / 3,4,2,3,0,4 / 3,3,1,2,2, 13 | 3,3,4,4,2 / 3,4,2,3,0,2 / 3,2,1,2,2, 13 | 67.0 | 51.0 | 40.0 | 55.2 | 13 | **42.2** | 44.2 / 40.2 |
| N2 Certification study kits | 4,3,3,3,4 / 3,1,3,4,1,2 / 4,3,2,2,4, 12 | 4,2,2,3,3 / 3,1,3,3,1,2 / 4,3,2,2,3, 13 | 62.5 | 46.0 | 56.5 | 54.7 | 12.5 | **42.2** | 46.0 / 38.4 |
| N10 Hebrew AI consumer app | 3,3,3,3,2 / 1,4,2,3,0,4 / 2,3,2,2,2, 13 | 3,3,3,3,3 / 1,4,3,3,1,5 / 3,3,2,3,3, 12 | 58.5 | 51.5 | 49.0 | 53.8 | 12.5 | **41.3** | 37.4 / 45.2 |
| N4 German guest-messaging desk | 4,3,4,2,2 / 3,5,2,3,1,2 / 4,2,2,2,2, 12 | 3,2,4,2,2 / 3,5,2,2,1,1 / 4,2,1,2,2, 12 | 57.5 | 53.0 | 45.0 | 53.2 | 12 | **41.2** | 44.8 / 37.6 |
| N14 Padel organiser apps | 2,3,5,4,4 / 1,2,1,4,0,4 / 3,3,1,2,1, 13 | 1,3,5,4,4 / 1,2,1,4,0,3 / 3,2,1,2,1, 12 | 67.5 | 38.0 | 37.0 | 49.6 | 12.5 | **37.1** | 38.4 / 35.8 |
| N5 Small-EU Meta-ads store | 4,3,2,2,3 / 4,1,3,3,1,1 / 3,3,2,2,3, 13 | 4,3,1,2,2 / 3,1,3,3,0,1 / 3,3,2,2,3, 13 | 53.5 | 42.0 | 51.0 | 48.4 | 13 | **35.4** | 38.0 / 32.8 |
| N6 Crowd Supply field tool | 3,1,3,3,2 / 2,1,2,2,2,2 / 4,3,3,2,3, 11 | 3,1,2,3,2 / 2,1,2,3,2,2 / 4,3,3,2,2, 11 | 47.0 | 38.0 | 59.5 | 45.9 | 11 | **34.9** | 35.2 / 34.6 |
| N13 Connector supplier | 1,1,4,4,3 / 1,4,1,4,1,4 / 4,2,0,1,1, 14 | 1,1,4,4,3 / 1,3,1,3,2,3 / 4,1,0,1,1, 14 | 50.0 | 46.5 | 28.0 | 44.2 | 14 | **30.2** (kill) | 32.0 / 28.4 |

**Where the reviewers disagreed by more than 5 points:**

| ID | Auditor | Red team | Why they differ |
|---|---|---|---|
| N2 | 46.0 | 38.4 | Red team: capital and CAC risk |
| N10 | 37.4 | 45.2 | Auditor: category already occupied. Red team: founder fit and channel. |
| N4 | 44.8 | 37.6 | Red team: German-language labour and Smoobu's native AI |

The mean absorbs these disagreements. No idea's position relative to the top cluster depends on them.

**Leader corrections (criterion steps):**

| Leader | Before | Change | After (CF / Scal / Dist, pen) | Dissent |
|---|---|---|---|---|
| H7 Blender add-ons | 80 / 58 / 67, pen 12 → 56.6 | Proven channel 3→2. Superhive median of 2.5 sales in the first 3 months; 5.6% reach 100+; supply tripled. | 80 / 58 / 61, pen 12 → **55.4** | Red team 54.8 (first customers −1). Not applied: it re-prices the same base rate already used for the proven-channel cut. |
| M1 Sage 50 API | 68 / 63 / 58, pen 12 → 52.0 | Depth 2→1 (both reviewers): vertical-SaaS ratio 0.12; 0 of 97 vendors in M1's verticals. Proven channel 2→1 (red team): Conductor is n=1 in a 69% random TrustMRR sample, and no 2024–26 accounting or ERP integration reached $1k MRR. | 68 / 60 / 52, pen 12 → **49.6** | Auditor 50.8 (depth only). Red team 48.4 (also defensibility 1→0). Penalty 13 would apply if the Sage 50 agreement matches the Sage 300 template. |
| H2 revival boards | 38.6 | Spending +1 (MiciMike's verified $133k raise without an audience). First customers +1 (about 92% of launched Crowd Supply campaigns funded). | 49 / 48 / 62, pen 10 → **41.2** | Auditor about 41. Neither reviewer would shortlist it: no orphaned target device (Bose published a local API). |
| H6 college-baseball API | 52.2 | None. The CFBD (CollegeFootballData) jump came from its 2025 API paywall and 2026 user surge. | 52.2 | — |
| M2 licensed data API | 44.4 | None. SoldComps ($347 → $19,984/month, April–September 2026) parses eBay pages against eBay's 2026 User Agreement, which is the opposite of M2's licensed premise. | 44.4 | Auditor allows at most +1.2 |

---

## 7. Five finalists: deep dives

**Selection rule:** the top five by Adjusted score, excluding ideas whose original specification was killed by a hard blocker. That excludes N1 and N11, whose remainders keep their scores in the ledger.

The finalists are N12, N9, N3, N7 and N2. N7 (43.5) and N8/N2 (42.2) are within noise of each other. N2 was chosen over N8 because it has a verified large-revenue comparable, and N8's Kalshi terms are unread.

**All scenario numbers below are [Hypothesis]:** model outputs built from the cited comparables, not observations.

### F1. WooCommerce Merchant Center policy monitor (N12): 48.0

**Offer**
- A WooCommerce plugin plus SaaS that continuously checks products, prices, stock, policies and checkout against Google Merchant Center rules.
- It alerts before a disapproval or suspension.
- Agencies get a multi-store dashboard.
- Price: about $29–79/month per store and about $199/month per agency [Hypothesis].

**Spending evidence**

| Fact | Status |
|---|---|
| Shopify analogue: $14,745 MRR, 244 subscriptions (about $60 each), 0 X followers; channels: affiliates, influencers, partnerships | [Verified: TrustMRR, Lemon Squeezy] |
| The analogue is flat at about $8k January–July 2026, then jumps; for sale at 0.9× revenue | [Verified] |
| WooCommerce merchants pay recurring fees for this | **[Unknown]** |

**Competition**
- Google for WooCommerce (800k installs) surfaces Merchant Center issues inside WordPress.
- Feed plugins (10k–90k installs) could add a check.
- Four 2025–26 newcomers have 0–30 installs.
- Free checkers (AdNabu) and a $99 one-off audit anchor the price.

**Acquisition and channel**
- WordPress.org is measured as near-zero for newcomers in this exact niche.
- The analogue's route is affiliates and partnerships, here Google Shopping agencies and WooCommerce developers.
- CAC [Unknown].

**Economics and labour**

| Item | Estimate |
|---|---|
| Capital | Under $1k: hosting, a test store, a Merchant Center account |
| Gross margin | 85–90% |
| Labour | Build 1–2 months part-time; then rule maintenance as Google policies change, plus partner recruiting (founder-led at first) |

| Scenario | Subscriptions | Owner profit |
|---|---|---|
| Downside | 0–20 | $0–800/month; the WordPress.org channel stays at zero and agencies don't adopt |
| Base (18–24 months) | 60–120 | **about $2.5–5k/month** |
| Upside | 300+, matching the Shopify analogue | about $12–15k/month |

**Key assumptions**
1. Merchants or agencies pay a recurring fee rather than using free checks.
2. Agencies or affiliates will sell it.
3. A crawler can see enough of the suspension causes to matter. Business verification and product claims are not visible to one.

**Track fit:** A, with an unproven B upside.

### F2. QR guest photo-sharing in an under-served language market (N9): 45.0

**Offer**
- A per-event web gallery that guests reach by scanning a QR code. No app install is needed.
- Hebrew first, or Polish.
- About €49–99 per event [Hypothesis].

**Spending evidence**

| Fact | Status |
|---|---|
| German comparable: $549k all-time since April 2024, 0 followers, Google Ads + SEO + Instagram, 45% margin | [Verified: TrustMRR] |
| Comparable is listed for sale at $1.5M | [Verified] |
| Strong seasonality: $6.5–9.3k/month in Nov–Feb versus $28–52k/month in Apr–Aug | [Verified] |

**Competition**
- 141–151 wedding photo-sharing apps released since 2024 per storefront, none with 100+ local ratings.
- Global web players: Kululu (free to start), POV, WedShoots.
- Israel has tiny 2025–26 app entrants only, but WhatsApp groups and photographers' print stations are substitutes [Hypothesis].

**Acquisition and channel**
- Google Ads on wedding and event queries.
- Wedding-venue and photographer referrals.
- CAC [Unknown].

**Economics and labour**

| Item | Estimate |
|---|---|
| Capital | Under $1k build, plus an ad test |
| Labour | Low after the build; per-event support is light |
| Recurring revenue | None; every sale is a new acquisition |

| Scenario | Owner profit |
|---|---|
| Downside | Google Ads cost per paid event exceeds the price; about $0 |
| Base | **about $1.5–3k/month averaged over the year**, with $4–6k peak months |
| Upside (several languages) | about $8–12k/month averaged |

**Key assumption:** Google Ads cost per paid event is at most €30 in a market whose web competitors have been counted.

**Track fit:** A.

### F3. Self-serve CONTPAQi integration API (N3): 43.6

**Offer**
- A hosted REST API plus a Windows agent, giving SaaS vendors and fintechs access to CONTPAQi Comercial and Contabilidad.
- About $40 per RFC per month, undercutting AR Software's $60 [Hypothesis].

**Spending evidence**

| Fact | Status |
|---|---|
| CONTPAQi claims 1.2M companies | [Vendor claim] |
| AR Software sells an API at $720/year per RFC; sales unknown | [Verified listing] |
| Bind ERP built its own connector | [Verified] |
| Vendors pay a third party for this | **[Unknown]** |

**Competition**
- AR Software.
- In-house connectors.
- CONTPAQi's own distributor network.

**Acquisition and channel**
- Developer search in Spanish.
- Integration pages.
- The founder is 8–9 hours ahead of Mexico.

**Economics and labour**

| Item | Estimate |
|---|---|
| Capital | Under $2k, including a CONTPAQi licence |
| Labour | Windows-agent support in Spanish, ongoing |

| Scenario | Paying vendors | Connected companies (RFCs) | Owner profit |
|---|---|---|---|
| Downside | 0–5 | — | under $500/month |
| Base (24 months) | 10–20 | 60–150 | **about $2–5k/month** |
| Upside (CONTPAQi + Aspel + Tally portfolio) | — | — | about $10–15k/month |

**Key assumptions**
1. At least 30 vendors would pay.
2. CONTPAQi's SDK terms allow a hosted service. These terms were **not found**.
3. A visible win isn't cloned within about 6 months, which is the measured QuickBooks Desktop precedent.
- **Kill test (red team):** of about 100 Mexican vendor integration pages, fewer than 10 list CONTPAQi.

**Track fit:** A.

### F4. Trend-timed collectible value-scanner micro-studio (N7): 43.5

**Offer**
- Ship a camera-based "what is this worth" app within weeks of a new collecting boom.
- Then localise it.
- Weekly or annual subscription.

**Evidence**

| Fact | Status |
|---|---|
| Early-cohort indie wins are real: Acorn has 15.5k ratings | [Verified] |
| Hit rate is 15–30% in the first 6–12 months of a boom versus 1–6% after clones | Agent A |
| TCG scanners: 1 of 5 hits in the early cohort; 6 of 104 in 2026H1 | [Verified] |
| Next Vision's ToyWorth reached #2 in LEGO value within months | [Verified] |
| 112 card-scanner entrants in 2026 | [Verified] |

**Risks**
- eBay's 2026 User Agreement bans scraping, so price data must be licensed; costs and terms are [Unknown].
- The founder is not a collector, and the early wins went to hobby insiders.
- It needs short-form video volume, which is founder labour or paid UGC creators.

**Economics and labour**
- Portfolio economics: about 1 hit per 8–16 launches.

| Scenario | Owner profit |
|---|---|
| Downside | 4–6 launches, no hit; lose about $1–2k |
| Base | One app at **$1–3k/month** within 12 months, decaying after 12–18 months |
| Upside | A hit at $10–30k/month for 6–18 months |

**Key assumption:** an outsider can identify a boom and ship before the studio wave.
- **Kill test:** backtest the first-scanner versus first-studio-clone gap for Labubu, Lorcana and One Piece using the iTunes API. Kill if the median gap is under 8 weeks.

**Track fit:** Track B only as a lottery, at about the 2–5% per-product base rate that H7 also has.

### F5. Certification study kits via paid social (N2): 42.2

**Offer**
- Printed and digital study kits for one niche professional certification.
- Sold through Meta and TikTok ads with no personal brand.
- One-off price of about $40–80.

**Evidence**

| Fact | Status |
|---|---|
| EF #94286: $2.1M revenue and $433k profit in 12 months | [Verified listing data; co-broker prepared] |
| #94286 margin decline: about $51k/month profit in H2 2025 to about $11.7k/month in Apr–Jun 2026, an 11% margin | [Verified: EF P&L] |
| Distinct from the excluded licensure exam-prep apps by format and channel only | — |

**Risks**
- n=1 survivor, with the niche undisclosed.
- CAC is unknown and the budget covers one test.
- Meta's health-adjacent ad review.
- Subject-matter-expert cost of about $500–1,000.
- Thin founder fit.

**Economics and labour**

| Scenario | Owner profit |
|---|---|
| Downside | The ad test fails; lose about $1.5–2k |
| Base | $20–40k/month revenue at 10–20% margin → **$2–8k/month** |
| Upside | The comparable's average, about $36k/month, which the comparable itself no longer earns |

**Key assumption:** first-order CAC at or below 40% of the average order value in a certification with weak incumbents.

**Track fit:** A, with high variance.

---

## 8. Cumulative leaderboard (all phases; * = corrected in Phases 5–8)

| Rank | Opportunity | Phase | Adjusted |
|---|---|---|---|
| 1 | Blender/VRChat add-ons (H7) | 3 | **55.4*** (was 56.6) |
| 2 | College-baseball data API (H6) | 3 | 52.2* |
| 3 | Framer vertical kit (K8) | 5 | 52.0* |
| 4 | Meshtastic family kits (H1) | 3 | 51.2* |
| 5= | monday.com Israeli invoicing app | 1 | 50.8* |
| 5= | Apify Actors (J7) | 4 | 50.8* |
| 7 | Hebrew tender + receivership intelligence (K13) | 5 | 50.6* |
| 8 | UK MTD prep for accountants | 2 | 50.2* |
| 9 | Israeli allocation verification | 1 | 49.8 |
| 10 | Sage 50 US/CA integration API (M1) | 7 | **49.6*** (was 52.0) |
| 11= | Ketubot (H10) | 3 | 49.4* |
| 11= | Spanish Holy Land box (H8) | 3 | 49.4 |
| 11= | Non-US availability alerts (H5) | 3 | 49.4 |
| 14 | Pay-per-call emergency lead sites (L6) | 6 | 48.8 |
| 15 | Hebrew/Russian memoir books (J1) | 4 | 48.6* |
| 16= | Hebrew personalised kids' books (J2) | 4 | 48.2 |
| 16= | Judaica STL (H4) | 3 | 48.2 |
| 18= | **WooCommerce Merchant Center monitor (N12)** | **8** | **48.0** |
| 18= | MT5 prop-rule utility (J9) | 4 | 48.0 |
| 20 | Remote b'nai mitzvah (H9) | 3 | 47.8 |

**Cross-phase verdict**
- The board is flat: #2–#20 span 47.8–52.2, about one noise band.
- H7 is nominal #1 by 3.2 points, within noise.
- After the Superhive re-measure, H7 is per product about a 2–5% lottery. That is the same order as TrustMRR's 3.9% and the App Store's 4.9%. The rubric's Cash-Flow score rewards its cheap, fast start, not its odds of reaching $2–5k/month.
- M1's fall removes the one top-cluster idea whose analogue was a verified newcomer success without an audience.
- Phase 8 shows that analogue is a statistical outlier (n=1) and already being copied.

---

## 9. Three most promising Phase 8 discoveries

1. **Fastest cash flow: QR event photo-sharing in Hebrew or Polish (N9).** It is cheap to build, paid per event and sold through search ads. It has a verified $549k comparable without an audience.
   - *Key assumption:* Google Ads cost per paid event is at most €30.
2. **Most scalable: WooCommerce Merchant Center monitor (N12).** It is recurring, high-margin and agency-multipliable.
   - *Key assumption:* agencies or affiliates sell it. The WordPress.org channel is measured at near zero.
3. **Best risk-adjusted: also N12.** It has the highest Phase 8 score, capital under $1k, and a desk-checkable kill test: re-query the four entrants' installs after 60 days.
   - *Runner-up:* N9.

**The most valuable Phase 8 output is not an idea but a set of measurements** that every later phase should use:
- newcomer base rates of 3.9–5.8%
- the price-per-account lift
- the team lift
- paid and partner channels outperforming launch sites
- the 6-month copy window

---

## 10. Research limitations

- **Survivor datasets.** TrustMRR, Empire Flippers/Flippa and App Store search contain few or no failures, so all base rates are upper bounds. All comparables are n=1.
- **Partial sample.** The TrustMRR sample is 69% of the sitemap; the crawl was stopped for runtime. Founding dates are self-entered, and 16% are missing.
- **Unverified load-bearing facts:**
  - CONTPAQi SDK terms
  - Kalshi developer terms
  - Fresha's Data Connector scope
  - newcomer CAC for any idea
  - WooCommerce merchants' willingness to pay
  - Sage 50 partner agreement text
- **Blocked sources:** listed in §1.
- **Scoring:** the new reconciliation rule (mean of reviewers) differs from Phases 6–7, where reconciliation was a judgement call. It is applied only to Phase 8's new ideas. Leader corrections still use named steps. The rubric still favours cheap digital starts.

---

## 11. Phase 9 direction (decided after this phase)

Phase 8's sharpest finding is that **the copy window is about 6 months**. Every visible newcomer niche checked had been entered within that time. AI-built supply roughly tripled from 2024 to 2026.

Ideas whose only edge is "first to notice" therefore decay before they pay back. That applies to H7, N7, N12 and M1.

**Phase 9 will look for copy-resistant positions open to this founder.** That means businesses where a newcomer's edge comes from something a fast follower cannot clone in weeks:
- a licence, certification or regulated status that takes months to obtain but is open to the founder;
- exclusive or contracted data, supply or rights;
- local network effects in thin markets, such as two-sided local marketplaces or community-run registries;
- physical presence or assets in Israel;
- Hebrew, Israeli-regulatory or Israeli-institutional knowledge;
- relationships that are bought (acquired small businesses with contracts) rather than built.

Each agent must give evidence of the moat (time-to-copy) as well as of spending, and use the Phase 8 base rates as the prior.

**Leader re-check:** desk-test the decisive assumptions of the top cluster that can still be resolved:
- **H6:** NCAA and conference data rights.
- **K8:** Framer marketplace newcomer outcomes.
- **H1:** Meshtastic kit newcomer outcomes on Tindie and Etsy.
- **M1:** the Sage NA partner programme terms, via Wayback.
