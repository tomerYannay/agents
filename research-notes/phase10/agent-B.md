# Phase 10 — Discovery Agent B (Physical): high-ticket physical goods through paid search or social

Agent P10-B · 2026-10-13 · WebSearch 6 of 6 (logged as P10-B) · Scratch: `scratchpad/p6plus/P10-B/` (scripts/ and data/)

## 0. Bottom line
- **Survivors in this model are steady, but they make Track A money, not Track B.** I pulled the full Empire Flippers public API today: 2,878 listings, 29 pages. Fourteen young US-supplier, high-ticket dealer/dropship stores had monthly P&Ls:
  - median profit **$4.5k/month** at a **10.5% net margin**;
  - median 9 owner hours a week;
  - median 19.5 months from first revenue to listing;
  - 8 of 14 had at least one loss month in their last 12.
- **Paid search alone does not survive copying.**
  - Under MAP, every dealer sells the same SKU at the same price, so Google bidding is the only lever.
  - The survivors that were mostly paid-search-led ran at **5–10% margins**: #67576 (71% paid traffic, 5%), #57358 (74%, 10%), #69490 (71%, 10%).
  - The better-margin survivors were organic-led: #87595 29%, #85563 18%, #81079 13% with 82% organic.
  - Followers bidding on the same terms push CPC toward each dealer's per-order contribution.
- **The model is already crowded at the newcomer end.**
  - Trustpilot's US "Sauna Store" category alone lists **74 companies**. About 34 of them have ≤12 reviews, and 14 show no review count.
  - Multi-brand dealers founded recently look like this: Topture (founded 2021) has 463 reviews.
  - Course sellers still push the model in 2026.
- **Distribution evidence is thin.**
  - Google Ads Transparency Center and Meta Ad Library were **unreadable**: JavaScript shell and socket hang-up. Nothing was bypassed.
  - No newcomer success rate exists. The only measurements are survivor P&Ls and category long tails.
