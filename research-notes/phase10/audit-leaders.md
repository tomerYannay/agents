# Phase 10 leader re-check (Leader Auditor, P10-AUDITL), 2026-10-13

Desk research only. I used public pages and public JSON APIs. No browser tools, sign-ups, purchases or contact with anyone. Every request used a generic User-Agent (`Mozilla/5.0 (compatible; research-bot)`), and no personal identifiers were sent. Blocked sources were reported, not bypassed.

- **WebSearch:** 4 of 8 used, each logged in `search-log.txt` as `P10-AUDITL`.
- **Scripts:** `scratchpad/p6plus/P10-auditL/scripts/`. **Data:** `.../P10-auditL/data/` (`sh/`, `apify/`, `h6/`, `h1/`, `monday/`).
- **Scoring method:** the same as Phases 5–9. One step on a criterion is worth weight/5 points. A Cash-Flow or Scalability point moves Adjusted by 0.4, and a Distribution point moves it by 0.2.
- **Penalty rule:** the penalty rises only when the decisive assumption is directly contradicted.
- **Double-counting check:** before recommending any step, I checked it against the earlier corrections:
  - H7: P5 (proven channel 4→3, scalable acquisition 3→2) and P8 (proven channel 3→2).
  - J7: P5 (proven channel 3→1, first customers 3→2, scalable acquisition 3→2).
  - H6: P6 (proven channel −1, scalable acquisition −1, defensibility −1, penalty 12→13).
  - H1: P6 (proven channel −1, defensibility −1, penalty 6→7).
  - monday app: P6 (proven channel −1).

## Summary

| Leader | Was | Recommended | Change | Decisive finding |
|---|---|---|---|---|
| H7 Blender add-ons | 55.4 | **55.4 (hold)** | 0 | New sample of 221 paid Jun–Oct 2026 Superhive add-ons, disjoint from Phase 8's. Results: median **2 sales** at 0–3 months (Phase 8: 2.5), 77% with at least 1 sale, **1% with 100+**. Add-ons aged 3–4.5 months have a median of 5. The distribution has not changed. Supply is still rising: about 390 new add-ons in Sep 2026, and about 490/month pace in 1–13 Oct. All of this is already priced by the P5 and P8 cuts. |
| H6 College-baseball API | 52.2 | **52.2 (hold)** | 0 | Paid-tier economics are low-ARPU. CFBD tiers are $1–30/month (Tier 2 at $5 is "most popular"). Graphtreon: 3,684 paid members, estimated earnings **$6K–29K/month**, so about $1.6–7.9 per member. Highlightly MLB+NCAA baseball is $7.99/$18.99/$44.99. BALLDONTLIE is $9.99–39.99 per sport and carries no NCAA baseball. At peer member counts (8–447, Phase 6), this implies about $15–3,500/month. That is the same ceiling Phase 6 priced. |
| H1 Meshtastic kits | 51.2 | **51.2 (hold)** | 0 | Amazon was blocked (curl got a "verify" bot page; WebFetch got 503). Rokland, Muzi Works, RAKwireless store, Meshnology and MerchantWords all returned 403. A search snippet surfaced no Amazon multi-pack listings. The Phase 9 trigger (Amazon $300+ bundles with fewer than 20 ratings) could not be tested. |
| monday.com invoicing app | 50.8 | **50.8 (hold)** | 0 | The marketplace is a JavaScript shell. Listing pages serve only meta text, and install and review counts are not public, so there is no newcomer data. Incumbents: Morning, iCount, Rivhit, EZcount, SUMIT and Invoice4U do not mention monday on their homepages or integration pages. The only route found is iCount↔monday through Make (known since Phase 1). The gap is still open, but demand is unmeasured. |
| J7 Apify Actors | 50.8 | **50.8 (hold)** | 0 | 1,500 randomly sampled Store Actors, with creation dates from the public Actor API. 2026 newcomers have a **median of 1 user in the last 30 days** at every age band. Share with 100 or more 30-day users: **0%** at 0–3 months (n=822), **1%** at 3–6 months (n=421), **3%** at 6–9.5 months (n=144). This is unchanged from Phase 5. 94–100% of new Actors are monetised (pay-per-event), so they compete on price too. |

