# Phase 6 — Discovery Agent F (Contrarian / non-obvious / emerging)

Assignment: (1) acquiring under-monetised digital assets ($2k–$50k) on public deal marketplaces; (2) licensing or white-labelling proven foreign products into under-served languages or geographies; (3) a small number of 2025–2026 structural shifts that create new direct-sale demand.
WebSearch used: **8 / 8** (all logged as P6-F). Most evidence comes from WebFetch and public JSON APIs: the Empire Flippers listings API, the WordPress.org plugins API, Flippa public search pages (server-rendered), Microns, Stonemaier, RevenueCat, Press Gazette and Freemius. All pages were accessed on 2026-10-13 unless stated otherwise.

Access limits I ran into:
- **Flippa:** the JSON API (`flippa.com/v3/listings`) returns 401 and needs authorisation. I did not try to get around this. I used Flippa's public search pages through WebFetch, which show only about 25–30 listings per query.
- **Acquire.com:** "View Listings" leads to a sign-up page, so its listing financials are login-gated and were not accessed.
- **SideProjectors:** rendered no listings.
- **Duke / Substack sale posts:** not checked (no search budget left).

---

## Part 0 — Deal marketplace measurements (the base data for opportunities F1–F4)

### 0.1 Empire Flippers (public API `api.empireflippers.com/api/v1/listings/list`)
[Verified: api.empireflippers.com, 2026-10-13]. I downloaded 175 listings currently for sale and 2,679 sold listings.

- **No assets under $50k for sale right now.** All 174 priced, for-sale listings are at least $50k.
  - $50k–100k band: 25 listings, median ask 22× monthly profit (≈1.8× annual), median profit $3,517/mo, median 10 owner-hours a week.
  - Over $100k: 149 listings, median 30× monthly.
- **Sold under $50k, 2025–26:** about 41 listings, using `updated_at` as a stand-in for the sale date (a weak proxy).
  - Median 26× monthly (≈2.2× annual). Median profit $1,450/mo.
  - Mix: display ads, affiliate, FBA, KDP, YouTube, dropshipping, with a couple of SaaS.
  - The latest examples are a $42.6k SaaS at $1,121/mo (38×), a $45.3k SaaS+subscription at $3,778/mo (12×), and a $44.0k YouTube channel at $5,503/mo (8×).
- **Multiples by type and period**, from sold listings using the same `updated_at` proxy (median monthly multiple):

| Type | 2019–21 | 2022–24 | 2025–26 |
|---|---|---|---|
| Display ads | 26× | 39× | 30.5× |
| SaaS | 32.5× | 45.5× | 39× |
| Subscription | 26.5× | 38× | 30× |
| YouTube | — | — | 22× |

  - Count of sold content sites:
    - Display-ads sites: 458 sold in 2022–24 against 76 in 2025–26.
    - Amazon-Associates sites: 158 in 2022–24 against fewer than 4 in 2025–26.

  This fits the content-site collapse after AI search, but because the date proxy is weak I treat it as directional only.
- **Financing is rare under $100k.** Empire Flippers' own guide says [Verified: empireflippers.com/buy-business-seller-financing/]:
  - "In 2025, we sold 168 businesses. Of those, 45 had earnouts" (27%).
  - The average 2025 earnout deal was $327,746.
  - "It's rare to find deals below $100K with a deal structure." Sellers under $100k "prefer to have all cash upfront."
  - The recommended down payment is about 60–70%.

### 0.2 Flippa public search pages
[Verified: flippa.com/search with filters, 2026-10-13. Only the first ~26–31 listings per query were visible.]

