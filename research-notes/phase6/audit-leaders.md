# Phase 6 leader re-check: what newcomers actually get (Evidence Auditor)

Date: 2026-10-13. Desk research only, using public pages and APIs. No browser, sign-ups or contact with anyone.
WebSearch: **8 of 12 used**, each logged as `P6-AUDIT-L`. Everything else came from WebFetch, curl and public APIs:
- Graphtreon pages and patron history.
- Patreon's public search API.
- The GitHub API.
- Shopify `products.json` for four Meshtastic vendors.
- Amazon search pages, which were not blocked this time.
- Framer marketplace pages.
- The Ifat Tenders JavaScript bundle and kones.co.il.
- mr.gov.il.

Scripts and downloads: `scratchpad/p6plus/audit-leaders/`.

**Scoring basis.** The earlier reports publish only the criterion totals (CF/Scal/Dist), not the score for each criterion. So every change below is stated as a step change on one named criterion. One step on a criterion is worth weight/5 points: proven channel 6, scalable acquisition 4, spending evidence 5, defensibility 3, first-customer difficulty 3. This is the same method Phase 5 used for H7 and J7. Penalties change only where a decisive assumption was directly contradicted.

## Summary

| Leader | Was | Recommended | Change | Main reason |
|---|---|---|---|---|
| H6 college-baseball API | 57.2 | **51.6** (52.6 if penalty kept) | −5.6 | CFBD needed about 5 years to pass 450 paid patrons, and sampled peer sports-data creators have 8–447. A free daily NCAA baseball dataset and a $7.99 paid NCAA API already exist. NCAA terms of service prohibit commercial use of its statistics. |
| H1 Meshtastic kits | 54.6 | **51.2** | −3.4 | Plain 2-packs now exist (RAK units at Rokland). Newer branded "communicator" devices priced near the kit's tier have 0–39 Amazon ratings and no "bought" badges. |
| monday.com Israeli invoicing app | 52.0 | **50.8** | −1.2 | Israeli invoicing vendors' own marketplace apps get almost no visible traction: Morning on Shopify 0 reviews, iCount on Shopify 0, Morning on Wix 16 reviews at 2.1★. monday install counts are not public. |
| K13 tender + receivership intelligence | 53.6 | **52.6** (50.6 without the spending-evidence increase) | −1.0 | Both planned differentiators already exist. Ifat covers receiver tenders and offers AI summaries. kones.co.il sells receivership listings at ₪249/month. |
| K8 Framer vertical kit | 53.2 | **53.2 (hold)** | 0 | Framer still shows no sales or remix counts. Only anecdotes were found, in both directions. Nothing measurable to justify a change. |

After this re-check, the board's top cluster (about 50.8–53.6) is tighter still. K13 (52.6), K8 (53.2) and UK MTD prep (52.6, not re-checked) now lead within noise. The remaining H7 (56.6) leads only because its marketplace correction was already made.

---

## 1. H6: college baseball/softball hobbyist data API (57.2 → 51.6)

### Verified
**Is CFBD an outlier? Yes. Its current size took seven years and came late.**
- CFBD today: 3,684 paid members, +652 in 30 days, $6K–29K/month, launched 8 Aug 2019 [Verified: graphtreon.com/creator/collegefootballdata, 2026-10-13].
- Its monthly paid-patron history, from the same page:

  | Date | Paid patrons |
  |---|---|
  | Mar 2020 | 43 |
  | Jan 2021 | 77 |
  | Nov 2021 | 143 |
  | Dec 2023 | 266 |
  | Oct 2024 | 416 |
  | Aug 2025 | 858 |
  | Jan 2026 | 1,375 |
  | Oct 2026 | 3,671 |

- So the strongest comparable reached about 40–150 paid patrons in its first 1–2 years, for college football, the biggest college-sports audience. Most of its growth came in 2025–26.
- The cause of that jump is not verified [Hypothesis]: it may be the free tier being capped at 1,000 calls a month, with higher limits gated behind Patreon. CFBD's site lists "API Tiers" and "Patreon".

**Peer sports-data and statistics creators on Patreon (Graphtreon, 2026-10-13):**

