# Phase 10: Discovery Agent C (Traditional services: productised B2B at $300+/month)

Label: P10-C. Date: 2026-10-13. WebSearch used: **6 of 6**, all logged in `search-log.txt`.
Scratch: `scratchpad/p6plus/P10-C/` (scripts in `scripts/`, data in `data/`).

## 0. Method and what the evidence can and cannot say

**Empire Flippers (EF).**
- I reused Agent P8-C's full pull of the public `api.empireflippers.com/api/v1/listings/list` (2,878 listings, pulled 2026-10-13, the same day).
- I re-analysed every listing tagged Service, Agency or Lead Gen (100 listings), plus non-content Subscription, SaaS and Other listings. For each I read the full summary, `work_required`, risks and the 12-month `metrics` series [Verified-EF: API, 2026-10-13]. "Verified" here means EF-vetted and seller-reported, as defined in Phase 8.

**Flippa.**
- The public search page ignores the `query=` parameter. Searches for bookkeeping, compliance, payroll, medical billing and virtual assistant all returned the same first page of "Service" listings, so niche counts cannot be taken from Flippa [Verified: flippa.com/search, 2026-10-13].

**Google Ads Transparency Center.**
- The public `SearchSuggestions` RPC answered once: "Collaborating Docs LLC", US, **100–200 ads** [Verified: adstransparency.google.com RPC, 2026-10-13].
- Every later call was redirected to `google.com/sorry` (a CAPTCHA). Per the access rules I stopped and did not retry around it.
- The Transparency Center cannot be searched by keyword anyway. Advertiser density per keyword therefore remains [Unknown] for every idea below. Agent E owns that measurement.

**CPC benchmarks.**
- WordStream's and Search Engine Land's pages returned 403.
- I used TheeDigital's reproduction of the **WordStream/LocaliQ 2026 report** (13,474 US search campaigns, Apr 2025–Mar 2026) [Secondary: theedigital.com, 2026-10-13]:

| Category | Avg CPC | Conversion rate | Cost per lead |
|---|---|---|---|
| All industries | $5.26 | 7.52% | $70.11 |
| Legal | $8.58 | 5.09% | $131.63 |
| Financial services & insurance | $3.46 | 2.55% | $83.93 |
| Health & fitness | $5.00 | 6.80% | $62.80 |

- LocaliQ also gives business services at about $5.58 CPC and $103.54 CPL [Secondary: search snippet only].
- None of these are niche-keyword CPCs. I use them only as category priors.

## 1. What EF says about B2B service winners (the main finding)

I hand-classified the B2B service businesses listed since 2021 (about 29, excluding content/lead-gen sites and B2C tutoring or marketplaces).

| Pattern | Count | Listings |
|---|---|---|
| Marketing, SEO, PR, content, link building, ads | **23 of ~29 (≈79%)** | 48371, 59835, 62149, 70621, 74444, 78971/85227, 81375, 82856, 83779, 84972, 85301, 86176, 86292, 87450, 87669, 88851, 91868, 91893, 92659, 94608, 95198, 95759 |
| Operations or back-office | **6** | 62527 (subscription "business specialists", 60 Philippine contractors), 86244 (STR guest messaging, ledger N4), 71155 (realtor software + consulting), 90599 (recruiting), 92628 (DJ booking), 65067 (services for financial professionals) |
| Bookkeeping, compliance, billing or payroll | **0** | none in 2,878 listings since 2014 |

**Implication.** The direction's example categories (compliance-as-a-service, catch-up bookkeeping) have **no EF comparable at all**. Either they don't transfer through brokers (licences, client trust in a named accountant), or online operators don't build them. I can't tell which. Any claim that those niches work for a newcomer is therefore [Hypothesis], not EF-backed.

**Price per account.** Listings at or above $300/month per account:
- 84972: retainers of $1.5k–8k; >120 clients; $147k/month profit.
- 87450: about $1,100/client.
- 59835: lifetime value about $11.5k against CAC about $490.
- 74444 and 85301: lifetime values of $18k and $15.8k.
- 86244: about $340/month ($44.6k ÷ 130 clients).

Below the floor: 88851 (about $89/subscriber: $22.2k ÷ 250+) [Verified-EF].

**Channels.** Paid acquisition is named in only 8 service listings:
- 71155: 26% paid traffic.
- 47663: 24% paid.
- 88851: Google, Microsoft and LinkedIn ads.
- 86244: ads plus referrals.
- 87450: outbound, paid and referrals.
- 84972: cold calling, Facebook ads and referrals.
- 87669: Meta ads.
- 92592: Google search ads.