| Query (asking $2k–50k, profit ≥$100/mo) | Results | Share of visible listings "Data Verified" | Visible listings under 1 year old | Median ask ÷ annual profit (visible, fixed-price) |
|---|---|---|---|---|
| Mixed types (site, SaaS, app, newsletter, plugin) | 1,226 | ~13/26 (50%) | ~8/26 | ≈1.4× (n=17) |
| SaaS only | 101 | ~21/26 | 12/26 | ≈2.1× (my calculation, n≈16) |
| iOS/Android apps | 91 | ~7/30 (≈23%) | ~9/30 (plus many at 1 year) | ≈2.1× (my calculation, n≈25) |
| Newsletters ($1k–50k, no profit filter) | **8** in total | 3/8 | 3/8 | 1.3×–4.1× (4 profitable listings) |

What these tables show:
- **Supply is plentiful but young.** Close to half of the visible SaaS listings were under 1 year old: AI micro-tools built to flip (AI blogging, AI receptionist, AI image tools). Their profit history is too short to value.
- **"Data Verified" on Flippa means a connected revenue source**, not an audited P&L. Treat it as a minimum bar, not proof.
- **Price cuts are common.** About 11 of 30 visible app listings showed price cuts of 13–43%, which suggests asking prices are often not where deals clear.
- **No visible listing mentioned seller financing.** Flippa only advertises third-party buyer financing.
- **Aged assets with real installed bases do appear.** Examples (seller claims, 2026-10-13):
  - A Quran recitation app (7 yrs, 1M+ downloads): $23,000 ask, $544/mo profit, Data Verified.
  - A Unity vet-care game (8 yrs, 10M+ downloads): $6,700, $290/mo.
  - A Shopify-apps package (19 yrs): $14,500, $246/mo, Data Verified.
  - Web Design Weekly (15-year-old newsletter, 19k subscribers): $9,999 with almost no revenue ($33/mo).

### 0.3 Microns
[Verified: microns.io homepage, 2026-10-13]
- **15 active listings.** The median ask is about **4.3× annual revenue**: revenue, not profit, and no profit figures are shown. My calculation from the listed figures.
- Only 5 of 15 had annual revenue above $4k.
- Some asks are far above revenue: an AI IELTS platform asks $30k on $300 a year, and a resume checker asks $10k on $864.
- **6 recent sales cleared at $1k–$5k:**
  - A writing newsletter with 2,800+ subscribers sold for $4,000 on $235 a year of revenue (about $1.43 per subscriber).
  - An "AI YouTube Growth" SaaS sold for $3,000 on $11,300 a year of revenue (0.27× revenue). That implies revenue was collapsing.

### 0.4 Secondary benchmarks
- **Acquire.com:** "2,000+ startups sold", "$500M+ closed deal volume", 500k+ buyers [Verified: acquire.com, 2026-10-13]. That implies an average deal of about $250k, so the sub-$50k segment is not its core.
- A search snippet attributes a 2023 sub-$100k average of **4.11× profit** to Acquire, and a July 2026 blog post (beancount.io) claims the smallest deals average 2.6× TTM revenue and 10.7× TTM profit; that post is internally inconsistent [Secondary, low reliability]. The Paddle-hosted Acquire 2025 report URL returned 404.
- **WordPress businesses:** usually 2–4× ARR; 2–3× when the seller starts the sale [Secondary: Freemius blog, Jan 2022].

### 0.5 Answers to the assignment questions
- **Realistic multiple, $2k–50k:**
  - Flippa: about 1.4–2.1× trailing annual profit (seller-reported) at asking price; cleared prices are probably lower given the frequent cuts.
  - Empire Flippers (vetted, $25–50k): about 2.2× annual.
  - Microns: priced on revenue, about 4× annual revenue, with weak profit disclosure.
- **What capital buys.** At about 2× annual profit, $1,000/mo of profit costs about $24k.
  - **Track A ($2–5k/mo) bought outright needs roughly $50–120k.** That is 25–60 times the $2k test budget.
  - Within the $2k budget you can only buy about $80–100/mo of profit, which was the previously excluded micro tier.
  - **So acquisition only works as an operator-uplift play**: buy at about 2× and lift profit 2–3×. It needs capital beyond $2k (flagged).
