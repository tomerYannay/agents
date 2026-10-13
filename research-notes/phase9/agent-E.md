# Phase 9 – Agent E (Distribution): contracted and term-gated distribution

Agent label: P9-E. Date: 2026-10-13. WebSearch used: **5 of 6**. Most evidence comes from public datasets and primary documents fetched directly:
- Texas DIR sales data (Socrata API, data.texas.gov);
- Sourcewell's awarded-contract spreadsheet and the solicitation records for RFP #030425;
- the Israeli Government Procurement Administration (מינהל הרכש) storefront and Nimbus tender PDFs;
- data.gov.il's central-tender dataset;
- the UK Contracts Finder API;
- ADA Member Advantage pages.

Scripts and data are in `scratchpad/p6plus/P9-E/`.

## Headline findings

1. **The best measurable term-gated channel is US cooperative purchasing contracts:**
   - Texas DIR: 2-year terms plus one 2-year renewal, 0.75% fee.
   - Sourcewell: 4-year terms plus up to three 1-year extensions, 1–2% fee.

   These are the US analogue of the G-Cloud work in Phase 6. Unlike G-Cloud, they publish **per-vendor sales**: Texas DIR posts every vendor sales report line.

2. **Holders of these contracts do far better than marketplace newcomers. This is mostly selection, not the moat.**
   - 94 vendors got their first DIR contract in 2023–24. In FY2026 (Sep 2025 to about Aug 2026):
     - 27 (29%) had $0 sales;
     - 44 (47%) had ≥$100k;
     - the median was $82.7k.
   - Phase 8 newcomer base rates were 4–6%.
   - But these holders are established firms, mostly IT staffing companies or SaaS makers that already had public customers. The contract removes buyer friction (no RFP needed). It does not create demand.
   - In the COTS-software solicitation, **16 of 50 holders awarded before 2025 sold nothing through DIR in FY2026.**

3. **These contracts are term-gated but not exclusive.**
   - Sourcewell's Public Safety Software RFP drew **80 proposals and made 39 awards (49%)**.
   - "No limit (minimum or maximum) on the number of awards has been imposed."
   - The moat is only against people who missed the window. Each category re-solicits about every 4 years. The G-Cloud timing problem that killed L10/L11 in Phase 6 applies here, but there are dozens of categories and several co-ops (Sourcewell, DIR, TIPS, BuyBoard, OMNIA), so some window is always open.

4. **Truly exclusive arrangements exist, but only incumbents hold them:**
   - Israeli central tenders: usually a single winner over a multi-year term.
   - National association endorsements: one provider per category.

   I found no evidence of a newcomer obtaining one within 3–9 months.

5. **Israel's G-Cloud analogue exists and is not in the ledger: Nimbus "tier 5", Central Tender 01-2022.** It is pass/fail, re-opens in rounds (2022, 2023, 2024, Oct 2025–Feb 2026), and admits Israeli or foreign ISVs listed on the AWS or GCP marketplace. Because it re-opens, it is not much of a moat, and I could find no winner list or spending data.

---

## E1. Co-op-contract-first niche public-sector SaaS (Sourcewell + Texas DIR)

1. **Concept.** Build one narrow workflow tool for US and Canadian local government or public safety. Win a Sourcewell award (valid in the US and Canada) and a DIR award (Texas, often used out of state) in a category whose solicitation is coming up. Then sell to agencies that can buy without their own RFP.

2. **Paying customer and geography.**
   - Customers: cities, counties, fire/EMS, K-12 and transit agencies in the US and Canada.
   - Sourcewell claims "50,000+ participating entities".
   - DIR data shows substantial "Out of State" buyers. Examples: Ondaro's ServiceNow sales were $4.07M of $4.66M out of state, and Veoci had out-of-state sales. [Verified: data.texas.gov a743-wj72, 2026-10-13]