The rest are referral, organic or outbound. Paid search is a minority channel even among survivors [Verified-EF].

**Owner hours.** The median is about 5 h/week across B2B service listings, which confirms P8. All of it is sales and QA oversight of 8–60 contractors.

**Trend check for young (≤3-year) B2B services** (monthly series):
- 59835: profit peaked at $38k (Dec 2021), then fell to $8–17k.
- 86244: −$0.3k to $18.8k a month, volatile.
- 78971 → 85227: profit fell 44% between the two listings.
- 92659: profit roughly halved, from $6.6k to $2.9–5.6k.
- 90599: $0–24k a month swings with 3–5 active clients.
- 87450 and 94608: grew.

So most young service survivors are volatile or declining at the point of sale.

**The cleanest non-marketing "contractor seats" comparable is #62527:**
- $78.1k/month revenue and $19.6k/month profit (25% margin); 4 h/week owner time.
- 60 Philippine contractors selling subscription access to "business specialists".
- 53% organic traffic; profit trend +16% [Verified-EF: API, 2026-10-13].

It is 5.4 years old at listing. That is not newcomer evidence.

## 2. Opportunities

### C1. Collaborating-physician + compliance service for NPs/PAs in restricted states, specialty-wedged (best)

1. **Concept.** In states that require it by law, nurse practitioners and PAs must have a physician collaboration or supervision agreement. The service matches each one to a collaborating physician (a paid 1099 contractor), drafts the state-compliant agreement, and runs the recurring compliance admin: chart-review logs, meeting attestations, ratio tracking and licence renewals, all in software. The wedge is one specialty with scarce collaborators and higher fees, e.g. psychiatric NPs (telehealth) or aesthetic NP/RN injectors (med-spa medical director plus good-faith exams).
2. **Customer and geography.** NPs/PAs and the clinics or telehealth companies employing them in the 23 reduced/restricted jurisdictions. Restricted: CA, TX, FL, GA, NC, SC, TN, VA, MI, MO, OK. Reduced: PA, OH, IL, IN, WI, KY, WV, NJ, AR, LA, MS, AL [Verified: AANP 2026 State Practice Environment map PDF, 05/2026].
3. **Model and price.** Recurring monthly fee per NP, plus an optional match fee.
   - Market rates: DirectShifts says most arrangements cost $500–1,200/month, restricted states $1,000–1,800, and controlled-substance programmes $1,500–3,000+ [Secondary/vendor: directshifts.com, 2026].
   - SingleAim's physician-pay interquartile range is **$450–750/month** (631 data points), with NC averaging $706, NJ $793 and MN $862 [Verified: singleaimhealth.com/collaborating-physician-pay, 2026-10-13; NC/NJ/MN figures from search snippets].
   - Collaborating Docs charges an onboarding fee plus a state-based monthly fee that includes physician malpractice insurance. Prices are not published [Verified: collaboratingdocs.com/pricing, 2026-10-13].
   - Zivian charges one flat monthly fee with no matching fee and a 7-day match [Verified: zivianhealth.com/collaboration].
4. **Spending evidence.**
   - The requirement is statutory: no agreement, no practice.
   - Collaborating Docs runs **100–200 Google ads** in the US [Verified: Ads Transparency RPC].
   - Zivian raised a $3M seed (Aug 2023) and claimed >2,500 licences managed and 20+ organisations within 10 months [Verified: crosslinkcapital.com press page; vendor claim].
5. **Competitors.** Collaborating Docs, Zivian Health, SingleAim, DirectShifts, and OpenLoop (named by DirectShifts). Customer complaints are not measured [Unknown].
6. **Entry strategy.** A single specialty and 2–3 states, priced at the incumbents' level but with faster matching in that specialty. The generalist incumbents compete on breadth. A specialty collaborator bench (psychiatrists, or aesthetic-trained physicians) is the only real wedge. If incumbents already fill those specialties well, there is **none credible** [Hypothesis: check specialty match times].
7. **Acquisition.**
   - NP side: Google Search on "collaborating physician [state]", "supervising physician for NP [state]", "med spa medical director [state]". Competitor paid activity is verified, but keyword density is [Unknown].
   - Category prior: health CPC $5.00, conversion rate 6.8%, CPL about $63 [Secondary].
   - Partners: NP programmes, billing companies, telehealth staffing firms [Hypothesis].
   - Physician side: Doximity or LinkedIn job ads [Hypothesis].
   - Newcomer outcomes: no measured data. The only entrant signal is Zivian, a 2023 seed-funded company that scaled licence count fast (vendor claim). No 2024–26 entrant raise was found.