- **Financing:** effectively unavailable under $100k on Empire Flippers ("rare") and not visible in Flippa's public listings. Earnouts are 27% of Empire Flippers deals but average $328k. [Hypothesis] Seller financing at $10–50k can only be negotiated directly with motivated sellers of aged, decaying assets, which is not possible in this desk phase.
- **Fraction with verifiable revenue:**

| Venue | Share with verifiable revenue |
|---|---|
| Empire Flippers | 100% (vetted, but nothing under $50k for sale) |
| Flippa, mixed types | ~50% "Data Verified" |
| Flippa, apps | ~23% |
| Flippa, SaaS | ~80% verified, but ~half under 1 year old |
| Microns | not indicated per listing |

  Strip out assets under 12 months old and unverified ones, and roughly **10–20% of visible sub-$50k Flippa listings are both aged and verified** (my estimate from the visible samples, [Hypothesis] for the full result sets).

---

## Opportunities

### F1. Aged mobile-app rescue: buy 3+-year-old, verified, under-maintained apps at about 2× annual profit and modernise them
1. **Concept.** Buy apps that already have a large installed base and decaying owner attention (examples: the Quran app with 1M+ downloads at $544/mo; the vet game with 10M+ downloads at $290/mo; the anti-spy app with 128k downloads at $995/mo).
   - The uplift levers are technical: update the SDK and target API, rework the ads and subscription paywall, test prices, localise app-store listings into more languages, and run AI-assisted feature refreshes.
2. **Paying customer.** Consumers worldwide, paying through app-store in-app purchases and subscriptions, plus ad networks.
3. **Model.** Own and operate. Revenue from IAP/subscriptions and AdMob.
4. **Spending evidence.**
   - 91 Flippa app listings at $2–50k with at least $100/mo profit [Verified: Flippa search, 2026-10-13].
   - Aged examples carry "Data Verified" tags (the Quran app, Magical Hands with 1.07M installs at $107/mo).
   - Empire Flippers sold-listings data shows buyers pay about 2× annual profit at the low end.
   - Revenue of each target is the seller's claim, verified only by the platform connection.
5. **Competitors and dislikes.**
   - Competing buyers are app-flipping studios and Flippa's own broker desk.
   - Buyers dislike unverified revenue (about 77% of visible app listings), and AI apps under 1 year old with no retention history.
6. **Entry strategy.** Screen strictly:
   - at least 3 years of age;
   - Data Verified, with at least 12 months of history;
   - organic installs (no paid UA dependence);
   - an obvious technical debt to fix (outdated SDKs, no subscription tier, English-only store listing).

   Avoid AI-wrapper apps. A dev operator can rebuild a codebase cheaply with AI tools, which non-technical buyers cannot; that is a real (if modest) edge.
7. **Acquisition mechanism.**
   - Deal flow: Flippa public listings plus "first access" windows. Users come with the asset; growth is ASO, a free channel.
   - Newcomer evidence: none. Uplift outcomes for small-app buyers are [Unknown]. Seller narratives ("Top 100 in Ukraine App Store") are vendor claims.
   - One structural lever was tested and found weak; see the app-store anti-steering shift in Part 3.
8. **Capital, ops, legality.**
   - $10–50k per asset, well above the $2k budget. Escrow through Flippa.
   - Israel-based operation is fine: app-store accounts transfer globally.
   - Risks: Apple/Google account-transfer rules; asset seizure if the prior owner used copied content (for example, unlicensed streaming apps such as "Lumina Play" and "Yalla Match" carry obvious IP risk).
