# Phase 8 — Discovery Agent A (Consumer & Prosumer): reverse-engineering App Store newcomer winners

Date: 2026-10-13. Dataset: Apple iTunes Search/Lookup APIs and Apple's public top-grossing RSS feeds (US plus DE, BR, GB, MX, ES, JP, AU contrasts). WebSearch used: 6 of 6 (all logged as P8-A). Scripts and raw data: `scratchpad/p6plus/P8-A/` (scripts/, data/).

## 0. Bottom line

- **Audience-free indie wins on the App Store are rare and front-loaded in time.**
  - Apps from individual developer accounts (heuristic) that are at least 15 months old reach ≥1k US ratings 4.9% of the time and ≥10k only 0.5% of the time. Company accounts reach those levels 19.1% and 5.2% of the time.
  - Upfront-paid apps are dead: 182 of 19,614 new apps are paid upfront, and none reached 1k ratings.
- **Where indies do win, three things recur:**
  1. **They entered a new hobby boom or app mechanic early.** These are the first 6–12 months of TCG card scanners or "earn your screen time" blockers. In those windows 15–30% of entrants reached 1k ratings, versus 1–6% for the later flood.
  2. **The app is "money-adjacent" and priced high.** Users pay because it helps them earn or win money: resale profit scanners, betting research, collectible values. Rating counts badly understate revenue here. PropGPT has only about 2.6k ratings but a verified $82k MRR, and its founder has 194 X followers.
  3. **They were serial shippers.** Each indie winner had a portfolio of 8–16 apps with one hit, and growth came through volume organic short-form video, not an existing audience.
- **Ratings are not revenue, and grossing ranks do not have published dollar thresholds.** Converting a category grossing rank into dollars is the single biggest unknown behind every idea below.
- **Proposed (ranked):**
  - A1: Trend-timed "collector value scanner" micro-studio.
  - A2: Prediction-market research/alert companion (US).
  - A3: Amateur-sport organiser apps for non-US storefronts.
  - A4: Post-booking cruise/travel price-drop monitor.

  All are Track A at base case. Only A1 and A2 have a plausible Track B tail.

## 1. Method and dataset

1. **US keyword harvest.**
   - 316 consumer and hobby queries (habit, sleep, Bible, TCG, budget, fishing, pickleball, and so on), each run against `search?entity=software&country=us&limit=200`.
   - 48,799 unique apps came back. Of these, **19,614 are non-game apps first released 2024-01-01 or later** (the newcomer sample).
   - A follow-up harvest of 46 targeted US terms added 3,095 more new apps (thrift, penny deals, Supabase, aurora, Lorcana and similar).
2. **Revenue-ranked view.**
   - Apple RSS top-grossing top-100 for all 23 US non-game genres (2,300 chart slots), plus overall top grossing in BR, DE and JP.
   - Genre charts for BR, DE and GB (Sports, Shopping, Finance) and for BR/MX (Reference, Book).
   - Every chart app was looked up for its first-release date and rating count.
3. **Developer profiling.** Full portfolios were looked up for 1,789 developers:
   - all developers with a ≥1k-rating newcomer;
   - all developers with a 2024+ app in a US genre grossing chart;
   - a random control of 400 developers whose newcomer apps have fewer than 10 ratings.
4. **Non-US contrast.** 40 local-language queries each in DE (2,364 new apps) and BR (2,545 new apps). Targeted probes for betting, gambling-blocker, padel, darts, prediction-market and gig-driver apps in BR, GB, DE, MX, ES and AU.

**Biases (read before using any rate):**
- Search results are relevance-ranked and capped at 200, which over-samples popular apps. All hit rates here are **upper bounds**.
- The "individual seller" flag is a name heuristic: no corporate suffix such as LLC, Ltd or Inc. It misclassifies some apps both ways.
- Ratings are US-storefront counts only.
- 2026 cohorts are young, so their low hit rates are partly an age effect. Where rates are compared, they are restricted to apps released before 2025-07-01 (at least 15 months old).
- Inference labels are used throughout.

