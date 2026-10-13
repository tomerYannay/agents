# Phase 6 — Discovery Agent C (Traditional / offline): lead generation, brokerage, and acquisitions

Date: 2026-10-13. WebSearch used: 8 of 8 (logged as P6-C; 2 returned nothing useful). Most evidence came from uncapped WebFetch/curl of primary pages: the Empire Flippers public listings API, SEC EDGAR (Angi 10-Q), the Google Ads Help Center, and Trustpilot.

**Blocked sources (not inferred around):** BizBuySell (all pages 403), BizQuest (403), Checkatrade (403), Angi IR site (403, so I used EDGAR instead), Flippa API (401) and its lead-gen filter page (useless), Reddit r/RankandRent JSON (403), Yad2 businesses-for-sale (bot wall), homeless.co.il (403), SideHustleNation (bot wall), Midrag pro pricing (not public).

## Key cross-cutting findings (read first)

1. **What lead buyers pay (US home services, 2026):**
   - **Google Local Services Ads (LSA):** blended CPL about $53 (electrical $39, HVAC $51, plumbing $57, drain $59). Source: SearchLight, Feb 2026, 888 contractors, $6.72M spend, 126,650 leads [Secondary: enrichlabs.ai summary of searchlightdigital.io, accessed 2026-10-13].
   - **Year-on-year rise:** 99 Calls reports LSA cost per charged lead up 11–69%. Roofing went $73.62→$106.87, water damage $171.64→$215.31, appliance repair $20.33→$34.35 [Anecdote/vendor, via Lead Smart paid press release, Sept 2026].
2. **What small publishers are paid.** Lead Smart (pay-per-call network, Sept 5, 2026) published median publisher payouts:
   - water damage $213, biohazard $210.50, fire damage $193, roofing CPL $130
   - personal-injury attorney $99, plumbing call $33.25, HVAC $38.50, electrical $24.50
   - all-vertical median $42, top decile above $189.50

   [Anecdote/vendor claim: pr.davisjournal.com Lead Smart release, accessed 2026-10-13].

   The same company's site advertises buyer-side prices of HVAC $135–225 and roofing $155–295 per call [Vendor claim: leadsmartinc.com, accessed 2026-10-13]. **So networks keep roughly 60–80% of what contractors pay.** Owning the contractor relationship is where the margin is. One Empire Flippers seller said this directly: "Previously the Seller worked directly with tradespeople which resulted in higher revenue but more work" (listing 48257).
3. **The incumbent aggregator is shrinking.** Angi Inc. 10-Q for Q2 2026 [Verified: sec.gov/Archives/edgar/data/1705110/000170511026000078/angi-20260630.htm, accessed 2026-10-13]:
   - US revenue down 12% year on year
   - Average Monthly Active Pros 106k vs 126k (−17%)
   - Service requests −6%; leads −13%
   - Network (third-party-site) service requests −38%

   Pros are leaving Angi, which supports the idea that they want alternatives. It is not proof they will buy from a newcomer.

   Bark is not "hated": 112,063 Trustpilot reviews, TrustScore 3.8, 8% one-star [Verified: trustpilot.com/review/bark.com, accessed 2026-10-13]. Thumbtack is private with no data. Midrag (Israel) claims 12,442 rated professionals in 149 sectors [Verified: midrag.co.il/Content/Products, 2026-10-13] and does not publish pro pricing.
