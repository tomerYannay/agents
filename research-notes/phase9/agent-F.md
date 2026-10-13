# Phase 9 — Discovery Agent F (Contrarian), label P9-F

Date: 2026-10-13. WebSearch used: **6 of 6** (all logged as `P9-F` in `search-log.txt`). Most evidence comes from public JSON APIs and registries: the Empire Flippers listings API, BLS BED survival tables, data.gov.il CKAN registries, and the iTunes Search API (country=il). Scratch data and scripts: `scratchpad/p6plus/P9-F/`.

## Bottom line

1. **Israel-specific advantages: mostly falsified for this founder.**
   - Israel's domestic market is small:
     - 406,904 active companies, with about 17–18k new companies a year.
     - Newcomer outcomes for Hebrew B2B apps are close to zero: of 290 independent Hebrew business apps released since 2024, the median has 0 Israeli ratings and 1 has 100 or more.
   - Earlier Israel ideas clustered at 48–51 and never broke 51. Their three best scores were all corrected downward once auditors found incumbents that our US-only search engine had missed.
   - The licences, registrations and open data that a founder can obtain in Israel within 3–9 months are abundant, and their holder counts are growing.
   - Two Israel-only assets are real, but they are enablers rather than moats:
     - non-dilutive Innovation Authority grants, open to Israeli residents only;
     - the EU adequacy status of Israel's data protection regime.
2. **The Phase 9 direction, in the form "moats a newcomer can get in 3–9 months for about $2k make newcomers earn more": largely falsified.**
   - Moat-holding survivors earn more in absolute terms, but buyers do not pay a higher multiple for the moat.
   - Newcomers who hold a contract or licence do not survive better than other entrants.
   - Low-barrier licences show no robust income premium for the self-employed.
   - Logically, a moat the founder can get in 3–9 months is a moat a fast follower can get in 3–9 months. That is roughly the 6-month copy window Phase 8 already measured, so it is "first to notice" with paperwork added.
   - The direction survives only in a narrow form. The moat must be **scarce**: a capped or fixed holder count, or a term contract, not merely a slow process. It must also attach to **already-measured spending**.

---

## Part 1 — Israel-specific advantages: honest test

### 1.1 Is the Israeli market big enough?

| Indicator | Value | Source |
|---|---|---|
| Companies in the Israeli register | 732,114 total; **406,904 active** ("פעילה"); 727k private | [Verified: data.gov.il `ica_companies` resource f004176c…, full pull via datastore_search, 2026-10-13] |
| New incorporations per year | 2015: 16.8k · 2019: 17.6k · 2021: 20.5k (peak) · 2022: 20.6k · 2023–2025: about 17.8k each · 2026 to date: 14.9k | same |
| Active CPAs | 32,153 active out of 42,883 licensed; about 0.9–1.0k new licences a year since 2019 (1.9k in 2018) | [Verified: data.gov.il `cpalist`, 2026-10-13] |
| Licensed real-estate brokers | **24,984 active**. The exam dataset has 151,516 attempts; 2024: 7,524 attempts and about 3.6k scoring 60 or more. (That 60 is the pass mark is my [Hypothesis].) | [Verified: data.gov.il `metavhim`, 2026-10-13] |
| Registered contractors (פנקס הקבלנים) | 24,373 registered. New registrations rose from 621 (2015) to 1,188 (2019) and 1,828 (2023); 1,460 in 2025 | [Verified: data.gov.il `pinkashakablanim`, 2026-10-13] |
| Licensed car dealers | 10,872 | [Verified: data.gov.il `socharim`] |

**Reading:**
- About 407k active companies is roughly 1/14 of the UK's company count. That figure is [Secondary: general knowledge, not fetched this phase].
- For Track B at $10–30k per month in owner profit, an Israel-only B2B product at Israeli SMB prices (₪50–200 per month, the norm for Morning/iCount-type tools [Anecdote]) needs roughly 300–1,500 paying accounts.
- That is 0.1–0.4% of active companies, which is arithmetically possible. However, Phase 8 measured that winners without an audience over-index on $300+ per account per month, and Israeli SMB software rarely prices there [Hypothesis].
- **Track A is plausible in Israel. Track B from Israel-only demand needs either high price per account or a non-software service with a large transaction pool.**