## 2. Base rates

**US newcomer sample (19,614 non-game apps, first released 2024-01-01 to 2026-10)** [Verified: iTunes Search API, 2026-10-13]

| Measure | All new apps | Apps released before 2025-07-01 (n=6,201) |
|---|---|---|
| Median US ratings | 2 | 11 |
| Zero ratings | 32.6% | — |
| ≥100 ratings | 14.5% | — |
| ≥1,000 ratings | 5.8% (1,129 apps) | 12.9% |
| ≥10,000 ratings | 1.3% (252 apps) | 3.2% |
| Individual-seller apps, ≥1k / ≥10k | — | 4.9% / 0.5% (n=2,711) |
| Company-seller apps, ≥1k / ≥10k | — | 19.1% / 5.2% (n=3,490) |

- **By release cohort:**
  - 2024: 3,527 apps; 15.1% reached ≥1k and 3.7% reached ≥10k.
  - 2025: 6,112 apps; 8.0% reached ≥1k.
  - 2026: 9,973 apps; 1.1% reached ≥1k so far.

  New-app supply has roughly tripled since 2024, consistent with AI-assisted building.
- **Pricing:**
  - Upfront paid: 182 apps (0.9%). The best has 784 ratings, and it is an established brand (SkySafari 8 Pro).
  - Subscription language appears in 54% of all new apps and 59% of ≥1k apps. Subscriptions are near-universal, so they are not a differentiator.
- **Localization:**
  - ≥10k winners support a median of 5 languages, and 35% support 10 or more.
  - Apps with fewer than 10 ratings support a median of 1 language, and 14% support 10 or more.
  - 91% of ≥10k winners were updated since July 2026, versus 60% of apps with fewer than 10 ratings. Winners are actively operated.
- **External base rate** [Verified: revenuecat.com/sosa-26-insights, 2026-10-13]. Among apps using RevenueCat (115k apps, $16B revenue):
  - 17% of new apps reached $1k MRR within two years, down from 19%. 4.6% reached $10k, down from 5.3%.
  - Monthly revenue one year after launch: about $72 on average; the top 25% start at $429; the top 10% at about $2.5k or more.
  - Hard paywalls convert 11% of downloads to paid by day 35, versus 2% for freemium. Revenue per install after two weeks is up to $2.32, versus $0.27.
  - Median realised first-year LTV per payer is $32 in North America and $23 globally.

  RevenueCat customers are already monetising apps, so this is a survivor-skewed population.
- **Revenue-ranked view (US genre grossing charts)** [Verified: Apple RSS and Lookup API, 2026-10-13]:
  - 648 of the 2,300 chart slots (28%) are held by apps first released in 2024 or later.
  - Their median rating count is 1,544, and **21.8% have fewer than 100 ratings**. In small genres, a new app can chart on grossing with almost no ratings.
  - Newcomer share by genre: DevTools 61, Reference 50, Graphics & Design 49, Shopping 48, Food & Drink 45, Entertainment 39 and Music 37 (of 100). Health & Fitness (16) and Education (16) are the hardest.
  - 109 of the 648 entries (16.8%) come from individual sellers. These cluster in DevTools (30), Shopping (15), Book (10), Reference (9) and Food & Drink (9).
- **Non-US contrast:**
  - Aged hit rate to ≥1k local ratings: DE 6.5% (49 of 751) and BR 11.0% (86 of 783).
  - Local winners are the same global studios and brands, localized: Bible Path and Learna (DEEP FLOW), Welmi, BitePal, Unrot. The rest are local banks and brands (Bradesco, Stellantis Financiamentos).
  - Overall top-grossing newcomers in BR, DE and JP are AI assistants (Claude, Grok, Gemini, Manus) and Singapore/China short-drama apps.
  - In BR and MX Reference, US studio apps translated into Portuguese/Spanish hold ranks 1–2 (Bible Path, Monkey Taps), alongside Next Vision scanners. Localization arbitrage is already being exploited by studios.
  - However, **small genre charts outside the US have even lower entry thresholds.** In BR, DE and GB Sports, Shopping and Finance charts, 15–51 of every 100 slots are 2024+ apps, many with 0–50 local ratings.

