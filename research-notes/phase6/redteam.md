# Phase 6 Red-Team Investor report (L1–L13 and the leader re-check)

Date: 2026-10-13. Desk research only. No browser tools, logins, sign-ups or contact with anyone.

**WebSearch: 7 of 8 used**, each logged as `P6-REDTEAM`. Uncapped checks used WebFetch, curl and public APIs:
- WordPress.org plugins API, the plugin-adoption handbook and the author profile.
- Google Business Profile guidelines.
- The Lead Smart press page and CallScaler.
- GCA (formerly CCS) RM1557.15 and gov.uk G-Cloud 15 pages.
- Elterngeldexperten and Einfach Elterngeld sites, and dejure.org (BSG ruling).
- TrustMRR Ton-piston, CollegeFootballData.com, and Destatis.

Scratch files: `scratchpad/p6plus/redteam/`.

**Scoring note.** Agents did not publish criterion scores for L1–L13, so I scored each criterion myself under the frozen rubric (0–5 × weight/5). I give the Adjusted score as a range because my calibration may differ from the rescoring lead's. My Adjusted figures for Phase 6 ideas came out about 3–5 points lower than discovery-agent enthusiasm would suggest. That is deliberate, given the Phase 5 rule that newcomer outcomes are required.

## 0. Headline

1. **No Phase 6 idea reaches the current top cluster (about 51–57).** My best risk-adjusted Phase 6 ideas are:
   - L6 (lead-gen / pay-per-call), about 47–50.
   - L9 (WordPress plugin takeover), about 45–48.
   - L2 (Spanish AI community) and L10 (G-Cloud micro-SaaS), about 44–48.

   Phase 6's real contribution is better measurement, not a new leader.
2. **New verified blockers or contradictions found this round:**
   - **L10/L11 G-Cloud timing.** GCA's RM1557.15 page says G-Cloud 15 started 06/08/2026, all lots end 05/02/2028, and the framework "will reopen after 18 months and again after 36 months" [Verified: gca.gov.uk/agreements/RM1557.15, 2026-10-13]. A supplier that is not already on the framework probably cannot list until about **February 2028**. Agent E read this as an open "18-month reopening window", and gov.uk's press wording is ambiguous ("join … during an 18-month re-opening window after launch") [Verified: gov.uk news, 2026-10-13]. GCA's own agreement page is the more specific source. GCA also lists "over 4,000 suppliers".
   - **L1 RDG.** BSG, 28.03.2019, B 10 KG 1/18 R held that helping with a **Kindergeld application** "erfordert eine rechtliche Prüfung des Einzelfalls iS des § 2 Abs. 1 RDG". It ruled this an unzulässige Rechtsdienstleistung by a Lohnsteuerhilfeverein, and not a permitted Nebenleistung under § 5 RDG [Verified: dejure.org summary, 2026-10-13]. Elterngeld is a sister family benefit, so the Elterngeld question is plausibly analogous. Incumbent GmbHs operate openly, and Elterngeldexperten's homepage claims no RDG licence [Verified]. So this is a serious, specific legal risk, not proof of illegality.
   - **L1 language gap partly closed:**
     - Einfach Elterngeld shows an English language switch [Verified homepage].
     - Elterngeldexperten shows English and French switches, but its /en/ page returned a 404, so its English content is unverified.
     - Elterngeldhelden already offers English and Italian (Agent A).
     - Elterngeldexperten already runs a **"Partner-Hebammen"** (partner-midwife) programme [Verified homepage]. That is the referral channel Agent A planned to use.
   - **L6 map-pack rank-and-rent is against GBP policy.** "Sales associates or lead generation agents … aren't eligible for a Business Profile". Virtual offices are not eligible. "The phone number must be under the direct control of the business" [Verified: support.google.com/business/answer/3038177, 2026-10-13]. Organic-only sites remain legal but weaker.
   - **L6 payouts overstated.**
     - CallScaler's marketplace states "$35–$90" as the typical payout per qualified call, with 60–120 s duration gates [Verified: callscaler.com/marketplace/water-damage].
     - The Lead Smart "medians" used by Agent C ($213 for water damage) come from Lead Smart's own paid press releases.
     - Lead Smart says it has more than 10,000 publishers, with "the heaviest concentrations" of non-US publishers in Pakistan and India. It is actively training more of them [Verified: leadsmartinc.com/news/press-global-affiliate-publishers-2026]. The founder competes with a low-cost global publisher supply and has no cost or skill edge.
   - **L7 there is no price wedge:**
     - Shelby NC pays TecNXS $7.50 per test. Victorville CA submits through SwiftComply at no charge. Walla Walla and Yakima WA say there is no tester cost or that the city pays [Secondary: search snippets; the city pages blocked fetching or returned 404].
     - Brycer/The Compliance Engine also does backflow (Lancaster OH) [Secondary].
     - The proposed "$7–10 tester fee" is the incumbent price, not a discount.
   - **L9 the target author is not absent:**
     - Claudio Sanches is an active WordPress contributor employed at **Liquid Web** (29 high-impact contributions in the last 12 months), and is listed as an author on WooCommerce core [Verified: profiles.wordpress.org/claudiosanches; WP.org API].
     - Brazilian replacements are actively maintained: Infixs "Correios Automático" (4,000 installs, updated 2026-10-10), Melhor Envio (10,000), official PagBank plugins (3,000 each), Mercado Pago (100,000), Virtuaria and linknacional (several plugins each) [Verified: WP.org API, 2026-10-13].
     - The WP.org adoption rules require the developer's consent, or 30 days without a reply. Approval "is not guaranteed", plugins with 100k+ users are less likely to be approved, and you "inherit the good and the bad" [Verified: developer.wordpress.org/plugins/wordpress-org/take-over-an-existing-plugin/].
   - **L12 the comparable is decaying fast.** Ton-piston shows last 30 days $10,517, but last 7 days $1,731 (about a $7.4k/30-day run-rate) and last 24 hours $134 (about $4k/month) [Verified: trustmrr.com/startup/ton-piston.md, synced 2026-10-13]. That is a seasonal spike from a founder with an audience, now fading.
   - **H6 data point:** CFBD now claims "21,000+ users" and "3,600+ Patreon supporters". It already runs a basketball API on a shared quota, and states that "commercial use is permitted" [Verified: collegefootballdata.com, 2026-10-13]. Adding baseball would cost the incumbent very little.