| Creator | Launched | Paid members | Earnings/month |
|---|---|---|---|
| Natural Stat Trick | 2017 | 243 | $592 |
| All Three Zones | 2016 | 171 | $1,402 |
| Prospect microstats (Mitchell Brown) | 2018 | 132 | $491 |
| American Soccer Analysis | 2019 | 86 | $372 |
| real biathlon | 2020 | 42 | $62–349 |
| Their Hockey Counts | 2020 | 8 | $33 |
| MySportsFeeds (a sports-data API) | 2016 | 31 | $54–245 |
| TheDataDB | 2018 | 447 | $836–4K |
| TJ Stats | 2022 | 245 | $1,669 |
| datadrivenhockey | 2023 | 162 | $284–1K |
| D3 Datacast | 2023 | 72 | $106–598 |
| Shooting Sports Analyst | 2024 | 339 | $902 |
| Pitch Profiler | 2024 | 144 | $252–1K |
| Evolving-Hockey | 2018 | 1,298 when it went private (2021) | — |

- Patreon's public search API, for queries such as "sports data", "sports api", "baseball data", "college baseball" and "hockey data", surfaced no other sports-data API with more than about 450 paid members.
- **Typical result: after 2–10 years, an established niche sports-data creator has about 30–450 paid members and earns about $100–1,700/month.** The 2022–2024 entrants have 72–339.

**College baseball is already covered:**
- **Highlightly MLB & NCAA API** covers "NCAA Division I college baseball", including live scores, player stats and the College World Series. Plans: Basic $0 (100 requests/day), Pro $7.99, Ultra $18.99, Mega $44.99 per month. Softball is not mentioned [Verified: highlightly.net/mlb-api/, 2026-10-13].
- **sportsdataverse/baseballr-data** is a GitHub Actions pipeline, updated daily in season, that scrapes stats.ncaa.org into free NCAA baseball schedule, play-by-play, roster, player-stat and team-stat datasets. The repo was pushed 2026-10-12 [Verified: GitHub README].
  - Its release assets show demand for free data: ncaa_baseball_pbp 3,561 downloads, games 2,204, schedules 2,198, rosters 1,971, player_stats 1,966, team_stats 1,900. softball groups 241 [Verified: GitHub releases API].
  - `sportsdataverse/softballR` (updated 2026-10-12) covers softball.
  - `baseballr` has 433 stars. NCAA-specific scrapers have at most 44 stars.
- **64analytics.com** (college baseball and softball analytics, transfer portal) is moving to Rule42. It is aimed at coaches and recruiting [Verified: homepage, 2026-10-13].
- **collegebaseballdata.com** is still a "Launching Soon" placeholder, copyright 2026 [Verified].
- **d1baseball.com** returned a 403 (Cloudflare challenge) and was not checked.

**Data rights:**
- NCAA.com's terms of service (last updated 21 Feb 2023) list "statistics, updated scores" as NCAA Content. They forbid using it "for commercial purposes" or "commercial exploitation of downloaded material" without permission [Verified: ncaa.com/tos].
- stats.ncaa.org returns 403 to automated requests.
- US law generally treats raw sports facts as not copyrightable, so the risk is mainly contract and terms of service rather than copyright [Secondary/general knowledge, not legal advice]. Highlightly and the free sportsdataverse projects operate openly.

### Still unknown
- What drove CFBD's 2025–26 surge.
- How many people model college baseball and how many would pay.
- Whether Highlightly or D1Baseball have paying subscribers.
- Whether the NCAA enforces its terms against hobbyist APIs.
- Whether CFBD will add baseball, which would cost it little since it already added basketball.

### Recommended rescoring

| Criterion | Change | Points | Evidence |
|---|---|---|---|
| Proven channel | −1 | Dist −6 | The channel works only on a multi-year horizon. Newcomer-equivalent outcomes are tens of patrons. |
| First customers | −1 | Dist −3 | A free daily dataset and a $0–7.99 API are already the default. |
| Scalable acquisition | −1 | Scal −4 | Same peer-ceiling evidence as above. |
| Defensibility | −1 | Scal −3 | Equivalent free data is maintained daily. |
| Cash-flow | none | 75 | |

- Distribution 64 → 55. Scalability 66 → 59.
- Balanced 69.2 → 64.6.
- Penalty 12 → 13, because the decisive data-rights assumption is partly contradicted by the NCAA terms.
- **Adjusted 51.6.** Keeping the penalty at 12 gives 52.6.
- The Phase 3 base case of 400 paying members is not supported. A realistic case is tens of members in year 1–2, about $50–300/month.

