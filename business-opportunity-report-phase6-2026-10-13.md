# Phase 6: Owned and Direct Distribution

**Date:** 2026-10-13
**Branch:** `local-research-phase6-10` (local continuation of Phases 1–5; the cloud `research` branch was not used)
**Working files:** `research-notes/phase6/` holds the six agent reports, the leader re-check, the shortlist audit, the red-team report and the shortlist.

---

## Bottom line

**No Phase 6 idea reaches the top of the cumulative board.**
- The best new candidate is **pay-per-call lead sites for emergency home-service trades (L6), at 48.8**. Water damage and biohazard are examples.
- It sits about 8 points below the leader and about 2–4 points below the #2–#10 cluster.

**The most important result is again a correction, this time to the leaders.** Phase 5's newcomer test (what do *new* sellers actually get?) was applied to five leaders whose channels had never been measured. Four of the five went down:

| Leader | Phase 5 | Phase 6 | Why |
|---|---|---|---|
| H6 college-baseball data API | 57.2 | **52.2** | The only comparable success, CFBD, had 43–416 paid patrons over its first 4½ years. 13 other sports-data creators on Patreon have 8–447. A $7.99 paid NCAA baseball API and a free daily dataset already exist. NCAA terms forbid commercial use of its stats. |
| K8 Framer kit | 53.2 | **52.0** | A consistency correction. Phase 5 credited Framer's $6.5M creator payouts as channel evidence, a standard Phase 5 itself dropped for H7 and J7. |
| H1 Meshtastic kits | 54.6 | **51.2** | 2-packs now exist (Rokland). Amazon's branded "communicator" nodes closest to the kit's price have 0–39 ratings. |
| monday.com invoicing app | 52.0 | **50.8** | Israeli invoicing vendors' own marketplace apps have 0–16 reviews. |
| K13 Hebrew tender intelligence | 53.6 | **50.6** | Ifat Tenders already covers receiver and liquidator tenders and already offers AI summaries. kones.co.il sells receivership listings at ₪249/month. |

**After the corrections:**
- Blender add-ons (H7, 56.6) are nominally #1.
- The next nine ideas sit between 50.6 and 52.6.
- H7's 4-point lead is still inside the roughly 5-point noise band, so **there is no evidence-backed leader.**

**The cross-cutting finding is now much stronger.** Phase 6 measured newcomer outcomes on four more channels:

| Channel | What newcomers get |
|---|---|
| Skool paid communities | Median **11 members** for new paid groups (n=454, upper bound from a "trending" sample) |
| UK G-Cloud | **86%** of listed suppliers earned nothing (Tussell, G-Cloud 10). Every small winner sampled was 10+ years old. |
| Lead-gen and content sites | Sales of these sites collapsed after 2023 on Empire Flippers. Google is moving local-service leads into its own ads. |
| Seeker-paid job search | The one verified newcomer success, Ton-piston, was carried by its founder's 51.6k-follower audience. |

The pattern from Phase 5 now holds on 11 channels: **channels pay incumbents and people who bring an audience; a newcomer without one gets close to nothing.** The founder's scarce asset is distribution, not product-building capacity.

---

## 1. Research methodology

**Unchanged:**
- Six independent discovery agents (A–F).
- A merged shortlist of 13.
- An independent Evidence Auditor, here split into two instances: one re-checked earlier leaders, one audited the shortlist.
- An independent Red-Team Investor.
- Rescoring with the frozen Phase 3 rubric: Balanced = 0.4·CF + 0.4·Scal + 0.2·Dist, minus a 0–15 evidence penalty.
- No weights, criteria or penalty ranges were changed.

**One transparency improvement:** Phases 3–5 published only criterion totals. From Phase 6, every new score is published at criterion level (section 6). Corrections to old scores are stated as named criterion steps of weight/5 points, the method Phase 5 used.

**Search budget.** The quota worked again in this phase.

| Role | Searches |
|---|---|
| Discovery agents A–F | 8 each (48) |
| Leader re-check auditor | 8 |
| Shortlist auditor | 5 |
| Red team | 7 |
| Research Director | 1 |
| **Total** | **69** |

All searches are logged in `research-notes/search-log.txt`.

Most evidence came from primary pages and public data:
- the Skool discovery JSON (about 2,300 groups);
- the Substack leaderboard API;
- the UK Contracts Finder OCDS API (213 G-Cloud call-offs) and the gov.uk G-Cloud spend CSV;
- the Empire Flippers listings API;
- the WordPress.org plugins API;
- SEC EDGAR (Angi 10-Q, distributor gross margins);
- TrustMRR verified-revenue pages;
- Graphtreon history pages;
- Israeli price-comparison pages (Zap).

**Blocked sources:**
- Capterra, G2, BizBuySell, Trustpilot, Tindie, d1baseball, stats.ncaa.org, monday.com support and marketplace pages, and Ifat's price endpoint.
- Several US city backflow pages and tuvsud.com.
- Skool rate-limited Agent A temporarily. The agent paused and resumed more slowly; nothing was bypassed.

**Boundaries kept:** no browser or signed-in account, nobody contacted, nothing bought, built or deployed, no logins or sign-ups.