3. **Model.** Annual SaaS subscription bought by purchase order against the master agreement. The vendor carries the co-op fee inside its price:
   - DIR fee: 0.75% [Verified: DIR-CPO-6079 contract PDF, cgi.com, 2026].
   - Sourcewell fee: "typically one percent (1%) to two percent (2%)" [Verified: Sourcewell RFP #030425 PDF].

4. **Spending evidence.**
   - DIR co-op sales were $3.38B in FY2025 and $3.84B in FY2026, across 525 and 582 vendors with sales [Verified: DIR datasets w64c-ndf7 and a743-wj72, computed 2026-10-13].
   - Sourcewell: ">$11 billion in contract sales volume" in 2023-24, "almost 800" contracts [Verified: Sourcewell Annual Report 2024 PDF].
   - The Public Safety Software RFP estimated "USD 80 Million" of annual transactions across its awards [Verified: RFP #030425].
   - Small software makers' FY2026 sales through DIR [Verified: DIR VSR data]:

     | Vendor | Product | FY2026 sales | Customers |
     |---|---|---|---|
     | Validas | — | $19.7k | 1 |
     | Saltus Technologies | digiTICKET | $30.7k | 3 |
     | Mongoose Research | — | $79.8k | 2 |
     | Periscope | — | $273k | — |
     | Veoci | — | $703k | 4 |

5. **Competitors and complaints.**
   - Every category already holds 1–39 awardees until about 2028–29. The Sourcewell median is 6 awards per solicitation (142 solicitations, 1,060 contracts, 932 suppliers) [Verified: Sourcewell contract-list.xlsx, updated 13-Oct-2026].
   - Public Safety Software alone has 39 holders, including large vendors (Motorola, CentralSquare, Tyler via other contracts) and small ones (3AM Innovations, PSTrax, Off Duty Management).
   - I did not gather buyer complaints [Unknown].

6. **Entry strategy.**
   - Target a category with **few holders and an imminent solicitation**. Then score well on the 40% price weight; financial viability is only 5% of points. In RFP #030425 the weights were Pricing 400 of 1,000 and Financial Viability 50 of 1,000 [Verified: Proposal Evaluation PDF].
   - The open Sourcewell solicitations I saw (closing Oct–Dec 2026) are mostly equipment. "Digital Procurement Platforms" closes 4 Nov 2026, too soon.
   - **None credible within 3–9 months without a product and reference customers.** Proposals are scored on "Ability to Sell and Deliver" and "Marketplace Success".

7. **Acquisition mechanism and channel evidence.**
   - The award itself plus co-op joint marketing. Step 12 of Sourcewell's process is "Develop and implement a joint marketing plan with awarded vendor(s)" [Verified: sourcewell-mn.gov/solicitations].
   - Newcomer outcomes measured on DIR:
     - COTS holders awarded 2023–24, FY2026 DIR sales: 16 of 50 had $0; 10 had $10–100k; 5 had $100k–1M; 19 had ≥$1M (mostly resellers such as SHI, CDW and Vertosoft). Median $78k.
     - All vendors new to DIR in 2023–24 (n=94): 29% had $0 and 47% had ≥$100k in FY2026.
   - Caveat: these are established firms. Sourcewell's own selling guide tells awardees to convert *existing* customers onto the contract [Secondary: search snippet, Sourcewell "Cooperative Contract Selling" PDF]. So part of DIR "sales" is migration, not new demand.

8. **Capital, operations and restrictions.**
   - Needs a US entity, insurance certificates (Sourcewell requires them) and a HUB subcontracting plan for Texas.
   - Texas cloud services also need **TX-RAMP**, which DIR's vendor page lists [Secondary: search snippet].
   - Insurance and compliance are likely ≥$2k/year [Hypothesis].
   - An Israeli founder can respond. Sourcewell accepted Carbyne, Compusult (Canada) and others, and its RFP is open to any responsive proposer. But "sales and service network ensuring availability" is an award factor [Verified: RFP §VI].

9. **Labour.** Public-sector sales cycles and implementation are founder-heavy at first. Renewals are sticky, so revenue can grow faster than hours after about 10 agencies [Hypothesis].

10. **Unit economics** [Hypothesis]. Annual contract value of $5–30k per agency. 10 agencies gives $50–300k ARR at about 80% gross margin. Track B is possible in years 2–4. Track A is not credible inside 9 months.

11. **Risks.**
    - Window timing: the category you build for may not re-solicit for years.
    - Holders with $0 sales (32% of COTS).
    - Copy risk is low during the term but resets at re-solicitation.
    - A product is needed before the award.

## E2. Contract-vehicle holder/reseller for small SaaS vendors (DIR/Sourcewell "Vertosoft model")

*Why this is not L11:* L11 was a G-Cloud reseller, killed for G-Cloud timing (reopens about Feb 2028) and a two-sided cold start. This idea uses US state and co-op vehicles that award in rolling batches (DIR COTS contracts start anywhere from Sep 2023 to Jan 2026), and it comes with measured reseller-newcomer outcomes.

1. **Concept.** Hold a DIR COTS (or similar) contract and add other vendors' SaaS brands to it. Agencies buy those brands through you, and you take a margin.

2. **Customer.** Texas and out-of-state public buyers. The supply-side customer is SaaS vendors that have no vehicle of their own.

3. **Model.** Reseller margin on licences [Unknown %].

4. **Spending and newcomer evidence** [Verified: DIR VSR data, 2026-10-13]:
   - Ondaro LLC: first contract Jun 2024; $248k in FY2025, then **$4.66M** in FY2026 (ServiceNow).
   - SATRDE LLC: $429k, then **$1.03M** (Zendesk, 7 customers).
   - Precision Task Group: $6.7M, then $42.1M (Workday and ServiceNow).
   - Vertosoft: $15.6M in FY2026 across 117 customers, including small brands such as SpareLabs ($354k).

5. **Competitors.** Carahsoft, Vertosoft, SHI, CDW-G and others already carry most vendors who have traction.

6. **Entry strategy.** Carry foreign, including Israeli, SaaS that has no US public-sector vehicle. That is the same "leftover vendors" problem the Phase 6 red team raised. **Weak.**

7. **Channel evidence.** Reseller newcomers clearly reach $1M+, but each did so with one blockbuster brand and existing relationships (Precision Task Group is a Workday partner).

8. **Restrictions.** Some DIR contracts bar designated resellers [Secondary: search snippet of a DIR contract]. You also need manufacturer authorisation, a HUB plan, credit exposure on pass-through, and a US entity.

9. **Labour.** Sales-led.

10. **Unit economics** [Hypothesis]. At a 3–8% margin, $1M of sales yields $30–80k gross. Track A requires about $1M+ in vehicle sales.

11. **Risks.** Vendors leave once they win their own award, and the margin is thin.

## E3. Nimbus tier-5 listing (Israeli government cloud marketplace) for an Israeli-built SaaS

1. **Concept.** List a narrow SaaS on the AWS or GCP marketplace. Then bid in the next Nimbus 01-2022 round so Israeli ministries can buy it through the government digital marketplace.

2. **Customer.** Israeli ministries, statutory units and associated bodies.

3. **Model.** SaaS via a marketplace "Private Offer".

4. **Spending evidence.** None found for tier 5 [Unknown].

5. **The moat is weak, and the documents show why** [Verified: Tender 01-2022 Publication 5 Booklet 1, Oct 2025; Accompanying Document, mr.gov.il attachments]:
   - The test is pass/fail. "The Tender Administrator will declare all of the services which were found to meet the parameters … as … Winner".
   - Thresholds are low: registered in Israel and compliant with the Public Bodies Transactions Law, or registered in a country with diplomatic relations with Israel.
   - The service must be on the AWS or GCP marketplace and pass a minimum cyber, privacy and security score.
   - Rounds reopen periodically (2022, 2023, Apr 2024, Oct 2025 with a Feb 2026 deadline).
   - Each service is offered by one bidder only. No Hebrew-only add-ons are allowed in the description.

6. **Entry strategy.** Hebrew-native workflow SaaS for ministries. The founder is Israeli, but so is every competitor.

7. **Channel.** Unproven. I could find no winner list, and the govextra minisite is JS-rendered.

8. **Requirements.** An AWS or GCP marketplace seller account, a security questionnaire, and Public Bodies Transactions Law compliance (tax-filing certificates). Cheap.

9–10. Labour and unit economics: [Unknown].

11. **Risks.** Listing is not the same as buying. Phase 6 found 86% of G-Cloud suppliers earn nothing, and the same is likely here [Hypothesis].

## E4. Single-winner Israeli central tenders for SaaS (killed for this founder)

- **Exclusivity is real.** The data.gov.il central-tender dataset covers 2009–21 and was last updated 2021. All 44 central tenders with listed winners show one winner each, mostly majors: VMware, Oracle, Citrix, Microsoft and telcos. One central tender for a queue-management system ran **21.11.2013 to 16.03.2023 with one winner** [Verified: data.gov.il resource 7038b3e6…, 2026-10-13].
- **A live example.** Central Tender 05-2025, "smart transport management and planning system" SaaS licences for all ministries, closes **26/12/2026** [Verified: mr.gov.il/ilgstorefront/he/p/4000599061].
- **No newcomer path.** Threshold conditions are typically references and an operating system. I did not read that tender's booklet [Unknown].
- **The Digitek framework (07-2023)** reopens in clusters (publications 5–8, 2025–26). It buys digital outputs, which means selling dev hours. Excluded by the founder's brief.

## E5. Exclusive association endorsement (killed: no newcomer path)

- **ADA Member Advantage** endorses about 27 categories with one provider each. Current holders include Best Card (processing), BaseKamp Design (web), Propio (interpreting), Weave (marked "New!") and HealthFirst [Verified: adamemberadvantage.com/endorsed-programs, 2026-10-13].
- **Due diligence takes time.** In ADA's own case study, the process "took a full year", with professional product review, proposals, financial statements and site visits [Verified: /due-diligence-process].
- **No newcomer examples.** A search for startup endorsements returned only HP (May 2026) and a 2019 Jonas Club deal [search #4]. State-level programmes such as TDA Perks list established vendors (Bank of America, CareCredit) [Verified: tdaperks.com].
- **No measured newcomer route.** It is also close to Phase 7's co-op and partner exclusions.

## E6. UK DPS and dynamic markets (killed as a moat)

- **Admission is open**, so the term does not block competitors.
- **Sample data.** MoJ Prison Education DPS: Contracts Finder lists 896 award notices since 2023. In a 100-notice sample, the median call-off was £38k, 74% went to SMEs, and there were 46 suppliers (Shannon Trust 23, PeoplePlus 16) [Verified: Contracts Finder API, 2026-10-13].
- **Not a fit for this founder:**
  - The work is labour services delivered in prisons.
  - Other DPS awards found were works, transport and consultancy.
  - Under the Procurement Act 2023, DPS is being replaced by dynamic markets, which are also open-admission [Secondary: background knowledge, not re-verified].

## E7. Exclusive placement and exclusive white-label (killed without spending searches)

- **Airport, hospital and university concessions** need capital and operations, and are close to P8's vending-placement exclusion.
- **Exclusive regional white-label of foreign SaaS** repackages L5 (exclusive distributor, killed) and L11.
- I found no public award data showing small or new winners, and spent no searches on these routes.

---

## Ranking

| Rank | Idea | Moat type | Rough Adjusted (my guess) | Track |
|---|---|---|---|---|
| 1 | E1 Co-op-first niche public-sector SaaS | Term-gated multi-award contract | about 42–45 | B (slow) |
| 2 | E3 Nimbus tier-5 listing | Pass/fail listing, periodic | about 37–40 | A? |
| 3 | E2 Contract-vehicle reseller | Term-gated vehicle | about 36–39 | A |
| — | E4, E5, E6, E7 | Exclusive but closed, or open (no moat) | killed | — |

None of these looks likely to enter the cumulative top cluster (about 50+). The main value of this round is **measurement**:

1. **Term-gated contracts give the first channel dataset where "holders" beat marketplace base rates by about 10×.** Among vendors new to DIR, 47% reached ≥$100k a year, against 4–6% newcomer base rates in Phase 8. But this rests on selection: awardees already had products and customers.
2. **Even inside the gate, about a third of software holders sell $0.**
3. **True exclusivity in procurement and associations goes to incumbents.**

**For the Contrarian (F) falsification question:** these moated positions do earn more per holder, but getting one requires an operating product and references first. They amplify an existing business. They do not start one.

## Top picks for deep diligence and their decisive unverified assumptions

1. **E1:** whether a Sourcewell or DIR category with ≤6 holders and a fitting software scope will re-solicit within about 12 months, and whether a vendor with 1–3 pilot customers can score into the award band. In RFP #030425 the lowest-ranked awardees scored about 700 of 1,000 against a top score of 843. Next step: pull Proposal Evaluation PDFs across 5–10 Sourcewell solicitations to find the lowest awarded score and the profile of the smallest winners. This is free WebFetch work.
2. **E3:** whether any ministry actually buys tier-5 listed SaaS. Next step: find the tier-5 winner list or buyer volumes, for example through a Freedom of Information request or the Nimbus minisite.
3. **E2:** reseller margin and whether DIR COTS allows adding brands mid-term [Unknown].

## WebSearch log (5 of 6 used)

1. Cooperative contracts and small vendors: explainers only.
2. Texas DIR vendor requirements: admin fee and HUB plan; designated resellers barred in some contracts.
3. Sourcewell small-vendor outcomes: none disclosed.
4. Startup exclusive endorsements: none found.
5. Nimbus tier 5: round history only.