**Board effect:** none. H7 55.4 · H6 52.2 · H1 51.2 · monday and J7 50.8.

---

## 1. H7: Superhive newcomer distribution, Jun–Oct 2026 (hold 55.4)

**Decisive assumption:** the founder can repeatedly land add-ons in the top ~2–5% of a marketplace whose supply tripled in 2026. Phase 8 measured a median of 2.5 sales in the first 3 months, with 5.6% of 2025–26 add-ons reaching 100+.

### Method
- I re-crawled the add-ons category in "Newest" order: pages 1–58, 1,373 listings, back to late May 2026.
- I opened the products at positions 4, 8, 16 and 20 on each page. Phase 8 used positions 0 and 12, so this sample does not overlap with Phase 8's.
- This gave 232 product pages, with 225 dated Jun–Oct 2026, of which 221 are paid. I read `published_at`, `order_items_count` (paid sales), `free_order_items_count` and `price` from each page's embedded JSON, the same fields Phase 8 used.
- **Caveats:**
  - Only currently published products are visible.
  - Phase 8 ran on the same date (2026-10-13), so this is a larger independent sample, not a later snapshot.

### Verified results [Verified: superhivemarket.com listing pages and product JSON, crawled 2026-10-13]

| Age at crawl (paid) | n | Median sales | ≥1 | ≥10 | ≥50 | ≥100 | p90 | Max | Median gross |
|---|---|---|---|---|---|---|---|---|---|
| 0–1 month | 72 | 1 | 76% | 14% | 0% | 0% | 12 | 28 | $19 |
| 1–2 months | 50 | 2 | 74% | 16% | 2% | 0% | 13 | 66 | $29 |
| 2–3 months | 48 | 2.5 | 81% | 19% | 4% | 4% | 18 | 443 | $28 |
| 3–4.5 months (Jun–early Jul) | 51 | 5 | 92% | 27% | 0% | 0% | 16 | 47 | $63 |
| **0–3 months, all** | **170** | **2** | 77% | 16% | 2% | **1%** | 14 | 443 | $24 |

- **Phase 8 sample, same window:** 0–3 months n=85, median 2, ≥10 13%, ≥100 0%. Combined (n=246): median 2, ≥10 14%, ≥100 1%.
- **Median price:** $14 (Phase 8: $15).
- **Top newcomers, Jun–Oct 2026:**
  - split-3dprint: 443 sales, $28, published 19 Jul.
  - squishyfx: 124 sales, $20, published 11 Aug.
  - dnaimporter: 88 sales.
  - opacityflow: 66 sales.
  - Everything else: 47 sales or fewer.
  - Only 2 of 320 combined paid add-ons reached 100 or more within 4.5 months.
- **Supply** (each sampled product stands for 6 listings, ±25%):

  | Month | New listings |
  |---|---|
  | Jun 2026 | ~258 |
  | Jul 2026 | ~216 |
  | Aug 2026 | ~276 |
  | Sep 2026 | ~390 |
  | 1–13 Oct 2026 | ~210, a pace of ~490/month |

  This is consistent with Phase 8's 250–385/month, possibly still rising.

### Reading
- The newcomer distribution has **not changed** from Phase 8:
  - The median is 2 against 2.5.
  - The early-life ≥10 share is 13–16%.
  - The ≥100 share in the first 3 months is about 1%.
- Early hits still occur. split-3dprint made about $12k gross in under 3 months. They are about 1 in 100–150.
- Rising supply is the same evidence type that P8 already used for proven channel 3→2. Applying it again would double count.

### Recommendation
- **No step change. Penalty stays at 12.**
  - CF 80, Scal 58, Dist 61.
  - Balanced = 0.4×80 + 0.4×58 + 0.2×61 = 32 + 23.2 + 12.2 = 67.4.
  - **Adjusted = 67.4 − 12 = 55.4.**