8. **Operations.**
   - US LLC; state-specific agreement templates (legal review about $2–5k [Unknown], possibly over budget); placement of physician malpractice cover (cost [Unknown]); BAA/HIPAA handling of chart-review logs.
   - Operable from Israel. The physicians are US contractors.
   - Legal: fair-market-value fees, and anti-kickback exposure where Medicare is involved, need counsel [Unknown].
9. **Labour.** Low agency drift. Matching and compliance admin are software plus one coordinator per roughly 100–150 NPs [Hypothesis]. Revenue scales with the physician bench, not founder hours. This is the least "hours-for-money" idea in this report.
10. **Unit economics** [Hypothesis built on the secondary prices above]:
    - NP pays $900/month, physician gets $600, malpractice and software cost about $75 → **about $225/month contribution per NP**.
    - CAC at CPL $63–100 and a 20–25% close rate is roughly **$250–500**. If 3 followers bid on the same state keywords, assume CPC +50–100% → CAC $400–1,000. Payback is still 2–5 months, provided NP retention is ≥12 months [Unknown].
    - Track A (about $3k/month owner profit) needs about 20–25 active NPs after a part-time coordinator.
    - Track B ($10k+) needs about 60–80 NPs. Zivian's claimed scale suggests demand of that size exists.
11. **Risks.**
    - VC-funded incumbents with no match fee.
    - States moving to full practice authority, which removes demand. The direction has been steady toward FPA.
    - Two-sided cold start: no physicians means nothing to sell.
    - Malpractice placement cost.
    - Easy to copy (defensibility ≤2).
    - Liability if a collaborator is negligent in chart review.

**Cheapest test (describe only).**
- Landing page for one specialty in TX + FL, with a "physician match + monthly rate in 48h" quote form.
- $800 of Google Ads over 3 weeks on exact-match state-plus-collaborator keywords.
- In parallel, a $300 Doximity or LinkedIn physician-interest ad at a stated $600/NP/month.
- **Kill if** any of these hold:
  - NP cost per qualified lead is above $120, or there are fewer than 7 qualified leads;
  - fewer than 2 NPs accept a quote of ≥$800/month;
  - fewer than 4 specialty physicians express interest at ≤$650/month.

### C2. Vertical offshore operations seats for US independent insurance agencies (EF pattern #62527)

1. **Concept.** A dedicated Philippine or LatAm service-desk contractor trained on the agency's management system (Applied Epic, HawkSoft, EZLynx), sold as a fixed monthly seat with QA, SOPs and AI-assisted task tooling. Tasks are non-licensed: certificates of insurance, endorsements, renewals prep and carrier-portal downloads.
2. **Customer.** US independent P&C agencies.
3. **Model.** Per seat per month.
   - Market: offshore insurance VAs $1,200–2,000; LatAm $2,000–3,500; Stealth Agents from $1,600; Wing about $1,380 for 30 h; MyOutDesk about $1,988 full-time [Secondary/vendor blogs via search, 2026-10-13].
4. **Spending evidence.**
   - Wing claims 500+ agencies and brokerages [vendor claim, search snippet].
   - EF #62527 shows the seat model at $78k/month revenue with a 25% margin [Verified-EF].
5. **Competitors.** Wing Assistant, Stealth Agents, HireInSouth, MyOutDesk, plus AI-receptionist vendors (Sonant) pitching replacement. What customers dislike: turnover (a vendor claims 78%/year in insurance) and 20–40 h of training per VA [vendor claims].
6. **Entry strategy.** Weak. Possible angles:
   - narrow tooling (pre-built system SOP libraries plus an AI QA layer per task type);
   - a Spanish-bilingual desk for Hispanic-market agencies [Hypothesis].

   Otherwise **none credible** against a dense, copyable field.
7. **Acquisition.**
   - Google "insurance virtual assistant". Category prior: financial services & insurance CPC $3.46, conversion 2.55%, **CPL about $84** [Secondary].
   - Partners: agency alliances and clusters. P7-C found no vendor-side fee terms.
   - Newcomer outcomes: [Unknown]. No public count of VA-firm survival.