---

## 2. monday.com Israeli invoicing app (52.0 → 50.8)

### Verified
- **No public newcomer data on monday:**
  - The marketplace pages are rendered by JavaScript. WebFetch gets only a heading.
  - Install counts are visible only in the developer's private Developer Center.
  - Public "evidence" is monday's promotional case studies: Pioneera at about $30k MRR, Jetpack Apps [Search snippets, P6-AUDIT-L].
- **Generic monday invoicing apps exist:** GetSign/Jetpack invoice automation, DocCreate, Paysaro, Easy Invoice (BAM Apps), eQuotes, and a QuickBooks integration [Search snippets, not opened]. Neither search surfaced an Israeli tax-invoice app (Morning, iCount, EZcount, Rivhit). As before, not finding one is not proof none exists.
- **Morning (Green Invoice):** its integrations page lists 17 partner integrations: Israeli CRMs and vertical tools such as Kala CRM, יועצים CRM, LeadMe, Prospero, Bllink and טיפולוג. **monday is not among them** [Verified: greeninvoice.co.il/add-ons/integrations/, 2026-10-13]. Morning publishes API documentation (/api-docs/ in its sitemap). iCount (/features/api/) and EZcount (/api) also publish APIs.
- **The best newcomer proxy: Israel-only invoicing apps on global marketplaces get almost no visible traction, even from the market leaders:**

  | App | Marketplace | Launched | Reviews |
  |---|---|---|---|
  | Morning | Shopify | 3 Jan 2023 | 0 |
  | iCount | Shopify | 3 Nov 2023 | 0 |
  | Morning | Wix | — | 16 (2.1★) |

  Sources: apps.shopify.com/green-invoice, apps.shopify.com/icount-invoices, wix.com/app-market/green-invoice, all 2026-10-13.
- **monday's own native invoicing:** not verified. support.monday.com returned 403.

### Still unknown
- How many Israeli monday accounts exist.
- Install counts for any monday app.
- Whether monday CRM's native quotes and invoices covers Israeli tax requirements, including the tax authority allocation number.

### Recommended rescoring
- **Proven channel −1.** Phase 1 credited platform-wide figures (1.6M installs, Pioneera). Under the Phase 5 rule, those don't count without newcomer data, and the Israeli-invoicing proxy points to near-zero marketplace pull.
- Distribution 54 → 48. Balanced 66.0 → 64.8. Penalty 14 kept. **Adjusted 50.8.**
- One weak positive, not scored: Morning's partner list suggests the monday gap is real. But Israeli SMBs who need CRM plus invoicing already get it natively from Israeli CRMs.

---

## 3. H1: Meshtastic family kits (54.6 → 51.2)

### Verified (Shopify `products.json`, 2026-10-13)
- **Multi-packs now exist, but only as plain quantity options:**
  - Rokland sells the RAK WisMesh Pocket v2 with a "2 PACK – US915" option at $154.94 (single unit $77.97), in stock.
  - Rokland also lists the WisMesh TAP v2 2-pack at $219.97, created 2026-04-14, sold out.
  - Rokland lists battery 2-packs and keychain-holder 1/2/5-packs.
  - Muzi lists a "Base Duo" at $35.
  - Meshnology (Heltec-based kits, 2025–26) and RAK (WisMesh starter kits, $24.99–39) sell single-unit dev kits.
- **No pre-paired family kit (3 handhelds plus a repeater, onboarding, support) was found** at RAK, Rokland, Muzi, Meshnology or LILYGO, or on Amazon. One WebSearch also found none. The "no multi-packs anywhere" claim from Phase 3 is out of date. The narrower "no pre-paired family kit" still holds.
- **Amazon newcomer signals** (search pages fetched 2026-10-13; prices not parsed, Israel locale):
  - Cheap nodes and kits still sell:

    | Product | Ratings | Bought past month |
    |---|---|---|
    | Seeed XIAO ESP32S3 kit | 31 | 500+ |
    | SenseCAP P1-Pro | 107 | 400+ |
    | XIAO nRF52840 kit | 8 | 300+ |
    | New ASIN B0H798S8M4 "LoRa Node for Meshtastic & MeshCore" | 20 | 200+ |

    That last listing is new and shows newcomers can sell cheap nodes.
  - **Branded, outcome-positioned "off-grid communicators" sell visibly less:**
    - SpecFive Trekker Bravo: 39 ratings.
    - SpecFive Trekker Delta: 2–11 ratings.
    - SpecFive Ranger: 2–4 ratings.
    - SpecFive Pulse Pack: no ratings, "Currently unavailable".
    - MiniTrekker MKII: 0 ratings.
    - KEEPTEEN solar repeater: 63 ratings.
    - None of these shows a "bought in past month" badge.

  These products are the closest analogue to a $349–449 kit sold on the outcome.