---

## 2. Research direction and why

**What Phases 1–5 left open:**
1. The top of the board was mostly low-capital digital goods sold through open marketplaces or one incumbent's audience (H7, H6, J7, K8, the monday app). Phase 5 showed that newcomers on such marketplaces earn close to nothing, and four leaders had never been checked that way.
2. No idea had any measured customer-acquisition cost. Ideas that sell direct (K13, K6, J1) were scored on hypotheses.
3. Recurring themes had become a bias: Israel-diaspora affinity niches (Phases 3–5), compliance deadlines (Phases 1–2) and marketplace digital goods (Phases 3–5).
4. Whole business models had never been examined:
   - lead generation and pay-per-lead;
   - owned-audience media and job boards;
   - B2B distribution and wholesale;
   - buying businesses above the $2k micro tier;
   - licensing and white-labelling;
   - non-English markets outside Israel.

**Phase 6 direction: "owned and direct distribution".** I looked for businesses that do not depend on ranking in an open marketplace, and where there is measurable evidence that small or new operators acquire customers through the channel. A dedicated auditor re-checked the five unmeasured leaders in parallel.

| Agent | Phase 6 assignment |
|---|---|
| A Consumer | Paid communities, courses and newsletters; search-intent consumer services; non-English, non-Israeli consumer markets |
| B Physical | B2B consumables, exclusive regional distribution of foreign brands, replenishment |
| C Traditional | Lead generation and brokerage in traditional trades; buying an existing small business with seller financing |
| D Software | Software sold direct to buyer populations that can be counted from public registries |
| E Distribution | Channels with measurable newcomer economics: job boards, sponsorship, reseller programmes, public procurement frameworks |
| F Contrarian | Buying under-monetised digital assets; licensing proven foreign products; 2025–26 structural shifts |

---

## 3. Research universe (about 40 distinct ideas)

| Agent | Viable ideas (key evidence) | Killed (reason) |
|---|---|---|
| **A Consumer** | **Elterngeld application concierge for non-German-speaking parents** (654,241 German births in 2025; Finanztest rated commercial advisers best; €169–329 packages) · **Spanish-language AI-agents community with a native co-host** (new paid Spanish "claude" groups: median 136 members) · **Operator partner for hobby-expert communities** (new dog groups: 7 of 29 ≥ $2k implied MRR) · MPU (driving-licence assessment) prep in Turkish, Russian or Arabic (70,135 MPUs in 2025, falling) | Paid flight alerts outside the US (local leaders are free) · US name-change kits (incumbents own the channel) · Life-event communities (median 5.5–11 members) · Mexican visa help (scam stigma, $25–160) · A Substack newsletter run without a public face · Brazil infoproducts |
| **B Physical** | **Bulk 3D-printing filament for Israeli print farms** (Bug 109 ₪/kg vs Bambu $11.19/kg) · DTF/sublimation consumables for print shops · **First authorised Israeli distributor of EU professional brands** (import reform verified) · Dental and jewellery resin · Winemaking inputs · Café cleaning supplies | Lab consumables (exclusive distributors) · Clinic hygiene (21% margins, Ministry of Health registration) · Cheap light consumables (the $75 VAT-free threshold) · Distribution in Eastern Europe or Latin America (needs brand contact) · Ordering portals (already in the ledger) · Tattoo supplies |
| **C Traditional** | **Pay-per-call / exclusive lead sites for emergency trades** (Lead Smart bid table; Google LSA cost per lead about $53; Angi revenue −12%) · Remote booking agency for independent instructors (one listing) · Senior-living placement · Buying a lead-gen site · Hebrew lead-gen · Buying an offline business | Personal-injury leads · Medicare leads · Bark/Thumbtack clone · Moving leads · Reselling leads in trades where Google now sells leads itself · Israeli lawyer referral fees |
| **D Software** | **Backflow-test tracking for small US water utilities, paid by testers per report** (BSI $15.95, SwiftComply $7.50) · Grease-trap/septic reporting · **Small-cemetery records and mapping** (Cemify $799–1,899/yr, profitable) · UK driving-instructor app · German driving-school admin | Appraisal forms (Reggora is free) · Microschools · Firearms-dealer records · Funeral homes (crowded) · Flight schools · Tester-side backflow app · Lists of newly licensed professionals |
| **E Distribution** | **G-Cloud micro-SaaS for one UK public-sector workflow** (213 call-offs in 2026; awards of £14–55k) · **G-Cloud reseller for non-UK SaaS** · Association career centres · **Seeker-paid local-language job search** (Ton-piston $9.8k MRR) · Public-sector award digest · City media for language communities | Employer-paid tech job boards (LaraJobs: 6 posts in 30 days) · Non-tech niche boards (free listings) · Israeli government procurement (sole-supplier exemptions) · AppSumo · Ad slots sold to indie makers · Generic affiliate programmes |
| **F Contrarian** | **Taking over abandoned high-install WordPress plugins** (161 plugins with ≥10k installs and no update in >2 years) · **Buying and modernising aged apps** (Flippa: about 2.1× annual profit) · Newsletter acquisition · Aged micro-SaaS · Board-game localisation licences (about $27k per title) · AI-assisted translation rights | Sub-$50k SEO and affiliate sites (Empire Flippers sales: 458 in 2022–24 vs 76 in 2025–26) · Moving bought apps to web checkout (RevenueCat: web 18.1% vs in-app 27.0% conversion) · Payments from AI crawlers · AI micro-SaaS under a year old · Machine translation of licensed books (model contracts bar it) |