3. **Leader re-check verdict:**
   - The H6 and H1 downgrades are fair. H1 is arguably insufficient on the penalty.
   - The monday downgrade is the minimum defensible.
   - The K13 downgrade is fair. I would withhold the +1 for spending evidence, but only lightly.
   - **The K8 hold is not consistent with how H7 and J7 were treated.** Downgrade it slightly.
   - **H7 as sole leader is a scoring artefact.** Its 3.4-point gap to #2 is under the 5-point noise threshold, and it got a lighter correction than H6 for similar newcomer evidence. Trim it to about 55–56 and present the top as a tie.

---

## 1. Per-idea red team (L1–L13)

Format for each idea:
- Top 3 failure modes.
- **Hard blockers (HB)** and **unverified concerns (UC)**.
- Verdict.
- My estimate (CF / Scal / Dist → Balanced; penalty; Adjusted range).
- The single cheapest validation experiment, for the founder to run later.

### L1: Elterngeld concierge for non-German-speaking parents (A1)

**Failure modes**
1. **Legal.** If the service is an unlicensed Rechtsdienstleistung, one competitor Abmahnung or Elterngeldstelle refusal ends it. The BSG Kindergeld ruling is the closest precedent, and it goes against the model.
2. **The wedge has shrunk.**
   - English is covered by at least two incumbents. Elterngeldexperten's English and French content is still unverified.
   - The remaining wedge is TR/AR/RU/UA. About 29% of 2025 births were to foreign-national mothers [Secondary: drweb.de; Destatis gives only the 654,241 total], roughly 190k a year. But many of these parents speak German.
   - Elterngeld is 65–67% of prior net income, with a €300 minimum. Lower-income households gain less from optimisation, so they will pay less for a €250–300 package. Bürgergeld offsets reduce the gain further [Hypothesis].