- **Net:** nothing here beats the Phase 9 leaders. My best is **B10-1, a quote-led B2B equipment dealer desk**. It fits Track A at best and is defensible only through organic/SEO and repeat B2B buyers, not through paid search. **B10-2, own-brand factory-direct high-ticket**, is the only route with Track B evidence (#88863: $58k/month). But it carries tariff, returns and creative risk, and has no newcomer data.

## 1. Data: Empire Flippers high-ticket physical cohort [Verified: api.empireflippers.com/api/v1/listings/list, pulled 2026-10-13, 2,878 listings]

### Method
- I took listings monetised as DropShipping or eCommerce, excluding FBA, whose first revenue came in 2021 or later. That gave 66 listings.
- From those, I hand-selected the ones whose summaries say "high-ticket", "authorized dealer", AOV ≥ $1,000, or US-based suppliers.
- Scripts: `P10-B/scripts/f1–f4.py`. Data: `P10-B/data/cohort.txt`.

### A. US-supplier authorised-dealer dropship stores (consumer and B2B)
| # | Niche | First revenue | Profit/mo | Margin | Owner h/wk | Traffic | Last-12-mo range | Sale price |
|---|---|---|---|---|---|---|---|---|
| 81079 | B2B hospitality equipment, AOV $2,649, 18 US suppliers | 2023 | $1,174 | 13% | 1 | 82% organic, Google Ads TACoS 12% | −$768 to $3,963 | $32.9k |
| 87595 | Niche electronic equipment, AOV ~$3,000, China factory, own label | 2023-09 | $1,734 | 29% | 1 | organic SEO only | −$113 to $5,745 (Jan–Feb 2026 ≈ $0) | $38.1k |
| 74833 | Elderly/mobility, AOV $1,353, 31 suppliers | 2023-03 | $3,613 | 15% | 5 (two partners, 8 h combined) | 38% organic, Google Ads TACoS 11%, CVR **0.25%** | −$2,506 to $9,662 | $115.6k |
| 79333 | Kitchen appliances / outdoor, VA | 2023-02 | $5,916 | 15% | 15 | — | $2,698 to $15,878 | $159.7k |
| 79158 | Survival/security, "authorized dealer", 27 suppliers | 2023-01 | $4,038 | 8% | 10 + 1 employee | 66% organic (fell Apr 2024) | $1.2k to $10.4k | $113.1k |
| 67576 | Bedroom high-ticket, 30 suppliers, 4 staff | 2021-08 | $6,146 | **5%** | 10 | **71% paid search** | $0.5k to $13.4k | $215.1k |
| 69750 | Water-feature equipment, quotes, 10 suppliers | 2021 | $9,272 | 9% | 8 | 48% organic, 12% paid | −$2.9k to $24.2k | $296.7k |
| 57358 | Beverage cooling, 20 suppliers, 2 staff | 2019 | $5,129 | 10% | 4 | **74% paid search** | $1.2k to $15.4k | $164.1k |
| 69490 | Garden/outdoor living, 9 suppliers | 2022-05 | $3,545 | 10% | 3 | **71% paid search** | −$4.6k to $14.5k | $109.9k |
| 80396 | Outdoor/sports, 40k SKUs, 5 suppliers | 2022 | $5,576 | 8% | 20 | — | $1.1k to $11.3k | $161.7k |
| 74319 | Home/kitchen/fitness | 2022-01 | $4,284 | 10% | 2 | 100% organic after stopping Google Ads | $0.7k to $7.6k | $129.1k |
| 85563 | Bidets/Japanese brands | 2021-08 | $6,260 | 18% | 10 | organic brand-keyword rankings | −$268 to $15.7k | $165.0k |
| 80170 | Roof tents | 2021-04 | $4,777 | 13% | 15 | 82% organic | −$575 to $11.1k (declining) | $114.6k |
| 87021 | Premium audio, hybrid stock | 2023-10 | $2,366 | 11% | 15 + 2 staff | organic | −$416 to $6.0k | $35.5k |

**Cohort statistics (n=14, survivors only, no denominator):**
- median profit $4,530/month;
- median margin **10.5%**;
- median 9 owner hours a week;
- 8 of 14 had a loss month in the last 12;
- median 19.5 months from first revenue to listing.

**Wider check (n=50).** Across all EF dropship listings mentioning US suppliers or high-ticket, from any year: median $3,984/month, IQR $1,971–8,470; median margin 12.5%, IQR 10–20%; median 5 h/week.

**Listing flow.** Listings fitting this description peaked in 2018 (11) and 2021 (11), then fell to 3–7 a year. All dropship listings on EF went 29 (2018) → 3 (2022) → 13 (2024) → 7 (2025) → 10 (2026 to date). These are survivor sale flows, not a newcomer rate.

### B. China-factory-direct, own-label or own-catalogue high-AOV stores (no dealer approval or MAP)
| # | Niche | First revenue | Profit/mo | Margin | Owner h/wk | Acquisition | Status |
|---|---|---|---|---|---|---|---|
| **88863** | Customisable designer lighting, 8–10 China suppliers | 2022-09 | **$58,192** (Jul 2025–Jun 2026 range $16k–$113k) | 18% | 6 + 3 Philippine VAs (50 h) | paid (TACoS 30%), "low CAC", Trustpilot | For sale, $1.98M |
| 95128 | Ergonomic furniture, fitness, massage; mostly China | 2024-07 | $9,421 (rising: $0.5k Oct 2025 → $16k Jul 2026) | 18% | **20** | **Google Ads, TACoS 46%** | For sale, $305k |
| 87595 | (see table A) | | | | | | |
| 88274 | High-ticket recovery (inventory, 3PL, China suppliers) | 2023-08 | $75.7k avg; swings **−$120.5k to +$321k** | 24% | 20 + contractors | Meta-led, TACoS 25% | Pending sold, $2.88M; inventory-heavy, out of budget |

### C. Wholesale-plus-retail catalogue dropship (mid-AOV)
- **#95869**: furniture and home goods; 16,000 SKUs; AutoDS; one VA; 30 min/day.
  - Profit **$30.8k/month** at 25%.
  - Faire (B2B) plus Shopify; "Google Top Quality Store".
  - Chargebacks under 2%. Returns use supplier prepaid labels.
  - Meta and Shopping are "minimally" used.
- This is not $1,500+ AOV, and its channel is a marketplace, Faire. I note it as context only.

**Reading.**
- High-ticket dealer stores are a real, repeatable **$1–9k/month** survivor outcome.
- They achieve it with low net margins (8–15%), several months of volatility, and 1–2 years of build.
- The few Track B cases are own-catalogue or own-brand, not authorised-dealer (#88863, #88274). They run on paid acquisition with creative and pricing control that MAP-bound dealers lack.

## 2. Channel, terms, returns and density evidence

### Paid-search benchmarks [Secondary: vendor compilations]
**Shopping campaigns.** Foundry CRO "Google Shopping Benchmarks by Category 2026" [Verified page, 2026-04-30; aggregates Store Growers, Triple Whale, LocaliQ, Echelonn; no sample sizes]:

| Category | CPC | CVR | CPA | ROAS | Break-even ROAS |
|---|---|---|---|---|---|
| Industrial/B2B | $1.50 | 1.2% | $125 | 2.0× | 2.86–5.0× |
| Home & Garden | $1.05 | 2.9% | — | 4.5× | — |
| Electronics | $1.42 | 1.8% | — | 3.8× | 3.3–5.0× |

- In this compilation, Industrial/B2B's **average ROAS is below its break-even range**.
- These figures are for typical-AOV goods. #74833 measured a **0.25% CVR** at AOV $1,353 [Verified-EF].

**Cost trend.** Channable data via PPC Land [Verified page, 2026-07-12], covering 10,000+ EU advertisers and €1.38B of spend, June 2025 → June 2026:
- CPC up 15%;
- Performance Max ROAS down 46%;
- Standard Shopping ROAS down 43%.

So the cost trend runs against newcomers.

**Advertiser density.**
- Google Ads Transparency Center returned only a JavaScript shell (Hebrew UI, no data).
- Meta Ad Library returned a socket hang-up.
- **Not measured; not bypassed.** Density proxies used instead are in "Category density" below.

### Dealer and dropship programme terms [Verified pages, 2026-10-13]
- **Currey & Company** (lighting/furniture), e-commerce dealer policy effective 2024-10-21:
  - Approval is at "sole and absolute discretion".
  - The applicant must submit its domains, or a **staging site** if not live.
  - Unapproved marketing is treated as a DMCA violation.
  - IMAP bans coupons, "see price in cart" and "click for price".
  - **Google Ads count as real-time pricing.**
  - A violation not cured within 24 hours can mean cancelled orders, suspension or termination "at any time … for any reason".
- **etúHOME** dropship terms:
  - Tax ID plus resale number; must be in the continental US.
  - MAP = its own site price, after promotions.
  - **Orders prepaid by card at submission; final sale.**
  - **No dropship returns accepted**: the reseller receives returns.
  - Damage claims must be filed within 48 hours with BOL notes and photos. Transit damage is "not responsible".
- **SHAD USA**: dropship programme for online retailers at **$5 per order**; margin from 35% off MSRP; **MAP = MSRP** enforced.
- **Hellbend** (jotform dealer application):
  - Tax ID and seller permit required.
  - Marketplaces (Amazon, eBay, Walmart) are banned; own-domain store only.
  - Discounts are capped at 15% below MSRP; MAP breach means immediate termination.
- **PullRite** (rv-pro.com, 2019): distributors may dropship only for **registered** e-commerce retailers. This is how dropship-from-distributor is gated, brand by brand.
- **Feniex** ($10 per dropship order, US only) and **Meadow Creek** (MAP = MSRP) appear only as [Secondary: search snippet].

**Implications.**
1. Dealer margin is fixed by MAP. Gross margin is about 25–35% off MSRP before freight and fees; EF cohort COGS of 70–86% matches.
2. Price cannot be used to win. Followers and incumbents sell at the identical advertised price.
3. Dropship returns and freight damage land on the store.
4. Supplier payment is upfront, while customer funds can be held.

### Payment holds [Verified: help.shopify.com reserves page, 2026-10-13]
- Shopify Payments can impose a fixed reserve (e.g. $1,000 for 120 days) or a percentage reserve (e.g. 10% for 120 days).
- Listed triggers include elevated chargebacks, a higher refund rate, extended delivery timelines and **"significant volume surges"**.
- Higher reserves and payout delays of 5–20 business days for new or high-risk accounts are [Secondary: blogs, unverified].
- A first $2,000 order paid to the supplier upfront, with any reserve or hold on the customer's payment, ties up most of a $2k budget.

### Returns and chargebacks
- **#95869 reports chargebacks under 2%**, called "notable for a 100% dropshipping model" [Verified-EF]. That is above the roughly 1% level where Shopify is said to start flagging accounts [Secondary].
- I found no LTL freight-damage rate [Unknown].
- #87021 sends returns to a consignment partner. #80396 shows back-order accounting distortions [Verified-EF].

### Category density and newcomer tail [Verified: trustpilot.com/categories/sauna_store?country=US, pages 1, 3 and 4, 2026-10-13]
- **74 companies** in US "Sauna Store".
- Leaders: Clearlight 1,697 reviews, OutletSpas 1,487, AquaRest 1,281, SaunaKits 638.
- Page 3 entrants have 2–12 reviews each (Rocky Mountain Saunas 6, Urban Sauna 5, Warrior Saunas 2, Saunny 2, …).
- Page 4 has 14 companies with no review count shown (Sauna Republic, Wyldsauna, Saunass, Dynamicsaunasdirect, Sauna and Plunge Direct …).
- The "Hot Tub Store" category has 83 companies.
- Topture, a multi-brand authorised sauna retailer **founded 2021**, shows 463 reviews [Verified: topture.com brand-facts page]. That is one visible newcomer survivor among dozens of 0–12-review entrants.
- Course sellers continue to promote "high-ticket dropshipping" in 2026: an ecommerceparadise podcast episode of 2026-04-10, plus trendtrack and omnisend blogs [Secondary: search results].

## 3. Opportunities

### B10-1. Quote-led B2B equipment dealer desk (US), long-tail search plus phone and quote, with organic/SEO as the profit engine
*Materially different from B8-4 (US consumer dealer) and C4 (factory-direct outside the US). Here the buyer is a US business, and the sales mechanism is quote, phone and repeat purchase, not Shopping-feed retail. Strongest comparables: #81079, #69750, #87595.*

1. **Concept.**
   - One niche of commercial equipment at $1.5–10k per order, sold as an authorised online dealer of 10–30 US brands or distributors that offer dropship.
   - Candidate niches [Hypothesis]: hospitality/bar equipment outside Webstaurant's core, salon/spa equipment, veterinary/clinic furniture, commercial water features, food-truck fit-out, lab benchtop.
   - Spec-heavy pages generated from manufacturer PDFs, a "request a quote" flow, net-terms partners, and a VA phone desk.
2. **Customer and geography.** US small businesses: restaurants, salons, clinics, contractors.
3. **Model and price.** One-off orders at AOV $1.5–3k. Repeat rates were 15% (#81079) and 33% (#87595).
4. **Spending evidence** [Verified-EF]:
   - #81079: AOV $2,649; $9k revenue/month; 18 suppliers; 1 h/week.
   - #69750: equipment quotes; $9.3k/month profit at a 9% margin.
   - #87595: $3,000 AOV; 29% margin.
5. **Competitors.** WebstaurantStore, KaTom, Global Industrial, Amazon Business, brand-direct sites and local dealers.
   - What buyers dislike [Hypothesis]: generic catalogues with no spec help, no quote or bundling for fit-outs, slow freight answers.
6. **Entry strategy.**
   - A narrow niche where the big catalogues are thin.
   - Spec and compatibility content that AI can produce at catalogue scale, which uses the founder's edge.
   - Fast quote turnaround.
   - This is credible but not unique. A follower can copy it in about 6 months; only accumulated rankings and repeat accounts persist.
7. **Acquisition.**
   - Google Search on model-number and spec long-tail plus Shopping. In the cohort, organic was 48–82% of traffic for the margin-healthy stores.
   - Newcomer CAC [Unknown].
   - Vendor Industrial/B2B Shopping benchmark: CPC $1.50, CVR 1.2%, CPA $125, ROAS 2.0× (below break-even). At high AOV, CVR is more likely 0.25–1% (#74833) → **CAC $150–600 per order** [Hypothesis from cited figures].
   - Advertiser density: Transparency Center unreadable.
8. **Capital and operations.**
   - US LLC, EIN and resale certificates: about $300–800 [Secondary, P8].
   - Shopify plus a staging store for dealer review (Currey requires one).
   - Supplier prepay on card, with Shopify reserve and hold risk. This is a working-capital float problem from the first order.
   - LTL freight and damage claims within 48 hours (etúHOME).
   - Sales-tax registration once economic nexus is reached.
   - Israel-operable with a US-hours VA. Dealer approval for a foreign-owned new store is unmeasured.
9. **Labour.** Cohort owners work 1–15 h/week, plus a VA or employees. Quote and phone work is delegable. Revenue can grow faster than hours, as #81079 (1 h/week) and #57358 (4 h/week) show.
10. **Unit economics** [Hypothesis built from verified inputs]. Per $2,000 order:
    - Gross margin 25%: $500.
    - Payment fee about 3%: $60.
    - Freight/damage/returns reserve about 3%: $60.
    - Contribution before ads: **≈$380**.
    - Paid CAC of $150–600 means about $0 to +$230 per paid order.
    - **When 3 followers bid on the same SKUs at MAP-identical prices**, CPC rises until marginal CAC nears the $380 contribution. Paid orders then go to about break-even, which matches the 5–10% margins of the paid-led EF survivors.
    - Owner profit therefore depends on organic share and repeat B2B accounts. At the cohort median ($4.5k/month at 10.5%), that means about $43k/month revenue, roughly 21 orders/month at $2k.
    - **Track A** reached after about 12–24 months (cohort median 19.5 months to listing). **Track B**: no dealer-model evidence.
11. **Risks and kill conditions.**
    - Dealer refusals.
    - Google's 2026 cost trend (CPC +15%, ROAS −43–46% in the EU).
    - Freight damage and chargebacks on $2k+ tickets.
    - SEO volatility (#79158 organic fell in April 2024; #80170 declining).
    - The followers argument above.
    - Supplier price or terms changes.

### B10-2. Own-label, factory-direct, customisable high-AOV catalogue (US buyers), Google Ads with Meta retargeting
*Different from N5 (EU, Meta, hero product, local language) and B8-4 (dealer under MAP). Here the store controls price and catalogue, buyers are in the US, and the product is customisable high-AOV goods. Comparables: #88863, #95128, #87595.*

1. **Concept.** A curated catalogue of customisable lighting, ergonomic furniture or niche equipment, shipped by 5–10 vetted Chinese or Turkish factories under the store's own label. The founder builds the product-configurator, catalogue and imagery pipeline. #95869 already uses an AI bulk-imaging system.
2. **Customer.** US homeowners and designers; for #87595, B2B buyers.
3. **Model.** AOV of several hundred to $3,000+ [Verified for #87595; #88863 and #95128 AOV not stated].
4. **Spending evidence** [Verified-EF]:
   - **#88863: $58.2k/month profit**, 18% margin, TACoS 30%, 3 VAs, 6 owner h/week, from September 2022.
   - #95128: $9.4k/month, TACoS 46%, 20 h/week, growing.
   - #87595: $1.7k/month, organic.
5. **Competitors.** Wayfair, Amazon, other factory-catalogue dropshippers sourcing the same catalogues, and brand DTC sites. Buyers dislike long shipping times and return friction [Hypothesis].
6. **Entry strategy.**
   - Customisation (the #88863 wedge), sample-verified quality and US-warehoused fast-ship SKUs.
   - Founder software for configurators and catalogue imaging.
   - **Copy risk is high**: the same factories sell to anyone.
7. **Acquisition.**
   - Paid Google and Meta: TACoS 30–46% in the comparables. The margin survives only because of own-price control (COGS 12% at #88863, 37% at #95128).
   - Newcomer outcomes [Unknown]. Density not measured (ad libraries unreadable).
8. **Capital and operations.**
   - Samples about $300–800; ads about $1k.
   - The real tariff burden on Chinese goods into the US in 2026 is [Unknown, not verified this phase].
   - Cross-border returns of large items are costly. #88863 relies on "trusted logistics agents".
   - Payment-hold risk from long delivery times (a listed Shopify reserve trigger).
   - Israel-operable.
9. **Labour.** Delegable to VAs (#88863: 3 VAs, 50 h/week combined; owner 6 h/week).
10. **Unit economics** [Hypothesis].
    - With COGS 30–40% and TACoS 30–45%, plus fees, freight and returns of about 10%, contribution is **10–20%**, which matches the 18% at #88863 and #95128.
    - **Under copying**: a follower can buy the same factory SKU, so price competition is possible here, unlike under MAP. CPC rises and the price floor drops. Only customisation and reviews hold up.
    - **Track B shown once** (#88863). Track A at #95128.
11. **Risks.**
    - Tariffs and customs.
    - Quality and returns from abroad.
    - Payment reserves on long delivery times.
    - A $2k budget buys about one catalogue test.
    - Creative and ads skill the founder lacks (Phase 8 red-team point on N5 applies).

### B10-3. US consumer authorised-dealer high-ticket store (B8-4 re-measured, not a new idea)
- **New measurements:**
  - Cohort A median $4.5k/month at a 10.5% margin.
  - **Paid-search-led stores run at 5–10% margins.**
  - Sauna/spa niches hold 74–83 companies per Trustpilot category, with a long 0–12-review tail.
  - Dealer terms forbid price competition (Currey IMAP covers Google Ads; MAP = MSRP at SHAD and Meadow Creek).
- **Verdict.** It confirms the Phase 8 kill for this founder. Track A ceiling, no edge in the paid channel, course-driven saturation.
- Keep it as a fallback only if B10-1's niche has no B2B angle.

### B10-4. Dropship from a distributor into a non-US market (C4 re-measured; UK/AU/EU)
- Channable shows EU CPCs up 15% year on year, with Czech Republic up 34.8% and Hungary up 42.1%, and Shopping ROAS down 43% [Verified page].
- EU and UK VAT, GPSR and CE place importer obligations on the store unless a local distributor dropships [Phase 8 Hypothesis, not re-verified].
- No young EF comparable outside the US in the high-ticket dealer set. #86090 (France, premium baby gear, organic, $2.9k/month, 30% margin) is the only one.
- **Verdict: weak.** One survivor, organic-led, no paid evidence.

### Killed or not proposed
- **Buying a young EF dealer store.** The cheapest are #81079 at $32.9k and #87021 at $35.5k, 16–18× the budget. This also falls under ledger exclusions such as "buying offline businesses with seller financing". Killed on capital.
- **Inventory-carrying high-ticket brands (#88274).** P&L swings from −$120k to +$321k a month, with stock and a 3PL. Killed on capital.
- **Pure Google Shopping arbitrage on MAP-bound brand SKUs.** Under followers this converges to break-even (see B10-1 economics; cohort paid-led margins of 5–10%). Not a standalone business.
- **Faire wholesale catalogue dropship (#95869).** Strong P&L ($30.8k/month), but not high-ticket and marketplace-led. Also near the ledger's "Faire wholesale agency" exclusion. Noted only.
- **Telehealth or compounded-GLP-1 "dropship" (#96575).** Regulatory exclusion, as in Phase 8.

## 4. Cheapest real-world tests (describe only; not run)

### B10-1 test, about $1.8k
**Steps:**
1. Desk: pick one niche and list 30 brands. Record how many publish an online-dealer or dropship programme, MAP, and returns terms. **Kill if fewer than 10 have dropship plus online-dealer terms.**
2. US LLC, EIN and resale certificate: about $500. Staging Shopify store with spec content: about $100.
3. Apply to 15 brands or distributors. **Kill if fewer than 4 approve within 6 weeks**, or if the approved catalogues lack the niche's core SKUs.
4. $1,000 Google Search on model-number and spec long-tail with a call extension and a quote form, about 600–700 clicks at $1.50.

**Kill thresholds:**
- Fewer than 2 orders **and** fewer than 6 qualified quote requests (business buyer, budget ≥ $1.5k).
- Or blended CAC above 60% of order contribution (about $230 per order at $380).

**Caveat:** at 0.25–1% CVR, $1k yields about 2–6 orders. The test detects only gross failure, not profitability.

### B10-2 test, about $1.8k
**Steps:**
1. Order samples from 3 factories for one customisable product line (about $600).
2. Run a store with configurator and $1,000 of Google plus Meta retargeting.

**Kill thresholds:**
- Fewer than 3 orders.
- Or TACoS above 45% at a 35% COGS.
- Or any factory returns or defect rate above 10% on the first 10 orders.

**Desk prerequisite:** verify the current US tariff rate for the HS code. **Kill if landed cost exceeds 45% of target price.**

## 5. Ranking, deep-diligence picks and decisive assumptions
| Rank | Idea | Why | Decisive unverified assumption |
|---|---|---|---|
| 1 | **B10-1 B2B equipment quote desk** | 14-store survivor cohort with stable Track A, low hours and delegable operations; the B2B repeat and quote mechanism is less copyable than retail Shopping | A foreign-owned new store gets ≥4 dealer or distributor dropship approvals in one niche, and reaches ≥40% non-paid order share within 12 months |
| 2 | **B10-2 Own-label factory-direct customisable catalogue** | Only Track B evidence (#88863 at $58k/month); price control avoids the MAP trap | Landed cost after 2026 US tariffs plus cross-border returns leaves ≥15% contribution at TACoS 30–45%, and a newcomer reaches TACoS ≤45% on a $1k test |
| 3 | B10-3 US consumer dealer store (B8-4) | Re-measured: repeatable but crowded | Same as Phase 8; now also contradicted on paid margins |
| 4 | B10-4 Non-US distributor dropship (C4) | Weak: one survivor, rising EU CPC | Local distributors dropship to a foreign-owned store |

**Honest assessment for the Director.**
- High-ticket physical goods match the "price per account" trait but not the "paid channel survives copying" requirement.
- Under MAP, paid search is a commodity auction. The survivors earn from organic rankings and repeat buyers, built over about 1.5–2 years.
- I would score B10-1 below the Phase 9 leaders. Proven-channel evidence is survivor-only, and copying compresses paid margins to about 5–10%.
- B10-2 carries tail upside but has the Phase 8 N5 fit problems (ads and creative skill, capital float).

**Search count: 6 of 6.** All logged as P10-B in `research-notes/search-log.txt`.

**Primary pages fetched:**
- EF API, 29 pages;
- Foundry CRO benchmarks; PPC Land (Channable);
- Currey e-commerce policy; etúHOME dropship terms; SHAD wholesale programmes; Hellbend dealer form; PullRite (rv-pro);
- Shopify Help reserves page;
- Topture brand facts;
- Trustpilot Sauna Store pages 1, 3 and 4.

**Blocked or unreadable:** Google Ads Transparency Center (JavaScript shell), Meta Ad Library (socket hang-up), Almost Heaven dealer locator (404), Trustpilot restaurant-equipment category (404).