**Market-level facts established in this phase:**
- **Buying businesses doesn't fit the budget.**
  - BizBuySell Q1 2026: median offline business sale $350k, with a 2.7× cash-flow multiple.
  - Empire Flippers: no listings under $50k.
  - Flippa: about 1.4–2.1× annual profit, with only about 10–20% of sub-$50k listings both over a year old and verified.
  - Seller financing below $100k is rare.

  Buying $1k/month of profit costs about $24k.
- **Distributor gross margins** from SEC filings: Patterson 21%, Henry Schein 31%, Grainger and MSC 39–41%, Fastenal 45%.
- **Israel's VAT-free threshold for personal imports is $75 again** (Knesset, June 2026). Stocking cheap, light consumables locally makes no sense.
- **Google Business Profile rules make lead-gen agents and virtual offices ineligible.** Google Local Services Ads become pay-per-lead Performance Max campaigns from August 2026 in US core trades.

---

## 4. Shortlist (13)

| # | Business | Paying customer | Spending evidence | Main competition | Differentiation | Acquisition | Capital | Main risk |
|---|---|---|---|---|---|---|---|---|
| L1 | Elterngeld concierge for international parents (Germany) | Expecting parents in Germany | Finanztest; €149–329 packages | Einfach Elterngeld (€24.95 software, English UI), Elterngeldexperten (EN/FR), Elterngeldhelden (EN/IT), free counselling | Turkish, Arabic, Russian, Ukrainian; cross-border cases | Search, expat groups, midwives | <$2k | RDG (BSG B 10 KG 1/18 R) |
| L2 | Spanish-language AI-agents community with a native co-host | Spanish-speaking small-business operators | New Skool groups: median 136 (upper bound) | 12+ new Spanish groups; 662 English | A real builder plus a vertical angle | Co-host's audience | <$1k | Finding a co-host; churn; fad |
| L3 | Operator partner for hobby-expert communities | Hobbyists, via expert partners | Base rate 18.5% ≥ $2k implied MRR | Skool agencies | Revenue share; partners chosen by data | Partner outreach | ~$0 | Agency drift; partners leave |
| L4 | Bulk filament for Israeli print farms | Farms, maker labs, schools | Retail volume on Zap | Bug, CopyTech, Ivo; self-import | 10 kg packs, auto-reorder | Zap, maker groups | $2.5–4k | Self-import lands at about 53–62 ₪/kg |
| L5 | First Israeli distributor of EU professional brands | Israeli professionals | Import reform only | Unknown | Exclusivity | Unknown | Over budget | No brand, no terms |
| L6 | Pay-per-call lead sites for emergency trades | Restoration contractors, via networks or direct | Angi 10-Q; LSA cost per lead; Lead Smart bid table | 10,000+ network publishers; Google LSA; Angi | Direct sale to contractors in the second stage | Organic SEO (no Business Profile) | <$1k | Google; realised payouts $40–110 per call |
| L7 | Backflow tracking, tester-pay (US/Canada) | Small water utilities and certified testers | BSI $495–8,995/yr plus $15.95–23.95 per report; SwiftComply $7.50 | BSI (patent), SwiftComply, VEPO, Tokay | Free to the utility; AI import of paper records | Direct to utilities (EPA list) | Insurance, US entity | No price wedge; municipal sales cycle |
| L8 | Small-cemetery records and mapping | US non-profit cemeteries | Cemify, Chronicle, PlotBox | Cemify at the low end | AI transcription of ledgers | Mail to state registries | <$2k | Slow acquisition; thin edge |
| L9 | Taking over abandoned WordPress plugins (Brazil first) | WooCommerce stores in Brazil | WordPress pro tiers generally | Maintained replacements (Melhor Envio 10k, Infixs 4k, official PagBank) | Existing installed base | Upsell inside the plugin | ~$0 | Author consent; trademarks; users migrating away |
| L10 | G-Cloud micro-SaaS for one workflow | UK councils, NHS, fire services | Verified call-offs of £14–55k | 1–3 incumbents per niche; suites | Price, fast onboarding | G-Cloud catalogue | £1m/£1m/£5m insurance | **Cannot list until about Feb 2028**; 86% of suppliers earn nothing |
| L11 | G-Cloud reseller for non-UK SaaS | UK public bodies | Reseller wins of £110–190k | Softcat, SCC, Generation Digital | Small foreign vendors | Two-sided outreach | UK Ltd, insurance | Same reopening block; margins unknown |
| L12 | Seeker-paid local-language job search plus AI | Students and junior job seekers (DE/PL/BR) | Ton-piston $9.8k MRR | Indeed, StepStone, free AI tools | Local language | Paid acquisition or SEO | <$2k | No audience; churn; scraping law |
| L13 | Buying and modernising aged apps | App users | Flippa P&Ls (seller claims) | Other buyers | Technical rebuild | Installed base | $6–25k+ | Over budget; no data on post-purchase uplift |