3. **Founder fit and operations.**
   - The founder speaks no German. Every case needs a German adviser who is also fluent in TR/AR/RU, which is a scarce combination.
   - Errors cost families thousands of euros, which creates liability.
   - It is a one-off purchase: no recurring revenue and no repeat customers.

**Hard blockers:** none verified. The RDG point is a verified precedent for a sister benefit, not a ruling on Elterngeld.

**Unverified concerns:**
- How incumbents are structured to stay inside the RDG (advice-only, with the client filing the application?).
- Google Ads CPC for these terms.
- Willingness to pay among TR/AR/RU parents.
- Incumbents own the midwife channel.

**Verdict: Down.** Estimate: CF 62 / Scal 38 / Dist 66 → Balanced 53.2; penalty 12–13; **Adjusted about 41–45.**

**Cheapest test:** pay for a one-hour fixed-fee opinion from a German lawyer on RDG (§ 2, § 5) for "AI intake + adviser checks + client files". This costs about €200–400, and nothing else is worth doing if the answer is no. Second test: a €300 Google Ads test on Turkish and Arabic Elterngeld queries, measuring CPC and lead form fills.

### L2: Spanish-language AI-agents community + cohorts (A2)

**Failure modes**
1. **The channel belongs to someone else.**
   - All acquisition depends on a native co-host with an audience. Such a co-host can launch their own Skool group (many have) and keep 100% instead of 50%.
   - Skool shows 12+ new Spanish "claude" groups in a year, so co-hosts have options.
2. **Fad and churn.**
   - The "AI agents" topic moves monthly, and the curriculum goes stale.
   - No Skool churn data exists. Vendor benchmarks are 5–8% a month for education and coaching, and communities "run hotter" [Secondary, P6-REDTEAM search].
   - Member counts are an upper bound: totalMembers may include comped, trial and possibly lapsed members [Unknown].
3. **Hidden labour.** Weekly live sessions, Q&A and template upkeep mean ongoing hours, and the work is partly reselling the founder's own dev expertise.

**Hard blockers:** none.

**Unverified concerns:**
- Co-host availability and terms.
- Real paying members versus listed members.
- Retention.
- Consumer-protection rules on income claims.

**Verdict: Hold** at a modest level. It is the one Phase 6 idea with newcomer outcome data in the exact niche, but those outcomes are conditional on an audience the founder lacks.

Estimate: CF 67 / Scal 50 / Dist 54 → 57.6; penalty 11–12; **Adjusted about 45–47.**

**Cheapest test:** desk-score 30 Spanish AI YouTubers and TikTokers on audience versus monetisation using public data. Then (later, with consent rules) make five partnership offers and count yes/maybe answers. Before that, re-pull the same Skool JSON in 60 days to measure how many of the 12 Spanish groups grew or died. This costs $0.

### L3: Revenue-share operator partner for hobby-expert communities (A3)

**Failure modes**
1. **It is an agency.** Partner sourcing, funnel building and course production are custom per partner. That is the dev-hours/service model the founder wants to avoid.
2. **Low base rate.** The newcomer median is 11–16 members. The claim that "operator involvement lifts success above 18%" is pure hypothesis.
3. **Partner leakage.** Once a community works, the expert can replace the operator with a $1k/month VA. Revenue-share contracts with individual creators are hard to enforce cross-border.

**Hard blockers:** none.

**Unverified concerns:** everything about uplift and retention.

**Verdict: Down** (bordering on Kill for founder-preference reasons). Estimate: CF 63 / Scal 44 / Dist 44 → 51.6; penalty 12; **Adjusted about 38–42.**

**Cheapest test:** the same 60-day Skool re-pull as L2, filtered to dog and divorce groups. If fewer than about 30% of 2026 groups grew, the base rate is too low for a revenue-share model.

### L4: Bulk filament for Israeli print farms and labs (B1/B2)