- **Not recommended:**
  - Scalable acquisition 2→1 (Scal −4, which would give 53.8). The evidence is the same base-rate and supply evidence used in P5 and P8.
  - Proven channel 2→1. The channel still produces some newcomer winners, as split-3dprint and squishyfx show, which is the P8 reason for scoring 2 rather than J7's 1.
- **Trigger for a cut:** a later snapshot (≥3 months on) showing the Jun–Oct 2026 cohort's median below 5 at 6–9 months. Phase 8's 2026 H1 cohort had a median of 12 at the same age.
- **Confidence:** medium-high on the facts (n=221, exact JSON counts); medium on the score.

---

## 2. H6: paid-tier economics of comparable sports-data APIs (hold 52.2)

**Decisive assumption (Phase 3):** hobbyist modellers pay enough per month, in enough numbers, for a college-baseball/softball API to reach Track A.

### Evidence
- **CFBD tiers** [Verified: collegefootballdata.com/api-tiers, 2026-10-13]:

  | Tier | Price/month | Calls/month |
  |---|---|---|
  | Free | $0 | 1k |
  | Academic | $0 | 3k |
  | Tier 1 | $1 | 5k |
  | Tier 2 ("most popular for analytics") | $5 | 30k |
  | Tier 3 | $10 | 75k |
  | Tier 4 | $15 | 125k |
  | Tier 5 | $20 | 200k |
  | Tier 6 | $30 | 500k |

  - CFBD also sells one-off packs ($19–49, Phase 8).
- **CFBD members and earnings** [Verified: graphtreon.com/creator/collegefootballdata, 2026-10-13]:
  - 3,684 paid members (+652 in 30 days) and 4,716 members in all; launched Aug 2019.
  - **Estimated earnings: $6K–29K per month.** Graphtreon estimates from tier prices; its daily earnings series is hidden.
  - That works out to about **$1.6–7.9 per paid member per month** [derived].
  - This one page covers both football and basketball.
- **Highlightly MLB & NCAA baseball API** [Verified: highlightly.net/mlb-api, 2026-10-13]:
  - BASIC $0 (100 requests/day); PRO $7.99 (7,500/day); ULTRA $18.99 (25,000/day); MEGA $44.99 (65,000/day). Annual billing gives up to 40% off.
  - Covers NCAA D-I baseball and the College World Series. Softball is not mentioned.
  - No customer counts are published.
- **BALLDONTLIE** [Verified: balldontlie.io, 2026-10-13]:
  - $9.99 or $39.99/month per sport; All-Access $299.99/month.
  - Covers NCAAF, NCAAB and NCAAW, but **not NCAA baseball**.
  - Claims "thousands of developers" [vendor claim].
