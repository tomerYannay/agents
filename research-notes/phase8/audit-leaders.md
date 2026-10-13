# Phase 8 leader re-check (Evidence Auditor, P8-AUDIT-L)

Date: 2026-10-13. Desk research only: public pages, public JSON and Wayback snapshots. No browser tools, sign-ups or contact with anyone. No personal identifiers were sent in any request; the User-Agent was generic.
WebSearch: **3 of 8 used**, all logged as `P8-AUDIT-L`. Everything else came from curl/WebFetch:
- Superhive listing and product pages (rate-limited at 2–2.5 s per request, no throttling seen);
- Gumroad's search JSON;
- 286 vendor websites (homepages, integration pages and sitemaps);
- Graphtreon, collegefootballdata.com, the CFBD/Rad Sports Analytics blog, and Wayback CDX snapshots;
- a Wayback copy of a Sage Developer Partner agreement PDF.

Scripts are in `scratchpad/p6plus/P8-auditL/scripts/` and data in `.../P8-auditL/data/`.

Scoring basis (as in Phases 5–7): one step on a criterion = weight/5 points. Proven channel 6, scalable acquisition 4, spending 5, defensibility 3, first customers 3, depth 3. The penalty changes only when a decisive assumption is **directly** contradicted.

## Summary

| Leader | Was | Recommended | Change | Main reason |
|---|---|---|---|---|
| H7 Blender/VRChat add-ons | 56.6 | **55.4** | −1.2 | First precise newcomer numbers. Median paid add-on: **2.5 sales in its first 3 months**; lifetime median plateaus at **about 10–15 sales (≈$90 gross)** after 6–21 months. New listings roughly **tripled**: about 100/month in 2025, about 250–385/month in Jun–Sep 2026. Hits still happen: 2.2% of the 2025–26 sample passed 500 sales. |
| M1 Sage 50 US/CA API | 52.0 | **52.0 (hold)** | 0 | Census ratio of Sage 50 US/CA to QuickBooks Desktop is **0.19 overall** (13 vs 70 vendors) but **0.12 for vertical SaaS without AP/finance platforms**. It is **0 of 97** in legal, nonprofit, property management and payroll. That is between the red team's kill (≤0.08) and keep (≥0.2) lines. Sage developer-agreement language found is restrictive but is not the Sage 50 agreement. |
| H6 College-baseball API | 52.2 | **52.2 (hold)** | 0 | CFBD's 2025 jump followed a **monetisation change**: API v2 in Jan 2025 capped free use at 1,000 calls/month behind Patreon tiers, and v1 shut down before the 2025 season. Its 2026 jump is a **top-of-funnel surge**: claimed users went from 9,000+ to 21,000+ between Jul and Oct 2026, with about 17% conversion unchanged. Neither is replicable by a newcomer, and the evidence cuts both ways. |

After this audit H7 is still nominal #1 (55.4), now about 3 points above H6 (52.2) and M1/K8 (52.0). That gap is inside the noise band.

---

## 1. H7: Superhive newcomer outcomes, 2026 vs 2025 (56.6 → 55.4)

### Method
- I crawled the add-ons category in "Newest" order, pages 1–185 of 248 (24 per page; page 146 returned a 500 error). That gives 4,388 listings, from Oct 2026 back to mid-2023.
- From each listing page I opened 2 product pages, at positions 1 and 13: 367 products in total.
- Each product page carries embedded JSON with exact `published_at`, `order_items_count` (paid sales), `free_order_items_count`, `product_ratings_count` and `price`.
  - Check: CatFlow's JSON shows 15 paid orders, and its visible badge shows "Sales 10+" [Verified: superhivemarket.com/products/catflow, 2026-10-13].
  - This is more precise than Phase 5, which used visible badges that hide counts under 10.
- Free and $0-minimum items are excluded from sales statistics (10 items).
- **Survivorship caveat:** only currently published products are visible, so older cohorts are flattered.

### Verified results [Verified: superhivemarket.com product JSON, crawled 2026-10-13]

**Outcomes by age at crawl (paid products):**