---

## 5. Adversarial review (auditor + red team)

### New candidates

| Idea | What held up | What was contradicted or weakened | Hard blocker? | Effect |
|---|---|---|---|---|
| L1 | Category spending; prices; 654k births | Finanztest is from issue 1/2023, not 2024. The test winner now sells **€24.95 form-filling software in English**. English and French service already exist. Elterngeldexperten runs the partner-midwife channel L1 planned to use. **BSG ruling B 10 KG 1/18 R (2019): helping with a Kindergeld application is an unlicensed legal service under the RDG.** | Possibly (the RDG question needs a German lawyer) | **Down** |
| L2 | The Skool figures replicate exactly from the saved data | Figures are an upper bound from a "trending" sample (one 215-member group had 1 member online); depends on a co-host who doesn't exist yet | No | Hold |
| L3 | Base rates replicate | Operator "lift" untested; drifts into agency work | No | Down |
| L4 | Retail price gap is real (Zap cheapest 84 ₪/kg) | Self-importing 10 kg lands at about 53–62 ₪/kg, roughly the planned sale price. Bambu sells bulk directly (about $14/kg US, about €11.50/kg DE, snippets). Farms are exactly the buyers most able to import themselves. | Near-fatal for margin | **Down sharply** |
| L5 | Reform verified | No brand, terms or demand | — | **Kill** |
| L6 | Contractors pay for leads (Angi 10-Q, LSA cost per lead); payout tables exist | The "$213 median" is a minimum bid per ZIP row, not realised earnings (it fell to $189 within weeks). Lead Smart's buyer list has no water-damage or biohazard vertical. CallScaler's typical payout is $35–90. Lead Smart has 10,000+ publishers, mostly in Pakistan and India. Business Profile rules exclude lead-gen agents; LSA migration verified. | No (organic-only path survives) | Down, but still best of batch |
| L7 | Per-report fees verified; EPA list of 148k public water systems | BSI charges *utilities* $495–8,995/yr plus tester fees, so "free to the utility" saves a small town as little as $495/yr. At least 2 of 9 sampled programmes don't charge testers. **BSI holds a US patent on the concept.** It is still signing new cities in 2024–26. | Patent scope unknown | Down |
| L8 | Cemify prices, profitability and size verified; NY has about 1,700 cemeteries | "Hundreds of cemeteries in 8 years" means acquisition is slow | No | Down |
| L9 | Install counts verified (60k/20k/10k) | The author is active (Liquid Web, WooCommerce core) and **parked the plugins** rather than abandoning them. Maintained Brazilian replacements exist. Adoption needs the author's consent or 30 days of silence, and trademark owners (WooCommerce, PagSeguro, Correios) are a listed reason for denial. | Consent is decisive | Hold, lower |
| L10 | Award examples verified via the API; insurance needs are £1m indemnity, £1m public liability and £5m employer's liability (the "£75m" was wrong, and applies to Lot 1b only) | **G-Cloud 15 started 6 Aug 2026 and reopens only after 18 months, about Feb 2028** (gca.gov.uk RM1557.15). Tussell: "86% … did not earn any revenue". Most sampled awards are incumbent renewals. | **Timing blocker until about 2028** | Down |
| L11 | Reseller wins verified | Same reopening block; margins and vendor appetite unknown | Timing | **Kill** |
| L12 | Ton-piston verified ($9,770 MRR, 936 subscriptions) | Revenue is fading (last 7 days about $7.4k/month annualised) and depends on the founder's audience; "founded" date is self-entered | No | Down |
| L13 | Listings and multiples verified | Capital 5–25× the budget; profits are seller claims; no data on post-purchase uplift | Capital | Down / park |

### Leader re-check: decisions

Both reviewers agreed with the direction of every correction. Where the three reviewers differed, I took the position closest to their median and kept the method traceable.

| Leader | Criterion changes adopted (points) | CF / Scal / Dist | Balanced | Penalty | Adjusted |
|---|---|---|---|---|---|
| H6 | Proven channel −1 (−6), Scalable acquisition −1 (−4), Defensibility −1 (−3) | 75 / 59 / 58 | 65.2 | 12→13 (NCAA terms partly contradict the data-rights assumption) | **52.2** (was 57.2) |
| H1 | Proven channel −1 (−6), Defensibility −1 (−3) | 61 / 49 / 71 | 58.2 | 6→7 | **51.2** (was 54.6) |
| monday app | Proven channel −1 (−6) | 74 / 64 / 48 | 64.8 | 14 | **50.8** (was 52.0) |
| K13 | Defensibility −2 (−6), First customers −1 (−3). The leader auditor's spending-evidence +1 was **not** adopted, because list prices are not transactions. | 74 / 60 / 55 | 64.6 | 14 | **50.6** (was 53.6) |
| K8 | Proven channel −1 (−6), for consistency with the H7/J7 standard: the Framer $6.5M payout total cannot be credited without newcomer outcome data | 84 / 56 / 45 | 65.0 | 13 | **52.0** (was 53.2) |
| H7 | No change. Its Phase 5 correction already used measured newcomer data, and no new contradiction was found. The red team argued for 54.5–56.0; I note this as a dissent. | 80 / 58 / 67 | 68.6 | 12 | **56.6** |