4. **Google is changing the local SERP economics now.** LSAs are moving into Google Ads as pay-per-lead Performance Max campaigns. Phase 1 is August 2026 (US plumbing, HVAC, electrical, appliance repair, cleaning, lawn, roofing, pest, moving). Broader US follows in late 2026, and non-US accounts and other categories in 2027 [Verified: support.google.com/google-ads/answer/17213585, accessed 2026-10-13]. Expect more paid-lead inventory above organic results in these categories, which is bad for new SEO lead sites in exactly these trades.
5. **Lead-gen site exit prices are measurable.** I pulled all 26 lead-gen listings from the public Empire Flippers API [Verified: api.empireflippers.com/api/v1/listings/list?monetizations=Lead Gen, accessed 2026-10-13]. 25 sold, 1 for sale.
   - **Multiples:** median 31× monthly net profit for pure lead-gen (n=11), about 2.6× annual.
   - **Small local-trades examples:**
     - 47115: contractor phone-call leads, $712/mo, sold for about $13.5k
     - 48163: contractor directory, 49 call leads in a month, $662/mo, about $15.9k
     - 48257 and 50357: the same 9-site tradespeople network, $1,818/mo (2020) and then $2,464/mo (2021) after a resale. All income came from one revenue-share call buyer, with 1 h/week or less of work.
     - 88006: 13-site plumbing network, $4,318/mo, listed Sept 2025, sold. No content was added for 12 months, but it depends on 8 PBNs the seller keeps renting at $10/site/mo.
   - **Survivorship and age:** these are survivors aged 2–10 years. Only 3 of the 26 were listed after mid-2024, so the flow of lead-gen exits has dried up. I read that as a [Hypothesis] that post-2023 Google updates hurt this class.
   - **Newcomer outcomes are not measurable.** Rank-and-rent income claims are self-reported podcast or blog anecdotes, such as a tree-service site reportedly earning $2k/mo for 8 years, and an Empire Flippers podcast guest claiming over $100k/mo with "rent-first, rank-later".
6. **Buying an offline business at about $2k is not realistic.**
   - **Q1 2026 BizBuySell** [Secondary: smallbiztrends.com, 2026-04-27]: 2,345 sales, median sale price $350,000, median cash flow $165,256, median revenue $713,404, average cash-flow multiple 2.7×. The SBA 7(a) seller note may count toward the down payment only up to 5%, and only on full standby. Citizenship rule changes since March 2026 narrowed SBA access for green-card holders and foreign nationals. 61% of buyers hope for seller financing.
   - **Q2 2026** [Secondary: search summary of eWeek/smallbiztrends]: 2,117 sales, median $349,250, cash flow $155,921, 2.7×. 90% of buyers expect seller financing, but only 29% of sellers plan to offer it and about half refuse.
   - **SBA SOP:** I could not open the SOP text. The SOP 50 10 index shows v8.1 effective Oct 1, 2026 [Verified: legacy.sba.gov SOP index, 2026-10-13].

---

## Opportunities

### C-1. Pay-per-call publisher sites in high-payout emergency verticals (US): own the traffic, sell the calls through networks
1. **Concept:** Build small organic (and later paid) local sites for urgent, high-ticket, low-comparison jobs: water-damage restoration, fire/smoke, biohazard and trauma cleanup, mold, emergency board-up. Route calls through a pay-per-call network, so there are no contractor sales.
2. **Paying customer:** The network (Lead Smart, eLocal-type buyers), and indirectly US restoration contractors. Geography: US metros and suburbs.
3. **Model:** Per qualified call (duration-gated) or per lead. Median publisher payouts are water damage $213, biohazard $210.50, fire $193, mold $65.50 [Vendor claim, Lead Smart, Sept 2026].
4. **Spending evidence:**
   - LSA water-damage CPL $215 [Vendor: 99 Calls, Sept 2026]. Restoration contractors pay heavily for these jobs.
   - Lead Smart claims 10,000+ publishers, more than $50M paid to publishers, and 2.4M calls tracked in 12 months [Vendor claim].
   - Empire Flippers sold call-lead sites with 1 revenue-share buyer earning $1.8–4.3k/mo [Verified, EF API].