**Failure modes**
1. **The real competitor is not Bug retail.**
   - Bambu's official stores already price bulk: US 6-roll refills at $13.99/kg; a German deal at about €11.50/kg for 10 rolls [Secondary: P6-REDTEAM search snippets]. Elegoo sells 10 kg for $110–130 [Verified by Agent B].
   - Heavy users (print farms) are exactly the buyers who self-import.
   - A business filament importer pays VAT just as a self-importing farm does (and both reclaim it as registered dealers). The local edge is only freight consolidation and speed. That fits a contribution of about 5–15 NIS/kg, not the 25–30 NIS/kg assumed.
2. **Tiny buyer pool.** Track A needs 350–450 kg a month, which is roughly 35–45 printers running at farm intensity, in Israel. The number of Israeli farms is unknown, and the only school/MoE evidence found was 2013–15 articles.
3. **Capital and inventory.**
   - The first useful shipment ($2.5–4k) exceeds the budget.
   - Moisture-sensitive stock needs sealed storage.
   - It is a commodity with no defensibility, and CopyTech/ALMA already private-label.

**Hard blockers:** none verified. Whether Bambu ships to Israel is unverified: its store geo-redirects to the US.

**Unverified concerns:** landed factory cost, duty on HS 3916, the farm count.

**Verdict: Down** (Track A at best, thin). Estimate: CF 47 / Scal 40 / Dist 45 → 43.8; penalty 12; **Adjusted about 32–37.**

**Cheapest test:**
1. Price a 10 kg order delivered to Israel from Elegoo, Bambu and AliExpress at checkout (no purchase).
2. Count Israeli Etsy/Shopify 3D-print sellers.

Kill if landed self-import is under about 60 NIS/kg, or if there are fewer than 30 farms.

### L5: First Israeli distributor of EU professional-consumables brands (B3)

**Failure modes**
1. **There is no product yet.** No brand, no terms and no demand evidence. "Distributor" is a category, not an opportunity.
2. **Capital and relationships.** MOQs are probably several thousand euros. The founder has no trade relationships, and incumbent importers actively hunt brands (Federation of Chambers board).
3. **Termination risk.** The brand takes the market back once it is built. Cosmetics need a Ministry of Health notification [Hypothesis].

**Hard blockers:** none, but the idea is untestable without contacting brands, which is outside desk-research rules.

**Verdict: Kill** as specified (it could re-enter as a specific brand later). Estimate: CF 34 / Scal 42 / Dist 31 → 36.6; penalty 14; **Adjusted about 22–28.**

**Cheapest test:** desk scan of 30 EU professional brands' distributor locators for an Israel gap, plus any published wholesale terms. Costs $0.

### L6: Pay-per-call / exclusive lead sites for emergency home-service verticals (C1+C2)

**Failure modes**
1. **The SERP is closing.**
   - LSA moves into PMax pay-per-lead from August 2026 [Verified by Agent C].
   - AI Overviews sit above organic results.
   - Restoration franchises (Servpro etc.) and national directories buy the top of the page.
   - Map-pack rank-and-rent is a **GBP policy violation** [Verified]. Organic-only local pages for "water damage [city]" are the weakest position on the page.
   - Empire Flippers shows that the flow of lead-gen exits dried up after mid-2024 (3 of 26 listed since then).
2. **Unit economics overstated and supply flooded.**
   - Typical marketplace payouts are $35–90 per qualified call [Verified: CallScaler], not the $213 "median" from Lead Smart's press releases.
   - Lead Smart's own PR describes thousands of trained publishers in Pakistan and India [Verified], plus a "pay-per-call academy" on Skool.
   - Calls are duration-gated (60–120 s), and disputes and fraud scoring come out of the publisher's revenue.
3. **Time to revenue, and the C-2 upgrade is founder sales labour.**
   - The first billable calls take 4–12 months with no newcomer data.
   - The direct-to-contractor upgrade means cold-selling US contractors across a 7–10 hour time gap. Contractors churn in slow months.

**Hard blockers:**
- GBP ineligibility for lead-gen operators [Verified]. This kills the map-pack variant only.
- Non-US publishers are accepted by at least Lead Smart [Verified], so that is not a blocker.

**Unverified concerns:**
- Organic ranking feasibility in 2026–27.
- Network payout stability.
- Contractor renewal.
- State referral rules.