- **Search** (P10-AUDITL #4): no indie college-stats API with a published MRR or subscriber count. The only TrustMRR sports hit had $0 and was not an API.

### Reading
- Comparable paid tiers cluster at **$5–45/month per account**, and the realised average for the one outlier is about $2–8. Nobody in the niche gets $300+/account; only BALLDONTLIE's all-sports bundle approaches it.
- **Implied ceiling:**
  - At peer creators' 8–447 paid members (Phase 6) and $5–8 ARPU, revenue is about $40–3,500/month.
  - Track A ($2–5k profit) needs roughly 400–1,000 paying members, which is CFBD-like scale. CFBD needed about 5 years to pass 400.
- This is the same ceiling Phase 6 priced through proven channel −1 and scalable acquisition −1. It is not a new contradiction.
- Highlightly's existing $7.99 NCAA baseball tier was also priced in Phase 6 (first customers/defensibility).
- It conflicts with the Phase 10 direction ($300+/account). That direction is not a rubric criterion, so it is not scored.

### Recommendation
- **No step change. Penalty stays at 13.**
  - CF 75, Scal 59, Dist 58.
  - Balanced = 30 + 23.6 + 11.6 = 65.2.
  - **Adjusted = 65.2 − 13 = 52.2.**
- **Possible reviewer dissent (not recommended):** margins or recurring revenue −1 for low ARPU. Phase 3 already modelled a $5–10 price, so ARPU is not new information.
- **Confidence:** medium. Graphtreon's earnings range is wide, and baseball demand is still unmeasured.

---

## 3. H1: Amazon Meshtastic bundles (hold 51.2)

**Decisive assumption:** a $349–449 pre-paired family kit converts through Amazon search, YouTube preparedness creators and mesh Discords.

### Evidence
- **Amazon search** `meshtastic kit`:
  - curl with a generic browser UA returned a 1.3 KB "verify" bot page.
  - WebFetch returned HTTP 503.
  - **[Blocked; not bypassed.]** This is the same as Phase 9.
- **Other public sales signals tried, all 403 (Cloudflare/Shopify bot block):**
  - Rokland 2-packs page and `products.json`.
  - Muzi Works, store.rakwireless.com, meshnology.com.
  - MerchantWords keyword preview.
  - heltec.org and shop.uniteng.com have no Shopify feed (404).
- **Search** (P10-AUDITL #3): no Amazon 2/3/4-pack Meshtastic bundle surfaced in snippets. Rokland offers 1- and 2-packs (WisMesh Pocket v2 at $84.97) [Secondary: search snippet]. Absence in snippets is not absence.

### Reading
- Nothing new is readable. The Phase 9 trigger (Amazon $300+ bundles with fewer than about 20 ratings and no "bought" badges → proven channel −1, giving 50.0) **could not be tested**.
- Phase 6 (Amazon branded $150+ nodes with 0–39 ratings) and Phase 9 (about 90% of Tindie Meshtastic listings with 0 reviews) stay the best evidence. Both are already priced.

### Recommendation
- **No step change. Penalty stays at 7.**
  - CF 61, Scal 49, Dist 71.
  - Balanced = 24.4 + 19.6 + 14.2 = 58.2.
  - **Adjusted = 58.2 − 7 = 51.2.**
- **Flag for the final report:**
  - H1's Distribution (71) is the highest among the leaders.
  - Its penalty (7) is below the historical 9–14 band.
  - Its decisive channel has been unreadable for two phases.
  - Under the rule these are not a direct contradiction. But H1 is the leader whose score rests most on unmeasured evidence.
  - A reviewer who treats two phases of unmeasurable channel as unpriced uncertainty could argue penalty 7→9, giving 49.2. I do not recommend it, because the rule needs a contradiction.
- **Confidence:** low.

---

## 4. monday.com Israeli invoicing app (hold 50.8)

**Decisive assumption:** enough Israeli monday accounts want a native tax-invoice app (Morning/iCount from a board item), and incumbents won't build it.

### Evidence
- **Marketplace newcomer outcomes: not publicly measurable.**
  - `monday.com/marketplace` and listing pages are a JavaScript shell. Only meta title and description are server-rendered; for example, `/marketplace/listing/37/stripe` returns 16 KB with no rating, review or install fields.
  - The marketplace JS bundle I inspected handles checkout, not listing data.
  - `monday.com/marketplace/sitemap.xml` returned 500.
  - support.monday.com returned 403.
  - Install counts are visible only in the developer's private Developer Center (Phase 6).
  - **[Unknown]** I did not attempt to reach private APIs.
- **Israeli invoicing incumbents and monday** [Verified: vendor pages fetched 2026-10-13]:

  | Vendor | Page(s) checked | monday mentioned? |
  |---|---|---|
  | Morning (Green Invoice) | integrations | 0 |
  | iCount | integrations page and homepage | 1 hit each, but only the weekday "Monday" in a date-picker script |
  | Rivhit | homepage | 0 |
  | EZcount | homepage | 0 |
  | SUMIT | homepage | 0 (the integrations URL I guessed was 404) |
  | Invoice4U | homepage | 0 |

  - **No incumbent advertises a monday integration.**
- **Make.com** [Verified: make.com/en/integrations/icount/monday via WebFetch; curl returned 403]:
  - It has a "Connect iCount and monday.com" page with 17 iCount actions, including "Create a Document", and 13 monday triggers.
  - Morning is not mentioned there.
  - This no-code route was already known in Phase 1 and is priced.
- **Searches** (P10-AUDITL #1, #2): no monday marketplace listing for an Israeli tax-invoice app surfaced, in Hebrew or English.
  - Workato lists an "Israel Tax Authority" connector.
  - NetSuite sells an Israel e-invoicing SuiteApp.
  - Third-party guides say the allocation-number threshold fell to NIS 5,000 from June 2026 [Secondary: beancount.io guide, search snippet; gov.il page returned 403]. Allocation numbers are issued through the invoicing vendor, so this broadens the need but does not change the app's role.

### Reading
- The Phase 1 wedge (no native Israeli invoicing app on monday) still appears open after a direct vendor-page check, a weak positive.
- Newcomer outcomes on monday remain unmeasurable from public data, so nothing confirms or contradicts the Phase 6 proven-channel cut.
- **Agent F's Israel caution (Phase 9):** the named evidence (Hebrew business apps median 0 Israeli ratings; Morning/iCount Shopify apps 0 reviews) is the same evidence type behind the P6 proven-channel cut. Applying it again would double count.

### Recommendation
- **No step change. Penalty stays at 14.**
  - CF 74, Scal 64, Dist 48.
  - Balanced = 29.6 + 25.6 + 9.6 = 64.8.
  - **Adjusted = 64.8 − 14 = 50.8.**
- **Not recommended:** spending evidence +1 for the open gap. An absence of competitors is not spending evidence.
- **Confidence:** low. The size of the Israeli monday base and the willingness to pay are still unknown.

---

## 5. J7: Apify Store newcomer outcomes in 2026 (hold 50.8)

**Decisive assumption (Phase 4):** a niche Actor attracts paying users through Apify Store search without the founder's own audience. Phase 5 measured 390 Actors under 1 month old: median 1 monthly user, and 0% of those under 3 months had 100 or more monthly users.

### Method
- **Public Store API:** `api.apify.com/v2/store?sortBy=newest`, in pages of 1,000.
  - The API returns at most about 10,000 results per query. To reach further back, I pulled the overall list plus 20 category lists.
  - That gave 8,089 overall and 138–8,870 per category: **~40,000 unique Actors** of the 84,166 listed in the Store.
- **Random sample:** 1,500 Actors (seed 20261013). For each, the public `GET /v2/acts/{id}` endpoint, which needs no token, gave the exact `createdAt`.
- **Fields joined from the Store list:**
  - `stats.totalUsers30Days`, the 30-day users, comparable to Phase 5's "monthly users";
  - `totalUsers`;
  - `pricingModel`.
- **Caveats:**
  - The "newest" sort is not strictly by `createdAt`. Actors are probably ordered by Store publication date.
  - Old cohorts are survivor-biased and under-covered, because large categories reach back only to Apr–Aug 2026.
  - User counts may include the developer's own test runs.
  - Users are not paying users. The Store shows no revenue per Actor.

### Verified results [Verified: api.apify.com/v2/store and /v2/acts/{id}, fetched 2026-10-13]

| Age at fetch | n | Median 30-day users | ≥1 | ≥10 | ≥100 | p90 | Max | Median lifetime users | Monetised (not free) |
|---|---|---|---|---|---|---|---|---|---|
| 0–1 month | 342 | **1** | 95% | 1% | 0% | 2 | 26 | 2 | 100% |
| 1–3 months | 480 | **1** | 85% | 4% | 0% | 3 | 124 | 2 | 99% |
| 3–6 months | 421 | **1** | 74% | 10% | 1% | 9 | 182 | 3 | 97% |
| 6–9.5 months (Jan–early Apr 2026) | 144 | **1** | 65% | 14% | 3% | 14 | 866 | 11 | 94% |
| Older than 2026 (survivors) | 108 | 2 | 77% | 21% | 7% | 61 | 4,442 | 72.5 | 91% |

- **Creation months in the sample:**

  | Month | Actors |
  |---|---|
  | Mar 2026 | 52 |
  | Apr 2026 | 69 |
  | May 2026 | 112 |
  | Jun 2026 | 166 |
  | Jul 2026 | 230 |
  | Aug 2026 | 263 |
  | Sep 2026 | 277 |
  | 1–13 Oct 2026 | 167 |

  - This reflects both supply growth and the newest-first sampling frame, so it is not a clean rate.
- **Store size:** 84,166 Actors listed today [Verified]. Phase 5 put new supply at about 600+ a day.

### Reading
- **No change from Phase 5.** The median 2026 newcomer has 1 thirty-day user at every age up to 9.5 months.
- Breakout is rare and slow:
  - 0 of 822 Actors under 3 months reached 100 thirty-day users.
  - 1% reach it by 3–6 months, and 3% by 6–9.5 months.
- That matches the ~4–6% newcomer base rate seen everywhere else. Nearly all newcomers charge (pay-per-event), so there is no free-tier gap to exploit.
- J7's P5 cuts already priced this (proven channel 3→1, first customers 3→2, scalable acquisition 3→2). Proven channel is already 1, the lowest level short of 0. The data shows a small, non-zero tail (3% ≥100 at 6–9 months), so 0 is not justified.

### Recommendation
- **No step change. Penalty stays at 12.**
  - CF 75, Scal 58, Dist 48.
  - Balanced = 0.4×75 + 0.4×58 + 0.2×48 = 30 + 23.2 + 9.6 = 62.8.
  - **Adjusted = 62.8 − 12 = 50.8.**
- **Not recommended:**
  - Speed to first sale −1 (CF −4, which would give 49.2). 85–95% of newcomers get at least one user within 3 months; "user" is not "paid", but the first-use speed is real. The paid-conversion question was already priced through first customers in P5.
- **Confidence:** medium-high on the facts (n=1,500, exact API fields); medium on representativeness, given the coverage caveats.

---

## Decisive unverified items after this audit
- **H7:** whether the Jun–Oct 2026 cohort's plateau stays near Phase 8's 10–15 lifetime sales despite supply of 400–500/month. This needs a re-crawl in 2027.
- **H6:** college-baseball paid demand at any price. No baseball-specific member counts exist (Highlightly publishes none).
- **H1:** Amazon/YouTube conversion of $300+ multi-node kits. Amazon, Tindie, Etsy and Shopify vendor feeds were all blocked live.
- **monday app:** the number of Israeli monday accounts and any monday app's install count. Neither is public.
- **J7:** how many 30-day users pay, and revenue per Actor. The Store publishes users and runs, not revenue.

## Searches (4 of 8, logged as P10-AUDITL)
1. Hebrew: monday invoicing integration with Morning/iCount/SUMIT/Rivhit. Only the Make iCount↔monday template surfaced.
2. monday marketplace Israeli tax-invoice app. None surfaced; Workato ITA connector; NIS 5,000 allocation threshold (snippet).
3. Amazon Meshtastic 2/3/4-pack bundles. No Amazon listings in snippets; Rokland 1–2 packs.
4. Indie sports-data API MRR/subscribers. None published for college stats.

## Sources
- [Superhive add-ons, newest](https://superhivemarket.com/categories/addons/browse?sort_date=desc)
- [CFBD API tiers](https://collegefootballdata.com/api-tiers)
- [Graphtreon CFBD](https://graphtreon.com/creator/collegefootballdata)
- [Highlightly MLB & NCAA API](https://highlightly.net/mlb-api/)
- [BALLDONTLIE](https://www.balldontlie.io/)
- [Make iCount + monday](https://www.make.com/en/integrations/icount/monday)
- [Morning integrations](https://www.greeninvoice.co.il/add-ons/integrations/)
- [iCount integrations](https://www.icount.co.il/integrations/)
- [Apify Store API](https://api.apify.com/v2/store)
- Search-only (not opened):
  - [Rokland 2-packs](https://store.rokland.com/pages/meshtastic-node-2-packs) (403)
  - [beancount.io allocation guide](https://beancount.io/blog/2026/09/22/israel-invoice-allocation-number-5000-nis-osek-murshe-b2b-guide)
  - [Workato ITA connector](https://www.workato.com/integrations/israel-tax-authority)
  - [TrustMRR SportSphere](https://trustmrr.com/startup/sportsphere.md)
