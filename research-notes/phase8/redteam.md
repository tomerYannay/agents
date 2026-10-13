# Phase 8 Red-Team Investor report (P8-REDTEAM), 2026-10-13

**Scope.** Why each of N1–N14 would fail *for this founder*. The founder is Israel-based, technical, part-time, has about $2k and wants to own a business. I also challenge the four leader items: H7, M1, H2 and M2/SoldComps.

**Searches and sources.**
- WebSearch: **8 of 8 used**, all logged as `P8-REDTEAM`. Topics:
  1. German hygiene training online
  2. Kalshi developer terms
  3. CONTPAQi SDK terms (wasted: nothing found)
  4. Bose SoundTouch end of life
  5. Prediction-market companion tools
  6. Smoobu AI replies
  7. eBay 2026 User Agreement
  8. Unified-API connector programmes
- Primary pages and APIs fetched with curl, using a generic User-Agent:
  - TÜV Nord's online Folgebelehrung page (price);
  - Fresha's Terms of Use and Partner Terms of Business (full text, grepped);
  - Kalshi's docs index;
  - the WordPress.org plugin API (Merchant Center plugins);
  - the iTunes Search API (padel, event photo-sharing and prediction-market apps; US, ES, SE, IT, BR, IL, PL and NL storefronts);
  - itsfoss.com (Bose) and valueaddedresource.net (eBay User Agreement text).
- **Blocked or failed:**
  - kalshi.com/developer-agreement returned HTTP 429 (rate-limited). I did not retry or bypass it, so the Developer Agreement text is unread.
  - The CONTPAQi 2026 price-list PDF downloaded (17.9 MB), but no local PDF-text tool was available, so it is unread.
- Scratch: `scratchpad/p6plus/P8-redteam/{scripts,data}`. No browser, contact, sign-ups or purchases.

**Conventions.** Frozen rubric. Step values are CF 5/4/4/4/3, Scal 3/4/4/4/3/2, Dist 4/4/6/3/3. "Steps" are the 0–5 criterion scores in rubric order. Scores are reproducible with `scripts/score.py`.

---

## 0. Headline

1. **No Phase 8 idea survives the red team above the noise band of the board's middle.**
   - The best are **N12, the WooCommerce Merchant Center monitor (47.4)**, and **N1, German hygiene certificates (47.0)**. Both have a newly verified blocker or weakness.
   - Every N-idea lands at 28–47. Nothing displaces H7, H6, M1 or K8.
2. **Phase 8's direction ("reverse-engineer newcomer winners") is right, but its datasets are survivor lists.** None of them contains the failures that the comparison needs:
   - **TrustMRR** is opt-in. Stealth listings hit 24% and for-sale listings 5.7% vs 3.0%. That 3.9% base rate is an upper bound.
   - **EF and Flippa** have an intake floor (5th percentile about $1.8k/month).
   - **App Store search** is relevance-ranked and capped at 200.
   - **RevenueCat's** data covers only apps that already monetise.

   Every "comparable" behind N1, N2, N4, N5, N9, N11 and N12 is **n=1 from those top slices**. Two of them are anonymous or stealth.
3. **Copy speed is now measured, not hypothetical.** In every niche I checked, the gap the agents found has already been entered:

   | Niche | Entrants | Their outcomes |
   |---|---|---|
   | WooCommerce Merchant Center suspension tools (N12) | 4 since Dec 2025 | 0–10 installs |
   | "Padel americano" apps (N14) | 111–132 released in 2026 per storefront | none ≥100 local ratings |
   | Wedding photo-sharing apps (N9) | 141–151 released 2024+ per storefront | none ≥100 local ratings |
   | Prediction-market apps (N8) | ≈90 per keyword since 2025H2 | the winners are DraftKings, FanDuel and Fanatics |
   | QuickBooks Desktop APIs (M1, N3) | 3 priced clones in 2026 | — |

   Agent E's "niches flood within about 18 months" is too generous for software. **The flood arrives within about 6 months of a winner becoming visible.**
4. **New hard or near-hard blockers found:**
   - **N1:** the B2C pull that made Alimentia work does not exist in Germany. The job-seeker's credential, the §43(1) IfSG Erstbelehrung, can only come from the Gesundheitsamt. Gesundheitsämter already sell it **online for €28** (LRA Fürth, Nürnberger Land), with video-ident in Ortenau. The part a private provider *can* sell, the 2-yearly Folgebelehrung, is an **employer duty**. TÜV Nord already sells it online for **€35 net**.
   - **N11 (Fresha route):** Fresha's Partner Terms forbid sharing login credentials ("must not be shared"; "disclose, share or resell any login…"). They also forbid providing the platform "as a hosted service or otherwise make available to any third party… without express prior written permission". Its Terms of Use ban scrapers and bots. There is no API or webhook. **The Fresha route is a kill.** D3 dies with it.
   - **H2 rescore (Bose target):** Bose moved the end of life to 6 May 2026 and published the local Web API under a royalty-free licence. AirPlay, Spotify Connect and the local app keep working, and 100+ GitHub projects use the API. **There is no orphaned-hardware gap to sell a board into.**
   - **M2/SoldComps:** eBay's User Agreement (posted 20 Jan 2026, effective 20 Feb 2026) now bans "any robot, spider, scraper, data mining tools… (including… LLM-driven bots…)" without eBay's express permission. SoldComps is a contract breach with revenue, not a template.