9. **Labour.** Low once modernised; ASO and ads run themselves. Revenue can grow faster than founder hours, and Empire Flippers sellers report 1–10 hours a week.
10. **Unit economics [Hypothesis].**
    - Buy at $20k for $800/mo (2.1×). If profit doubles to $1,600/mo within 9 months, payback is about 12 months and the asset value rises to about $38k.
    - Track A needs 3–4 such assets ($60–80k).
    - Track B only via a portfolio or roll-up of 15 or more apps; capital-bound.
11. **Kill risks.**
    - Installs on old apps decay structurally: store algorithms favour fresh apps.
    - Claimed revenue is often seasonal or one-off.
    - Uplift may simply not happen (unmeasured).
    - The capital gap against the $2k budget.

### F2. Aged B2B micro-SaaS bought at $10–50k (verified Stripe, under-priced, owner fatigue), then raise prices and repair SEO
1. **Concept.** Target B2B tools with long tenure and real paying customers. Examples:
   - a Shopify-apps package (19 yrs, $14.5k ask, $246/mo profit);
   - a Google Maps rank tracker (522 subscribers, $15.2k/mo profit; above band, shown for reference);
   - Sendwo (3 yrs, 8,250 users, $39.9k ask, $1.12k/mo profit).

   Levers: price increases (old SaaS is typically under-priced, [Hypothesis]), annual plans, SEO repair, and an AI-assisted rebuild of a fragile stack.
2. **Paying customer.** SMBs or agencies, global, paying by card subscription.
3. **Model.** Monthly or annual SaaS subscriptions.
4. **Spending evidence.**
   - 101 Flippa SaaS listings at $2–50k with profit [Verified: Flippa, 2026-10-13].
   - Empire Flippers sold SaaS (all sizes) at a 39× monthly median in 2025–26.
   - A recent Empire Flippers sale of $42.6k on $1,121/mo [Verified: Empire Flippers API].
   - Acquire claims 2,000+ startups sold [Verified: acquire.com].
5. **Competitors and dislikes.**
   - Competing buyers are many: Acquire's 500k+ registered buyers bid up the clean deals.
   - Buyers dislike that about half the cheap listings are less than 1 year old (AI micro-SaaS), with negligible customer counts (for example, "18 organic users").
6. **Entry strategy.** Stick to unglamorous, non-AI, aged B2B niches where AI-flippers are not competing. Use technical due diligence (code audit, Stripe cohort churn) as the edge.

   No credible entry at the "AI tool" end; that segment is a supply glut.
7. **Acquisition mechanism.**
   - Inbound comes from the tool's existing SEO and integrations. Deal flow: Flippa public listings plus Acquire (login-gated, not accessed).
   - Newcomer acquirer outcomes: [Unknown].
8. **Capital, ops, legality.** $15–50k (over budget). Remote operation is fine. Stripe-account and data-processing transfer is needed (GDPR DPA if EU customers).
9. **Labour.** Support load is the risk. It is delegable to a part-time VA once the code is stabilised.
10. **Unit economics [Hypothesis].** $40k buys about $1,500/mo. A 20–30% price increase at 5% extra churn gives about $1,800/mo. Track A with one or two assets; Track B only as a roll-up.
11. **Kill risks.**
    - Churn hidden in seller-reported MRR.
    - Platform dependency (for Shopify apps, the 2025 policy changes).
    - Bidding competition pushes multiples to 3–4×, which kills the payback.

### F3. Small-newsletter acquisition plus paid-recommendation monetisation (Boosts / SparkLoop) and niche sponsorship
1. **Concept.** Buy newsletters with large, engaged lists and little monetisation. Monetise via:
   - paid recommendation networks (beehiiv Boosts, SparkLoop partner programs), which pay per referred subscriber;
   - direct sponsorship.
