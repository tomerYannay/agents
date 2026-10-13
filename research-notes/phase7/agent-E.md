# Phase 7 — Agent E: Distribution-first / partner-channel economics

**Agent:** E (Distribution-first and existing customer spending) · **Date:** 2026-10-13 · **WebSearch used:** 8 of 8 (label P7-E, all logged in `research-notes/search-log.txt`). Most evidence comes from WebFetch/curl of public pages and was measured by scripts. Scripts and data: `.../scratchpad/p6plus/P7-E/{scripts,data}/`.

## Summary

I measured what partner channels actually give to **new** small suppliers, using public directory data.

| # | Channel | Measured newcomer result |
|---|---|---|
| 1 | Shopify Partner Directory (vendor partner programme). 6 countries, 507 listed partners, full profiles | 67% of partners whose Shopify account dates from 2024 or later have **zero** verified client reviews. 10% have ≥5 reviews in the last 12 months. Results split sharply by market: Germany 0 of 29, mid-size non-English markets (IL/PL/BR/MX/TR) 9 of 60. |
| 2 | Odoo partner network (implementation partners with tiers and commission) | 4,443 partners (Gold 340 / Silver 885 / Ready 3,218). Entry-tier "Ready" partners have a median of **1–10 lifetime customer references** depending on country. |
| 3 | Odoo App Store (product sold to partners and their clients) | On older "newest paid" pages, **88–92% of paid listings have 0 purchases**. |
| 4 | Pax8 (MSP distributor line card) | 155 vendor pages, 16–31 added per year, almost all funded vendors. No newcomer data. Not open to a solo newcomer in practice. |
| 5 | Telarus (technology services distributor) | Roughly 400+ suppliers, mostly telecom/enterprise. No onboarding criteria or newcomer data published. |
| 6 | Tiendanube/Nuvemshop agency programme | Free to join, low entry bar (Silver = 1 store + US$100 GMV). The directory returns HTTP 403, so it could not be measured. |