### 1.2 How did earlier Israel ideas score? (frozen rubric, ledger values)

| Group | n | Median Adjusted | Max | Share ≥ 48 |
|---|---|---|---|---|
| Israel-domestic (monday invoicing, K13, allocation, J1, J2, H11, K6, J10, K4, J5, L4, L5, M12, N10) | 14 | 43.5 | 50.8 | 36% |
| Diaspora/affinity (H10, H8, H4, H9, J4, J11) | 6 | 48.0 | 49.4 | 50% |
| All other ideas | 63 | 43.8 | 55.4 | 17% |

- Israel-domestic ideas reach the 48–51 band more often than other ideas, but **none has reached the top 4**.
- **All three of the best were corrected down after audit**, each time because an Israeli incumbent was found late:
  - monday invoicing app, 52.0 → 50.8: Israeli invoicing apps on Shopify/Wix had 0–16 reviews.
  - K13, 53.6 → 50.6: Ifat already covers receivers and has AI summaries.
  - J1, 51.0 → 48.6: MyHeritage MyStories.
- Allocation verification also met Luca AI, Finbot and ERP vendors. Finbot shows up below with 18 apps released since 2024.
- **Generalisable lesson:** part of the apparent "Hebrew moat" was a measurement artefact. The WebSearch engine is US-only and weak in Hebrew (logged repeatedly in P5–P7), so Israeli incumbents are under-discovered at the idea stage and found at audit. Any future Israel idea should start with a −1 to −3 point prior for undiscovered incumbents.

### 1.3 Newcomer outcomes in Israeli B2B software (new measurement)

**Method:**
- I ran the iTunes Search API with country=il for 10 Hebrew SMB terms: invoice, bookkeeping, appointment booking ×2, business management, price quote, attendance report, client management, receipts, and fees.
- This returned 1,143 unique apps.
- I kept apps whose genre is Business, Productivity, Finance or Utilities and that support Hebrew (HE language code or a Hebrew title).
- Ratings are Israeli-store ratings. Data, script `it.py` and the follow-up split are in scratch.

**Results (2026-10-13):**
- **314 such apps were released in 2024 or later**: 42 in 2024, 53 in 2025 and **219 in 2026 to date**.
  - This roughly fivefold rise in Hebrew business-app supply is consistent with Phase 8's finding that AI tripled supply.
  - Caveat: the search ranking may favour recent apps.
- **290 of them are from independent sellers** (not white-label factories). Their **median is 0 Israeli ratings**: 11 have 10 or more and **1 has 100 or more**.
- The broader (description-based) filter also surfaced white-label "one app per barber" factories: ZENAT ONLINE LTD with 123 apps and a single developer with 93.
- **Incumbents also have small absolute counts:**

| App | Israeli ratings |
|---|---|
| Morning by Green Invoice (released 2023) | 171 |
| iCount | 236 |
| Simple Tor (appointments) | 773 |
| שכרניק (salary calculator) | 1,470 |

  So absolute rating thresholds understate Israeli success. Relative to incumbents, however, the newcomer median of 0 is still a near-total failure rate.
- Earlier phases measured Israeli invoicing apps on Wix/Shopify at 0–16 reviews [Verified P6].

**Conclusion:** Hebrew is not a copy barrier in 2026. Israeli developers, with AI tools, are already flooding Hebrew SMB categories. The founder's "foreigners can't copy" advantage protects only against foreigners, who were never the threat.

### 1.4 Israeli licence/registry "moat screen" (holder counts as a scarcity test)