5. **Leader calls:**
   - **H7:** trim to **54.8** (range 53.8–55.4). Still nominal #1, but it is a ~2–5%-per-product lottery, and the rubric's Cash-Flow score hides that.
   - **M1:** **downgrade to 48.4** (range 47.4–50.8). M1 rests on n=1 (Conductor) and a 0.12 vertical ratio. There is new clone evidence, and the Sage template terms lean adverse.
   - **H2:** Agent B's rescore is only **partly justified**: about **+2.6 to 41.2**, and it stays out of the shortlist because there is still no viable target device.
   - **M2:** SoldComps does **not** raise M2. **Hold 44.4.**

---

## 1. Cross-cutting attacks (apply to every N-idea)

| Attack | Evidence | Who it hurts most |
|---|---|---|
| **Survivorship** | See headline 2 above. Also: EF's "5 owner hours/week" is a sale-readiness artefact. Sellers cut their own hours *before listing*, using teams of 8–35 contractors (Agent C). | N2, N4, N5 (EF n=1–2 comparables); N1, N9, N11, N12 (TrustMRR n=1) |
| **Copy/flood** | Headline 3. AI-built supply roughly tripled App Store newcomers (2024 → 2026) and Superhive listings (2025 → Q3 2026). Tally drew 6+ npm relays in Sep–Oct 2026. | N3, N7, N8, N9, N12, N14 |
| **Paid-ads CAC** | No idea has a measured newcomer CAC. $2k buys about 1–2 credible ad tests. German Meta CPM about doubled Jul 2025 → Jul 2026 [vendor benchmark, Agent B]. Kickstarter-style launches cost $75–150 per backer [vendor]. TrustMRR's "paid channels 3–6× lift" is reverse-causal: winners can afford ads. | N1, N2, N5, N9, N10 |
| **Labour** | TrustMRR: solo 0.79× vs 2–5-person team 4.35×. Organic video is founder labour, and it decays when posting stops (AppAlchemy $17k claimed → $5.5k verified). | N4 (service), N7, N8 (video volume), N5 (creative) |
| **Israel fit** | Time zones: EU UTC+1/2 vs Israel UTC+2/3 is fine. Mexico (UTC−6) gives about 2 working-hour overlap. The US gives 0–3 hours. Language: German (N1, N4), Czech or Swedish (N5) and Spanish (N3) need hired natives for content, support and B2B sales. Ads-only B2C can work without it; outbound B2B in German or Spanish cannot. | N3, N4, N5, N1 |
| **Capital** | Inventory, GPSR "responsible person", IOSS/VAT (N5); enclosure, certification and prototypes (N6); ad budget to learn (N2, N10). | N2, N5, N6 |

---

## 2. Per-idea red team