**Dissents recorded:**
- **H6:** the leader auditor proposed 51.6, also cutting first customers. The shortlist auditor called that double counting. I adopted 52.2.
- **H1:** the red team proposed a penalty of 9 (49.2); the shortlist auditor proposed keeping 6 (52.2). I adopted the middle position (penalty 7, 51.2).
- **H7:** see the red-team dissent above.

---

## 6. Phase 6 scoring (frozen rubric, criterion level)

**Points per criterion step:**

| Score | Step value per criterion |
|---|---|
| Cash flow | Spending ×5 · Speed ×4 · Capital ×4 · Margin ×4 · Labour independence ×3 |
| Scalability | Depth ×3 · Recurring ×4 · Acquisition ×4 · Leverage ×4 · Defensibility ×3 · Founder fit ×2 |
| Distribution | Clarity ×4 · Discoverability ×4 · Proven channel ×6 · First customers ×3 · Beyond founder ×3 |

Each cell below shows the 0–5 step scores for the criteria in that order.

| ID | CF steps | **CF** | Scal steps | **Scal** | Dist steps | **Dist** | Balanced | Penalty | **Adjusted** |
|---|---|---|---|---|---|---|---|---|---|
| L6 Pay-per-call lead sites | 4,1,4,4,4 | 68 | 4,3,2,4,1,4 | 59 | 4,3,2,2,3 | 55 | 61.8 | 13 | **48.8** |
| L2 Spanish AI-agents community | 4,2,5,3,2 | 66 | 3,4,2,2,1,3 | 50 | 4,3,3,2,3 | 61 | 58.6 | 12 | **46.6** |
| L10 G-Cloud micro-SaaS | 5,0,3,5,3 | 66 | 3,5,1,4,2,3 | 61 | 2,2,2,0,3 | 37 | 58.2 | 12 | **46.2** |
| L9 WordPress plugin takeover | 2,1,4,5,4 | 62 | 2,4,2,4,1,5 | 59 | 4,4,1,1,3 | 50 | 58.4 | 13 | **45.4** |
| L7 Backflow tester-pay platform | 4,0,2,4,3 | 53 | 3,5,1,4,2,3 | 61 | 5,4,2,1,2 | 57 | 57.0 | 12 | **45.0** |
| L12 Local-language job search | 3,3,4,4,4 | 71 | 4,2,1,4,1,4 | 51 | 4,2,1,2,2 | 42 | 57.2 | 13 | **44.2** |
| L8 Cemetery software | 3,1,4,4,3 | 60 | 2,5,1,3,1,3 | 51 | 5,4,1,2,2 | 54 | 55.2 | 12 | **43.2** |
| L1 Elterngeld concierge | 4,3,4,3,2 | 66 | 3,1,2,3,1,1 | 38 | 5,4,2,2,3 | 63 | 54.2 | 12 | **42.2** |
| L13 Aged-app acquisition | 3,3,0,3,4 | 51 | 3,3,2,4,1,5 | 58 | 3,3,2,3,3 | 54 | 54.4 | 13 | **41.4** |
| L3 Community operator partner | 3,2,5,3,1 | 58 | 3,4,1,2,1,3 | 46 | 3,3,2,2,2 | 48 | 51.2 | 12 | **39.2** |
| L4 Bulk filament (Israel) | 3,3,1,2,2 | 45 | 1,4,2,2,0,2 | 39 | 4,3,2,2,2 | 52 | 44.0 | 13 | **31.0** |
| L11 G-Cloud reseller | 4,0,3,2,2 | 46 | 3,3,1,2,1,2 | 40 | 2,2,1,0,1 | 25 | 39.4 | 13 | **26.4** (kill) |
| L5 First Israeli distributor | 2,1,1,3,2 | 36 | 3,4,1,2,3,1 | 48 | 2,2,1,1,1 | 28 | 39.2 | 14 | **25.2** (kill) |

**Notes on the most important judgement calls:**
- **L10:** spending evidence is the strongest of any idea in Phases 1–6 (5/5: verified award notices with buyer, value and date). But speed to first sale and first customers score 0, because listing is impossible until about February 2028 and 86% of listed suppliers earn nothing. Customer clarity is 2/5 because no specific workflow has been identified yet.
- **L6:** spending evidence 4/5 rests on the Angi 10-Q and LSA cost-per-lead data, not on the network bid table. Proven channel is 2/5: networks do buy calls, but how quickly a new site ranks organically is unmeasured.
- **L1:** recurring revenue is 1/5 (a one-time purchase with some cross-sell). Founder fit is 1/5 (no German).
- **L9:** a large existing install base earns discoverability 4/5. Proven channel and first customers are 1/5, because the takeover itself is gated by the author's consent and the users are already moving to maintained replacements.
- **Penalties:** all are in the historical 12–14 band. None got less than 12, because every idea's decisive assumption is unverified.