**Verdict: Down slightly but still the best Phase 6 idea.** It has the highest margins, resellable assets, low labour once ranking, and a verified contractor spend pool. Estimate: CF 72 / Scal 57 / Dist 51 → 61.8; penalty 12–13; **Adjusted about 47–50.**

**Cheapest test:** build 3 organic-only pages (no GBP) for biohazard or trauma cleanup in 3 second-tier metros, about $150 total. Track Search Console impressions and positions for 90 days before buying any call tracking. Kill if none reaches the top 10 by day 120.

### L7: Backflow compliance tracking, tester-pays per report (D1/D2)

**Failure modes**
1. **No wedge.**
   - The tester fee is borne by testers and property owners, not the utility, so the buyer (the utility) does not care about a lower fee.
   - Incumbents already charge $0–7.50 in several cities: SwiftComply in Gig Harbor and Victorville, TecNXS in Shelby [Secondary].
   - Brycer/The Compliance Engine also operates in backflow (Lancaster OH), so there are at least six incumbents.
   - Utilities choose on references, state-form support and liability comfort.
2. **Municipal and foreign-vendor friction.**
   - It needs a US entity, general and cyber liability insurance, and security questionnaires (water is critical infrastructure).
   - Council or board votes create 6–18-month cycles.
   - On-site training is expected.
   - Liability if an overdue assembly contaminates supply.

   None of this is fatal, but CAC and time-to-first-revenue are severe for a part-time Israel-based solo founder.
3. **Onboarding labour.** Importing paper records and mapping forms for each utility, plus mailed notices, is founder or contractor work. Small utilities (300–5,000 assemblies) yield about $3–13k a year each, so Track A needs about 10 utilities, which is 2–3 years of sales.

**Hard blockers:** none verified.

**Unverified concerns:** insurance cost (may exceed the budget), state data rules, share of small systems still on paper.

**Verdict: Down.** It is still a good model (recurring, mandatory, switching costs), but the wrong founder and timeline for Track A. Estimate: CF 57 / Scal 64 / Dist 39 → 56.2; penalty 12; **Adjusted about 42–46.**

**Cheapest test:** desk-count, in two states, the city pages that name their backflow vendor and fee. That gives the share of systems with no vendor. Then get one public quote for $1M general liability plus cyber insurance for a foreign-owned US LLC. Kill if fewer than 20% of systems have no vendor, or if insurance is over $3k a year.

### L8: Low-cost records and mapping software for small cemeteries (D3)

**Failure modes**
1. **The market is already served at the low end.** Cemify ($799–1,899/yr), CemeteryFind (from $995/yr) [Secondary], CIMS, Chronicle and PlotBox, plus free spreadsheet templates.
   - Volunteer boards that won't pay $800 probably won't pay $400–600 either. Their default is a spreadsheet.
2. **The setup labour is the product.**
   - Digitising ledgers and maps is per-cemetery service work. AI transcription of old handwriting was found weak in Phase 5 (K11).
   - Support for elderly volunteer boards means phone calls in US hours.
3. **Slow direct acquisition and a low ceiling.** Cemify took about 8 years to reach "hundreds" of customers. Track A needs about 150 customers, and Track B is unrealistic.

**Hard blockers:** none.

**Unverified concerns:** board willingness to pay, transcription accuracy, CAC by direct mail.

**Verdict: Down.** Estimate: CF 62 / Scal 50 / Dist 39 → 52.6; penalty 12; **Adjusted about 39–43.**

**Cheapest test:** run AI transcription and map tracing on 2 public-domain cemetery ledger scans (state archives) and time the reviewer hours. Kill if it takes more than 6 hours for a 1,000-plot cemetery.

### L9: Take over abandoned high-install WordPress plugins (Brazil cluster first) + pro tier (F4)

**Failure modes**
1. **Consent and scrutiny.**
   - The flagship author is active, employed at Liquid Web, and is a WooCommerce core author. He parked these plugins; he did not disappear.
   - He may refuse, ask for real money, or prefer handing them to the Brazilian community.
   - WP.org adoption without consent depends on a 30-day silence, and approval "is not guaranteed".
   - Buying plugins to monetise them is the exact pattern the WordPress community treats with suspicion (past malware cases).