8. **Operations.** Contractor hiring and payroll (Deel/Wise), with low capital: first seat cost is about $700–1,000/month for a Philippine full-timer [Hypothesis]. Operable from Israel; Philippine time zones work for US mornings via night shift.
9. **Labour (agency drift: high).** This is staffing. Revenue scales with contractors, not founder hours (62527 owner: 4 h/week). But churn, QA and hiring are permanent management load, and margin is a labour markup.
10. **Unit economics.**
    - Seat at $1,600, contractor at $800, QA and tools at $150 → **about $650/month per seat** [Hypothesis].
    - CAC at CPL $84 and a 10–15% close rate is $560–840. With 3 followers, about $800–1,300.
    - Payback is 1–2 months if seats last ≥6 months [Unknown].
    - Track A needs 6–8 seats; Track B needs 25–40 seats plus a hired operations manager. Price is the main lever, and copying compresses it.
11. **Risks.** AI agents eat the task set. Price compression. Contractor turnover. Licensing creep (unlicensed staff quoting).

**Cheapest test.**
- $700 of Google Ads plus a landing page offering a 2-week paid trial seat at $1,600/month for COI/endorsement work.
- **Kill if** CPL is above $150, or 10 discovery calls produce fewer than 2 signed seats.

### C3. Compliance operations desk for newly registered small RIAs (not CCO-of-record)

1. **Concept.** A fixed-fee programme for new SEC-registered investment advisers with ≤10 employees. It covers annual compliance calendar, Form ADV/CRS updates, Marketing Rule review of ads and social posts, code-of-ethics attestations, and annual review packs. Delivery is by ex-compliance contractors with AI pre-review software. The firm's own principal stays CCO, which avoids being named CCO with that liability.
2. **Demand (transaction trigger, verified).** The SEC monthly adviser file (Sept 2026, 17,210 SEC RIAs) shows SEC-status effective dates of 1,178 in 2024, 1,321 in 2025 and **1,372 in Jan–Sep 2026**. Of the 2026 cohort, 1,205 have ≤10 employees [Verified: sec.gov ia09012026.csv, 2026-10-13]. Caveats: these are survivors only, and the effective date may include state-to-SEC switches. State-registered RIAs add more but are not counted.
3. **Price.**
   - Full outsourced-CCO services run at $5–8k/month (Key Bridge, InvestmentNews 2023).
   - Setup is $10–25k plus $8–15k/year ongoing (Advisor Perspectives 2021).
   - Law-firm OCCO is $450/h [Secondary: search snippets; AP page 403].
   - A software-leveraged tier at **$600–1,200/month** sits below these [Hypothesis].
4. **Competitors.** Many outsourced-CCO and compliance-software firms (not enumerated; [Unknown] count). Dislikes: price, and generic templates [Unknown].
5. **Entry strategy.** A price tier for 1–10-person new RIAs, triggered by the public registration feed (new SEC registrants are identifiable monthly). Plausible but unverified.
6. **Acquisition.**
   - Google "RIA compliance consultant" / "outsourced CCO". Category prior: financial services CPC $3.46, CPL about $84; niche CPC [Unknown].
   - Partners: custodians' new-RIA programmes, RIA launch consultants [Hypothesis].
   - Newcomer outcomes: [Unknown].
7. **Operations.** Needs contractor ex-CCOs; errors-and-omissions insurance [Unknown cost]. Founder fit is low: no securities domain experience. Operable from Israel.
8. **Labour (agency drift: high).** This is regulated consulting with software assist. Scales with contractors; quality and liability stay with the founder.
9. **Unit economics** [Hypothesis]:
   - $900/month fee, contractor about 4 h/month at $75 plus software → about $550 contribution.
   - CAC with CPL $84–150 and a 15% close rate is $560–1,000. With followers, $900–1,500.
   - Track A needs about 8 clients; Track B 25–40. Churn is low once installed [Unknown].
10. **Risks.** Liability for missed filings. An SEC enforcement-driven trust premium favours brand-name firms. Founder fit. Agency drift.

**Cheapest test.**
- $600 of Google Ads plus a landing page with a fixed-price "first-year compliance programme" at $900/month.
- **Kill if** CPL is above $200, or fewer than 2 of the first 8 calls accept the price.
- A desk check before spending: count how many of the 2026 small registrants already list an outsourced compliance provider. Form ADV Schedule D names service providers.

### C4. Niche catch-up + monthly bookkeeping for one vertical (weakest; kept because the direction named it)

1. **Concept.** A one-off cleanup of 1–3 years of books ($1,500+), then $300–600/month. Delivery is offshore bookkeepers with AI categorisation, for one vertical with messy payouts (Shopify/Amazon sellers or STR hosts).
2. **Spending evidence and competitor reality.**
   - Bench shut down on 27 Dec 2024 after raising about $100M. It claimed 35k customers; Employer.com bought it by 1 Jan 2025 and puts the active base at about 12k [Verified: americanbanker.com, 2026-10-13].
   - Bench now lists $199/$399/$649 a month. **Current-year catch-up is free on annual plans**; more than a year behind is quoted [Verified: bench.co/pricing, 2026-10-13].
   - In other words, the leading productised player gives away the "catch-up" wedge, and VC-scale productised bookkeeping failed once.
   - EF has zero bookkeeping comparables.