**Comparison with the two reviewers' independent ranges:**
- 11 of 13 scores fall inside or within 1 point of the red team's ranges.
- The two exceptions are L10 (46.2 vs 44–48, inside the range) and L12 (44.2 vs 40–44, 0.2 above it).

---

## 7. Five finalists: deep dives

**How they were chosen:** the top five by Adjusted score are L6, L2, L10, L9 and L7. They also cover all three objectives. L1 is noted as a conditional sixth, depending on a legal opinion.

### F1. Pay-per-call lead sites for emergency home-service trades (L6): 48.8

- **Offer:** a small network of organic-only sites for water-damage restoration, biohazard/trauma cleanup, fire restoration and mould remediation. Each site serves one metro area and one trade, built with original, useful content and published honestly as a referral service, with **no fake Google Business Profile**.
  - **Stage 1:** route calls through a pay-per-call network.
  - **Stage 2:** once a site produces steady calls, sell them exclusively to one local contractor per metro at a monthly rate or per qualified call.
- **Customer:** restoration contractors (through the network, then directly).
- **Spending evidence:**
  - Contractors already buy leads at scale. Angi's Q2 2026 10-Q shows the incumbent is shrinking: US revenue −12%, active pros −17%, leads −13% [Verified: SEC EDGAR].
  - Google LSA blended cost per lead is about $53, with roofing about $107 and water damage about $215 [Secondary: SearchLight Feb 2026; vendor 99 Calls].
  - Realised network payouts are probably **$35–110 per qualified call** [CallScaler typical $35–90; Lead Smart's bid table is a minimum offer, not realised earnings].
- **Competition:**
  - 10,000+ network publishers, largely offshore.
  - Google itself, which now sells local-service leads through ads.
  - Angi, Thumbtack and Bark.
  - National restoration franchises with their own ad budgets (Servpro, ServiceMaster).
- **Entry strategy:** high-ticket, low-frequency emergency trades where buyers search urgently. Organic content only. Monetise directly once the calls exist, keeping the network's cut (Agent C's evidence suggests networks keep about 60–80%, from vendor figures).
- **Startup capital:** about $150–300 per site in domains and hosting; under $1.5k for 5–8 test sites. Content is AI-assisted with human editing.

**Economics [Hypothesis; payouts from the ranges above]:**

| Scenario | Months 9–12 | Owner profit |
|---|---|---|
| Downside | Sites don't rank in 9–12 months | **−$1.5k** sunk, plus time |
| Base | 40 billable calls/mo × $60 network payout | **~$2.2k/mo** |
| Upside | 8–10 metros sold directly at $100–150/call, 150 calls/mo | **$12–18k/mo** (direct sales take founder time) |

- **Labour:** about 10 hours/week for 6 months building content, then 2–4 hours/week. Direct sales to contractors are founder labour until delegated.
- **Key assumptions:**
  1. A new organic-only site in 2026 can reach the top 3–5 results for metro-level emergency queries despite AI Overviews and Google's own ads.
  2. Networks accept Israel-based publishers.
  3. Realised payouts are at least $50 per qualified call.
- **Limitations:** no newcomer data on lead-site ranking times. Phase 6 only knows the post-2023 collapse in content-site sales, which is a negative signal.

### F2. G-Cloud micro-SaaS for one narrow UK public-sector workflow (L10): 46.2

- **Offer:** a single-workflow cloud tool (booking, licence checks, registers, policy libraries) for councils, NHS trusts and fire services, priced at about £6–12k a year against incumbents' £15–45k. It would be sold through the G-Cloud 15 catalogue and direct award.
- **Spending evidence (strongest in all phases):**
  - **213 verified 2026 call-offs,** 108 of them to SMEs.
  - Small niche awards of £14,304–£50,900 to named suppliers [Verified: Contracts Finder OCDS API].
  - G-Cloud runs at about £3bn a year.
  - In the 2018 spend data, the 2017 micro/small newcomer cohort billed a median of £62k in their second year, but 45 of 178 billed nothing [Verified: gov.uk CSV].
- **Barriers:**
  - **G-Cloud 15 reopens to new suppliers only after 18 months, about February 2028** [Verified: gca.gov.uk RM1557.15].
  - 86% of G-Cloud 10 suppliers earned nothing [Verified: tussell.com].
  - Every small winner sampled was incorporated 1999–2016.
  - Insurance: £1m professional indemnity, £1m public liability, £5m employer's liability. Cyber Essentials, UK hosting, WCAG accessibility and a DPIA pack are also needed.
- **Entry strategy:**
  - Use the award data (renewal dates, values, incumbents) to find a workflow with 10 or more awards a year under £50k and only 1–2 incumbents.
  - Prepare for the 2028 reopening.
  - Meanwhile test whether below-threshold direct purchases outside G-Cloud are possible [Unknown; the Procurement Act 2023 rules for low-value buying were not checked].
- **Startup capital:** about £1–3k for a UK Ltd, Cyber Essentials and insurance (premiums unknown), plus build time.

**Economics [Hypothesis]:**