| Age at crawl | n | Median sales | ≥10 | ≥50 | ≥100 | p90 | Max |
|---|---|---|---|---|---|---|---|
| 0–3 months (Jul–Oct 2026) | 84 | **2.5** | 13% | 0% | 0% | 11.5 | 32 |
| 3–6 months | 44 | 4 | 30% | 7% | 5% | 39.5 | 1,325 |
| 6–9 months | 33 | 12 | 58% | 12% | 3% | 59.6 | 197 |
| 9–12 months | 25 | 13 | 52% | 16% | 8% | 291 | 726 |
| 12–15 months | 30 | 11 | 60% | 17% | 13% | 119 | 616 |
| 15–18 months | 25 | 10 | 52% | 16% | 8% | 179 | 503 |
| 18–21 months | 24 | 15.5 | 62% | 25% | 17% | 215 | 925 |
| 21–25 months (late 2024) | 23 | 24 | 74% | 35% | 22% | 373 | 437 |

**Outcomes by publication cohort:**

| Cohort | n paid | Median | ≥10 | ≥50 | ≥100 | Median price |
|---|---|---|---|---|---|---|
| 2024 (pages 135–185) | 64 | 37 | 86% | 42% | 31% | $9 |
| 2025 H1 | 50 | 12.5 | 56% | 20% | 12% | $9 |
| 2025 H2 | 50 | 12.5 | 58% | 14% | 10% | $10 |
| 2026 H1 | 80 | 7 | 42% | 11% | 5% | $11 |
| 2026 Q3–Oct | 89 | 3 | 13% | 0% | 0% | $15 |

**Key readings:**
- **Early-life sales are small but usually non-zero.**
  - 79% of add-ons less than 3 months old have at least 1 sale.
  - Their median is 2.5 sales, and their median gross is about **$30**.
  - Phase 5's "<10 in the first 2–3 months" was right. The precise median is about 3.
- **Sales plateau.** The median does not grow much after about 6 months: 12 at 6–9 months, 11 at 12–15, 10 at 15–18.
  - A typical add-on's lifetime is about **10–15 copies**.
  - Gross revenue for add-ons aged 6–15 months: median **≈$90**, p75 ≈$340, p90 ≈$1,600 (price × paid orders, before the Superhive fee).
- **Same-age comparison, 2026 vs 2025:** the snapshot cannot give equal-age data for both cohorts. The 2026 H1 add-ons at 6–9 months (median 12) match the 2025 cohort's lifetime at 12–18 months (10–11). So **I find no evidence that a 2026 newcomer sells less than a 2025 newcomer at the same age.**
  - The 2024 cohort is clearly stronger (median 37). Part of that is survivorship, and part may be lighter competition then.
- **Hits still happen, but they are rare.**
  - Of 269 sampled paid add-ons from 2025–26, **15 (5.6%) have ≥100 sales and 6 (2.2%) have ≥500**: Light Master Pro 1,325 (May 2026, $12); MultiSculpt 925; TraceGenius Ultimate 726; Stylized Water 635; Simple N-Panel 616; Aperture 503.
  - This matches Phase 5's "curated winners 100–2,000+", but now as a base rate: **about 2% reach Track-A scale** (Light Master Pro ≈ $16k gross in 5 months, about $3k/month).
- **Supply growth.** Monthly new listings were estimated from where sampled publish dates fall in the list (2 samples per 24-listing page, so ±25%):
  - 2024: about 50–90 a month.
  - 2025: about 85–120 a month.
  - Jan–May 2026: about 110–170 a month.
  - **Jun–Sep 2026: about 250–385 a month**, with Sep 2026 the highest.
  - 2026 to date (9.4 months) is about 1,800 listings, against about 1,200 in all of 2025. That is roughly **3× the 2025 monthly rate** by Q3 2026, consistent with Phase 5's "~385/month, up 2.5×".
- **Ratings are scarce:** only 12% of 0–3-month add-ons and 22% of the 2026 cohort have any rating, so rating counts are a poor proxy for sales.
- The `creator_featured` flag appears to be a creator-level attribute. It did not separate outcomes consistently, so it is not interpreted.

**Superhive context:** no press or forum evidence of a creator backlash was found. Superhive's AI policy allows AI assistance and recommends disclosure [Secondary: search snippet of support.superhivemarket.com article 311; P8-AUDIT-L #3].

### Gumroad
- The "blender addon" search reports 2,823 products, the same total as the Phase 5 file one day earlier.
- The "newest" sort returns the same first item as Phase 5's file, so it is not a reliable recency order.
- Product JSON shows `sales_count: null` unless the seller opts in, and there are no publish dates.
- Of the first 198 "newest" results, 52% have at least 1 rating. The median rating count is 1 and the maximum is 32. 54% are pay-what-you-want, so ratings include free downloads.
- **Gumroad newcomer sales cannot be measured from public data.** [Verified: gumroad.com/products/search JSON and a product page, 2026-10-13]