3. **Competition.** Very dense: Bench, Pilot, e-commerce specialists including Israeli Finaloop, and thousands of firms. Entry strategy: **none credible** beyond hyper-niche plus price.
4. **Acquisition.** Financial services CPL about $84 and the lowest conversion rate of any category (2.55%) [Secondary]. Newcomer outcomes: [Unknown].
5. **Agency drift.** High. It is an accounting firm with tax-season peaks.
6. **Unit economics** [Hypothesis]:
   - $450/month at a 50% gross margin → $225/month.
   - CAC $500–1,200 → payback of 3–5 months, getting worse under copying.

**Cheapest test.**
- $500 of ads on "[platform] bookkeeping catch up".
- **Kill if** CPL is above $120, or fewer than 2 of 10 leads accept $1,500+ for cleanup.

I expect this to fail.

## 3. Killed or not proposed

| Idea | Reason |
|---|---|
| Single-trade LSA/local-SEO productised agency | Strongest EF P&L of all (#84972: $147k/month profit, $1.5–8k retainers, 100+ clients in one sub-niche, cold calling + Facebook ads). But it repackages P8 C3 and the med-spa ads agency already in the ledger. Pure agency. |
| LinkedIn prospecting for financial advisers (#92659, #65067) | #92659 profit roughly halved over 12 months and is still for sale. |
| Realtor email-blast services (#78971/85227) | −44% between listings. Needs an owned list. |
| Remote recruiting (#90599) | 3–5 active clients; months at $0–2k; founder-sold. |
| Manufacturer marketing subscription (#88851) | About $89/account, below the $300 floor. It is the only clear Google/Microsoft/LinkedIn paid B2B service in EF. |
| STR guest messaging (#86244) | Ledger N4. |
| SOC 2 readiness-as-a-service via Vanta/Drata partners | Pure consulting, needs audit credibility the founder lacks, partner economics unread, crowded [Hypothesis; not researched further]. |
| Done-for-you US sales-tax filing | VC software incumbents (Numeral, Kintsugi, Avalara, TaxJar) sell this as software. No price or labour wedge [Hypothesis]. |
| Med-spa licensing/compliance consultancy (Flippa) | The one Flippa listing is 10 years old, $7.18k/month revenue, n=1 [Anecdote: Flippa card]. Folded into C1 as the aesthetic wedge. |

## 4. Ranking and decisive assumptions

1. **C1: NP/PA collaborating-physician service (specialty wedge).**
   - Why first: statutory recurring demand in 23 jurisdictions; $500–1,200/month price; verified paid-search activity by an incumbent (100–200 Google ads); lowest agency drift.
   - **Decisive assumption:** a specialty physician bench can be recruited at ≤$650/NP/month while NPs pay ≥$850, and specialty NPs are under-served by Zivian or Collaborating Docs (match-time gap).
2. **C2: Insurance-agency offshore operations seats.**
   - Why second: the only EF-backed operations comparable (#62527); low capital.
   - **Decisive assumption:** paid-search CAC stays below about $900/seat with ≥6-month seat retention despite a dense, copyable field and AI substitution.
3. **C3: Small-RIA compliance operations desk.**
   - Why third: verified monthly trigger list (about 1,200 small SEC registrants so far in 2026). But high drift and poor founder fit.
   - **Decisive assumption:** new small RIAs will pay $600–1,200/month to a non-brand provider, and are not already bundled by custodians or launch consultants.
4. **C4: Niche catch-up bookkeeping.** Expected kill: the incumbent gives catch-up away free.

**Cross-cutting conclusions for the Director.**
- EF does not support "compliance-as-a-service" or "catch-up bookkeeping" as proven newcomer service categories. B2B service survivors there are about 79% marketing services, mostly referral- or outbound-acquired.
- High-ticket paid-search services that survive copying need a supply-side asset that followers cannot rent instantly: C1's physician bench is the closest. Contractor-seat models (C2, C3) have no such asset, so 3 followers bidding on the same keywords would push CAC up roughly 1.5–2× [Hypothesis], and owner margin would erode toward the 19–25% seen in #86244 and #62527.

WebSearch count: **6 / 6**.