| Scenario | By when | Revenue / profit |
|---|---|---|
| Downside | No award by 2029 | −£2–4k |
| Base | 3 contracts × £10k/yr by 2029 | about £30k/yr (**~$3k/mo**) at 85–90% margin |
| Upside | 15 contracts | **£150k/yr** (Track B) |

- **Labour:** low per contract, but founder-heavy in sales and assurance.
- **Key assumption:** a buyer will direct-award a new, reference-less supplier when its incumbent comes up for renewal. Every observed award says buyers prefer incumbents.

### F3. Spanish-language AI-agents community with a native co-host (L2): 46.6

- **Offer:**
  - A paid community at $29–59 a month, plus $300–600 cohorts, teaching small-business operators to build automations and agents (Claude Code, n8n).
  - Ideally with one vertical angle, such as Spanish-speaking real-estate agents or accountants.
  - The founder builds the curriculum and does live builds; a native co-host with an audience fronts it for a revenue share.
- **Evidence:**
  - **The only newcomer outcome data in this exact niche:** 12 new paid Spanish "claude" groups, median 136 members, 8 at ≥ $2k implied MRR [Verified: Skool JSON, 2026-10-13; upper bound].
  - English is saturated (662 groups).
  - Across all English paid groups, new ones have a median of 11 members.
- **Competition:** 12+ new Spanish groups in a year, mostly marketers reselling prompts.
- **Entry strategy:** real technical depth plus a vertical focus.

**Economics [Hypothesis]:**

| Scenario | Members | Owner profit |
|---|---|---|
| Downside | 20 × $45 | about $350/mo after a 50% co-host share |
| Base | 150 × $45 = $6.75k MRR | **~$3k/mo** |
| Upside | 600 members | **~$12k/mo** |

- **Labour:** 8–12 hours a week of live sessions and content.
- **Key assumptions:** a Spanish-language creator with 20–50k followers will partner on a revenue share, and monthly churn stays under about 10%. Retention data does not exist yet. Re-pulling the saved Skool cohort in 60 days would measure growth and death rates cheaply.

### F4. Taking over abandoned high-install WordPress plugins (L9): 45.4

- **Offer:** adopt stale WordPress.org plugins with large active install bases, modernise them, and add a paid pro tier at about $49–99 a year.
- **Evidence:**
  - **161 plugins with ≥10k installs and no update in over 2 years** among the 5,995 most popular [Verified: WordPress.org API].
  - The named Brazilian cluster has 60k, 20k and 10k installs.
  - **Contradictions:** the author is active and parked the plugins. Maintained replacements exist. Takeover needs consent or 30 days of no reply, approval is "not guaranteed", and trademark owners are a listed reason for denial [Verified: developer.wordpress.org].
- **Entry strategy:** screen all 161 for plugins that have **no maintained replacement and no trademark in their name**. That screening is free desk work and the obvious next step.

**Economics [Hypothesis]:**

| Scenario | Outcome | Owner profit |
|---|---|---|
| Downside | No adoption granted | $0 cash, time lost |
| Base | One 30k-install plugin, 0.5% pay $69/yr (150 × $69 ≈ $10k/yr) | **~$0.9k/mo** |
| Upside | Portfolio of 4–6 plugins | **$5–8k/mo** |

- **Labour:** support load grows with installs.
- **Key assumption:** stale listings can be adopted, and 0.5–1% of active installs pay. Neither is known.

### F5. Backflow-test compliance platform, paid by testers per report (L7): 45.0

- **Offer:**
  - Utilities pay nothing or a low fee.
  - Certified testers pay about $7–10 per filed report.
  - State-specific forms, plus AI-assisted import of the utility's paper and Excel device records, which is the real barrier to switching.
- **Evidence:**
  - BSI charges utilities $495–8,995 a year **plus** $15.95–23.95 per report from testers.
  - SwiftComply charges testers $7.50.
  - BSI is still signing new cities in 2024–26.
  - The EPA lists about 148k public water systems with contacts [Verified].
- **Barriers:**
  - BSI holds a US patent on the concept (scope unknown).
  - Some utilities pay the vendor themselves.
  - Municipal security reviews and insurance (premiums unknown).
  - A probable 6–18 month sales cycle.
  - Incumbents can match any fee.

**Economics [Hypothesis]:** about $8k a year of contribution per mid-size utility.

| Scenario | Utilities | Owner profit |
|---|---|---|
| Downside | 0 within 12 months | −$1–2k in insurance and entity costs |
| Base | 10 within 24 months | **~$6k/mo** |
| Upside | 40 | **~$25k/mo** (Track B) |

- **Labour:** low once a utility is onboarded; support for testers.
- **Key assumptions:** small utilities will adopt a foreign-owned solo vendor without demands beyond the budget, and BSI's patent does not cover the tester-pay model.

### Conditional sixth: Elterngeld concierge (L1): 42.2

L1 has verified spending, high-intent search demand and delegable delivery. It is held back by:
- the RDG risk from **BSG B 10 KG 1/18 R**;
- €24.95 English-language software from the category's test winner;
- no German-speaking founder.

It should advance only if a €200–400 opinion from a German lawyer confirms the model is lawful.