### Unknowns
- The Superhive creator revenue share for 2026 was not re-verified.
- Refunds and delisted products are not visible.
- VRChat-specific add-ons were not separated: Superhive tags were not crawled, and Booth/Jinxxy were not checked.
- How much of the volume is AI-generated.

### Recommended rescoring

| Criterion | Change | Points | Evidence |
|---|---|---|---|
| Proven channel | 3→2 | Dist −6 | The newcomer median is now measured precisely: about 3 sales in 3 months and about 12 lifetime (≈$90 gross). Only about 2% reach Track-A scale, and supply has tripled. This meets the red team's Phase 7 trigger (median <5 in the first months → about 53). The channel still produces some newcomer winners, unlike J7 (proven channel 1), so 2 rather than 1. |
| Speed to first sale | hold | 0 | 79% get at least 1 sale within 3 months, so the first sale is fast. |
| Scalable acquisition | hold at 2 | 0 | Already cut in Phase 5 on the same type of evidence. Not stacked. |
| Penalty | hold 12 | 0 | The decisive assumption (the founder can build top-decile add-ons) is neither confirmed nor contradicted. |

- Distribution 67 → 61.
- Balanced 0.4×80 + 0.4×58 + 0.2×61 = 67.4.
- **Adjusted 55.4** (was 56.6).
- The red team's 53 would also need a scalable-acquisition or margin cut. I don't support that: acquisition was already cut for the same evidence.

**Track A in practice:** at the measured median, about $90 lifetime per add-on, Track A needs either one top-2% hit or a catalogue of roughly 30+ products with top-quartile results. That makes it a hit-seeking portfolio business.

---

## 2. M1: integration-page census, Sage 50 vs QuickBooks Desktop (hold 52.0)

### Method
- I hand-built a list of **286 North American SaaS vendors** in 10 groups: construction 49, field service 40, distribution/inventory/logistics 35, payroll/time 30, AP/finance/fintech 30, nonprofit/church 24, property management 26, legal 20, manufacturing 16, other 16.
  - Seven QuickBooks-ecosystem tools (SaaSAnt, Transaction Pro, Zed Axis, A2X, Synder, Webgility, CommerceSync) were excluded because they are QuickBooks-specific by construction.
- For each vendor I fetched the homepage, up to 7 integration/partner/accounting links, `/integrations`, sitemap URLs naming QuickBooks or Sage, and up to 4 of those pages.
  - A second pass covered vendors that mention QuickBooks without saying Desktop: 143 vendors, up to 6 QuickBooks pages each.
- Regex classification, then manual cleaning of every Sage 50 hit and of the QuickBooks Desktop hits from the first pass.
- 246 vendors returned pages and 40 failed (bot blocks or JS-only).
- **Bias:** the list skews toward larger, well-known vendors; there was no random frame. Help centres were not crawled, which undercounts both QuickBooks Desktop and Sage 50.

### Verified results [Verified: vendor pages fetched 2026-10-13; per-vendor evidence in `data/census/census.json`]

| Group | Vendors | Any QuickBooks | QBD explicit | Sage 50 US/CA | Sage 100C / 300 CRE | Intacct |
|---|---|---|---|---|---|---|
| Construction | 49 | 32 | 17 | 3 | 10 / 13 | 14 |
| Field service | 40 | 28 | 13 | 1 | 0 | 2 |
| Distribution/logistics | 35 | 26 | 6 | 2 | 0 | 3 |
| Manufacturing | 16 | 9 | 2 | 1 | 0 | 0 |
| AP / finance / fintech | 30 | 22 | 10 | 6 | 1 / 3 | 14 |
| Payroll/time | 30 | 22 | 9 | 0 | 0 | 3 |
| Property mgmt | 26 | 16 | 3 | 0 | 0 / 2 | 1 |
| Legal | 20 | 15 | 1 | 0 | 0 | 0 |
| Nonprofit | 24 | 19 | 5 | 0 | 0 | 4 |
| Other | 16 | 7 | 4 | 0 | 0 | 1 |
| **Total** | **286** | **196** | **≈70** | **13** | 11 / 18 | 42 |