5. **Competitors and complaints:** National restoration directories, franchise brands (Servpro, Paul Davis, etc.) that buy their own Google Ads, other call publishers, and LSA/PMax ads above organic results. Contractor complaints about shared Angi-style leads are documented only by vendors. Restoration buyers specifically want exclusive live calls, which is what pay-per-call sells [Hypothesis].
6. **Entry strategy:** Pick the highest-payout, lowest-volume verticals (biohazard/trauma, fire, sewage backup) in second-tier metros, where national players buy ads but organic local results are thin. Use AI-assisted production of genuinely local, compliant pages, plus call tracking. This is a unit-economics bet, not a moat. The honest alternative is "none credible beyond execution and vertical choice".
7. **Acquisition mechanism:** Organic search and Google Maps. Running PPC is possible, but most networks restrict or price it differently. Evidence the channel works: the EF exits above (older sites). **Newcomer outcomes are [Unknown]**, with no public dataset of new sites' time-to-first-call. Two specific threats:
   - A Google Business Profile for a non-existent "business" violates Google's guidelines, so map-pack rank-and-rent is a suspension risk. Organic-only sites are weaker.
   - The LSA→PMax migration (Aug 2026–2027) and AI Overviews push organic results further down.
8. **Capital, ops and restrictions:**
   - Costs: domains, hosting and call tracking at about $30–100/site/mo. The $2k covers 5–10 test sites plus content.
   - Israel operability: yes for the work. Whether a network accepts non-US publishers is [Unknown], to check on network T&Cs.
   - Legal: TCPA does not apply to inbound calls. Restrictions are network quality rules (no misleading brand impersonation).
9. **Labour dependence:** Very high leverage once ranking. The EF sellers report 0–1 h/week. Building is front-loaded founder work that AI tooling helps.
10. **Unit economics:** [Hypothesis] One ranking site producing 8–15 billable calls/mo × about $150 average payout ≈ $1.2–2.2k/mo, at more than 90% margin.
    - **Track A:** needs 2–4 working sites.
    - **Track B:** needs 15–40 sites, or the C-2 direct-sale upgrade. Assets resell at about 31× monthly profit (EF median), which gives an exit value.
    - **Time to first revenue:** [Unknown], plausibly 4–12 months. This is the weak point for "speed to first sale".