2. **Paying customer.** Other newsletter operators (paying per referred subscriber) and B2B sponsors. Global, English.
3. **Model.** CPA per subscriber recommended, plus a flat sponsorship fee per send.
4. **Spending evidence.**
   - **Per-subscriber payouts:** Boosts CPA about $1.50–3 and SparkLoop $2–7 per subscriber [Secondary: third-party blogs and comparisons via search; no official figure].
   - **SparkLoop:** claims "$millions" paid to operators monthly and "thousands" of newsletters [Anecdote/vendor claim: sparkloop.app].
   - **Deal comparables:**
     - Flippa (8 newsletter listings, $1–50k): Pips Post (45k subscribers, ~50% open rate) at a $5,900 auction start; B2B Whales (45k subscribers) at $35,000; Red Herring Reads (8.3k subscribers, $606/mo) at $15,300.
     - Microns: a newsletter with 2,800 subscribers sold for $4,000.

     All [Verified: Flippa and Microns pages, 2026-10-13; metrics are seller claims].
5. **Competitors.**
   - Newsletter acquirers such as Duke (not checked) and holding companies.
   - Buyers dislike inflated lists (giveaway- or Boost-bought subscribers with low opens), e.g. the crypto newsletters with 84k "active" subscribers and negative profit.
6. **Entry strategy.** Look only for aged lists with a verified open rate of at least 35% in a B2B niche that sponsors pay for. Avoid lists grown through paid Boosts, which are mostly low-intent.

   "None credible" for consumer and crypto lists.
7. **Acquisition mechanism.** The list is the channel. Supply is the problem: only **8 newsletters** at $1–50k on Flippa, against 1,226 assets of other types.
8. **Capital, ops, legality.** $5–35k. ESP account migration; list consent must transfer under GDPR/CAN-SPAM; Israel-based operation is fine.
9. **Labour.** Writing is the bottleneck. AI-assisted curation helps but quality risk is high. A sponsor sales motion is needed for real money.
10. **Unit economics [Hypothesis].** A 20k-subscriber list at $1–1.5 per subscriber costs about $20–30k.
    - Recommendations: if 2% of readers a month accept a recommendation at $2, that is about $800/mo.
    - Sponsorship: at a $25 CPM-equivalent on 8k opens, four sends a month, about $800/mo.
    - Track A is possible; Track B needs several lists.
    - The 2% acceptance rate is a pure assumption.
11. **Kill risks.**
    - Recommendation-network payouts depend on platform policy.
    - Inflated lists.
    - Thin supply means you overpay.

### F4. Abandoned high-install WordPress plugins (especially regional-commerce infrastructure): take over maintenance or ownership, then add a paid tier
1. **Concept.** Take over plugins with large active-install bases whose authors stopped maintaining them. Commerce plugins are the priority because store owners pay.
   - Brazil is a striking cluster [Verified: WordPress.org plugin API, 2026-10-13]. All three are by one author, Claudio Sanches:
     - `woocommerce-extra-checkout-fields-for-brazil`: **60,000 installs**, last updated Feb 2024, rating 96 (515 ratings);
     - `woocommerce-correios` (Brazilian postal shipping): 20,000 installs, last updated Jan 2025, 868 ratings;
     - `woocommerce-pagseguro`: 10,000 installs, last updated Aug 2020.
   - These are localisation infrastructure for an under-served geography. That combines the acquisition and geography angles.
2. **Paying customer.** Brazilian WooCommerce merchants, or more generally store owners on stale commerce plugins.
3. **Model.** Freemium: the free plugin stays on WordPress.org; a pro add-on is sold at about $49–99 a year, for example shipping-label automation, PIX reconciliation or NF-e invoicing (prices are [Hypothesis]).
4. **Spending evidence.**
   - **Supply measured:**
     - Among the 5,995 most popular plugins (all at least 1,000 installs), **161 have 10,000+ installs and no update in over 2 years**, and 120 more have 10,000+ installs and none in 1–2 years.
     - 27 commerce, booking or membership plugins with 5,000+ installs have had no update in 18 months or more.

     [Verified: WordPress.org API, 2026-10-13]
   - **WordPress.org's official "adopt-me" tag** lists only 18 plugins, all with 1,000 installs or fewer, so the good supply is not formally offered.
   - **Freemium benchmarks:** about 2.1% feature-gated conversion, up to 7.4% with stronger product-led growth [Secondary, cited by Freemius blog, Aug 2026; not WordPress-specific].
   - Plugin-specific paid conversion: [Unknown].