2. **The install base is decaying to maintained competitors.**
   - Correios users are migrating to Infixs (4,000, updated weekly) and Melhor Envio (10,000).
   - PagSeguro is superseded by the official PagBank plugins and Mercado Pago (100,000).
   - The 60,000-install checkout-fields plugin is simple and still works, so there is little reason to pay. Upgrades come only from new features (NF-e, label automation), where Virtuaria, linknacional and webmaniabr already sell.
3. **Support load and language.** Portuguese support for 20–60k installs is labour that starts on day 1, while revenue starts only if 0.5–1% convert. That figure is unmeasured, and the 2.1% benchmark comes from Freemius generally, not stale utility plugins.

**Hard blockers:** none. The adoption process exists [Verified]. A 60k plugin is below the 100k "less likely" line.

**Unverified concerns:** transfer price, pro conversion, share of live stores.

**Verdict: Hold.** It is cheap to test, budget-compatible, founder-fit is high, and distribution is built in. But the Brazil cluster specifically is weaker than presented. The broader screen of 161 plugins with 10k+ installs and no update in 2+ years is the real asset; look for plugins without maintained replacements. Estimate: CF 63 / Scal 60 / Dist 55 → 60.2; penalty 13; **Adjusted about 45–48.**

**Cheapest test:** desk work first. For the 161 candidates, use the WP.org API to flag those with no maintained alternative (no plugin with 1k+ installs updated in the last 6 months for the same function), and those whose authors are inactive across WP.org. Then one consent email per top-5 candidate (in a later phase). This costs $0.

### L10: G-Cloud micro-SaaS for one narrow UK public-sector workflow (E1)

**Failure modes**
1. **Timing.**
   - The founder probably cannot be on G-Cloud 15 until about February 2028 [Verified: GCA agreement page; gov.uk wording ambiguous].
   - Before then, sales must be direct below-threshold purchases or through a listed partner, which gives no catalogue discoverability.
   - Speed to first sale is about 0 on the rubric.
2. **Newcomer odds.**
   - 14% of G-Cloud 10 suppliers won anything [Secondary: Tussell].
   - Every sampled small winner was incorporated between 1999 and 2016, and no supplier under 2 years old was seen winning.
   - Buyers want references, Cyber Essentials, a DPIA pack, UK support hours and accessibility statements.
3. **No workflow chosen.** Agent E's own conclusion is "no credible entry strategy yet". Price-undercutting incumbents with 10–25-year relationships rarely moves risk-averse buyers.

**Hard blockers:** the framework-entry timing is near-hard for 2026–27 [Verified source, interpretation flagged]. It is not fatal to the business (direct sales are possible) but fatal to the G-Cloud channel thesis.

**Unverified concerns:** the next reopening date, non-UK eligibility, insurance minimums (Joint Schedule 3).

**Verdict: Down.** Estimate: CF 66 / Scal 64 / Dist 49 → 61.8; penalty 13–14; **Adjusted about 44–48.** It might score higher on paper, but speed and first-customer difficulty dominate.

**Cheapest test:**
1. Get the exact G-Cloud 15 reopening date from GCA's published documents.
2. Pull 12 months of Contracts Finder awards under £50k to find workflows with 10+ awards a year and at most 2 incumbents.

Kill if there is no such workflow, or if reopening is 2028.

### L11: G-Cloud reseller / route-to-market for non-UK SaaS (E2)

**Failure modes**
1. The same timing blocker as L10. A reseller needs a listing too.
2. **Two-sided cold start.** You need vendors willing to give a 10–25% margin, and UK buyers wanting those vendors. Established resellers (Softcat, Generation Digital, Eficode) already serve vendors with real UK traction. The vendors left over are those without traction.
3. **Credit exposure and contract liability** on licence pass-through. Thin margin on lumpy, rare deals.

**Hard blockers:** timing (as L10).

**Unverified concerns:** margin, vendor appetite.

**Verdict: Kill.** Estimate: CF 46 / Scal 40 / Dist 34 → 41.2; penalty 13; **Adjusted about 27–31.**