### N1. German online food-hygiene certificate (Alimentia model)
**What I checked:**
- **§43 IfSG.** The Erstbelehrung (the job-seeker's "Gesundheitszeugnis") is Gesundheitsamt-only. Gesundheitsämter now run it **online**:
  - LRA Fürth: €28, certificate issued immediately.
  - LRA Nürnberger Land: €28, paid online.
  - Ortenaukreis: online with video identification.

  [Secondary: search snippets of bayernportal.de and ortenaukreis.de; Bremen LMTVet info sheet: Erstbelehrung "nur beim Gesundheitsamt", Folgebelehrung "durch den Lebensmittelunternehmer".]
- **The private product:** TÜV Nord's 20-minute "Online-Unterweisung Folgebelehrung nach §43 IfSG" costs **€35.00 net / €41.65 gross** [Verified: tuev-nord.de page, fetched 2026-10-13]. HygieneschulungNow (Berlin) holds ZFU approval no. 7613826 for an online Folgeschulung [Secondary: zfu.de snippet].

**Top 3 failure modes:**
1. **The buyer is wrong.** In Spain, a job-seeker buys a €12 certificate to show employers, so pull is B2C and individual. In Germany, the individual credential is a state monopoly that the state already sells online. What remains is an employer obligation that employers can meet in-house for free: §43(4) lets the employer give the instruction. Alimentia's search-ads engine therefore points at a much thinner, B2B, price-anchored-at-€0 demand.
2. **Incumbents already sell online.** TÜV Nord (a trusted brand, €35) and ZFU-approved e-learning providers do. The undercut at €12 is real, but "cheap certificate from an unknown foreign site" is a weak sell to a food business facing inspection. Agent E flags inspector acceptance [Unknown].
3. **Liability and founder fit.**
   - A German-qualified content signatory is needed.
   - LMHV training content must be substantive.
   - Every page, ad and support reply is in German.
   - Track B needs country-by-country rule research (Italy regional, Austria WKO).

**Hard blockers:** for the *Erstbelehrung*, yes (Gesundheitsamt only). For the Folgebelehrung and LMHV training, none: third parties are allowed [Verified by Agent E: IHK Frankfurt].

**Unverified:** German CPCs; employer willingness to pay vs doing it in-house; inspector acceptance.

**Verdict:** **Weak.**
- Steps: CF 3,3,4,4,4 = 71 · Scal 2,2,3,4,1,2 = 49 · Dist 3,4,2,2,3 = 55 → Balanced 59.0, penalty 12 → **47.0**.
- **Decisive assumption:** German food employers (not job-seekers) buy a paid third-party online Folgebelehrung/LMHV certificate at ≥500 a month for ≤€5 ad cost each.
- **Cheapest desk check:** count Google results and ad presence for "Folgebelehrung online" and "Hygieneschulung online Zertifikat" (incumbent count and prices). Read 3 Gesundheitsamt pages to see whether they publish free Folgebelehrung material for employers.
- **Kill line:** ≥5 online providers at ≤€20, or free official employer kits.

### N2. Certification study kits via Meta ads
**Top 3 failure modes:**
1. **n=1 survivor.** EF #94286 is the strongest young P&L in a dataset that only shows winners. Its niche is undisclosed, so we may pick the same certification and fight the seller, or the buyer, of a $433k/year business.
2. **CAC is unknown, and the budget is one test.** $2k covers SME review ($500–1,000) and about $1k of ads. Meta health-adjacent ad review and exam-trademark rules apply. One failed creative round ends the test before learning.
3. **Thin founder fit.**
   - No healthcare domain.
   - No ad-buying track record.
   - One-off revenue (recurring = 1).
   - AI-generated study guides flood Amazon (supply growth is general, not measured for this niche).

**Hard blockers:** none (trademark and "no real exam items" are manageable).

**Verdict:** **Weak.**
- Steps: CF 4,2,2,3,3 = 57 · Scal 3,1,3,3,1,2 = 44 · Dist 4,3,2,2,3 = 55 → 51.4, penalty 13 → **38.4**.
- **Decisive assumption:** first-order CAC ≤40% of AOV in a certification where incumbents are weak.
- **Cheapest desk check:** for 5 candidate certifications, compare the review recency and count of the top-10 Amazon guides with exam volume. Also check Meta Ad Library for active advertisers per certification. If there are ≥3 active advertisers with fresh creatives, the gap is not real.

### N3. CONTPAQi self-serve integration API (Mexico); variants Tally, Pastel
**Top 3 failure modes:**
1. **Demand is unshown.**
   - AR Software's $720/year licence has unknown sales and 15 GitHub stars.
   - A Shopify thread from 2023 is the only merchant signal.
   - Conductor is n=1 among about 7.9k TrustMRR profiles, and no 2024–26 accounting or ERP integration reached $1k MRR (Agent D).
   - Mexican SaaS buyers' willingness to pay is below US levels [Hypothesis].
2. **Terms and channel are gated by a distributor network.** CONTPAQi is sold "exclusively through certified partners" [Secondary: search P8-REDTEAM #3]. No public SDK licence surfaced. Sage's template shows what a desktop-ERP developer agreement typically says: no use "for the benefit of any third party"; resale only "under separate agreement". A hosted middleman resold to vendors is the most exposed use.
3. **Founder fit and copy risk.**
   - Spanish docs, sales and support.
   - Mexico is 8–9 hours behind Israel.
   - Windows-agent installs on customers' machines.
   - Tally already drew 6+ indie relays in two months, and the QuickBooks Desktop niche drew 3 clones in 6 months. A visible CONTPAQi win would be cloned, possibly by AR Software itself.

**Hard blockers:** none verified. The SDK terms are **[Unknown]**: the search found nothing, and the price list was unreadable locally.

**Verdict:** **Weak.**
- Steps: CF 2,1,4,5,3 = 59 · Scal 2,5,2,4,1,2 = 57 · Dist 3,2,1,2,3 = 41 → 54.6, penalty 13 → **41.6**.
- **Decisive assumption:** ≥30 vendors or fintechs pay about $40 per RFC per month, and CONTPAQi permits hosted resale.
- **Cheapest desk check:** an integration-page census of about 100 Mexican SaaS, POS and e-commerce vendors, counting CONTPAQi vs Alegra/Bind (as F proposed). **Kill if fewer than 10 list CONTPAQi.**

### N4. German human-plus-AI guest-messaging desk for STR managers
**Top 3 failure modes:**
1. **The AI half is bundled; the human half is a low-margin service.**
   - Smoobu, the German PMS, ships native AI-suggested replies (Gemini 2.5 Flash, translation, built from guidebook and house rules). Guestway (claims 70% automation) and ProhostAI already plug into Smoobu [Secondary: support.smoobu.com and integration pages via search #6].
   - Guesty sells a human desk itself.
   - What is left is a night-shift service at about 19% margin (the EF #86244 anchor).
2. **Selling and staffing in German from Israel.**
   - Acquisition is outbound to German property managers, with no newcomer channel data.
   - The desk needs German-native agents around the clock; Philippines staff do not write German guest messages.
   - The founder cannot do the sales calls.
3. **The comparable is a survivor and a French incumbent.** #86244 started in 2022, came out of the French market, and is n=1.

**Hard blockers:** none. GDPR needs a data-processing agreement, which is routine.

**Verdict:** **Weak.**
- Steps: CF 3,2,4,2,2 = 53 · Scal 3,5,2,2,1,1 = 50 · Dist 4,2,1,2,2 = 42 → 49.6, penalty 12 → **37.6**.
- **Decisive assumption:** German managers with 5–50 units pay about €20 per listing per month for a *human* desk on top of free PMS AI.
- **Cheapest desk check:** count German "Gästekommunikation"/co-host service offers with public prices on Google and on Airbnb co-host listings for 3 cities.

### N5. Local-language Meta-ads store in a small EU market (and the high-ticket dealer variant)
**Top 3 failure modes:**
1. **Capital.** $2k gives one or two product tests. A winning test then needs a working-capital float for ads plus supplier or COD settlement lag. GPSR needs an EU responsible person. IOSS/VAT, COD refusals and returns apply. EF's $9.4k median for non-English EU is **14 survivors**, with no denominator.
2. **No moat.**
   - Winning products are copied by other ad-spying dropshippers.
   - Ad-account bans.
   - CPMs rising (German CPM about 2× in a year, vendor data).
   - Defensibility 0.
3. **Founder fit.** Creative and customer service in Swedish or Czech. Health claims (an "orthopaedic" brace) run into medical-device rules. Nothing in the model uses the founder's software edge.

**The high-ticket dealer variant:**
- It needs a US LLC.
- Dealer approval for a foreign-owned unknown store is "moderate–hard" [Secondary].
- It is promoted by course sellers, so saturation is likely.
- Verified outcomes are $1.2–5.9k/month after about 2 years.

**Verdict:** **Kill for this founder** (capital and fit), not for the market.
- Steps: CF 4,3,1,2,2 = 50 · Scal 3,1,3,3,0,1 = 39 · Dist 3,3,2,2,3 = 51 → 45.8, penalty 13 → **32.8**.
- **Decisive assumption:** a $1–1.5k test finds a product with first-order CAC ≤35% of AOV.
- **Cheapest desk check:** in Meta Ad Library, count active local-language advertisers for 3 candidate products in SE/CZ. **Kill if ≥5 already run localised creatives.**

### N6. Firmware-first field tool on Crowd Supply via Elecrow/Soldered
**Top 3 failure modes:**
1. **The 75%+ rejection gate comes first, and hardware is not this founder's craft.** Enclosure, CE/FCC, BOM risk and delivery delays sit outside the software skill set.
2. **Time to first dollar is 6–12 months, and revenue is one-off.** Developer and bench tools have a median of $21.2k (n=20). After fees and BOM that is about $10k gross profit once, so Track A needs 2–3 products a year.
3. **Partner terms are unknown.** The Aviary and Inkubator pages do not say who pays for production before payout or what the revenue split is. If the partner takes a share, margin falls.

**Hard blockers:** none verified.

**Verdict:** **Weak.**
- Steps: CF 3,1,2,3,2 = 45 · Scal 2,1,2,3,2,2 = 40 · Dist 4,3,3,2,2 = 58 → 45.6, penalty 11 → **34.6**.
- Proven channel gets 3, the best in Phase 8, because Crowd Supply has a real denominator.
- **Decisive assumption:** the partner funds production to payout, and Crowd Supply accepts a first-time creator with no hardware track record.
- **Cheapest desk check:** read the Elecrow Aviary and Soldered Inkubator FAQs and terms for cost-sharing and IP clauses. Count first-time bench-tool creators on Crowd Supply with no prior hardware repository.

### N7. Trend-timed collectible value-scanner micro-studio
**Top 3 failure modes:**
1. **The window closes faster than an outsider can spot it.**
   - TCG scanners went from 1/5 and 4/13 early cohorts to **6/104 in 2026H1**.
   - Next Vision clones every vertical within months.
   - Individual-developer apps reach 1k ratings 4.9% of the time.
   - The early-window 15–30% hit rate was earned by **hobby insiders**. The founder is not a collector.
2. **Value data is a terms-of-service problem.** eBay's 2026 User Agreement bans scrapers and LLM bots without permission [Verified: valueaddedresource.net, quoting the agreement]. Licensed price APIs (PriceCharting, TCGplayer) cost money and restrict use [Unknown terms].
3. **Video labour.** The PropGPT spike came on video #70. That is daily founder posting or paid UGC, which $2k barely tests.

**Verdict:** **Weak.**
- Steps: CF 3,3,4,4,2 = 65 · Scal 3,4,2,3,0,3 = 51 · Dist 3,2,2,2,2 = 44 → 55.2, penalty 13 → **42.2**.
- **Decisive assumption:** an outsider can identify a boom and ship before the studio wave.
- **Cheapest desk check:** backtest with the iTunes API. For Labubu/Pop Mart, Lorcana and One Piece, find the release date of the first scanner app vs the first studio clone. **Kill if the median gap is under 8 weeks.**

### N8. Prediction-market research and alert companion
**Top 3 failure modes:**
1. **Free tools already cover the feature set.** Alerts.chat is a free price-alert service for Polymarket and Kalshi. Oddpool tracks whales; WhaleWatch, ProbSights and Vaxelo AI also exist [Secondary: search #5]. Kalshi serves market data without authentication [Verified: docs.kalshi.com/llms.txt], so the barrier to entry is zero.
2. **The flood and the platforms.** About 86–97 new apps per keyword since 2025H2. The ≥1k-rating winners are DraftKings, FanDuel, OG.com and Fanatics. Prediction Radar (#40 Finance) is the only indie companion signal, and it is n=1 and 6 weeks old.
3. **Regulatory and terms fragility.**
   - Kalshi API use is bound by a Developer Agreement I could not read (HTTP 429).
   - State litigation over sports contracts and CFTC posture can shrink the market [not re-verified].
   - Apple's gambling-adjacent review.
   - PropGPT's revenue is props-betting research, which is not the same user.

**Verdict:** **Weak.**
- Steps: CF 3,3,4,4,2 = 65 · Scal 3,4,2,3,0,2 = 49 · Dist 3,2,1,2,2 = 38 → 53.2, penalty 13 → **40.2**.
- **Decisive assumption:** traders pay $10–20/month for third-party research despite free alert tools.
- **Cheapest desk check:** read Kalshi's Developer Agreement and Polymarket's API terms (once the rate limit clears), and estimate Prediction Radar's revenue rank over 8 weeks from RSS Finance grossing snapshots.

### N9. QR guest photo-sharing in an under-served language market
**Top 3 failure modes:**
1. **The comparable is one stealth German site.** Global app supply is flooded: 141–151 wedding photo-sharing apps released 2024+ appear in IL, PL and NL storefront searches, none with ≥100 local ratings. WedShoots and POV are free or cheap anchors (POV has 1,949 NL ratings).
2. **Israel, the natural fit, has substitutes.** Hosts use WhatsApp groups, and photographers sell live photo-print and magnet stations [Hypothesis]. Any other market means a language the founder does not have.
3. **Per-event, seasonal, no recurrence.** Recurring = 1. Every sale is a new acquisition through Google Ads at unknown CPC.

**Verdict:** **Weak.**
- Steps: CF 3,3,4,3,4 = 67 · Scal 2,1,3,4,1,3 = 47 · Dist 4,3,2,2,3 = 55 → 56.6, penalty 13 → **43.6**.
- **Decisive assumption:** Google Ads cost per paid event ≤€30 in one chosen market.
- **Cheapest desk check:** for IL and PL, count web (non-app) QR photo-sharing sellers advertising on wedding queries. Check Google Ads Transparency Center for advertisers on "QR wedding photos" in each country.

### N10. Hebrew-localised AI consumer app (paid social plus creator revenue share)
**Top 3 failure modes:**
1. **Category choice is everything, and the obvious ones are taken.** Calorie tracking has CalBuddy (2,520 IL ratings), Calcounti (3,372) and Cal AI (3,879, Hebrew UI). 4 of about 16 Hebrew newcomers passed 400 ratings, but the sample was biased toward visible apps.
2. **Small ceiling and Israel drift.** About 10M people means low depth. This is the Israel-niche drift that brief lesson 3 warns against. It is justified only because newcomer outcomes are measured.
3. **Economics.** 50% creator revenue share plus Apple's 15–30% plus Israeli ad CPA. CalBuddy's revenue figures are self-reported.

**Founder fit is the best in Phase 8:** native language, local creators, and no time-zone or legal friction.

**Verdict:** **Viable with conditions.**
- Steps: CF 3,3,3,3,3 = 60 · Scal 1,4,3,3,1,5 = 56 · Dist 3,3,2,3,3 = 54 → 57.2, penalty 12 → **45.2**.
- **Decisive assumption:** one specific category has Israeli paid CPA ≤50% of 12-month LTV and no Hebrew-native app above about 300 ratings.
- **Cheapest desk check:** an iTunes IL census across about 30 top US AI-app categories (ratings of the best Hebrew-native app per category). Kill any category where a Hebrew app already has >1k ratings.

### N11. Review-and-rebooking add-on for Fresha/Booksy salons (with D3)
**What I checked [Verified: terms.fresha.com/partner-terms and /terms-use, fetched 2026-10-13]:**
- **Partner Terms.** Partners must not "license, sublicense, sell, resell… provide as a hosted service or otherwise make available to any third party the Fresha Platform Services in any way without express prior written permission". Partners must "ensure each Authorised User uses their own unique, verified login credentials, which must not be shared". They must not "disclose, share or resell any login… password or account details".
- **Terms of Use.** These ban "'scrape' content", "launch an automated program or script, including… web spiders, web crawlers, web robots", and reverse engineering "to… build a competitive product".
- **Fresha's own messaging.** It already sends automated "thank you for visiting" SMS and runs its own review policy and marketplace reviews.

**Top 3 failure modes:**
1. **There is no compliant trigger.**
   - No API and no webhooks (Supergood).
   - Credential-based automation breaches the Partner Terms on the *salon's* side, so the customer carries the breach.
   - Email parsing of booking notifications is fragile and still unsanctioned.
   - **The Fresha route, and D3, are dead.**
   - Booksy's terms were not fetched (URLs 404).
2. **The platform can ship it.** Fresha controls post-visit messaging and has every incentive to keep reviews on Fresha.
3. **The comparables are French, n=2, with undisclosed channels.** Coucou (Planity) and MyFrank. Vagaro, which has an API, is already served by Reviewflowz at $70–80.

**Verdict:** **Weak.** The Fresha variant is a kill; the idea survives only on booking platforms with a public API and no incumbent add-on.
- Steps: CF 3,2,4,4,3 = 64 · Scal 3,5,2,4,1,3 = 62 · Dist 4,2,1,2,2 = 42 → 58.8, penalty 14 → **44.8**.
- **Decisive assumption:** a large salon platform with a public API (Booksy? Timely? Square Appointments?) lacks a Google-review add-on.
- **Cheapest desk check:** read Booksy's partner/API pages and the app marketplaces of Square Appointments and Timely. Count review add-ons on each.

### N12. Ongoing Merchant Center policy monitor for WooCommerce stores and agencies
**What I checked [Verified: api.wordpress.org plugin query, 2026-10-13]:**

| Plugin | Listed | Active installs |
|---|---|---|
| Suspension Shield for WooCommerce – Google Merchant Center | 2026-07-20 | 10 |
| FeedProof for WooCommerce | 2026-06-19 | 0 |
| PW Feed Store Readiness Audit | 2026-08-06 | 0 |
| Cirrusly Commerce | 2025-12-14 | 0 |

All four have 0 ratings. Feed managers dominate the space: Google for WooCommerce at 800k installs, CTX Feed 90k, Product Feed PRO 80k.

**Top 3 failure modes:**
1. **"No WooCommerce monitor found" is false.** Four 2025–26 entrants exist, and their outcome is about 0 installs. That is the measured newcomer channel result for this exact niche.
2. **The comparable's channel may not transfer.** The anonymous Shopify leader (n=1, listed for sale) declares affiliates and influencers, which suits Shopify dropshipping culture. WooCommerce merchants are more agency-served. Feed-plugin vendors with 80k–800k installs can add a "suspension check" tab.
3. **Crawlers cannot see most suspension causes.** Business verification and product claims are invisible to them. Free checkers (AdNabu) and a $99 one-off audit anchor the price.

**Verdict:** **Weak.** It is the top-scoring N-idea, but only because the rubric rewards cheap starts (CF 74).
- Steps: CF 2,3,5,5,4 = 74 · Scal 2,4,2,4,0,4 = 54 · Dist 4,3,1,2,2 = 46 → 60.4, penalty 13 → **47.4**.
- **Decisive assumption:** WooCommerce merchants or agencies pay a recurring fee for monitoring.
- **Cheapest desk check:** re-query the WordPress.org API in 60 days for the four entrants' install growth. Check whether the Shopify leader's App Store reviews skew to dropshippers.

### N13. Connector supplier to unified-API aggregators
**Top 3 failure modes:**
1. **No buyer behaviour is shown.** No unified-API vendor (Apideck, Codat, Merge, Chift, Nango) publishes a third-party or community connector licensing or revenue-share programme [Secondary: search #8]. Apideck pitches *platforms* to partner, not connector suppliers. The only analogue found is Globus, a storage-data programme.
2. **Concentration and build-vs-buy.** About 10 possible buyers, each of whom prefers to own core connectors. A single "no" ends the business.
3. **Business-development labour from Israel with no references.** This is enterprise selling, which is the opposite of audience-free.

**Verdict:** **Kill.**
- Steps: CF 1,1,4,4,3 = 50 · Scal 1,3,1,3,2,3 = 43 · Dist 4,1,0,1,1 = 26 → 42.4, penalty 14 → **28.4**.
- **Decisive assumption:** an aggregator licenses an external agent.
- **Cheapest desk check:** scan the Apideck, Chift and Codat docs for connectors credited to third parties ("powered by", "partner-built").

### N14. Amateur padel, beach-tennis and darts organiser apps outside the US
**What I checked [Verified: iTunes Search API, 2026-10-13]:**

| Storefront | Apps returned for "padel americano" | Released 2024+ | Released 2026 | Max local ratings among new apps | Paid |
|---|---|---|---|---|---|
| ES | 181 | 163 | 124 | 25 | 11 |
| SE | 175 | 145 | 111 | 33 | 13 |
| IT | 172 | 157 | 123 | 17 | 13 |
| BR | 186 | 170 | 132 | 13 | 11 |

The median new app has 0 ratings in every storefront. Playtomic has 77,453 ES ratings.

**Top 3 failure modes:**
1. **Flooded:** over 110 new entrants per storefront in 2026 alone.
2. **The grossing ranks are probably cents.** A Sports grossing #62–#95 with tiny ratings in BR/DE implies very low thresholds. Rank-to-dollar data is [Unknown].
3. **Playtomic** (club booking plus matches) can add organiser features for free.

**Verdict:** **Kill.**
- Steps: CF 1,3,5,4,4 = 65 · Scal 1,2,1,4,0,3 = 37 · Dist 3,2,1,2,1 = 35 → 47.8, penalty 12 → **35.8**.
- **Decisive assumption:** a top-100 non-US Sports grossing rank is worth ≥$20 a day.
- **Cheapest desk check:** find any TrustMRR or RevenueCat-verified padel or darts app and compare its 30-day revenue with its chart rank.

---

## 3. Leader challenges

### H7 Blender add-ons: 55.4 is still slightly overrated → **54.8 (range 53.8–55.4)**
- **What the auditor measured:**
  - Median paid add-on: 2.5 sales in 3 months and about 10–15 lifetime (≈$90 gross).
  - 5.6% reach 100+ sales and 2.2% reach 500+.
  - Supply is about 3× the 2025 rate.
  - The proven-channel cut (3→2) is right.
- **What is missing:** *first customers* (Dist, 3 points a step). Getting the first *paying* customers in Track-A volume now takes a top-2–5% product. "79% get ≥1 sale" measures speed to the first $10, which is already credited under speed. First customers −1 gives Dist 58, Balanced 66.8 and **54.8**.
- **Why I do not raise the penalty:** the decisive assumption (top-decile execution) is now *measured* as a 2–5% base rate, not contradicted. Better measurement should not raise the penalty, so penalty 13 (53.8) is the strict reading only.
- **Rubric caveat the report must carry:** H7's CF 80 rewards a cheap, fast start, not reaching $2–5k. Per product, H7 is a lottery at about **2–5%**. That is comparable to TrustMRR's 3.9% ($3k MRR) and the App Store's 4.9% (individual developers, 1k ratings). It is not better.
- **Ranking:** H7 stays nominal #1 only because every alternative carries an unpriced blocker. Its lead over H6 (52.2) is about 2.6 points, which is noise.

### M1 Sage 50 API: **downgrade 52.0 → 48.4 (range 47.4–50.8)**
Four independent pieces of new evidence point the same way. Each maps to a *different* criterion, so this is not stacking:

| Criterion | Change | Evidence |
|---|---|---|
| Market depth (Scal) | 2→1 (−3) | Vertical-SaaS ratio is **0.12**, closer to my Phase 7 kill line (0.08) than to keep (0.2). The 0.19 headline is propped up by AP platforms (BILL, Tipalti and others) that build in-house. M1's own Phase 7 customer list (property management, payroll, nonprofit) scores **0 of 97**. |
| Defensibility (Scal) | 1→0 (−3) | New mechanism: three QuickBooks Desktop clones in about 6 months, one ("Desktop Accounting API") with a generic multi-product name and Conductor's exact price. Phase 7's 1 assumed incumbents (Rutter, Conductor) would be slow; AI-built clones are not. |
| Proven channel (Dist) | 2→1 (−6) | Conductor is n=1 in a 69% random TrustMRR sample. No 2024–26 accounting or ERP integration reached $1k MRR. Dev tools and APIs have a 0.63× lift. This is the same standard that set J7's proven channel to 1. |
| Penalty | hold 12 (13 strict) | The Sage DPP template (§3.3.2 "shall not… allow others to use… for the benefit of any third party"; §3.5 resale "only under separate agreement") leans adverse. It is not yet the Sage 50 text, so it is not a direct contradiction. |

- Steps: CF 3,2,4,5,3 = 68 · Scal 1,5,2,4,0,5 = 57 · Dist 4,3,1,2,4 = 52 → Balanced 60.4, penalty 12 → **48.4** (13 → 47.4).
- The auditor's 50.8 downside, which cut only depth, is the generous end.
- M1 falls into the 47–49 pack with N12, N1 and L6. It is **no longer a podium idea**.
- **Decisive assumption:** the Sage 50 US/CA partner agreement permits a hosted API used by third-party vendors.
- **Cheapest check:** the 2025 "Sage NA Tech Partner Program" PDF (403 to curl). Try a Wayback copy.

### H2 revival boards: Agent B's rescore is **partly justified → about 41.2** (from 38.6); still not shortlist-worthy
- **For:**
  - MiciMike is a verified, audience-free $133k outcome on the same channel. That fixes Phase 3's "no newcomer proof": spending +1 (CF +5).
  - Crowd Supply's measured funding rate (~92% of launched campaigns) supports first customers +1 (Dist +3).
  - This gives CF 49, Scal 48, Dist 62 → Balanced 51.2, penalty 10 → **41.2**.
- **Against (why not more):**
  - Phase 3's fatal flaw, "no target device identified", is **still unfixed**:
    - **Bose SoundTouch** is not orphaned. End of life moved to 6 May 2026. Bose released the local Web API under a royalty-free licence. AirPlay, Spotify Connect and the local app keep working. 100+ GitHub projects already use the API [Verified: itsfoss.com, 8–9 Jan 2026]. Software, much of it free, fills the gap.
    - **Belkin Wemo** devices are $10–40 plugs and switches. A $50–99 replacement board cannot beat a new Matter plug [Hypothesis on economics].
  - The category is being copied (LocalDot).
  - The founder is not a hardware engineer.
- **Decisive assumption:** a still-orphaned device with a large installed base exists, with no free software fix and no cheaper replacement product.
- **Cheapest desk check:** list 2025–26 cloud shutdowns and filter out any where the vendor published a local API or where the device costs under $60 new.

### M2 licensed data API: SoldComps does **not** change M2 → **hold 44.4** (range 42–45)
- SoldComps' $347 → $19,984/month (Apr–Sep 2026) is real [Verified by Agent D]. But it is built by parsing eBay pages.
- eBay's User Agreement (posted 20 Jan 2026, effective 20 Feb 2026) prohibits "any robot, spider, scraper, data mining tools… or other automated means (including… LLM-driven bots…) to access our Services for any purpose, except with the prior express permission of eBay" [Verified: valueaddedresource.net quoting the agreement; robots.txt policy since Dec 2025].
- So SoldComps is evidence for an **unlicensed** data business, the opposite of M2's "licensed" premise, and the slot is taken.
- It shows the outlier tail exists on Apify and RapidAPI. That is one winner against a measured median of 1 user per Actor, so proven channel stays 1.
- Any temptation to raise M2's spending or proven-channel score from SoldComps should be refused.

---

## 4. Recommended ranking

**Red-team Adjusted (midpoints):**
- Leaders: H7 54.8 · H6 52.2 · K8 52.0 · H1 51.2 · **M1 48.4** · M2 44.4 · H2 41.2.
- Phase 8, in order: **N12 47.4** · **N1 47.0** · N10 45.2 · N11 44.8 · N9 43.6 · N7 42.2 · N3 41.6 · N8 40.2 · N2 38.4 · N4 37.6 · N14 35.8 · N6 34.6 · N5 32.8 · N13 28.4.

| Idea | CF | Scal | Dist | Pen | Adj | Verdict |
|---|---|---|---|---|---|---|
| N12 WooCommerce Merchant Center monitor | 74 | 54 | 46 | 13 | **47.4** | Weak |
| N1 German hygiene certificate | 71 | 49 | 55 | 12 | **47.0** | Weak |
| N10 Hebrew AI consumer app | 60 | 56 | 54 | 12 | **45.2** | Viable with conditions |
| N11 Salon review add-on (Fresha route killed) | 64 | 62 | 42 | 14 | **44.8** | Weak |
| N9 QR event photos | 67 | 47 | 55 | 13 | **43.6** | Weak |
| N7 Collector scanner studio | 65 | 51 | 44 | 13 | **42.2** | Weak |
| N3 CONTPAQi API | 59 | 57 | 41 | 13 | **41.6** | Weak |
| N8 Prediction-market companion | 65 | 49 | 38 | 13 | **40.2** | Weak |
| N2 Certification study kits | 57 | 44 | 55 | 13 | **38.4** | Weak |
| N4 German STR desk | 53 | 50 | 42 | 12 | **37.6** | Weak |
| N14 Padel/darts organiser apps | 65 | 37 | 35 | 12 | **35.8** | Kill |
| N6 Crowd Supply field tool | 45 | 40 | 58 | 11 | **34.6** | Weak |
| N5 Local-language EU store | 50 | 39 | 51 | 13 | **32.8** | Kill (for this founder) |
| N13 Connector supplier to aggregators | 50 | 43 | 26 | 14 | **28.4** | Kill |

- **Track A (realistic $2–5k/month):**
  1. **N10:** best founder fit; one ad test resolves it.
  2. **N1:** only if the employer-B2B demand check passes.
  3. **N12:** only if one of the four entrants shows install growth.
  4. **N3:** only if the census passes.
- **Track B:** none credible within $2k. **N2** and **N5** have Track-B proofs (EF), but both need ad capital and skills the founder lacks. **N7** and **N8** have lottery tails.
- **Risk-adjusted:** H7 (54.8) still sits above every N-idea. The cheapest information per dollar is:
  - the N10 category census (free, iTunes API);
  - the N1 incumbent and price scan (free);
  - the M1 Sage 50 partner-agreement text (free, if Wayback has it).
- **Kill:** N13, N14, N5 (for this founder), and the Fresha variant of N11 together with D3.

**WebSearch used: 8 of 8** (`P8-REDTEAM`; #3 on CONTPAQi terms found nothing).
- **Verified hard blockers:** N1 Erstbelehrung (Gesundheitsamt-only, already online at €28); N11/D3 Fresha Partner Terms (no credential sharing, no third-party hosted provision without written permission).
- **Verified contradictions of agent claims:**
  - N12: "no WooCommerce monitor exists" is false; 4 entrants found.
  - H2: "Bose SoundTouch streaming and multi-room stopped" is wrong; Bose released the API, and AirPlay and Spotify Connect remain.

**Sources:**
- [TÜV Nord online Folgebelehrung](https://www.tuev-nord.de/de/weiterbildung/seminare/online-unterweisung-folgebelehrung-nach-43-infektionsschutzgesetz-ifsg)
- [Bayernportal online Belehrung (Fürth)](https://www.bayernportal.de/dokumente/onlineverfahren/5701950913345)
- [Bremen LMTVet Schulungspflichten](https://www.lmtvet.bremen.de/sixcms/media.php/13/Info_34_Schulungspflichten.pdf)
- [ZFU listing 7613826](https://zfu.de/download-pdf/lehrgangssuche-uebersicht/7613826)
- [Fresha Partner Terms](https://terms.fresha.com/partner-terms) · [Fresha Terms of Use](https://terms.fresha.com/terms-use)
- [Kalshi docs](https://docs.kalshi.com) · [Kalshi Developer Agreement (429, unread)](https://kalshi.com/developer-agreement)
- [itsfoss: Bose SoundTouch API](https://itsfoss.com/news/bose-soundtouch-api/)
- [Value Added Resource: eBay User Agreement 2026](https://www.valueaddedresource.net/ebay-bans-ai-agents-updates-arbitration-user-agreement-feb-2026/)
- [Smoobu AI suggested replies](https://support.smoobu.com/hc/en-us/articles/38213708537106-How-do-I-use-AI-suggested-replies-for-guest-messages)
- [Alerts.chat](https://pm.wiki/uk/projects/alerts-chat) · [Oddpool whales](https://oddpool.com/whales)
- [CONTPAQi price list 2026 (unread locally)](https://www.contpaqi.com/hubfs/Listas%20de%20precios/Lista_de_Precios_Sistemas_CONTPAQi_2026.pdf)
- [Apideck: platforms and unified APIs](https://www.apideck.com/blog/what-platforms-gain-from-working-with-a-unified-api-provider)
- WordPress.org plugin API; Apple iTunes Search API (all accessed 2026-10-13).