5. **Competitors.**
   - In Brazil, commercial alternatives exist (shipping aggregators, payment gateways' own plugins), [Unknown] in detail.
   - Users of a stale plugin dislike broken compatibility and unanswered support threads.
6. **Entry strategy.** Because the code is GPL, you can fork without permission, but a fork starts at zero installs. The value is the WordPress.org slug and its update channel, which needs the author's agreement to transfer.

   That requires contacting authors, which is out of scope now and should be flagged for a later phase. The fallback is "fork plus SEO in Portuguese", which is weak.
7. **Acquisition mechanism.**
   - The WordPress dashboard update channel plus in-plugin upsell: a proven mechanism for freemium plugins in general (e.g. Freemius's business model).
   - Newcomer evidence: [Unknown].
   - Trust risk: WordPress.org scrutinises ownership changes because acquired plugins have been used to push malware (a historical pattern, [Secondary/background]).
8. **Capital and legality.**
   - Purchase price unknown; plausibly a few hundred dollars to a few thousand for unmonetised plugins [Hypothesis]. This is the only acquisition play that might fit the $2k budget.
   - Portuguese support is needed (AI-assisted is feasible).
   - Brazilian tax-invoice (NF-e) integrations are complex but are exactly a developer's strength.
9. **Labour.** Support load scales with installs, which is the main labour risk. The code itself is low-maintenance once fixed.
10. **Unit economics [Hypothesis].** 60,000 installs, of which perhaps 30–50% are live stores; 1% buying a $79-a-year pro tier is about 240–300 buyers, or about $1.6–2k/mo. Track A plausible; Track B only with a portfolio of plugins.
11. **Kill risks.**
    - The author refuses to transfer.
    - Active installs are mostly dead sites.
    - WooCommerce core or the payment providers ship the feature themselves (e.g. the PagSeguro official plugin).

### F5. Licensed board-game localisation into a mid-size language, funded by pre-orders
1. **Concept.** License proven hobby games (with BoardGameGeek traction) into an under-served language such as Portuguese (Brazil), Turkish, Czech, Hungarian or Romanian. Co-print with the originator's factory and pre-sell through a localised crowdfunding or pre-order page.
2. **Paying customer.** Hobby gamers in the target country, through direct pre-orders and local game shops.
3. **Model.** Buy units at about 30% of MSRP and sell at full MSRP direct, or at about 50% to retail.
4. **Spending and terms evidence.**
   - Stonemaier, a major indie publisher: localisation partners pay "roughly 30% of MSRP," half upfront and half before shipping (manufacturing cost plus $2–4); the MOQ is the factory's, "typically 1500 units"; partners arrange freight; translation turnaround is about 2–3 months [Verified: stonemaiergames.com/?p=8635, author comments dated 2023-10-14 and 2026-01-01].
   - Suggested IP-licence royalty is about 10% [same source, 2024-09-14 comment].
   - Designer royalties are 3–7% [Secondary: BGDF forum].
   - Minimum guarantees are common in foreign-language licences [Secondary: legalmoveslawfirm.com].
   - Gamefound collected about $165M in 2024 [Secondary via search].
5. **Competitors.**
   - Established localisers dominate big languages: Rebel and Lucky Duck in Poland, Galápagos in Brazil (Asmodee-owned), Devir in Spain [Secondary/background, not verified this phase].
   - Originators increasingly localise themselves through Gamefound's multi-language campaign tool (e.g. Witcher: Legacy, €10.26M and 14,000+ backers) [Secondary via search].
6. **Entry strategy.** Only languages and titles the majors skip: mid-weight titles in languages of 10–30M speakers. Whether localisers can still win that segment is [Unknown].
7. **Acquisition mechanism.** Local hobby communities (Facebook groups, local forums), local-language crowdfunding. No newcomer outcomes found: my search for local-licensee campaigns returned none.
8. **Capital.** 1,500 units × ($60 MSRP × 30%) is about $27k, plus freight and duty and translation. **That is roughly 15× the budget.** Pre-orders could fund it only if the campaign hits about 1,000+ backers. Inventory risk is real; operating from Israel is possible but adds 3PL logistics in the target country.
9. **Labour.** Per-title project work; delegable (translators, a 3PL).
10. **Unit economics [Hypothesis].** Selling 1,500 units direct at $60 brings $90k in revenue against about $27k for units, about $10k freight and duty, and about $8k for platform and marketing. That is a gross of about $45k per title, lumpy.
    - Selling through retail at 50% brings $45k in revenue, leaving almost nothing.
    - Track B only with direct sales and a pipeline of titles.
11. **Kill risks.** Originators keep localisation in-house; there's a 1,500-unit MOQ against unknown local demand; and a hobby-market slowdown.

### F6. Translation-rights licensing of niche non-fiction into under-served languages, using AI-assisted human translation
1. **Concept.** License translation rights to proven niche non-fiction (technical hobbies, professional how-to) for languages the original publishers ignore. Produce the translation with AI plus a human editor and sell via KDP, local e-book stores and direct.
2. **Paying customer.** Readers in Polish, Turkish, Vietnamese or other mid-size languages.
3. **Model.** Advance plus a 6–10% royalty to the rights holder ([Hypothesis]; no data found).
4. **Evidence.**
   - Contractual friction is documented: the Authors Guild model clause bars machine translation without the author's written consent; the Danish translators' model contract bars machine translation and post-editing [Secondary via search, 2026].
   - Veen Bosch & Keuning (Simon & Schuster Netherlands) ran an AI-translation pilot on fewer than 10 titles, with author consent [Secondary].
   - Small-publisher advances and outcomes: [Unknown].
5. **Competitors.** Local publishers. KDP is already flooded with AI translations (consistent with the Phase 5 lesson).
6. **Entry strategy.** "None credible" yet. The cost advantage of AI translation is exactly what rights holders are now writing out of contracts.
7–11. Not developed further. It is listed so the Director can see licensing was tested beyond board games.

---

## Part 3 — Structural shifts (2025–2026) tested for new direct-sale demand

1. **Apple anti-steering ruling and web checkout.** The US injunction came in April 2025. The Ninth Circuit partly upheld it in December 2025, leaving room for a "reasonable commission"; rehearing was denied in March 2026 and Apple petitioned for certiorari in May 2026 [Secondary via search].
   - The thesis was: buy small subscription apps and move buyers to web checkout to save fees.
   - **RevenueCat's own experiment contradicts it** [Verified: revenuecat.com/blog/growth/iap-vs-web-purchases-conversion-test, update dated 2025-05-28]:
     - about 12,500 US users of Dipsea;
     - web-only checkout converted 18.1% against 27.0% for in-app purchase;
     - web take-home was about 6.5% lower than in-app at a 30% fee;
     - at the 15% Small Business Program rate, web returned only about 77¢ per in-app dollar.
   - **Killed** as a value-creation lever for small apps.
2. **AI search reducing human traffic.**
   - TollBit partner sites went from 1 AI bot per 200 human visits (early 2025) to 1 per 31 (end of 2025), and human page requests fell 9.4% quarter on quarter in Q2 2025 across about 400 sites [Secondary via search, Press Gazette].
   - Empire Flippers' sold-listing counts for display-ads and Amazon-Associates sites collapsed after 2024 (Part 0.1, directional).
   - Implications:
     - (a) Cheap SEO content sites are falling knives: avoid them, despite low multiples.
     - (b) Owned lists (newsletters) and assets with direct users (apps, plugins) should hold value better. This supports screening F1, F3 and F4 over content sites.
3. **AI-crawler licensing (TollBit, Cloudflare pay-per-crawl) as a new revenue line for small content owners.**
   - TollBit's co-founder, April 2026: AI revenue "is not going to make their year this year" [Verified: Press Gazette, 2026-04-14]. No per-crawl prices or small-publisher payouts were found.
   - **Killed** for now as a basis for buying content archives.
4. **AI-built supply flooding deal marketplaces.** About half the visible Flippa SaaS listings at $2–50k were less than 1 year old, mostly AI wrappers.
   - This shift does not create demand; it degrades the median sub-$50k listing.
   - The contrarian implication is to filter hard for age (at least 3 years) and non-AI B2B utility.

---

## Killed ideas (and why)
- **Buying listed sub-$50k SEO content and affiliate sites:** AI-search traffic decline, and Empire Flippers' sold volumes collapsed after 2024. Cheap for a reason.
- **Web-checkout uplift on acquired iOS apps:** RevenueCat's experiment shows web checkout loses for small developers at the 15% rate.
- **AI-crawler licensing income from content archives:** no measurable payouts yet; TollBit itself says it is not material.
- **Buying "AI micro-SaaS" under 1 year old on Flippa or Microns:** asks of 10–100× annual revenue on Microns, no history, glut.
- **Inflated crypto and consumer newsletters:** e.g. 84k "active" subscribers with negative profit.
- **Seller-financed sub-$100k online deals:** Empire Flippers says such structures are "rare"; none visible on Flippa. Not a dependable way around the capital gap.
- **Translate-and-license books with AI:** contract clauses now block machine translation (F6, kept only as a record).

---

## Ranking, top picks and decisive assumptions

All acquisition plays (F1–F3) **exceed the $2k budget by 5–25×**, which is flagged as the core constraint. The only budget-compatible play is F4 (if plugin transfers are cheap).

| Rank | Idea | Track fit | Main constraint |
|---|---|---|---|
| 1 | **F4 Abandoned high-install WordPress commerce plugins (Brazil cluster first)** | A (B via portfolio) | Transfer cost and author consent [Unknown] |
| 2 | **F1 Aged mobile-app rescue (≥3 yrs, verified, organic)** | A, needs $20–80k | Capital; uplift unmeasured |
| 3 | **F3 Newsletter acquisition plus recommendation/sponsor monetisation** | A | Supply (8 listings); payout figures secondary only |
| 4 | F2 Aged B2B micro-SaaS | A (B roll-up) | Capital; buyer competition |
| 5 | F5 Board-game localisation licensee | B | About $27k+ per title, MOQ 1,500; originators self-localise |
| 6 | F6 Translation-rights licensing | — | Contractual AI bans |

**Top 3 for deep diligence, with the decisive unverified assumption for each:**
- **F4:** that owners of stale plugins with 10,000+ installs will transfer the WordPress.org slug for under about $2–5k, and that at least 0.5–1% of active installs will pay for a pro tier. That second figure can be tested in desk research by finding comparable freemium plugins that disclose sales, such as Brazilian WooCommerce pro plugins on their own sites.
- **F1:** that a technical operator can at least double profit on aged apps within 9–12 months. No public data on post-acquisition uplift exists. The next step is to find documented flip case studies with before-and-after App Store or RevenueCat numbers, and to measure organic install decay on aged apps.
- **F3:** that aged B2B newsletters with verified open rates of at least 35% can be bought for under about $1.5 per subscriber, and that recommendation networks pay about $2 per subscriber at a meaningful volume. The next step is to read beehiiv and SparkLoop's own published payout data and search Duke-type sale posts.

**WebSearch count: 8 of 8** (all logged in research-notes/search-log.txt as P6-F).