- **Blocked:** Tindie (403). Kickstarter and Crowd Supply were not checked.

### Still unknown
- Sales of the 2-pack variants.
- Whether a higher-priced family kit converts on Amazon or YouTube.
- Ad costs.
- Plans by RAK or Seeed to bundle.

### Recommended rescoring

| Criterion | Change | Points | Evidence |
|---|---|---|---|
| Proven channel | −1 | Dist −6 | Amazon converts for $30–60 nodes. Newcomer evidence at the kit's price and positioning is weak. |
| Defensibility | −1 | Scal −3 | Incumbents have started selling packs. |
| Penalty | +1 (6 → 7) | — | The audit fact that justified Phase 3's unusually low penalty ("no multi-packs exist") is partly contradicted. |

- Cash-flow 61. Scalability 52 → 49. Distribution 77 → 71.
- Balanced 60.6 → 58.2. **Adjusted 51.2.**

---

## 4. K8: Framer vertical kit (hold at 53.2)

### Verified
- **Framer template pages show no sales, remix or view counts.** Coska, for example, shows only its publish date (13 Feb 2026), update date, licence and a "Remix" button [Verified: framer.com/marketplace/templates/coska/, 2026-10-13].
- Creator profiles show listing and follower counts only. @amar-kzr has 10 listings, all visible ones free. @anvics has 8 free templates and 142 followers.
- Many new creators publish free templates and earn through Framer's referral commission when someone remixes and upgrades.
- **Newcomer anecdotes (Framer community, all self-reported):**
  - Struxent: template published 21 Feb 2026, first commission 28 Feb, first sale 3 Mar, "4 months, zero marketing". The total is shown only in an image [Verified page; amount not readable].
  - Another creator claims $1k in Dub.co affiliate sales in the first month from two hero templates. This is not template sales [Verified page, anecdote].
  - An essay uses "$500 in its first month" as an example. It is not data.
- A search snippet claims one creator went from $11.60/month (Jun 2025) to $2–2.8k/month in early 2026, with 849 sales. Two candidate profiles were opened and neither contained it, so it is **unverified**.
- **A possible artefact in Phase 5's evidence:** category pages show 24 tiles per page. The therapy, fitness and health pages each embed about 64 template objects (about half paid) and about 78 slugs in their page data. Phase 5's "24 therapy templates" may be one page's tile count, not the category total [Unverified, pagination not confirmed].

### Still unknown
- The median result for a new Framer template creator.
- How sales or remixes are distributed across templates.
- Whether functional plugins (which earn no referral) sell at all.

### Recommendation
- **Hold at 53.2.** The new evidence is anecdotal in both directions: fast first commissions on one side, a flood of free supply and invisible counts on the other.
- Phase 5 already held Distribution at 51 and applied a penalty of 13 for the unmeasured channel.
- If the Phase 5 Distribution score credited the $6.5M payout figure as channel evidence, it should drop one step (Distribution 51 → 45, Adjusted about 52.0). The criterion breakdown isn't in the reports, so I can't confirm this.
- Do not raise K8 on the anecdotes.

---

## 5. K13: Hebrew tender + receivership intelligence (53.6 → 52.6)

### Verified
**Ifat Tenders** (tenders.co.il, the site's own Ifat Tenders branding) [Verified: the site's main JavaScript bundle text and sitemap, 2026-10-13]:
- **Subscription structure:**
  - Plans by number of categories: one category, two categories, or all categories ("סיווג אחד / שני סיווגים / כל הסיווגים").
  - Prices are shown as "₪ / per month" for a one-year commitment, with an option to show half-year pricing, excluding VAT.
  - The actual numbers are loaded from the site's API and could not be retrieved without logging in. **Ifat's prices are still unknown.**