**Cheapest test:** count, from award data, non-UK SaaS sold via resellers versus direct. If almost none of the ones sold via resellers are small vendors, kill.

### L12: Seeker-paid local-language job search + AI application tools (E4)

**Failure modes**
1. **The only comparable is audience-driven and decaying.** Ton-piston's founder has 51.6k X followers, and its run-rate fell from about $10.5k to about $4–7k a month within weeks of peak season [Verified: TrustMRR].
2. **Free substitutes.**
   - Google gives AI Pro free to German students and apprentices in 2026 [Secondary].
   - ChatGPT and other free tools write cover letters.
   - Incumbent boards (StepStone, Azubiyo, Pracuj) own the job-seeker traffic.
3. **Structural churn plus scraping and terms-of-service risk.** Seekers leave when hired. Aggregating listings without licences invites blocking and legal letters. Paid CAC for students is unmeasured, and a €10/month product with about 3-month lifetimes cannot afford much CAC.

**Hard blockers:** none verified.

**Unverified concerns:** whether a non-French market lacks an equivalent, CAC, scraping legality.

**Verdict: Down.** Estimate: CF 71 / Scal 48 / Dist 38 → 55.2; penalty 13; **Adjusted about 40–44.**

**Cheapest test:** a €200 TikTok/Meta ads test in one market and season (for example a Polish internship landing page with a waitlist), measuring CPA per email. Kill if it is over €3 per signup.

### L13: Acquire and modernise aged mobile apps (F1)

**Failure modes**
1. **Capital.** $10–50k per asset, 5–25× the stated budget. Seller financing under $100k is "rare" [Verified: Empire Flippers].
2. **Unmeasured uplift and adverse selection.**
   - Only about 23% of Flippa app listings are Data Verified.
   - 11 of 30 app listings had price cuts (13–43%).
   - Aged installs decay, and sellers time exits at the peak.
   - There is no public before/after uplift data.
3. **Platform and IP risk.**
   - Store policy changes (target-API deadlines, account-transfer reviews).
   - Hidden copied content: Quran recitation audio licensing, unlicensed streaming apps.
   - AdMob account bans after a transfer.

**Hard blockers:** the capital gap against the stated budget is fatal unless the founder adds capital (a founder decision, not a market fact). App transfers themselves are allowed on both stores.

**Verdict: Down** (parked until capital is available). Estimate: CF 55 / Scal 56 / Dist 45 → 53.4; penalty 13; **Adjusted about 38–43.**

**Cheapest test:** desk-track 20 aged Data-Verified Flippa app listings for 90 days, recording whether they sell, at what final price, and post-sale store rank. This gives cleared multiples and decay. Costs $0.

---

## 2. Red team of the leader re-check