| Israeli licence or registration | Holders | Trend | Copy barrier for a newcomer |
|---|---|---|---|
| Real-estate broker | 24,984 | about 3.6–4k exam passes a year | One exam and a few months. Abundant |
| Registered contractor | 24,373 | new registrations ×3 from 2015 to 2023 | Weakening |
| CPA | 32,153 active | about 1k a year | Years of training (not reachable for founder) |
| Car dealer | 10,872 | n/a | Abundant |
| Food importer certificate | 3,098 | n/a | Abundant (Agent B's area) |
| Fire-extinguisher inspector | 1,573 | n/a | Abundant |
| Notary | 7,735 | n/a | Requires senior lawyer |
| Patent attorney | 582 | n/a | Years |
| Medical-tourism agent (MoH) | 330 | n/a | Registration. Market already excluded (inbound tourism) |
| Bulk-mail permit (Communications) | 108 | n/a | Declining mail |
| Radon-testing permit (MoEP) | 32 | dataset stale: permits expired 2017–2019 | Scarce, but **no current testing mandate found** [Secondary: 2014 MoEP env-health report; Technion radon project] |

All counts: [Verified: data.gov.il CKAN datastore_search totals, 2026-10-13].

**Pattern:**
- Israeli licences the founder can get in 3–9 months have holder counts in the thousands to tens of thousands, and those counts are growing.
- The only scarce one in the screen, radon at 32 holders, has no verified buyer obligation. Scarcity without spending is not a business.

---

## Part 2 — Falsifying the Phase 9 direction

Question: do moated small businesses actually earn more **for newcomers**?

| # | Test | Result | Direction |
|---|---|---|---|
| 1 | **Empire Flippers, 2,854 listings** (2,679 sold plus 175 for sale; public API, 2026-10-13). I tagged a listing as moated by regex for a licence, a government/long-term/exclusive/B2B contract, certifications (FDA/GMP/ISO/SOC2…), exclusive distribution, or patent flags. | Only **36 of 2,854 (1.3%)** are tagged, and **1** is a licensed business. EF cannot represent licensed businesses. Moated listings have **3× the median monthly profit** ($10.4k vs $3.2k; among long summaries $10.1k vs $3.8k), but **the same or lower multiple** (30× vs 31× monthly; for businesses 3 years old or younger, 24.5× vs 28×). | Moats correlate with size. **Buyers pay no premium for them.** Confounded by brand size (mostly large FBA brands citing certifications or exclusive suppliers). |
| 2 | **US federal contracting**: new entrants who already won a contract. CSIS (Hunter et al., 2018, FPDS 2001–16). | "around 40 percent of new entrants exit … after three years, around 50-60 percent after five years"; only about one-fifth remain at the end of the window [Verified: dair.nps.edu/handle/123456789/2730, 2026-10-13]. | Holding a contract does **not** beat the BLS base rate (row 3). |
| 3 | **BLS BED establishment survival** by sector, 5-year (2019 cohort) and 10-year (2015 cohort) | All private 51.5% / 34.7%. Licence-heavy sectors: Health care 53.6/36.4; Finance & insurance 53.7/38.4; Professional 50.7/34.3. Less licensed: Retail 60.7/44.2; Food services 57.4/41.6; Other services 58.3/42.1 [Verified: bls.gov/bdm/us_age_naics_*_table7.txt, 2026-10-13]. | Licence-heavy sectors show **no survival advantage**; if anything they show a disadvantage. This is a sector-level proxy. |
| 4 | **Federal new-entrant share** | FY23: 1.4% of obligations went to never-before prime awardees; new small-business entrants fell about 60% in a decade [Verified: thirdway.org, 2024-06-25]. | Contract moats concentrate on incumbents, which helps the holder but blocks the newcomer. |
| 5 | **UK G-Cloud** (framework-contract moat, ledger L10) | 86% of suppliers earn nothing [Verified P6]. | Holding the contract vehicle ≠ revenue. |
| 6 | **Occupational licensing research** | Zapletal (Census CES-17-20): licensing "does not significantly affect the equilibrium number of practitioners or prices," but reduces entry and exit [Verified: lehd.ces.census.gov paper profile, 2026-10-13]. Fredriksen (2020, J. Labour Market Research 54), German 2004 crafts deregulation: "no robust effects" on incomes of the self-employed [Verified: econpapers.repec.org, 2026-10-13]. Same study's background: dereg tripled business counts within 10 years [Secondary: search summary]. | Licences slow churn but do not robustly raise self-employed income. |
| 7 | **Insurance agencies** (licence + renewal book) | Finance/insurance about 47% closed by year 5 (BLS via Insurance Business mag); new-agent failure about 50–80% [Secondary/Anecdote: SmartChoice whitepaper citing Insurance Journal]. Break-even about year 3 [Anecdote]. | Licensed businesses with recurring books are still slow and fail-prone for newcomers. |
| 8 | **Taxi licences** (Haltiwanger et al. 2024, CES-24-42) | After ridesharing, incumbent earnings fell where fleets were unlimited; losses were smaller or absent in heavily regulated markets [Verified: Census paper profile]. | A **capped-quantity** moat does protect, but it was bought, not obtained in 3–9 months. |
| 9 | **Israeli registries** (Part 1.4) | Moats obtainable in months have thousands of holders and rising counts. | Abundant. |

**Verdict:**
- Rows 1 and 8 support the claim that moats help: moated survivors earn more, and quantity caps protect incumbents.
- Rows 2–7 and 9 contradict the version Phase 9 needs, namely that a newcomer obtaining a moat in 3–9 months for about $2k earns more:
  - contract holders exit at base rates;
  - licence-heavy sectors do not survive longer;
  - low-barrier licences confer no robust income premium;
  - buyers do not price moats into multiples.
- **Recommended amendment to the direction:**
  1. Require **holder scarcity**: a capped or quota-limited holder count, or a term-limited award, with the number of holders flat or falling. A slow application process alone is not scarcity.
  2. Treat any moat obtainable by the founder in under about 9 months as equivalent to "first-mover plus 6 months". Score its defensibility at no more than 2 of 5 unless holder counts are capped.
  3. Prefer **buying** an existing moat-holder with measured cash flow over obtaining a new one. This is Agent C's acquisition route, but Phase 6 showed capital at 5–25× the budget, so the moat that works is the one the founder cannot afford.

---

## Opportunities (ranked; few by design)

Three ideas survived as candidates. None is strong. I report them because Part 1 asked for the best Israel-specific edges, not because they clear the bar.

### F9-1. Israeli-grant-funded B2B product for an existing leader (capital advantage, not a moat)
1. **Concept:** Use Israel Innovation Authority Tnufa/ideation funding, available only to Israeli residents, to fund the 6–12 months needed by an existing leaderboard idea that needs runway (e.g., H6 data API, M1-type integration API). This replaces the $2k constraint with non-dilutive capital.
2. **Payer:** Not a customer. The grantor is the IIA; customers are those of the attached idea.
3. **Model:** Grant reportedly covers 80–85% of an approved budget of about ₪200–250k [Secondary: Pertama Partners guides; conflicting figures]. Royalty terms are [Unknown]. The official 2026 Critical-Minerals Tnufa challenge offers ₪1M/₪250k prizes [Secondary: IIA call page via search; site returns 403 to fetch].
4. **Spending evidence:** Grant programme exists [Secondary]; approval rates are [Unknown].
5. **Competitors:** Every Israeli pre-seed founder applies.
6. **Entry:** Apply with a product that already has spending evidence. A competitive advantage is not credible beyond quality of the application.
7. **Acquisition:** Not applicable.
8. **Ops:** Israeli residency is required [Secondary]. The application takes weeks to months. Grant conditions may restrict IP transfer abroad [Hypothesis; IIA know-how rules].
9. **Labour:** Neutral.
10. **Economics:** Adds about $40–60k of runway if approved [Secondary/Hypothesis]. It does not create revenue.
11. **Kill:** Approval rate or IP restrictions; deep-tech bias against small B2B tools [Hypothesis].

My estimate: not scorable as a standalone opportunity. Treat it as a **modifier** to the capital-feasibility criterion of whichever finalist is chosen.

### F9-2. GDPR-adequate offshore back-office desk for EU/UK accountants (Israel adequacy as edge vs India)
1. **Concept:** AI-plus-human bookkeeping and compliance prep from Israel for EU/UK accounting firms. The sales hook is that personal data goes to an **EU-adequate country**, so no SCCs or transfer-impact assessment are needed. Indian and Philippine offshore providers need those.
2. **Payer:** Small EU/UK accounting firms (UK, NL, IE, DE).
3. **Model:** Per-client monthly prep fee [Hypothesis: £30–100 per client per month].
4. **Spending evidence:**
   - Offshore prep vendors exist and sell: Outbooks and QX, recorded in ledger R/UK MTD (scored 50.2).
   - EU adequacy for Israel was confirmed 15 Jan 2024. The Commission found that data transferred to "…Israel… continues to benefit from adequate data protection safeguards" [Verified: EC press release IP/24/161 via presscorner API, 2026-10-13].
   - Whether buyers choose vendors on adequacy is [Unknown].
5. **Competitors:** Indian, Philippine and South African offshore firms with lower labour cost; EU-local outsourcers; vendors' own AI agents (Sage MTD agent, noted in the ledger).
6. **Entry:** Compliance-framed positioning ("no SCC/TIA paperwork") toward GDPR-cautious DACH/NL firms. This is differentiation on paper. I cannot show buyers weight it, so it is **close to "none credible"** until tested.
7. **Acquisition:** Accountant directories and outbound; partner channels such as practice-software marketplaces. No newcomer outcome data.
8. **Ops:** Israeli labour is expensive compared with India, which erodes margin. Language coverage is limited (German/Dutch staff needed).
9. **Labour:** Service; scales with hired staff; AI reduces hours [Hypothesis].
10. **Economics:** Owner profit [Unknown]. Fits Track A at best.
11. **Kill:** Buyers treat SCCs as boilerplate (likely), so adequacy confers no pricing power. Also Israeli wage cost.

**Material difference from ledger "UK MTD prep" (R):** the segment (EU/DACH firms, any workflow) and a regulatory-transfer edge rather than a deadline. Still weak.

My estimate: about 41–44 Adjusted.

### F9-3. Bank-feed reconciliation for Israeli accounting firms via the Israeli open-finance regime
1. **Concept:** A tool for some of Israel's 32,153 active CPAs and for bookkeepers. It pulls client bank and card data under the Financial Information Services Law (2021) and auto-reconciles it into Israeli bookkeeping systems (Hashavshevet, Rivhit, iCount, Morning).
2. **Payer:** Israeli accounting and bookkeeping offices.
3. **Model:** Per client file per month [Hypothesis: ₪20–50].
4. **Spending evidence:** [Unknown]. Incumbents with open-finance licences (e.g., Finanda, Riseup, Finbot) imply a market [Anecdote], but there is no transaction data.
5. **Competitors:**
   - Finbot: 18 Israeli App Store apps since 2024 (iTunes, 2026-10-13).
   - Existing licensed aggregators and bookkeeping-system vendors adding feeds.
   - Banks' own exports.
6. **Entry:** Either the licence itself (moat) or using a licensee's API (no moat). Licence equity and insurance requirements were updated in 2024–25, but amounts were not found [Verified: barlaw.co.il/08mm, dated 2024-12-29: requirements exist; no figures]. Licensee count is [Unknown].
7. **Acquisition:** Through the CPA channel, which is concentrated and countable, but no newcomer data.
8. **Ops:** Licence likely needs capital and insurance beyond $2k [Hypothesis]. Regulated data handling.
9. **Labour:** Software, so it scales.
10. **Economics:** [Unknown]. Track A only, given the Israeli SMB price norm.
11. **Kill:** Licence cost; bookkeeping vendors build the feed natively; no buyer data.

My estimate: about 40–43 Adjusted. It is the only Israeli idea where the moat (a licence plus regulated data) is plausibly scarce. The decisive unknown is the licence's capital requirement and how many licensees already hold it.

---

## Killed (with evidence)

| Idea | Why killed |
|---|---|
| Hebrew SMB apps (invoicing, booking, attendance, quotes) | 290 independent 2024+ Hebrew business apps: median 0 Israeli ratings, 1 with 100 or more. Supply ×5 from 2024 to 2026. White-label factories with 93–123 apps (iTunes API, 2026-10-13). |
| Tech-enabled Israeli real-estate brokerage (licence as moat) | 24,984 active licensees; about 3.6–4k exam passes a year; one-exam barrier. The licence is abundant. It remains a labour-heavy service with no moat. |
| Services to newly registered contractors (classification, tenders) | Registrations tripled from 2015 to 2023 (24,373 registered). Overlaps K13 and M8 and adds no new moat. |
| Radon-testing permit service | 32 permit holders, but the dataset is stale (2017–19 expiries). Search found no current testing mandate or price. Scarcity without spending. |
| Israeli open data products (company, vehicle, transactions registries) | Data is open to every Israeli competitor. The "foreigners can't copy" advantage is irrelevant because local copiers are the threat. Market is about 407k active companies. |
| Buying Israeli licence holders | Licences here are abundant, so the purchase buys cash flow, not a moat. Capital is beyond the budget (L13/Phase 6 precedent). |

---

## Ranking, deep-diligence picks, decisive assumptions

1. **Falsification finding (methodological, highest value):** amend the Phase 9 scoring per Part 2. Defensibility counts only for capped or scarce holder sets, with holder-count trend data attached.
2. **F9-3 Israeli open-finance bank feeds**
   - Decisive unverified assumption: an Israeli financial-information-service licence (or a licensee's resale API) is obtainable for under about $10k and within 9 months, **and** fewer than about 10 non-bank holders serve accountants.
3. **F9-2 Adequacy-based back office for EU accountants**
   - Decisive assumption: EU/UK firms pay a premium for, or switch over, avoiding SCC/TIA paperwork. This is likely false.
4. **F9-1 IIA grant as a capital modifier**
   - Decisive assumption: small B2B export software qualifies for Tnufa, and IP/royalty terms do not restrict selling abroad.

**Overall recommendation:** do not open a Phase 10 Israel-niche track. Use Israel only as:
- a cost and grant base (F9-1);
- a GDPR-adequate jurisdiction (F9-2);
- a Track A cash bridge.

Any Israeli idea should carry a −1 to −3 point prior for undiscovered Hebrew incumbents.

## Sources (opened this phase unless marked)
- Empire Flippers API: api.empireflippers.com/api/v1/listings/list (Sold and For Sale), 2026-10-13
- BLS BED Table 7: bls.gov/bdm/us_age_naics_{00,23,44,51,52,53,54,56,61,62,71,72,81}_table7.txt, 2026-10-13
- CSIS/NPS: dair.nps.edu/handle/123456789/2730 (2018)
- Third Way, "12 solutions…" (2024-06-25)
- Census CES paper profiles: lehd.ces.census.gov/applications/creat/paper-profile/1270 (Zapletal CES-17-20; Haltiwanger et al. CES-24-42)
- Fredriksen 2020: econpapers.repec.org/RePEc:iab:iabjlr:v:54:i::p:a008
- EC IP/24/161 (2024-01-15) via the presscorner API
- Barnea Jaffa Lande barlaw.co.il/08mm (2024-12-29)
- data.gov.il CKAN: ica_companies, cpalist, metavhim, pinkashakablanim, socharim, notary, justice-patent-attorneys, medical-tourism-agent-list, radon-practitioners, fcs-importers, inspectors_fire_extinguishers, lists-permit-holders-for-the-provision-of-large-scale-post (2026-10-13)
- iTunes Search API, country=il, 10 Hebrew terms (2026-10-13)
- Search-summary only (not opened): SmartChoice whitepaper and insurancebusinessmag.com (insurance agencies); Pertama Partners (Tnufa); 2014 MoEP Environmental Health report and Technion (radon); Goldfarb and Gornitzky (blocked or unreadable)
- Blocked: bizbuysell.com (403), innovationisrael.org.il (403), goldfarb.com (403), goettingen-research-online (403); data.gov.il SQL and dump endpoints (WAF)