## 3. Profile of the winners

**Developer type** [Verified data, classification is my heuristic]

| Group | Single-app developer | 2–4 apps | 5+ app studio | Established (had a pre-2024 app with ≥10k ratings) | Individual-seller name |
|---|---|---|---|---|---|
| ≥10k-rating newcomers (n=252) | 34.9% | 23.4% | 12.7% | 29.0% | **6.0%** |
| 1k–10k newcomers (n=877) | 32.5% | 30.0% | 23.1% | 14.4% | 19.3% |
| New entries in US genre grossing (n=648) | 39.0% | 24.5% | 23.3% | 13.1% | 16.8% |
| Control: newcomers with <10 ratings (400 developers) | 35.5% | 32.0% | 31.8% | 0.8% | **63.0%** |

The ≥10k "single-app" developers are mostly funded single-product companies, not hobbyists. Examples: Cal AI (Viral Development LLC, 370k ratings), Tolan (184k), Bevel, Granola, Shotsy and MeAgain.

**What the ≥10k winners are** [Verified list; motives are Hypothesis]:
- **Brands and platforms:** Google Gemini, Grok, Claude, Apple, Meta, Fox, Abbott.
- **Studios running paid user acquisition:**
  - DEEP FLOW: Learna, 433k ratings.
  - HUBX: Home AI 160k, Tattoo AI 51k.
  - Next Vision: StarSnap, AntiqSnap, FoilSnap, WoodSense.
  - PIXELCELL: YarnPal 34k, Sewpal 12k; 36 apps in total.
  - Turkish, Vietnamese and Hong Kong utility shops: TV remotes, cleaners, VPNs.