11. **Risks:** Google updates and SERP changes (the biggest), network payout cuts (Lead Smart's own data shows payouts swinging month to month), GBP suspensions, call fraud and quality disputes, and the single-buyer concentration seen in the EF listings.

### C-2. Direct-sold exclusive leads to local contractors ("rent-first, rank-later") in trades where Angi is losing pros (US first; UK/AU later)
1. **Concept:** Generate leads in a trade or metro with a cheap paid campaign and then a ranking site. Sell them exclusively to one contractor per territory, for a monthly rent or per exclusive lead. This captures the 60–80% spread the networks keep.
2. **Paying customer:** Owner-operated US contractors with high job values (roofing, restoration, foundation/basement waterproofing, septic, tree removal, garage doors).
3. **Model:** Flat site rent ($500–2,000/mo per anecdotes) or per exclusive lead/call. Pricing would need to beat buyer-side network call prices ($135–295) and compete with LSA CPLs ($39–107) on exclusivity [Hypothesis].
4. **Spending evidence:**
   - Angi Q2 2026: US revenue $200M+ scale, but active pros −17% and leads −13% year on year [Verified: EDGAR]. Pros are spending, and some are churning off Angi.
   - LSA cost per lead is rising 11–69% year on year [Vendor].
   - The EF 48257 seller says direct contractor sales earned more than the network.
5. **Competitors and complaints:** Angi/HomeAdvisor (shared leads sold to 3–8 pros, per vendor blogs), Thumbtack, LSA/PMax, local SEO agencies on retainers, and rank-and-rent operators (popularised by courses, so supply is rising). The complaints are shared leads and paying for non-converting leads. Only vendor sources quantify this, for example one vendor's estimate of cost per booked job: LSA $168, Thumbtack $250, Angi $542 [Anecdote/vendor].
6. **Entry strategy:**
   - **Offer:** exclusive leads, pay only for answered calls of 60 seconds or more, with a month-to-month cancel option. This is a better unit-economics promise than Angi's shared model.
   - **Targeting:** start where a C-1 site already produces calls, so the founder sells proven volume rather than a promise.
   - **Pitch:** use public review counts to find contractors who are visibly not on LSA.
   - **Ad funding:** paid ads only to prove a territory. Paying Google CPCs to resell leads against Google's own LSA at about $50 is thin arbitrage [Hypothesis].
7. **Acquisition mechanism:** Two parts:
   - Demand: same as C-1.
   - Contractor side: cold calls or emails to contractors. These are founder-hours, and with a US time-zone gap can be done from Israel or delegated to an offshore SDR.

   Evidence that the channel produces purchases is only anecdotal (the "rent-first" podcast at over $100k/mo, self-reported 2022; a tree site at $2k/mo, self-reported). Newcomer close rates and churn are [Unknown].
8. **Capital and ops:**
   - Test: $500–1,500 ad spend per territory, plus call tracking and a US phone number.
   - Payment collection: Stripe via a US LLC, or Payoneer; operable from Israel.
   - Restrictions: lead-quality disputes. Some states regulate home-improvement "referral" or "salesperson" roles, which is [Unknown] and per state.
9. **Labour dependence:** Selling and retaining contractors is founder labour at first. Fulfilment (leads) is automated. Revenue can outgrow hours once tenants renew.
10. **Unit economics:** [Hypothesis] One exclusive territory in a high-ticket trade at $1,000–2,000/mo rent. Five territories make about $5–10k/mo, at 80%+ margin after tooling. Track A is plausible. Track B means 15–30 rented territories, comparable to the anecdotal operators.
11. **Risks:** Contractor churn when a slow month hits ("no leads = cancel"), payment collection from small trades, SEO/GBP risk as in C-1, and a crowded rank-and-rent course market (supply side).

### C-3. Remote "booking agency" for independent local instructors or technicians (SEO-driven marketplace taking a margin)
1. **Concept:** Build a branded multi-city booking site where consumers buy a packaged local service, fulfilled by independent contractors who bring their own equipment. The operator keeps the spread between the consumer price and the contractor rate. The model comes from a live EF listing; candidate verticals are driving lessons, in-home swim lessons, piano/tutoring, and mobile bike repair.
2. **Paying customer:** Consumers in the US (the EF case), possibly UK/AU.
3. **Model:** Packages paid upfront online; contractor paid per lesson.
4. **Spending evidence:** EF listing 96995, "driver education" [Verified: EF API, first listed 2026-09-07, for sale]:
   - Revenue $6,471/mo, net $3,113/mo (48% margin); asking $112,057 (36×)
   - About 150 instructors in about 65 US cities
   - A full-time operations manager; owner about 2 h/week
   - Organic search led, after moving from a local to a national domain

   This is one data point, from a seller.
5. **Competitors:** Local driving schools, Thumbtack/Angi categories, and national chains in some cities. What customers dislike is [Unknown].
6. **Entry strategy:** Replicate in a vertical or geography where local providers are fragmented and online booking is poor. A candidate is UK/AU private driving instructors, where instructors are individually licensed [Hypothesis, unverified]. AI-assisted scheduling, dispatch and contractor onboarding keeps ops light. Otherwise "none credible" until a vertical gap is measured.
7. **Acquisition mechanism:** City-by-city organic SEO; Google Ads for "[service] near me". The EF listing proves organic SEO worked for one operator. Newcomer evidence is [Unknown].
8. **Capital and ops:** Low capital ($500–2,000 for sites, ads tests and insurance research). It needs contractor recruitment, vetting, insurance and licensing per vertical. Driver education is state-regulated in the US, and teen driver ed often requires a licensed school, which is [Unknown] per state. It runs remotely with a US-hours ops person.
9. **Labour dependence:** Ops-heavy (scheduling, refunds, contractor churn), but delegable. The EF case uses one full-time manager.
10. **Unit economics:** [Hypothesis, scaled from the one listing] About $6.5k/mo revenue gives about $3k/mo owner profit after a manager. This is Track A. Track B requires multi-vertical or national scale.
11. **Risks:** Contractor misclassification (US 1099 vs employee, for example California's AB5), insurance and liability, regulatory licensing of the service, and contractors disintermediating repeat customers.

### C-4. Senior-living / memory-care placement leads (US): referral-fee brokerage with the highest per-conversion value found
1. **Concept:** A metro-specific senior-living and memory-care guidance site plus a phone advisor. Communities pay a referral fee on move-in.
2. **Paying customer:** Assisted-living and memory-care communities in mid-size US metros.
3. **Model:** A success fee per move-in. Sources give 70–80% of first month's rent, about $3–5k [Secondary: beancount.io blog 2026-07-19], up to 100% of first month rent plus care [Secondary: Senior Housing News, 2017-03-20, verified page]. Texas and Oklahoma require flat fees. Arizona regulates referral-agency disclosure, and 2026 AZ HB4085 proposed a 50%-of-first-month cap (status unverified; page blocked).
4. **Spending evidence:** The fee structure is long-standing across operators (Senior Housing News describes it as a major operator cost line). Placement-agency franchises are marketed, and a home-based senior-care business listed with $123,623 income [search snippet only; BizQuest blocked]. Volume data for small agencies is [Unknown].
5. **Competitors:** A Place for Mom and Caring.com dominate SERPs. Local in-person placement agents and franchises such as Assisted Living Locators. Operator complaints include high upfront cost and double-billing between agencies [Verified: SHN]. Family complaints about aggregators passing contact details to many communities are widely reported, but I did not verify them this phase [Unknown].
6. **Entry strategy:** Hyper-local, no-spam positioning ("your details go to at most 3 communities you approve"). Focus on memory care in second-tier metros where national aggregators' content is generic. Use AI to keep accurate pricing and availability pages per community. Credibility versus APFM's brand is unproven.
7. **Acquisition mechanism:** Local SEO and Google Ads for "memory care near me / [city]". CPCs are likely high (not measured). Partnerships with elder-law attorneys and discharge planners need in-person relationships. No newcomer evidence.
8. **Capital, ops and restrictions:**
   - Costs: modest for the site, but family advisory calls need US-hours humans.
   - Regulation: state rules (AZ, TX, OK, OR, WA and others) on registration, disclosure and fee form. Anti-kickback exposure if Medicaid-funded residents are involved [Verified: SHN cites OIG advisory].
   - Payment terms: the fee is often paid 30–90 days after move-in (hypothesis).
9. **Labour dependence:** High-touch advising; delegable to US-based advisors on commission.
10. **Unit economics:** [Hypothesis] 2 move-ins/month × $4k ≈ $8k revenue in one metro. Long sales cycle (weeks to months), so first revenue may take 3–6 months. Track B is possible, but it is an ops business.
11. **Risks:** Regulatory tightening (fee caps), APFM SERP dominance, long cycles, reputational sensitivity with vulnerable families, and labour intensity.

### C-5. Acquire a small lead-gen site on seller financing or earn-out (instead of building)
1. **Concept:** Buy an existing call-lead site or network ($13–30k class, $650–1,000/mo profit) with a seller note or revenue share. Then upgrade monetisation from network to direct contractor sale (C-2) to multiply revenue. The Phase 3 exclusion covered micro-acquisitions under $2k cash; this is materially different (larger, financed, lead-gen-specific, monetisation upgrade).
2. **Paying customer:** As C-1/C-2.
3. **Model:** Asset purchase at about 31× monthly profit (EF median, pure lead-gen n=11) [Verified: EF API].
4. **Spending evidence:** 25 of 26 EF lead-gen listings sold, including a $4.3k/mo plumbing network in 2025, so buyers exist. Each asset's revenue is documented by EF vetting.
5. **Competitors:** Other buyers. Small sites are often bought fast on Flippa, Empire Flippers and Motion Invest (Flippa could not be queried).
6. **Entry strategy:** Target sites whose sellers sell to a network (as in EF 48257 and 50357, 100% to one revenue-share provider). Upgrade to direct-sold exclusive leads. This is a genuine value-creation lever, as the seller explicitly noted.
7. **Acquisition mechanism:** Deal sourcing on marketplaces, which is easy. Financing is hard: EF and Flippa deals are usually cash and escrow. Seller financing appears in a minority of small deals [Unknown frequency].
8. **Capital:** **Needs more than the $2k budget.** Realistically $5–15k down even with a 50% seller note on a $15–30k site. Flag: outside budget unless the founder adds capital.
9. **Labour dependence:** Low (sellers report 0–1 h/week). The upgrade to direct sales adds sales labour.
10. **Unit economics:** [Verified multiples; hypothesis on upgrade] A $15k site at $650/mo pays back in about 23 months as-is. If direct sales double or triple the revenue per call, payback is 8–12 months. Track A needs 3–5 such assets ($50–100k capital).
11. **Risks:** Buying a site just before a Google update (sellers time exits), PBN-dependent rankings (88006), single-buyer revenue, and opaque traffic durability.

### C-6. Hebrew lead-gen for high-ticket Israeli services outside Midrag's strength (Israel)
1. **Concept:** Owned Hebrew comparison/quote sites for high-ticket services, selling exclusive leads to Israeli providers. Candidates: private mortgage advisors, real-estate appraisers, home solar/battery installers, pergolas/aluminium, accessibility contractors. Excluded overlaps avoided: mamad renovation, electricity-supplier brokerage, arnona, tax-refund firms were not checked.
2. **Paying customer:** Israeli SMB service providers.
3. **Model:** Per lead (NIS) or monthly exclusivity.
4. **Spending evidence:** **[Unknown].** I found no published Israeli per-lead prices (one Hebrew search returned nothing relevant). Midrag does not publish pro pricing; it shows 12,442 rated pros in 149 sectors. Whether Google LSA (and its 2027 PMax migration) covers Israel is [Unknown]; the Google page names "non-US accounts" generally.
5. **Competitors:** Midrag (reviews plus a lead centre), Zap-style directories, Facebook lead-ad agencies [Hypothesis], and Google Ads.
6. **Entry strategy:** None credible until lead prices and buyer willingness are measured. The founder's Hebrew and local presence lets them sell directly, unlike C-2.
7. **Acquisition mechanism:** Hebrew SEO, where competition is thinner than in English [Hypothesis], plus Google/Facebook ads. No evidence collected.
8. **Capital and ops:** Low; fully operable from Israel. Israeli Bar fee-sharing rules likely bar lawyer referral fees, so lawyers are excluded [Hypothesis, unverified].
9. **Labour dependence:** As C-2, but the market is small: a few thousand providers per vertical.
10. **Unit economics:** [Unknown]. Probably Track A at best given market size.
11. **Risks:** A small market, Midrag and Facebook-agency incumbency, and price-sensitive SMB buyers.

### C-7. Buying an existing offline/service business with seller financing, run remotely through a manager (US/Israel): assessed, deferred
1. **Concept:** Buy a cash-flowing service business (cleaning, pest, laundromat, vending/route) with a seller note, and install a manager.
2. **Paying customer:** Its existing customers.
3. **Model:** The operating business's own revenue.
4. **Spending and price evidence:**
   - BizBuySell Q1 2026: median sale $350k, median cash flow $165k, 2.7× multiple. Service businesses are 42% of deals, median $350k (+13%) [Secondary: smallbiztrends, 2026-04-27].
   - Q2 2026: median $349k, cash flow $156k [Secondary].
   - BizBuySell listings were blocked (403), so I could not sample small listings.
5. **Competitors:** The roughly half of buyers who are "corporate refugees", well-financed searchers, and SBA-backed US buyers.
6. **Entry strategy:** None credible at $2k. The founder cannot use SBA 7(a), whose ownership rules changed in March 2026 against foreign nationals [Secondary]. Only 29% of sellers plan to offer financing [Secondary, Q2 2026], and a seller rarely finances 100%. Typical small-deal structures still need 10–30% down, which is $35k+ even on a $350k median deal.
7. **Acquisition mechanism:** N/A (deal sourcing).
8. **Capital and ops:**
   - Far above budget.
   - Remote ownership from Israel requires a US entity, banking, and possibly an E-2 visa if the founder ever relocates. A manager typically costs $50–80k/yr, which absorbs a third to half of the cash flow at the median [Hypothesis].
   - Israel: Yad2 and homeless.co.il listings were blocked, so no data.
9. **Labour dependence:** Delegable via a manager, but needs oversight.
10. **Unit economics:** Median $165k cash flow minus a manager (about $65k) minus seller-note debt service gives about $40–70k/yr owner profit. That is Track A territory, but it needs $35–100k equity.
11. **Verdict:** Deferred. Revisit only if the founder has $50k+ capital, or for sub-$100k "micro" service businesses, which need listing data that was blocked.

---

## Ideas killed (and why)
- **Personal-injury / mass-tort legal lead-gen:** highest payouts ($99/call median for PI), but brutal CPC competition, bar-rule fee-sharing limits, and fraud scrutiny. No credible entry.
- **Medicare/ACA/insurance lead-gen:** TCPA and CMS marketing rules, and a regulator-heavy, compliance-driven market. Not suited to a newcomer.
- **Generic Bark/Thumbtack-style horizontal marketplace clone:** Bark has 112k reviews at 3.8 (not hated). It needs two-sided liquidity and big capital.
- **Moving and auto-transport lead brokerage:** low lead prices, notorious fraud, and close to excluded ideas (H12 dumpster, boat transport).
- **Paid-ads-only lead arbitrage in LSA categories:** reselling Google-clicked leads competes with Google's own pay-per-lead product at about $39–66 CPL in the main trades. The margin is structurally thin, and the August 2026 PMax migration makes it worse.
- **Israeli lawyer referral fees:** likely prohibited fee-sharing [Hypothesis]; not pursued.

## Ranking (Agent C)
1. **C-2 Direct-sold exclusive contractor leads.** Strongest unit economics (captures the 60–80% network spread), clearest pain signal (Angi active pros −17%, LSA CPL up 11–69%). Main issues are founder sales labour and newcomer close rates.
2. **C-1 Pay-per-call publisher sites in emergency verticals.** Lowest labour and resellable assets (31× monthly). The SEO/SERP risk is the main issue. C-1 and C-2 are one asset with two monetisations; I recommend diligencing them together (build C-1, upgrade to C-2).
3. **C-3 Remote booking agency for independent local providers.** One verified live example ($3.1k/mo profit, 150 contractors, 65 cities). Needs a vertical with a measured gap.
4. **C-4 Senior-living placement leads.** Highest value per conversion, but regulated, labour-heavy and SERP-dominated.
5. **C-5 Financed acquisition of a lead-gen site.** A good later lever; over budget now.
6. **C-6 Hebrew high-ticket lead-gen.** Evidence is unknown.
7. **C-7 Offline business acquisition.** Deferred; not feasible at $2k.

## Top candidates for deep diligence and their decisive unverified assumptions
- **C-2 (with C-1 as its supply):** Will US contractors in one high-ticket trade pay a remote unknown operator about $1,000+/mo, or about $100+ per exclusive answered call, and renew for 3+ months? Measurable without contact only through indirect signals: the rent-first operators' disclosed churn, and contractor-forum pricing. It is otherwise a field test, which is outside desk-research bounds.
- **C-1:** Can a new 2026 site, without a fake Google Business Profile, rank organically for "[emergency service] [city]" and produce 8+ billable calls/month within 6–9 months, despite LSA→PMax and AI Overviews? Also: do pay-per-call networks accept Israel-based publishers? Check network T&Cs, and get SERP-feature counts for target keywords from public SERP samples.
- **C-3:** In which vertical or geography is there an under-served fragmented supply of independent providers with poor online booking, and what is the contractor-pay vs consumer-price spread? The single EF example shows 48% net margin with a manager. Find 2–3 more comparable listings or companies.

**WebSearch count: 8/8** (2 wasted: the rank-and-rent income query returned housing stats, and the Hebrew lead-price query returned nothing). Data files and scripts: /private/tmp/claude-501/-Users-tomeryannay-Projects-agents/33458dff-96bb-4d90-98b6-5161ecb65c2e/scratchpad/p6plus/C/