**QuickBooks Desktop count:**
- 54 first-pass hits minus 10 false positives (blog or comparison text, a "doesn't work with Desktop" notice, a forum request) = 44.
- Plus 26 found in the second pass, not individually vetted.
- **Range 65–70.**

**Sage 50 US/CA listers (13), cleaned:**
- Vertical SaaS (7): ServiceTitan ("Sage 50 US/Canada"), busybusy, Workyard, HCSS ("Sage 50 (PeachTree)"), ProShop ERP, OrderEase (Canada), Deposco (logo only, probable).
- AP/finance platforms (6): BILL, Stampli, Tipalti, MineralTree, AvidXchange, Avalara.
- Excluded:
  - UK/DE contexts: Deputy (gb), GoCardless, AutoEntry, Pepperi (German).
  - False matches: "Peachtree City GA", "Peachtree Decks", a TimeSlips comparison, a Peachtree pricing comment.
- Workforce.com has `/integrations/sage50` but its region is unclear, so it is left out (+1 if counted).
- **10 of the 13 Sage 50 listers also list QuickBooks Desktop.** Sage 50 is a second desktop connector added by vendors that already serve QuickBooks Desktop, which is Conductor's customer base.

**Ratios against the red-team thresholds (kill ≤0.08, keep ≥0.2):**
- All vendors: 13/70 = **0.19** (0.19–0.21 across the QuickBooks Desktop range; 0.20 if Workforce is included).
- Vertical SaaS only, excluding AP/finance: 7/60 = **0.12**.
- Legal, nonprofit, property management and payroll: **0 Sage 50 among 97 vendors**, against 18 that list QuickBooks Desktop.
- **Verdict: neither kill nor keep.** The overall figure brushes the keep line only because AP platforms, which integrate with everything and build in-house, are counted. For the vertical-SaaS buyers M1 targets, the ratio is about 0.12. Demand concentrates in construction, field service, distribution and manufacturing.

**Other Sage products:**
- In construction, Sage 300 CRE (13 vendors) and Sage 100 Contractor (10) are listed far more often than Sage 50 (3). Intacct is the most-listed Sage product overall (42).
- **Agave API already offers a unified construction API covering QuickBooks Desktop, Sage 300 CRE, Sage 100 Contractor and Sage Intacct, but not Sage 50** [Verified: agaveapi.com/integrations, 2026-10-13]. Pivoting M1 to construction-focused Sage products is therefore taken.