**Conclusion:**
- The channel with the best *measured* newcomer economics is a **vendor-run implementation directory in a mid-size, non-English market**. In this data that is Shopify in Israel, Poland, Brazil, Mexico and Türkiye. There about 1 in 7 recent entrants gets a steady flow of verified paid jobs within about 2 years. In Germany the figure is about 1 in 30.
- The partner also earns a 4-year annuity: **20% of subscription plus 0.1% of online GMV** on every store it launches (Shopify's official terms since 10 Aug 2026).
- That is the only borrowed-distribution channel here with **positive, measured newcomer evidence**. But it is a services business that leans on the founder's labour. It is close to two ledger exclusions: L3 "operator partner / agency drift" and the Phase 5 "fixed-scope builds via expert directories". I explain below why I think it differs (gated vendor directory, rev-share annuity, measured newcomer flow). The Director may still judge it a repackage.
- Product-side partner channels (the Odoo App Store, MSP distributors, TSDs) show the same "newcomers get ~nothing" pattern as Phases 5–6.

---

## Channel measurements (the core evidence)

### A. Shopify Partner Directory: newcomer outcomes by country

**Method**
- Scraped the public directory location pages and every listed partner's public profile (React-Router stream data, no login). Countries: Israel, Poland, Brazil, Mexico, Türkiye, Germany. n=507, all listed partners in those countries.
- Fields: `partnerSince` (Shopify partner account start), directory `createdAt`, `partnerProgramTier`, `numberOfRatings`, and the dates of the latest 10 reviews.
- So "reviews in the last 12 months" is a lower bound for partners at the 10-review cap.
- [Verified: shopify.com/partners/directory/locations/{country} and /partner/{handle}, accessed 2026-10-13]

**What a review means.** A review requires the merchant to have given the partner collaborator access for more than 1 week and to be on a paid plan. If contact came through the Directory, Shopify sends an automatic review request at 90 days. So a review is a **verified paid client engagement**. It is not necessarily a lead the directory produced; partners can ask any collaborator client for one. [Secondary: Shopify Help Center snippets via WebSearch: partner-directory/how-it-works, manual/partner-directory/hiring-help]

**Listing is gated:**
- "Plus tier is the minimum tier for guaranteed directory eligibility." Plus needs at least US$500k annual revenue to Shopify from referral/co-sell, or at least 2 Plus or 40 Standard shops in 5 years, plus 10 Verified Skills across 3 or more people.
- "A limited number of Registered tier partners are also eligible." [Verified: help.shopify.com/en/partners/grow-your-business/partner-directory/join, 2026-10-13]
- In practice 225 of the 507 listed partners (44%) are Registered tier, so newcomers do get listed. The selection rule for them is [Unknown].

| Country | Listed partners | Live Shopify stores* | Stores per listed partner | Zero reviews (all) | Reviews last 12m (lower bound) | Share of 12m reviews to top 3 | Partners since 2024: n / ≥5 reviews in 12m / ≥10 total |
|---|---|---|---|---|---|---|---|
| Israel | 38 | 12,162 | 320 | 47% | ≥59 | 46% | 5 / 1 / 1 |
| Poland | 40 | 16,656 | 416 | 60% | ≥77 | 39% | 13 / 1 / 2 |
| Brazil | 57 | 30,336 | 532 | 46% | ≥106 | 28% | 16 / 5 / 4 |
| Mexico | 82 | 41,299 | 504 | 39% | ≥138 | 22% | 6 / 0 / 0 |
| Türkiye | 68 | 17,813 | 262 | 44% | ≥167 | 18% | 20 / 2 / 1 |
| Germany | 222 | 102,909 | 464 | 53% | ≥224 | 13% | 29 / 0 / 0 |

\*[Secondary: StoreLeads country pages storeleads.app/reports/shopify/{CC}/top-stores, "updated Oct 9 2026", fetched 2026-10-13]. These are third-party counts.

**Pooled results:**
- Partners since 2024 (n=89): median 0 reviews, 67% zero, 8 with ≥10 lifetime, 9 with ≥5 in the last 12 months.
- Partners since before 2020 (n=155): median 3, 39% zero.
- Registered-tier partners since 2024 (n=55): 34 have zero, 6 have ≥5 in the last 12 months.
- "Since 2024" includes some large agencies that re-registered (dotSource, Jung von Matt), so the true solo-newcomer rate is if anything *lower* in Germany.

**Newcomers who got traction:**

| Partner | Country | Since | Tier | Reviews (last 12m) |
|---|---|---|---|---|
| jands-venancio | BR | 2024-07 | Select | 75 (10 at cap) |
| vex-agency | BR | 2024-11 | Registered | 64 (10) |
| SEDER Studio | IL | 2024-03, listed 2025-05 | Select | 41 (9) |
| mto-management | TR | 2025-07 | Registered | 24 (10) |
| hyper-effekt | PL | 2024-07 | Plus | 21 (10) |
| rafael-almeida2 | BR | 2024-07 | Registered | 20 (10) |

So **a newcomer can reach about 1–6 verified paid jobs a month within about 18–24 months in BR/IL/TR/PL. It has not happened in Germany in this sample.** This is the strongest newcomer evidence for any borrowed channel in Phases 5–7. It still means about 85% of newcomers get little.

**Partner economics.** From 10 Aug 2026 the Launch Partner earns "20% of subscription fee + 0.1% of net eligible online GMV (4-year term)" on all plans except Starter/Lite. GMV excludes B2B and is capped at US$100M a year. Before that date the 20% share was perpetual, with no GMV share. [Verified: help.shopify.com/partners/help-support/faq/earnings, 2026-10-13]

**Listed starting prices** (few partners show one): median US$150 in Israel, $100 in Türkiye, $400 in Mexico, $300 in Germany, $715 in Poland, $1,000 in Brazil. [Verified: directory listing data]

### B. Odoo partner network

**Programme terms:**
- Tiers: Learning / Ready / Silver / Gold.
- Ready needs 10 new Enterprise users a year and 1 certified person.
- Fee: US$2,450 (Learning $490).
- "Commission on Enterprise: up to 20%".
- "Potential leads" are a listed benefit but not for Learning. [Verified: odoo.com/become-a-partner, 2026-10-13]
- Older agreement copies give commission of 10% for Ready, 15% Silver, 20% Gold. [Secondary: search snippets of the Odoo partnership agreement PDF and Viindoo copies]
- Odoo list price: Standard US$16.90–21.10, Custom $32–40 per user per month. [Verified: odoo.com/pricing, IL geo, 2026-10-13]
- So a 10-user Custom client is worth about **$380–480 a year in commission to a Ready partner**. The money is in implementation, which is labour.

**Partner counts and references.** Global: 4,443 partners (Gold 340, Silver 885, Ready 3,218). Customer references per partner, which are cumulative and public: [Verified: odoo.com/partners/country/*, 2026-10-13]

| Country | Partners | Gold refs (median) | Silver refs (median) | Ready refs (median) |
|---|---|---|---|---|
| Israel | 7 | 61 (n=1, Layline) | 52 (n=3) | 10 (n=3: 1, 10, 22) |
| Poland | 20 | 62.5 | 25 | 2 (n=11) |
| Türkiye | 38 | 46.5 | 13.5 | 3 (n=28) |
| Mexico | 165 | 62 | 24 | 8 (n=104) |
| Germany | 105 | 77.5 | 23.5 | 3 (n=69) |
| Brazil | 52 | – | 16 | 1 (n=47) |

**Israel has about 240 published Odoo customer references across 7 partners**, which is real spending. But the Gold partner (Layline) already runs a full Israeli suite: "Israel – E-Invoicing … communicating directly with the israeli tax authority", EZCount digital signatures, Open Format, Unified Report, payroll import. [Verified: laylinetech-treetoscope.odoo.com/website/info, 2026-10-13]

Odoo's own public 19.0 code has only a basic `l10n_il` (chart of accounts and taxes). Poland and Türkiye get e-invoicing modules (KSeF, Nilvera). [Verified: GitHub odoo/odoo addons@19.0 listing and l10n_il manifest, 2026-10-13]

### C. Odoo App Store (products sold into the partner channel)

- About 3,225 pages × 20 paid listings across versions. [Verified: apps.odoo.com browse?order=Newest&price=Paid, 2026-10-13]
- Pages 1–5: 24% of listings have ≥1 purchase. These are mostly established apps re-released for a new version.
- Pages 100–104, 300–304 and 600–604: **8%, 8% and 12% have any purchase; median 0.**
- Only 4 listings mention Israel (downloads: 11, 1, 1, 1).
- This matches Phase 5's CodeCanyon Odoo result (1–16 lifetime sales).

### D. Distributor line cards: Pax8 and Telarus

**Pax8:**
- Claims 47,000+ MSPs and 800,000+ SMBs. [Anecdote/vendor claim: pax8.com vendor page via search, 2026]
- Its public WordPress API lists **155 vendor pages**, created by year: 2022: 63, 2023: 18, 2024: 31, 2025: 27, 2026: 16. [Verified: pax8.com/en-us/wp-json/wp/v2/vendors, X-WP-Total=155, 2026-10-13]
- These are curated vendor pages and may be fewer than the full catalogue.
- Featured vendors are funded companies (Acronis, CrowdStrike, SentinelOne, NinjaOne, Ironscales).
- No onboarding criteria or newcomer vendor results are published.

**Telarus:** "400+ suppliers" (third-party profile); new-supplier PRs such as PolyAI (2025); top supplier is Comcast. No criteria or newcomer data.

**Verdict:** these are line cards for vendors that already have traction. They are not a route to first customers.

### E. Tiendanube/Nuvemshop agencies (LatAm)

- Free programme since May 2026, 5 levels.
- Silver = US$100 GMV + 1 new store with an active plan in the last 12 months. Gold = $75k GMV + 8 stores. Platinum = $750k + 15.
- Commissions are "based on the monthly plan value of the new stores you create". The rate and whether it recurs: [Unknown]. [Verified: ayuda.tiendanube.com/cuales-son-los-nuevos-niveles-del-partners-program-agencies-de-tiendanube, 2026-10-13]
- The partner directory pages return HTTP 403 to scripted access, so newcomer outcomes are not measured.

### F. Not measured (honest gaps)

- **Referral agreements with accountants, lawyers or brokers paying recurring commissions.** No public dataset on what referral partners deliver. The one benchmark search found nothing (logged as WASTED).
- **Bank and insurer SMB marketplaces, and Israeli equivalents.** Not reached within the search cap, and the US-only engine is weak for Hebrew.
- **HubSpot Solutions Directory.** JS-rendered with no public JSON found, so not measured.

---

## Opportunities

### E1. Israeli Shopify "launch partner" studio: Hebrew migrations and builds, plus a rev-share annuity
1. **Concept.** Become a Shopify Partner targeting Israeli merchants moving from Wix, WooCommerce or local platforms to Shopify. Sell fixed-scope packages (migration, Hebrew/RTL theme, Israeli payment and invoicing setup) delivered by contractors. Each store launched earns Shopify's 4-year 20% + 0.1% GMV share.
2. **Customer.** Israeli SMB and D2C merchants. 12,162 live Israeli Shopify stores and 227 Plus stores [Secondary: StoreLeads].
3. **Model.** One-off package US$1.5–5k [Hypothesis; the few listed Israeli starting prices have a median of $150 per service]. Optional monthly care plan. Shopify pays the rev share automatically [Verified].
4. **Spending evidence.** At least 59 verified paid partner engagements reviewed in Israel in the last 12 months across 38 listed partners. One 2024 entrant (SEDER Studio) has 41 reviews, 9 within the last 12 months. [Verified: directory data] Job values: [Unknown].
5. **Competitors.**
   - 38 listed Israeli partners. The top 3 took 46% of recent reviews (SEDER, no-name4, matat). Several are app makers rather than service firms.
   - Many Israeli Wix/WordPress agencies sit outside the directory.
   - What customers dislike: [Unknown]. No complaint data gathered.
6. **Entry strategy.**
   - The supply-side gap is measurable: 320 stores per listed partner and 47% of listed partners with zero reviews.
   - Differentiate with an AI-assisted, fixed-price **migration** product (data, SEO redirects, Hebrew RTL QA), not open-ended builds.
   - This is plausible but **thin** differentiation.
7. **Acquisition.**
   - The Shopify directory: newcomers get flow in about 1 in 7 cases outside Germany, measured above.
   - Listing for a Registered-tier newcomer is discretionary ("limited number"), so first jobs must come from elsewhere: own SEO, Israeli e-commerce Facebook groups [Unknown efficacy].
   - Directory flow only builds after a review base exists.
8. **Ops.**
   - Capital under $1k (Partner account is free; Verified Skills courses are free). Contractors are paid per job.
   - Fully operable from Israel.
   - No platform restriction beyond partner terms. The rev share cannot be split or transferred without consent [Verified].
9. **Labour.**
   - Delivery can be delegated to contractors. Sales calls and QA stay with the founder at first.
   - The annuity grows without hours, but slowly. A Basic store's subscription share is small; the GMV share matters only for stores of roughly $300k+ a year.
10. **Unit economics [Hypothesis].**
    - 20 packages a year × $2.5k × 45% margin is about $22k a year.
    - Annuity after 3 cohorts: about 60 stores × ~$150–400 a year, so $9–24k a year.
    - Owner profit about **$2–3.5k/month at maturity (year 2–3).**
    - Fit: Track A, borderline. Track B: no.
11. **Risks.**
    - Israeli market is small (12k stores, versus Wix's strength locally).
    - Directory listing may be refused.
    - Agency drift (ledger L3) and the founder's dislike of service work.
    - The Phase 5 exclusion "fixed-scope builds via expert directories". It differs because this is a vendor-gated directory with measured newcomer review flow and a vendor-paid annuity, not an open freelance marketplace.
    - Shopify cut the perpetual share to 4 years in 2026 and may cut it again.

### E2. Operator-led Shopify partner in Türkiye or Brazil (founder as systems owner, local lead as face)
1. **Concept.** Same productised migration/launch model as E1, in a larger non-English market where measured newcomer flow is best. Brazil: 5 of 16 partners who joined in 2024 or later have ≥5 reviews in the last 12 months. A local, revenue-sharing operator handles sales and client contact. The founder supplies an AI-assisted delivery pipeline and manages contractors.
2. **Customer.** Brazilian merchants (30,336 live stores, 431 Plus) or Turkish merchants (17,813, 205 Plus) [Secondary: StoreLeads].
3. **Model.** Packages; Brazil listed starting-price median US$1,000, Türkiye $100 [Verified listing data]. Plus Shopify rev share.
4. **Spending evidence.** At least 106 (BR) and at least 167 (TR) verified paid engagements reviewed in the last 12 months. Top-3 concentration is only 28% (BR) and 18% (TR), so flow is more evenly spread than in Israel or Germany.
5. **Competitors.**
   - Brazil: 57 listed partners. Shopify also competes with Nuvemshop/VTEX, so Shopify-specialist supply may be thinner.
   - Türkiye: 68 listed partners, with low listed prices that suggest price pressure.
   - What customers dislike: [Unknown].
6. **Entry.** Language-local delivery at Brazilian prices, with founder-built migration tooling as the cost advantage. Credible only with a native operator; otherwise "none credible" for this founder alone.
7. **Acquisition.** Directory flow (measured), after first reviews. First reviews could come from the operator's network [Unknown].
8. **Ops.**
   - Capital $1–2k.
   - The operator's share (30–50%) cuts margin.
   - Brazil: invoicing (NF-e) and contracts need a local entity or the operator's entity [Unknown cost].
   - Türkiye: currency volatility.
   - Israeli founder working with a Turkish partner: possible political and payment friction [Hypothesis].
9. **Labour.** More delegated than E1, but needs partner management.
10. **Unit economics [Hypothesis].** Owner share about $1–3k/month by year 2. Track A at best.
11. **Risks.**
    - Finding a trustworthy operator; the operator may later take the clients.
    - The review flow may reflect agency incumbency (several newcomers may be re-registered firms).
    - Weak FX.

### E3. Tiendanube/Nuvemshop agency partner (LatAm alternative channel)
1. **Concept.** Same productised launch/migration offer on LatAm's local leader, where joining is free and Silver takes 1 store.
2. **Customer.** LatAm SMB merchants.
3. **Model.** Packages plus the platform's level-based commission on plan value. Rate and duration: [Unknown].
4. **Spending evidence.** Programme rules [Verified]. No transaction data. The directory is blocked (403).
5. **Competitors.** [Unknown].
6. **Entry.** As E2. Needs Spanish/Portuguese delivery.
7. **Acquisition.** Whether Tiendanube passes leads to agencies: [Unknown]. Not measured.
8. **Ops.** As E2.
9. **Labour.** As E2.
10. **Economics.** [Unknown]; Track A at most.
11. **Risks.** The whole channel is unmeasured. Keep it only as a comparator to E2.

### E4. Odoo Ready partner with a vertical package (Türkiye or Israel)
1. **Concept.** Become an Odoo Ready partner and sell a fixed-scope vertical bundle (for example wholesale/distribution with inventory and Israeli or Turkish e-invoicing) using contractors. Earn implementation fees, the 10% licence commission and hosting/support retainers.
2. **Customer.** SMEs with 5–50 users.
3. **Model.**
   - Implementation $5–20k [Hypothesis].
   - Commission about $380–480 a year per 10-user client [derived from Verified pricing and the commission].
   - Partner fee $2,450 a year.
4. **Spending evidence.** About 240 published Odoo references in Israel; 4,443 partners worldwide [Verified].
5. **Competitors.** Israel: Layline (Gold, 61 references) already offers full Israeli compliance; 3 Silver partners hold 37–55 references each. Türkiye: 38 partners, Gold 39–56 references.
6. **Entry.** Israel: none credible against Layline's compliance suite unless a vertical is unserved [Unknown]. Türkiye: language barrier.
7. **Acquisition.** Odoo "potential leads" for paying tiers; the volume per Ready partner is [Unknown]. Measured outcome: Ready partners' median lifetime references are 1–10.
8. **Ops.** $2,450 fee; certification needed; projects carry implementation liability.
9. **Labour.** High; ERP projects are consulting-heavy.
10. **Economics [Hypothesis].** A Ready partner with 5 projects a year makes roughly $2–4k a month, mostly from labour. Track A only, and labour-bound.
11. **Risks.** Scope creep, retention penalties, and a commission too small to matter.

### E5. MSP-distributed micro-SaaS via Pax8 (or a TSD line card)
1. **Concept.** A narrow security/compliance tool for MSPs, distributed on Pax8 so 47k MSPs can resell it.
2. **Customer.** MSPs (US/UK/EU/ANZ).
3. **Model.** Per-seat monthly, billed through the distributor.
4. **Spending evidence.** Distributor scale claims only [vendor claims]. No vendor-level sales data.
5. **Competitors.** Funded security vendors already on the line card.
6. **Entry.** None credible for a newcomer without MSP traction. The line card adds only 16–31 vendor pages a year [Verified count].
7. **Acquisition.** Unmeasured. Distributors add vendors after MSP demand exists.
8. **Ops.** Security/compliance liability; SOC 2 expectations [Hypothesis].
9. **Labour.** Product-scalable if adopted.
10. **Economics.** [Unknown].
11. **Risks.** The channel won't accept a vendor without traction, and MSP direct sales are slow.

---

## Killed ideas and why

- **Odoo App Store modules sold to partners.** 88–92% of paid listings have 0 purchases (measured), matching Phase 5 CodeCanyon.
- **Israeli Odoo compliance module.** Layline's Gold suite already covers ITA e-invoicing, EZCount, Open Format and Unified Report (verified). Phase 1 also excluded allocation-number tools.
- **TSD (Telarus/Avant) supplier.** Enterprise telecom line card; no newcomer data; no published entry path.
- **Buying books of Shopify rev-share stores.** Rev share "can't be split" and Launch Partner status can't be transferred without Shopify's prior written consent (verified).
- **Accountant/broker recurring-referral distribution.** No public data on what such partners deliver. Phase 2 (UK MTD via accountants) already scored weak on distribution. Without data it fails the Phase 5 rule.
- **Shopify partner in Germany.** 0 of 29 partners joined since 2024 have ≥5 reviews in the last 12 months; the market is saturated.
- **Bank/insurer SMB marketplaces.** Not measured within the budget. Their vendor admission typically favours established vendors [Hypothesis]. Pass to Agent A/C if they cover it.

## Ranking (Agent E)

| Rank | Idea | Assessment |
|---|---|---|
| 1 | **E1** Israeli Shopify launch/migration partner | The only borrowed channel with positive measured newcomer evidence in the founder's home market; low capital; Track A borderline |
| 2 | **E2** Operator-led Shopify partner in Brazil/Türkiye | Best measured newcomer odds (BR 5 of 16), but depends on an operator |
| 3 | **E4** Odoo Ready vertical partner | Real spending, but labour-bound, and Israel is held by Layline |
| 4 | **E3** Tiendanube agencies | Unmeasured |
| 5 | **E5** Pax8 MSP SaaS | Gatekept |

**Cross-cutting finding for the Director:**
- Partner and directory channels behave like marketplaces, but with a gate.
- Newcomers who get in see a long tail of zero: about 2/3 have no verified job after 1–2 years.
- About 10–15% achieve steady flow in mid-size non-English markets, versus about 0% in saturated markets (Germany).
- Product-side channels into partners (app stores, distributors) look worse than service-side ones.
- Borrowed distribution is real, but only for **services-shaped** offers and only in **less-saturated markets**. That conflicts with the founder's wish to avoid selling hours.

## Top candidates for deep diligence and the decisive unverified assumption

| Idea | Decisive unverified assumption |
|---|---|
| **E1** | A new Registered-tier Israeli partner gets a directory listing and reaches about 2 or more paid jobs a month at ≥US$2k average within 12 months. That needs: (a) Shopify's Registered-tier selection rule; (b) Israeli job values (only 7 of 38 Israeli partners list prices); (c) whether SEDER-type newcomers had prior client books. |
| **E2** | A reliable Brazilian or Turkish operator can be engaged on revenue share. Brazil's 2024 newcomer success (5 of 16) also has to reflect new firms, not re-registered agencies. Check `partnerSince` against company founding dates for the 9 successful newcomers. |
| **E4** | Odoo routes enough "potential leads" to a Ready partner to beat a median of 1–10 lifetime references. Per-partner lead volume is undisclosed. |

**WebSearch count: 8 / 8.**

### Sources (accessed 2026-10-13)
- https://www.shopify.com/partners/directory/locations/{israel,poland,brazil,mexico,turkey,germany} and /partners/directory/partner/{handle} (scraped; data in scratchpad `P7-E/data/*_prof.json`)
- https://help.shopify.com/partners/help-support/faq/earnings · https://help.shopify.com/en/partners/grow-your-business/partner-directory/join
- https://storeleads.app/reports/shopify/{IL,TR,PL,BR,MX,DE}/top-stores
- https://www.odoo.com/partners/country/{israel-100,poland-173,turkiye-215,mexico-150,germany-56,brazil-29} · https://www.odoo.com/become-a-partner · https://www.odoo.com/pricing · https://apps.odoo.com/apps/modules/browse?order=Newest&price=Paid · https://laylinetech-treetoscope.odoo.com/website/info · https://api.github.com/repos/odoo/odoo/contents/addons?ref=19.0
- https://www.pax8.com/en-us/wp-json/wp/v2/vendors · https://www.pax8.com/en-us/vendors/
- https://ayuda.tiendanube.com/cuales-son-los-nuevos-niveles-del-partners-program-agencies-de-tiendanube