- **Singapore/China short-drama apps:** NetShort 223k, DramaWave 186k.
- **Faith apps:** Bible For Women 255k, Haven 150k, Bible Widgets 118k, Creed 70k. 18 of 39 aged Bible apps reached ≥1k ratings, almost all from studios.
- **"Earn money" apps:** Freecash 153k, Scrambly 99k, SideShift.
- **A handful of indies:**
  - Free Plant Identifier (Mohamed Aberkane, 25k).
  - Acorn TCG (Juanjo Valino, 15.5k).
  - Doodle Magic (Hai Nguyen Minh, 53k).
  - Scroll The Bible (JCBSN LLC, 3 apps, 16.9k; US Book grossing #6).
  - Several apparent piracy/streaming apps (AnimeKai, "Live Football TV"). These are not replicable.

**Cluster hit rates (apps at least 15 months old, ≥1k ratings)** [Verified data; upper bounds]:

| Cluster | Hit rate | Developer mix |
|---|---|---|
| Bible/Christian | 46% | studios |
| TV remote/cast | 37% | studios |
| Phone cleaner | 36% | studios |
| Language learning | 33% | |
| AR drawing | 30% | |
| AI video/photo generators | 29% | |
| GLP-1 trackers | 28% | |
| TCG/sports-card scanners | **21%** | **5 of 8 winners are individuals, the most indie-friendly cluster** |
| Other faiths | 20% | 3 of 5 individuals |
| Screen-time blockers | 18% | |
| Calorie AI | 17% | |
| Habit/journal | 8% | |
| Meal planner | 6% | |
| Collectible identifiers (coins, antiques) | 6% | |
| Plant/bird ID | 4.5% | |
| Budget apps | 4.5% | |
| Racket sports | 3% | |
| Tarot/astrology | 3% | |
| Instrument learning | 0% | |
| Dev-SaaS companions (Supabase, Vercel, SSH, server monitors) | 0% | |
| Auction, estate-sale, liquidation and penny-deal apps | 0% | |

**The window effect (entrants and ≥1k hits per half-year cohort)** [Verified data]:

| Cluster | 2024H1 | 2024H2 | 2025H1 | 2025H2 | 2026H1 |
|---|---|---|---|---|---|
| TCG/card scanner | 1 of 5 | 4 of 13 | 3 of 20 | 8 of 29 | 6 of 104 |
| Screen-time blocker | 0 of 6 | 2 of 19 | 7 of 24 | 5 of 43 | 2 of 100 |
| Calorie AI | 6 of 19 | 7 of 34 | 5 of 52 | 4 of 61 | 1 of 87 |
| AI note taker | 6 of 15 | 4 of 34 | 6 of 46 | 1 of 52 | 0 of 45 |

- The early TCG winners were indies: Acorn, MyDex, Ha Vu Thi Thu, Manh Nguyen and Dang Minh Duc.
- Studios followed 6–12 months later: Next Vision (StarSnap 28k, FoilSnap 14k), MAVELLI (HoloDex 24k), Scate and Scaling Engine.
- Then came the 2026 flood: 104 TCG-scanner entrants in 2026H1. Screen-time apps followed the same path. On a broader screen-time/focus keyword set, 168 apps entered in 2026H1 and 115 of them were individual sellers; 2 reached ≥1k ratings.

**Money-adjacent apps convert few ratings into large revenue:**
- **PropGPT** (betting research) [Verified: trustmrr.com/startup/propgpt-ai-props-analysis, fetched 2026-10-13; verified via Superwall API key]:
  - MRR $82,021; 30-day revenue $86,392; lifetime $951,951; 2,101 active subscriptions.
  - Founded September 2024. Founder has 194 X followers.
  - Only 2,638 US ratings. US Sports grossing #75.
  - Acquisition [Secondary: Starter Story automated profile, which carries its own accuracy caveat]: "our 70th video … hit 600,000 views and that raised our ARR from around 8K to 38K in about three days," plus "a few thousand dollars" spent on influencers.
- **ThriftAI** (resale profit scanner, smallstack ApS; 8 apps, one hit):
  - 20.6k US ratings. US Shopping grossing #6, GB #7, DE #20.
  - Revenue: third-party estimates of $40–60k/month [Anecdote: screensdesign.com, unsourced and internally inconsistent].
- **Contrast:**
  - A RevenueCat-verified identifier app "making $200/month from ASO alone" showed $70 over 30 days and 15 subscriptions [Verified: trustmrr.com/startup/hidden-mobile-app, 2026-10-13]. Discovery through App Store search alone yields very little.
  - Bet Block (BR gambling blocker, 2,548 BR ratings) is absent from BR top-100 grossing in Utilities, Health, Productivity and Lifestyle. A high rating count without a paywall does not mean revenue.

**Serial-shipper pattern** [Verified portfolios]:

| Developer | Apps | Hits |
|---|---|---|
| Juanjo Valino | 10 | 1 (Acorn TCG; the rest have ≤304 ratings) |
| Alberto Moral | 16 | 1 (MyDex) |
| smallstack ApS | 8 | 1 (ThriftAI) |
| Quad Innovations | 3 | 1 (Prediction Radar, 525 ratings within 6 weeks, US Finance grossing #40; also a TCG scanner) |
| JCBSN | 3 | 2 Bible hits |

## 4. Replicable patterns for an audience-free solo founder

1. **Ride a boom early.** In a new hobby boom or OS mechanic, the first 6–12 months give 15–30% hit rates. After studios clone it, rates drop to 1–6%. Speed of shipping matters more than polish, which suits AI-assisted development.
2. **Money-adjacent value at a high price.** Users who earn or win money accept weekly plans ($6.99–9.99/week for PropGPT) and hard paywalls. Few ratings can still mean high revenue.
3. **Distribution is volume organic short-form video, optionally boosted by small influencer buys.** It is not App Store search alone, which yields about $200/month in the cited case. The video channel needs no prior audience, but it is founder labour (about 70 videos before the PropGPT spike) that can partly be delegated to UGC creators.
4. **Portfolio of shots.** Expect 1 hit in about 8–16 launches. Budget accordingly, and kill quickly.
5. **Target small genre charts.** In Shopping, Reference, Travel, Weather, Food & Drink and DevTools (US), and in Sports, Shopping and Finance outside the US, newcomers chart on grossing with fewer than 100 ratings. Rank-to-dollar conversion is [Unknown]; no public threshold data was found in two searches.
6. **Localize hits fast.** Winners support 5 or more languages, and US studios already take BR/MX charts with translated apps.

**Not replicable without capital or an existing audience:** paid-user-acquisition studios (remotes, cleaners, AI photo, Bible), VC-funded consumer AI (Cal AI, Tolan), brand apps, short-drama content, and piracy apps.

## 5. Opportunities

### A1. Trend-timed "collector value scanner" micro-studio
1. **Concept.** Watch for collectible and resale booms. Within 2–4 weeks of a boom becoming visible, ship a camera scanner that identifies the item and gives a value or profit estimate (examples: a new TCG such as Lorcana or One Piece, Pop Mart/Labubu, LEGO minifigs, sneakers or watches as they spike). Localize hits into 5–10 languages. Kill misses after 6 weeks.
2. **Paying customer and geography.** Hobby collectors and flippers. US first, then GB, DE, BR and MX through localization.
3. **Model.** Hard paywall with a 3-day trial, then weekly ($4.99–6.99) or annual ($29–49) plans. Apple takes 15% under its small-business programme.
4. **Spending evidence:**
   - TCG cohorts (above): early 2024H2–2025H2 entrants reached ≥1k ratings 15/62 times; 5 of 8 aged winners are individuals.
   - In US Reference grossing: Acorn (indie) #89 and MyDex (indie) #82. Acorn also ranks #33 in MX Reference.
   - ThriftAI ranks Shopping #6 US, #7 GB and #20 DE.
   - Pop Mart and Funko price scanners (Jalm Studio) chart in BR Shopping (#42, #79) and GB Shopping (#64) with 0–11 ratings. [Verified: RSS and Lookup, 2026-10-13]
   - Revenue per app: [Unknown]. The best anchor is ThriftAI at $40–60k/month [Anecdote].
5. **Competitors.** Next Vision runs 23 apps and clones every hit vertical within months (CoinSnap 307k ratings, ComicSnap, VinylSnap, ToyWorth). Also Scate, MAVELLI and Scaling Engine. Users complain about aggressive paywalls and inaccurate values [Hypothesis; reviews were not mined].
6. **Entry strategy.** Timing, not features. Be in the first wave of a boom and own the top search terms before studios arrive. Combine this with a community feed or price-history data that a studio clone lacks. Measured window: about 6–12 months.
7. **Acquisition.** Organic TikTok/Reels/Shorts in hobby niches (pack openings, "what's it worth"), 1–2 posts per day, plus $500–1,000 in micro-influencer tests.
   - Newcomer evidence: indies did win early TCG cohorts, and PropGPT's video-volume result shows the mechanism.
   - CAC: [Unknown].
8. **Operations.**
   - Capital: under $2k (Apple developer fee $99/year, Vision/LLM API costs, creator tests). No inventory.
   - Fully operable from Israel.
   - Value data comes from public sold-price sources or licensed price APIs. Scraping eBay or TCGplayer carries terms-of-service risk; this is unverified and must be checked per source.
   - Trademark caution in names (Pokémon and similar).
9. **Labour.** Building is fast with AI. Marketing is the labour sink, delegable to UGC creators at about $20–50 per video [Hypothesis]. Revenue can outgrow founder hours once one hit is found.
10. **Unit economics** [Hypothesis]:
    - Downside: 4 launches, 0 hits, about $2k lost.
    - Base: 1 hit at a RevenueCat top-quartile level, about $0.5–3k/month gross, roughly $0.4–2.5k owner profit after fees and API costs.
    - Upside: an Acorn/ThriftAI-scale hit at $10–40k/month.
    - Fit: Track A at base, with a real but low-probability Track B tail.
11. **Kill risks.** Studio clones running paid acquisition within months. Value-data access. Booms fading. Apple guideline 4.3 spam rejections for template apps. Already flooded verticals (the 2026 TCG cohort has 104 entrants).

**Ledger note.** This differs from K10 (quilting/hobby app studio, scored 47.4). K10 chose stable hobbies, and the 2026 quilt apps it measured got 0–23 ratings. A1 chooses money-pull collectibles at boom onset, with measured cohort decay as the rule for when to enter. It also differs from Phase 3 "collectible price guides", which were data/content products sold without a camera app or video channel.

**Decisive assumption:** a solo founder can repeatedly spot a boom early and get one app to roughly 1k paying-intent installs through organic video before studio clones arrive. In other words, the measured 15–30% early-cohort hit rate holds for an outsider rather than just for hobby insiders.

### A2. Prediction-market research and alert companion (US)
1. **Concept.** An app for Kalshi/Polymarket users: market movers, whale and odds-change alerts, resolution calendars, and AI summaries of what moves each market. It does not take trades.
2. **Paying customer.** US prediction-market traders, a fast-growing segment.
3. **Model.** Subscription at $9.99–19.99/month or a weekly plan, mirroring PropGPT's high-ARPU research positioning.
4. **Spending evidence** [Verified: Lookup and RSS, 2026-10-13]:
   - Prediction Radar (Quad Innovations; released 2026-09-02; 525 ratings) is already **US Finance grossing #40** within about 6 weeks.
   - "Polymarket Alerta Previsão IA" (indie) is **BR Finance #16** with 15 ratings.
   - Adjacent proof of willingness to pay: PropGPT at $82k MRR [Verified].
   - The platforms are big: the Polymarket app has 60.7k US ratings, DraftKings Predictions 15.5k and FanDuel Predicts 6.7k.
5. **Competitors.** The platforms' own apps; Prediction Radar and Ratio (Quad Innovations); and a flood of 2026 entrants (searching "prediction market" finds 43 new apps in 2026H1 and 35 in 2026H2, of which only about 14 have ≥100 ratings).
6. **Entry strategy.** We are at the start of the window, so speed matters. Specialise by segment (sports-event markets vs politics/economics) or by power-user tooling (portfolio P&L across both platforms, tax export). [Hypothesis]
7. **Acquisition.** Short-form video on market moves, plus X/Reddit posting around big events. Comparable newcomer outcome: Prediction Radar charted fast, but its channel is [Unknown].
8. **Operations.**
   - Capital under $1k. No inventory. Operable from Israel.
   - Depends on the platforms' public APIs. Whether their terms permit third-party commercial apps is [Unknown], to be verified.
   - Prediction markets face US state litigation and regulation [Secondary/Hypothesis; not re-verified this phase]. There is also gambling-harm reputational risk.
9. **Labour.** Data pipelines can be automated. Content marketing is the labour.
10. **Unit economics** [Hypothesis]. Base: $1–5k/month owner profit if one niche tool charts in Finance. Upside follows PropGPT ($80k+ MRR) if a viral loop hits. Fit: Track A to B.
11. **Kill risks.** The platforms ship the same features natively. API access is revoked. Regulatory shutdowns. The flood clones the app within months.

**Decisive assumption:** prediction-market users pay a PropGPT-like subscription for third-party research tools, rather than relying on free platform features and X accounts, and API terms permit it.

### A3. Amateur-sport organiser apps for non-US storefronts (padel, beach tennis, darts, five-a-side)
1. **Concept.** Small utilities for amateur organisers: Americano/Mexicano padel draws, beach-tennis "Super 8", darts scoring with stats, team sorting. Localized into PT, ES, DE, IT and SV.
2. **Paying customer.** Club organisers and regular players in ES, BR, IT, DE, GB and the Nordics.
3. **Model.** Small subscription or lifetime unlock.
4. **Spending evidence** [Verified: RSS and Lookup, 2026-10-13]. Newcomers with tiny rating counts appear in Sports grossing top-100 charts:
   - RSApps Nordics: Padel Americano at BR #62 and GB #77; PadelMax at BR #94; DartsOn at DE #48.
   - Americano Padel Manager (indie): BR #95 and DE #92.
   - Beach Tennis Super 8 (indie, 30 ratings): BR #91.
   - Sorteio de Times (indie): BR #63.
   - Escalação Futebol and a tournament-bracket app (indie): BR #65 and #97.
   - Revenue at those ranks: [Unknown], likely small.
5. **Competitors.** RSApps Nordics, Playtomic (court booking), Padelio (683 ES ratings), Vola (1,024 ES ratings). The US padel search found 140 new apps and none at ≥1k.
6. **Entry strategy.** Language and format gaps (Italian padel, Swedish/Finnish padel, beach tennis in BR/IT) plus cross-country localization. [Hypothesis]
7. **Acquisition.** App Store search in low-competition local languages, plus club WhatsApp/Facebook groups. Evidence of new-entrant revenue: chart presence only.
8. **Operations.** Trivial capital. Fully remote.
9. **Labour.** Low once built. A portfolio can grow without the founder's time.
10. **Unit economics** [Hypothesis]. $50–500/month per app; a 10-app portfolio could reach $1–3k/month. Fit: Track A only.
11. **Kill risks.** Low-rank grossing may mean only $5–20/day. Playtomic adds the same features for free.

**Decisive assumption:** a top-100 rank in non-US Sports grossing corresponds to at least about $20/day per app.

### A4. Post-booking cruise and travel price-drop monitor (US)
1. **Concept.** Users add an existing cruise booking (later hotels and rental cars). The app alerts them to price drops and walks them through the repricing or refund request.
2. **Paying customer.** US cruisers, who rebook frequently and spend high amounts.
3. **Model.** Subscription or a fee per saving.
4. **Spending evidence** [Verified: RSS and Lookup]:
   - CruiseSignal (indie, one app, released 2026-05, 32 ratings) ranks **US Travel grossing #78**.
   - JetBack (flight post-booking savings) ranks #37 with 736 ratings.
   - The flight-deal apps Going (#14) and Airclub (#10) show the appetite for saving money on travel.
5. **Competitors.** CruiseSignal; cruise forums; travel agents who reprice for clients; AutoSlash for car rentals (web) [Hypothesis].
6. **Entry strategy.** Breadth across all cruise lines plus automated refund-request guidance. Weak: this is a fast-follower position.
7. **Acquisition.** Cruise Facebook groups, TikTok cruise content, App Store search. Newcomer evidence: one chart datapoint.
8. **Operations.** Collecting fares from cruise-line sites is a terms-of-service and blocking risk [Unknown]. Operable from Israel.
9. **Labour.** Data maintenance is ongoing.
10. **Unit economics.** [Unknown]. Fit: Track A at most.
11. **Kill risks.** Data access. A single-datapoint evidence base. Thin differentiation.

**Decisive assumption:** reliable, ToS-compliant fare monitoring is feasible across major cruise lines.

## 6. Killed ideas (with evidence)

- **Non-US sports-betting "tips/AI predictions" apps (PropGPT pattern exported).** Aged apps with ≥100 ratings: 0 in BR ("palpites futebol": 124 new apps; "análise apostas": 30), 0 in GB ("football predictions": 95 new), 0 in DE ("sportwetten tipps": 48 new). The US props culture does not transfer. One exception: "Dicas de Apostas – Scouter" at BR Sports #75. [Verified, 2026-10-13]
- **Dev-SaaS mobile companions (Supabase, Vercel, Cloudflare, SSH).**
  - They chart in US DevTools grossing with 0–100 ratings, but that chart's threshold is evidently tiny.
  - A Vercel iOS client earned about $197 in 30 days from 20 subscriptions. [Secondary: search snippet of TrustMRR; the page itself returned 404]
  - 0 aged ≥1k across the supabase, vercel, ssh and server-monitor searches.
- **US thrift/resale profit scanners.** ThriftAI dominates, followed by a flood (126 "thrift" entrants, about 10 indie clones in Shopping grossing with 0–400 ratings). The EU Vinted variants are already flooded in DE/GB Shopping charts (PreLoved AI, Vintly, Navi, Vinotify) and overlap the Phase 3 exclusion.
- **Penny-deal, clearance, auction, estate-sale and liquidation apps.** 0 indie winners among aged apps. The 2026 wave (Penny, Drop, DealHawk, Scavenger) has fewer than 100 ratings each.
- **Bible/faith apps (US or localized to BR/MX).** High hit rates, but driven by studios and paid acquisition. US studio apps already hold BR/MX Reference #1–2.
- **"Earn your screen time" blockers, including Brazil gambling blockers.** The 2026 flood has 1–2% hit rates. Bet Block's 2.5k BR ratings do not show up in BR grossing charts, so it does not monetise.
- **Paid-upfront consumer apps.** 0 of 182 reached 1k ratings.
- **Class-action settlement finders.** US flood of 6+ apps (Settlemate 75k ratings); aged hit rate 6%. Outside the US, class actions are scarce.
- **Gig-driver profit tools (US/BR).** US: 117 new apps, none ≥1k. BR: 16 new, the best at 596 ratings.
- **Tanning/UV and aurora weather niches.** 117–135 new entrants, studio-led (Beam Tanning, TITANO). Aurora: 0 aged ≥1k.

## 7. Ranking, deep-diligence picks and decisive assumptions

1. **A1 Trend-timed collector value scanner micro-studio.** Strongest measured pattern: cohort data across 4 clusters, named indie winners, cross-storefront chart presence.
   - Decisive unverified assumption: an outsider can hit the early window and acquire users through organic video before studio clones arrive.
2. **A2 Prediction-market companion (US).** Live early window. A newcomer reached Finance grossing #40 in about 6 weeks.
   - Decisive unverified assumptions: users pay for third-party research, and Kalshi/Polymarket API terms permit commercial apps.
3. **A3 Non-US amateur-sport organiser portfolio.** Low risk and low ceiling.
   - Decisive unverified assumption: a low Sports-grossing rank equals at least about $20/day.
4. **A4 Cruise price-drop monitor.** Weakest: a single datapoint plus data-access risk.

**Top 2–3 for deep diligence:** A1, A2, then A3.

**Cross-cutting unknown to resolve first:** the dollar value of category grossing ranks (US Shopping, Reference, Finance; BR/DE Sports). The one verified calibration point is US Sports #75 at about $86k over 30 days (PropGPT). Small-genre thresholds are likely far lower and remain [Unknown]. Two WebSearches found no public mapping.

**WebSearch count:** 6 of 6 (P8-A).

**Sources:**
- [RevenueCat SOSA 2026 insights](https://www.revenuecat.com/sosa-26-insights/)
- [TrustMRR: PropGPT](https://trustmrr.com/startup/propgpt-ai-props-analysis)
- [TrustMRR: hidden mobile app](https://trustmrr.com/startup/hidden-mobile-app)
- [TrustMRR: Mobile Apps category](https://trustmrr.com/category/mobile-apps)
- [Starter Story: PropGPT growth channels](https://www.starterstory.com/businesses/propgpt-670445/growth-channels)
- [Screensdesign: ThriftAI](https://screensdesign.com/showcase/thriftai-profit-identifier)
- [MacStories: The Shape of the App Store](https://www.macstories.net/linked/the-shape-of-the-app-store/)
- [Mobile World Live: Distimo App Store rankings explained](https://www.mobileworldlive.com/apple/app-store-rankings-explained-distimo/)
- [AppRadar: Top grossing apps](https://appradar.com/blog/top-grossing-apps-app-store)
- Apple iTunes Search/Lookup API and RSS feeds (itunes.apple.com), accessed 2026-10-13.