### Sage developer-programme terms
- The current Sage 50 US/CA documents could not be fetched. developer.sage.com and sage.com return 403 to curl and WebFetch.
- A search found the "Sage NA Tech Partner Program" PDF (Mar 2025, covers Sage 50 US/CA; a not-for-resale copy plus the SDK; "benefits… subject to revision") [Secondary: search snippet, P8-AUDIT-L #2].
- **The only full agreement text retrieved** is the Sage Software, Inc. "Development Partner Program" terms (©2022, hosted under developer.sage.com/300/) [Verified: web.archive.org snapshot 2024-11-23 of developer.sage.com/300/guides/DevPartnerProg_Agreement.pdf]:
  - The licence is "personal, nonexclusive, non-sublicensable, nontransferable, revocable… solely to develop and test the User Applications". Tools may be copied "for development purposes only and not for production purposes".
  - §3.3.2: the developer "shall not sublicense, transfer, sell, lend, rent, lease… the Licensed Software or Tools, and shall not use, or allow others to use, the Licensed Software or Tools for the benefit of any third party."
  - §3.3.4: no "conversion functionality that converts end user data from the Licensed Software to a competing product or service".
  - §3.5: "not granted any right… to sell or distribute the Licensed Software. Such right, if any, will be granted only under separate agreement."
  - Fees: an initial authorization fee and annual renewal fees "set forth in the Application" (amounts not public).
  - It incorporates "Then-Current" Partner Hub documents.
- **Reading:**
  - The template contemplates selling **User Applications** (add-ons) to Sage end users, which a connector is. It is silent on a hosted API resold to other software vendors.
  - "For the benefit of any third party" and the anti-conversion clause are adverse for a unified-API middleman serving migration tools and fintechs.
  - This is the Sage 300 programme's agreement, not verified as the Sage 50 US/CA text.
  - **Status: still unresolved; leaning adverse.** It is not a confirmed hard blocker.

### Unknowns
- The actual Sage 50 US/CA partner agreement and fees.
- Help-centre-only integrations (both platforms).
- Whether vendors already listing Sage 50 would outsource it. The likely buyers are the roughly 50–60 vendors that list QuickBooks Desktop but not Sage 50, and whether their customers ask for Sage 50 is not visible.

### Recommended rescoring: hold 52.0

| Criterion | Change | Reason |
|---|---|---|
| Market depth (2) | hold | The census lands where Phase 7 already priced it ("10–20% of QuickBooks Desktop", Track A only). Not cut, because the overall ratio does not breach kill. |
| Customer clarity (4) | hold | Segments are now narrower (construction, field service, distribution, manufacturing), which offsets the zero in four verticals. |
| Defensibility (1) | hold | Agave's coverage shows unified-API vendors add desktop connectors when demand justifies it, as already assumed. |
| Penalty 12 | hold | Restrictive template language, but not the Sage 50 agreement. This is not a direct contradiction (Phase 6/7 rule). If the Sage 50 agreement carries the same §3.3.2/§3.5 wording without a resale addendum, raise the penalty to 13–14 (51.0–50.0). |

- If a reviewer prefers the vertical-only ratio (0.12, closer to kill than keep), the consistent cut is Market depth 2→1 (Scal −3): Adjusted **50.8**. I record that as the downside reading, not my recommendation.

---

## 3. H6: what drove CFBD's 2025–26 Patreon jump (hold 52.2)

### Verified facts

**Patron series** (paid members, from the monthly and daily graphs) [Verified: graphtreon.com/creator/collegefootballdata, 2026-10-13]:

| Year | Off-season | Football season |
|---|---|---|
| 2024 | 244 (Jul) | 416 (Oct) |
| 2025 | 493 (Jun) | 568 (Jul) → 858 (Aug) → 1,273 (Nov) |
| 2026 | 1,575 (Jul) | 2,541 (1 Sep) → 3,509 (1 Oct) → 3,661 (10 Oct) |

- Graphtreon headline: 3,684 paid, +652 in 30 days, $6K–29K/month, 4,716 total members.
- Growth is **strongly seasonal**: each year's gains come in Aug–Oct, with slow decay off-season.
- Jan–Jul 2026, which covers the whole basketball season including March Madness, added only about 200 patrons. CFBD's **second sport added little.**
- The 2026 daily gains peaked at +75/day around 29 Aug and ran at about 30–60/day through September.

**2025 jump: a paywall change.**
- "API v2 is now in general availability" (published 4 Jan 2025): "The free tier has been set at 1000 monthly calls… Patreon Tier 1 ($1/mo) 5,000… Tier 2 ($5/mo) 30,000… Tier 3 ($10/mo) 75,000 (+ GraphQL)". v1 was to "be shut down prior to the start of the 2025 season", and from May 2025 both hostnames pointed to v2 [Verified: radsportsanalytics.com/blog/api-v2-is-now-in-general-availability/].
- Earlier: free API keys were required from April 2021 [Verified: …/api-keys-available/, 23 Feb 2021]. GraphQL has been Tier-3-only since 31 Aug 2024 [Verified: …/building-dynamic-queries…graphql-api/].
- The 2025 season was therefore the first in which heavy free users had to pay. The step up from 568 to 1,273 patrons coincides with it.

**2026 jump: more users, not better conversion.**
- Homepage claims over time [Verified: Wayback snapshots of collegefootballdata.com, 2026-04-21, 06-07, 07-02, 08-19, 09-05, 10-03; live page 2026-10-13]:

  | Date | Users | Patreon supporters |
  |---|---|---|
  | Apr–Jul 2026 | 9,000+ | 1,400–1,500+ |
  | Aug 19 / Sep 5 2026 | 13,500+ | 2,000–2,600+ |
  | Oct 2026 | 21,000+ | 3,500–3,600+ |

- The paid share stays at about 16–17%, so the jump came from new sign-ups.
- In the same window CFBD launched paid packs (Starter Pack $49, AI API Launchpad $19, AI Builder Pack; blog posts Jul–Aug 2026), renamed its blog "Rad Sports Analytics" (16 Jul 2026), and added tiers up to Tier 6 ($30, 500k calls) [Verified: collegefootballdata.com, /api-tiers, blog sitemap].
- The free tier is still 1,000 calls a month, so there was no new paywall in 2026.
- **The cause of the sign-up surge is not verified.** Candidates [Hypothesis]:
  - The 2026 season is described as the first with a full lineup of US prediction-market platforms for college football [Secondary: Saturday Down South promotional articles, search snippet P8-AUDIT-L #1].
  - AI coding assistants raise API call volume, and CFBD sells AI-oriented packs.
  - CFBD's own content/SEO push.
- No media mention was found.
- **A free competitor exists in the agent channel:** the `machina-sports/sports-skills` "cfb-data" agent skill (661 installs, updated 4 Sep 2026) serves college-football data from ESPN with "No API keys required" [Verified: skillselion.com/skills/machina-sports/sports-skills/cfb-data, 2026-10-13].

### What it means for H6
- **Against replicability:**
  - The 2025 jump came from monetising a six-year-old free user base, which a newcomer does not have.
  - The 2026 jump scaled an incumbent funnel with stable conversion.
  - Basketball, the incumbent's own second sport, added very few patrons.
  - The multi-sport rebrand ("Rad Sports Analytics") makes an incumbent baseball/softball product more plausible, which threatens H6's niche.
- **For demand:**
  - Paying hobbyist sports-data demand grew about 2.3× within a year (1,573→3,661 YoY on 10 Oct), and it pays at $1–30 a month.
  - Anything that grows modelling demand (prediction markets, AI-assisted modelling) would also lift college baseball. But that is [Hypothesis] for baseball.
  - Kalshi/Polymarket college-baseball market depth was not checked.
- **Net:** this does not overturn the Phase 6 findings (peer creators have 30–450 paid members; a free daily NCAA dataset and a $7.99 API exist; NCAA terms are restrictive).
  - The incumbent-expansion risk is already scored under defensibility (Phase 6 −1).
  - The demand-growth signal is football-specific and the cause is unverified.
- **Hold 52.2. No criterion change.**
- **Cheapest next check:** whether Kalshi or Polymarket list NCAA baseball markets, with volumes, for the 2026 College World Series. If they do, the demand side of H6 strengthens. If they don't, the 2026 surge is irrelevant to baseball.

---

## Board effect

| Rank | Opportunity | Adjusted |
|---|---|---|
| 1 | H7 | **55.4** (was 56.6) |
| 2 | H6 | 52.2 |
| 3= | M1 | 52.0 (downside reading 50.8) |
| 3= | K8 | 52.0 |

The top four are within 3.4 points, which is noise.

## Decisive unverified assumptions
- **H7:** that this founder can repeatedly land add-ons in the top ~2–5% (≥100–500 sales) on a marketplace whose monthly supply tripled in 2026.
- **M1:** that the Sage 50 US/CA partner agreement permits a hosted API used by third-party vendors (the template text found says "separate agreement"), and that the roughly 50–60 vendors listing QuickBooks Desktop but not Sage 50 have unmet Sage 50 demand.
- **H6:** that college-baseball modelling demand grows the way 2026 football demand did (prediction markets?) without CFBD/Rad Sports Analytics adding baseball first.

## Searches
**3 of 8 used**, logged as P8-AUDIT-L:
1. CFBD 2026 surge and prediction markets.
2. Sage 50 developer agreement terms.
3. Superhive 2026 add-on flood.

Sources: [collegefootballdata.com](https://collegefootballdata.com/) · [SDS Kalshi CFB article](https://www.saturdaydownsouth.com/news/college-football/how-to-use-kalshi-for-college-football-week-0-trade-cfb-with-kalshi-promo-code-sds) · [skillselion cfb-data](https://skillselion.com/skills/machina-sports/sports-skills/cfb-data) · [Sage NA Tech Partner Program PDF](https://developer.sage.com/100-us/guides/Sage%20NA%20Tech%20Partner%20Program.pdf) (403 to fetch) · [Sage DevPartnerProg Agreement](https://developer.sage.com/300/guides/DevPartnerProg_Agreement.pdf) (read via Wayback) · [Sage community thread 227809](https://communityhub.sage.com/ca/sage_50/f/general-discussion/227809/developer-license-to-support-integration/554843) · [Superhive AI policy](https://support.superhivemarket.com/article/311-superhive-market-ai-policy) · [Superhive AI post](https://superhivemarket.com/posts/understanding-ai-on-superhive-a-customers-guide)