- **Plan benefits listed:** 100% of public tenders, tender results, exclusive tenders, exemption notices, a "smart agent", free help submitting a tender, and support.
- **It already covers receivership sales:** the home copy lists "מכרזי כונס" (receiver tenders). Its real-estate category says it gathers "all liquidation and receivership notices" offering apartments from receivers, local authorities and private bodies.
- **It already has AI summaries:** each tender has a "רכישת סיכום AI" (buy AI summary) action. The button text reads "לרכישת סיכום חכם והמלצות – ללא עלות עד 31/12/26" (smart summary and recommendations, free until 31/12/26). Tender pages have tabs for threshold requirements (דרישות סף), clarification questions and contractor tours.
- Daily email updates. Its "smart agent" scans "thousands of opportunities every month".
- Phone sales and support at 03-5635000. It has a new-subscriber flow and a publishing service for tender issuers.

**kones.co.il ("מרכז הכונס")** [Verified: kones.co.il and /register, 2026-10-13]:
- Receivership apartments and vehicles, plus business and second-hand listings, with live online vehicle auctions.
- **₪249/month, monthly, no commitment, after a 7-day free trial.**
- Listing IDs run to about 166,700. This suggests a large catalogue, but it is not a transaction count.

**Government Procurement Administration (mr.gov.il)** [Verified, 2026-10-13]:
- Free search across 22,131 tender records, with category and status filters.
- A free mailing list ("לרשימת הדיוור").

**Other aggregators:** two Hebrew WebSearches surfaced none. The search engine is US-based and weak for Hebrew, so this is not proof of absence.

**Legal status of reusing court-receiver notices:** not verified. Ifat and Kones both openly commercialise receivership and liquidation notices. That shows the practice is tolerated in the market, not that it is legal [Inference].

### Still unknown
- Ifat's prices and subscriber counts. Kones subscriber counts.
- Whether contractors find Ifat's matching poor.
- Rules on reusing material from the Execution Authority and court notices.

### Effect on the entry strategy
Phase 5's entry strategy depended on three things:
1. A receivership feed Ifat might not have. **It has one.**
2. AI matching and summaries. **Ifat ships AI summaries, free through 2026.**
3. Pricing below Ifat. **Ifat's price is unknown.** Kones sets a ₪249/month anchor.

The remaining wedge is narrow: possibly a cheaper SMB tier, or better matching quality, neither of which is evidenced. Per the brief, that wedge is currently **not credible**.

### Recommended rescoring

| Criterion | Change | Points | Evidence |
|---|---|---|---|
| Spending evidence | +1 | CF +5 | Two long-running paid incumbents with published subscription structures. Kones lists ₪249/month. These are not transaction counts, so this increase can be withheld. |
| Defensibility | −2 | Scal −6 | Both differentiators already shipped by incumbents. |
| First customers | −1 | Dist −3 | Must displace an incumbent that gives AI summaries away free through 2026. |

- Cash-flow 74 → 79. Scalability 66 → 60. Distribution 58 → 55.
- Balanced 67.6 → 66.6. Penalty 14 kept. **Adjusted 52.6.**
- Without the spending increase: **50.6.**

---

## Cross-cutting conclusions
1. The newcomer test lowered all four leaders it could measure (H6, H1, monday app, K13). The largest correction is H6: its only channel evidence was a seven-year-old incumbent whose first two years look like a typical niche creator's.
2. **Direct-sale ideas are not immune.** K13's problem is not the channel. The incumbent has already copied the differentiators, so K13 needs a new entry strategy, not more channel evidence.
3. Data sources that work and should be reused:
   - Graphtreon history series (embedded `monthlyGraph_patronSeriesData`).
   - Patreon's public `/api/search` JSON.
   - Shopify `products.json`.
   - Amazon search HTML via curl with `--compressed` (worked from this IP).
   - Text inside SPA JavaScript bundles, which reveals product features and pricing structure.
4. **Decisive unverified items for Phase 7 deep diligence:**
   - H6: CFBD's patron curve before the paywall change, and whether the NCAA enforces its terms.
   - H1: sell-through of RAK/Rokland 2-packs and of $150+ branded nodes.
   - monday app: whether any Israeli invoicing app exists on monday, and Israeli monday account numbers.
   - K13: Ifat's prices, and the quality of its AI summaries.
   - K8: the median sales of a new Framer template.

WebSearch count: 8 (P6-AUDIT-L).