---

## 8. Cumulative leaderboard (all phases, frozen rubric; * = corrected in Phase 5 or 6)

| Rank | Opportunity | Phase | Adjusted |
|---|---|---|---|
| 1 | Blender/VRChat add-ons (H7) | 3 | **56.6*** |
| 2 | UK MTD prep for accountants | 2 | 52.6 (newcomer re-check still pending) |
| 3 | College-baseball data API (H6) | 3 | **52.2*** (was 57.2) |
| 4 | Framer vertical kit (K8) | 5 | **52.0*** (was 53.2) |
| 5 | Meshtastic family kits (H1) | 3 | **51.2*** (was 54.6) |
| 6 | Hebrew/Russian memoir books (J1) | 4 | 51.0 |
| 7= | monday.com Israeli invoicing app | 1 | **50.8*** (was 52.0) |
| 7= | Apify Actors (J7) | 4 | 50.8* |
| 9= | Hebrew tender + receivership intelligence (K13) | 5 | **50.6*** (was 53.6) |
| 9= | Ketubot (H10) | 3 | 50.6 |
| 11 | Israeli allocation verification | 1 | 49.8 |
| 12 | **Pay-per-call emergency lead sites (L6)** | **6** | **48.8** |
| … | H8 49.4 · H5 49.4 · J2 48.2 · H4 48.2 · J9 48.0 · H9 47.8 · K12 47.6 · **L2 46.6** · **L10 46.2** · **L9 45.4** · **L7 45.0** · … | | |

(Strict order: H8 and H5 at 49.4 rank above L6.)

**Cross-phase verdict:**
- The board is now **flat**: ranks #2–#12 span 50.6–52.6, which is noise.
- H7 is nominally #1, 4 points clear. That is still inside the noise band, and the red team argues it should be lower.
- **No opportunity in Phases 1–6 has evidence that a newcomer like this founder can acquire customers.** That, rather than scoring, is the binding constraint.

---

## 9. Three most promising Phase 6 discoveries

1. **Fastest cash flow: Spanish-language AI-agents community with a native co-host (L2).** Revenue starts the month a co-host launches, there is measured newcomer traction in this exact niche, and capital is near zero.
   - *Key assumption:* a Spanish-language creator with 20k+ followers will partner on a revenue share, and churn stays under about 10% a month.
   - *Runner-up:* L1, if the RDG opinion is clean.
2. **Most scalable: G-Cloud micro-SaaS (L10),** with backflow tracking (L7) as the alternative available now. Both are multi-year public-sector contracts with very high margin and the best verified spending in the research, but both have slow, reference-driven buying.
   - *Key assumption:* a public buyer will award a reference-less new supplier. For L10 that cannot be tested before about 2028.
3. **Best risk-adjusted: pay-per-call emergency lead sites (L6).** Highest Phase 6 score; under $1.5k at risk; the asset is resellable; it can move from network payouts to direct contractor contracts.
   - *Key assumption:* a new organic-only site ranks for metro emergency queries within 9–12 months in 2026's Google, with AI Overviews and Google's own lead ads.

---

## 10. Research limitations

- **Unverified load-bearing facts:**
  - CAC remains unmeasured for every idea.
  - How quickly new sites rank (L6).
  - Scope of BSI's patent and insurance premiums (L7).
  - Whether L1 is lawful under the RDG.
  - Whether WordPress.org will grant adoption (L9).
  - Whether a G-Cloud buyer would award a new supplier, and whether low-value direct purchases outside the framework are possible (L10).
  - Co-host availability and community churn (L2).
- **Sources that blocked fetching:** Capterra, G2, BizBuySell, Trustpilot, Tindie, d1baseball, stats.ncaa.org, monday.com marketplace and support pages, Ifat's price endpoint, tuvsud.com, and several US city pages.
- **Measurement caveats:**
  - Skool member counts are an upper bound on payers, sampled from "trending" sorts, so they overstate newcomer success.
  - Empire Flippers sale dates are approximated by a last-updated field.
  - The Tussell 86% figure is from G-Cloud 10 (2018 data).
- **Scoring caveats:**
  - Phases 3–5 did not publish criterion-level scores, so leader corrections are stated as criterion steps on the published totals.
  - UK MTD prep (now #2) has not had the newcomer re-check. It should be next.
  - The rubric still rewards low capital and high margin, which favours digital ideas.
  - Penalties stayed in the 12–14 band.

---

## 11. Phase 7 direction (decided after this phase)

Phases 5–6 together show the same thing on 11 channels: **acquisition, not product, is the binding constraint**, and open channels reward incumbents and people who bring an audience. Phase 7 will therefore look for businesses where **distribution can be borrowed, contracted or inherited** from parties who already own the customer relationship, rather than built from scratch. Examples:
- white-label supply or build-and-run arrangements for companies, associations, franchisors or distributors who already sell to the end customer;
- revenue-share partnerships with audience owners, measured systematically;
- wholesale to retailers and businesses rather than direct-to-consumer.

Phase 7 will also complete the leader newcomer re-check for UK MTD prep (#2) and J1 memoir books (#6).