| Leader | Auditor | My view | Range |
|---|---|---|---|
| H6 | 57.2 → 51.6 | **Fair, maybe slightly generous.** CFBD's own page now shows 21k+ users and 3.6k patrons (about 17% paid), basketball already added on a shared quota, and commercial use permitted. The incumbent can add baseball cheaply, and Highlightly already sells NCAA baseball for $7.99. CF 75 still credits fast first sales that peer data (tens of patrons a year) does not support. A −1 on speed to first sale (CF −4) is justified. | **50–52** (point 50.0 with the extra step) |
| H1 | 54.6 → 51.2 | **Fair on criteria; the penalty is still too low.** A penalty of 7 is far below the historical 9–14 band, for an idea whose core claim (a $349–449 kit sells) has zero newcomer evidence at that price, and whose branded comparables show 0–39 ratings. A penalty of 9 is more consistent. | **49–51** (49.2 at penalty 9) |
| monday app | 52.0 → 50.8 | **Minimum defensible, slightly insufficient.** Two further points: Israeli CRMs already bundle invoicing (substitute), and the invoicing vendors' own apps get 0–16 reviews. That supports an additional −1 on first-customer difficulty (Dist −3, Adjusted −0.6). | **50.0–50.8** |
| K13 | 53.6 → 52.6 (50.6 without +1) | **Downgrade fair.** The +1 spending credit is defensible: Kones publishes ₪249/month, and Ifat is a long-running paid business. But the auditor concluded the entry strategy is "not credible". Under the brief, an idea with no credible entry should not sit in the top cluster. I would credit the spending and also take −1 on scalable acquisition, because any acquisition now means displacing an incumbent that gives AI summaries away free (Scal −4, Adjusted −1.6). | **51–52** |
| K8 | hold 53.2 | **Hold not justified.** The same newcomer logic that took H7 −2.8 and J7 −4.6 applies here. Framer's page data shows a flood of free templates with no sales visible, and plugins earn no referral. The penalty of 13 was set for "unmeasured", but Phase 5 also measured near-zero median newcomer outcomes on every comparable open marketplace (6 of 6). By that pattern, the evidence is now more than unmeasured. Proven channel −1 (Dist −6) → 52.0. | **51.5–52.0** |
| H7 | 56.6 (P5-corrected) | **Sole leadership is not justified.** It was corrected only −2.8 with penalty 12 kept, while H6 got −5.6 and a penalty +1 for comparable evidence. H7's newcomer evidence is better than H6's: real unit sales, curated picks 11 of 12 at 10+ sales, one 1,900-sale breakout. But new supply is about 2.5× (about 385 a month) and the median is under 10 sales in 2–3 months. One more step on first-customer difficulty (Dist −3) plus penalty 12→13 gives about 55.0. Even at 56.6, its gap to #2 (53.2) is 3.4, under the 5-point noise threshold. | **54.5–56.0** |

**Board after my adjustments:** H7 about 55 / K8 about 52 / K13 about 51.5 / UK MTD 52.6 (not re-checked; it needs the same newcomer test) / H6 about 50–51.6 / monday about 50.4 / H1 about 49–51.

The honest statement is: **H7 leads narrowly, within noise of four ideas.** The report should present a tied top cluster, not a sole leader.

---

## 3. Overall rankings (Phase 6 ideas; leaders listed for context)

**Track A ($2–5k/month owner profit, realistic within about 12–18 months part-time):**
1. **L9** WP plugin takeover (broad screen, not Brazil-specific). Cheapest to test, budget-compatible, distribution built in.
2. **L6** organic pay-per-call sites. Slow to rank, but low labour once working, and assets resell.
3. **L2** Spanish AI community. Only with a co-host; labour-heavy.
4. **L1** Elterngeld concierge. Only if the RDG check is clean; one-off revenue.
5. **L8** cemeteries. Slow but real.
6. **L7** backflow. Real but 2–3 years to Track A.
7. L12, then L4.
8. L3, L13, L10, L11, L5 do not fit Track A within budget and timeline.

**Track B ($10–30k+/month route):**
1. **L6** (C-2 direct contractor sales across territories).
2. **L7** (40+ utilities with mandatory recurring fees). It has the best structural moat of the batch but the slowest ramp.
3. **L10** (only after about 2028 framework entry).
4. **L2** (600+ members, rare).
5. L9 (portfolio), then L13 (capital-bound roll-up).

**Risk-adjusted (my Adjusted midpoints):**

| Rank | Idea | Adjusted (midpoint) |
|---|---|---|
| 1 | L6 | 48.5 |
| 2 | L9 | 46.5 |
| 3 | L2 | 46 |
| 4 | L10 | 46 |
| 5 | L7 | 44 |
| 6 | L1 | 43 |
| 7 | L12 | 42 |
| 8 | L8 | 41 |
| 9 | L13 | 40.5 |
| 10 | L3 | 40 |
| 11 | L4 | 34.5 |
| 12 | L11 | 29 |
| 13 | L5 | 25 |

None enters the cumulative top 10 (cut-off about 50.6).

**Suggested finalists for Phase 6 deep dives:** L6, L9, L2, plus L7 as the Track B structural candidate. L1 only if the cheap RDG opinion is treated as a later gating step.

**Kill:** L5 and L11 as specified. **Defer:** L13 (capital) and L10 (until the reopening date is confirmed).

WebSearch count: **7 of 8** (P6-REDTEAM).
