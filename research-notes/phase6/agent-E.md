# Phase 6 — Discovery Agent E: Distribution-first opportunities and existing customer spending

Agent: E | Date: 2026-10-13 | WebSearch used: 8 of 8 (logged as P6-E) | Data: public pages, the gov.uk CSV, the Contracts Finder OCDS API, the data.gov.il CKAN API, TrustMRR public Markdown pages and the Companies House public search. Scratch data is in `scratchpad/p6plus/E/`.

## Method
I started from channels where money is visibly changing hands and tried to measure what **newcomers or small operators** get from each one, not just the leaders. Then I fitted a business to the channel. Five channel families were tested:

1. **UK public-procurement frameworks.** I used G-Cloud spend data (the 2018 gov.uk CSV, about 9.6 MB, which I analysed myself) and live 2026 award notices pulled from the Contracts Finder API (213 unique G-Cloud call-off awards).
2. **Israeli government procurement.** I used the data.gov.il "exemptions" dataset (165,705 records).
3. **Niche job boards.** I counted postings and checked prices directly, and used TrustMRR pages where revenue is verified through the payment provider's API.
4. **Newsletter and media sponsorship.** I used vendor rate cards plus one verified-revenue community-media business.
5. **Association career centres and reseller/affiliate programs.**

Headline finding: **UK G-Cloud is the only channel I found where per-transaction buyer spending, small-supplier wins and newcomer failure rates can all be measured from public data.** It is also the only one where non-UK companies are seen winning awards. Job boards and newsletters can be measured for the leaders but not for newcomers. Reseller and affiliate programs publish no newcomer data at all.

---

## E1. G-Cloud micro-SaaS for one narrow UK public-sector workflow
**1. Concept.** Build one small cloud tool for a single workflow that UK councils, NHS trusts or fire services buy in £15–55k direct awards. Examples from 2026 awards include registrar booking, cycle-training booking, growth-chart software, driving-licence checks for staff, children's-home policy libraries, and dental course administration. List it on G-Cloud 15 (Lot 2, Cloud Software) and sell through catalogue search and direct award.

**2. Paying customer and geography.** UK public bodies: councils, NHS trusts, fire and rescue services, arm's-length bodies and universities.

**3. Model and price.** An annual subscription bought by direct award under the framework, typically 1–3 years plus a 12-month extension. Observed small SME awards are about £14k–£55k per contract.

**4. Spending evidence.**
- **2026 call-offs.** I pulled 213 unique G-Cloud award notices from Contracts Finder for parts of Jan, May and Sep 2026; the API rate-limited the other months. [Verified: Contracts Finder OCDS API, accessed 2026-10-13]
  - 108 of the 213 went to suppliers flagged SME.
  - The median award was £138.6k, and 40 awards were under £50k.
  - Small niche SaaS awards to SMEs included:
    - Stopford "Registrar Booking System": £14,304
    - Maxinity "Dental Max-course": £16,500
    - Licence Check Ltd "Driving Licence Checks" (Essex Fire): £18,000
    - Signis "Children's homes online policies" (Dorset): £30,200
    - Oyster "Legal case management": £30,970
    - Harlow Printing "Growth Chart Software": £43,088
    - Clarity "TfGM Cycle Training Booking": £44,120
    - Policy in Practice "Low Income Family Tracker": £50,900
- **Framework size.** G-Cloud 15 went live in August 2026. It is worth about £14bn over 4 years, with about £3bn a year flowing through it, and about 90% of its suppliers are SMEs. New suppliers can join during an **18-month reopening window** and at intervals after that. [Verified: gov.uk "G-Cloud relaunches with biggest upgrade in its history", 10 Aug 2026]
- **Recent spend split.** £2.9bn in FY24/25, with SMEs taking 42%. SME spend rose 9.7% in FY25/26. [Secondary: TechMarketView via search snippet]
- **2018 micro-supplier outcomes (my own analysis of the gov.uk CSV).** [Verified: gov.uk G-Cloud spend CSV to Dec 2018, accessed 2026-10-13]
  - In calendar 2018, 346 micro suppliers had any G-Cloud spend, with a median of £139k each.
  - In the "Cloud Software" lot specifically, 141 micro suppliers had spend, with a median of £60k. 43 of them billed under £25k.
  - Cohort test: 178 micro or small suppliers first billed in 2017. In 2018 their median was £62k, 45 billed nothing, 96 billed over £50k and 46 billed over £250k.

**5. Competitors and what buyers dislike.** Each niche usually has 1–3 established vendors, all checked on Companies House and incorporated between 1999 and 2016: Stopford 1999, Maxinity 2003, Clarity 2007, Licence Check 2008, Policy in Practice 2009, Signis 2014. [Verified: Companies House search, 2026-10-13] Large suites (Access, OneAdvanced, Civica) bundle these functions. I found no public data on what buyers dislike [Unknown]. The usual complaints about legacy council software (dated UX, per-module pricing) are a [Hypothesis].

**6. Entry strategy.** Target workflows where the buyer currently uses spreadsheets or a legacy desktop tool, and where the whole annual spend is under the threshold that triggers a full tender. Win on price (for example £6–12k a year against £15–45k), fast onboarding and a pre-written security and DPIA pack. The 2026 award data provides the target list: each notice names the buyer, product category, value and contract end date, so renewals can be predicted. Without a specific under-served workflow found from renewal data, the honest position is "no credible entry strategy yet."

**7. Acquisition mechanism and newcomer evidence.** The channel works like this:
- The buyer searches the G-Cloud catalogue by keyword, saves a shortlist, evaluates it and direct-awards.
- Contracts Finder publishes each award, so incumbents' renewal dates can be found.
- Low-cost outbound to named budget holders adds to this.

Newcomer outcomes are poor in aggregate. A Tussell analysis of G-Cloud 10 found **only 480 of 3,474 suppliers (14%) won any business** in 12 months. [Secondary: Tussell via ComputerWeekly/ChannelWeb search snippets; the pages returned 403] My 2018 data agrees: roughly 970 suppliers billed anything, against a supplier base in the thousands. Conditional on winning, though, the 2017 micro and small cohort's median was about £62k in year two. Every small SME winner I sampled was 10 or more years old. **I found no example of a company under 2 years old winning.**

**8. Capital, operations and Israel operability.**
- **Non-UK suppliers do win G-Cloud awards.** In my 2026 sample: Sayari Labs Inc (US, £54k), Freshworks Inc (US, £10.8k), American Well Corp UK, and Via Technologies Europe B.V. (NL). [Verified: Contracts Finder awards]
- Formal G-Cloud 15 eligibility rules for non-UK suppliers were not found [Unknown]. A UK Ltd is the cheap hedge.
- Likely requirements: Cyber Essentials (about £300–600 a year, [Hypothesis]), professional indemnity insurance, UK/EU data hosting, and accessibility (WCAG) compliance. G-Cloud 15 Lot 1b needs Cyber Essentials Plus and £75m insurance, so avoid Lot 1b. [Secondary: search snippet]
- This fits inside $2k, excluding the founder's build time.

**9. Labour dependence.** After the sale, delivery is software. Support is light but buyers expect phone and email support. Each sale takes founder time (clarification questions, security questionnaires), but revenue compounds through multi-year contracts.

**10. Unit economics.** [Hypothesis built on the verified award sizes]
- One award of about £8–20k a year is roughly 85–90% gross margin.
- 5 contracts would give about £50–80k a year, which is Track A.
- 20 or more contracts, or a niche-wide standard, would be needed for Track B.
- Time to first sale is plausibly 6–18 months [Unknown; no newcomer data].

**11. Risks.**
- The 14% win rate.
- Buyers favouring incumbents with references.
- Procurement Act 2023 changes.
- Data residency and assurance burden.
- **Kill test:** if, among buyers whose contracts are near renewal, nobody will even take a demo call, kill it.

---

## E2. G-Cloud reseller and route-to-market for non-UK SaaS vendors
**1. Concept.** A UK entity that lists, resells and supports a portfolio of foreign (Israeli, EU or US) SaaS products on G-Cloud 15. It handles the framework paperwork, assurance, invoicing and call-off administration, and earns a reseller margin on licences. This is the "partner/reseller program" channel combined with the procurement channel.

**2. Paying customer and geography.**
- Buyers: UK public bodies.
- Suppliers and partners: foreign SaaS vendors without a UK public-sector team. Israeli B2B SaaS vendors are a natural pool. This is a materially different model from the ledger's "SaaS group buying for Israeli startups".

**3. Model and price.** A reseller margin on licence value, plus optional paid onboarding. The margin percentage is [Unknown]; 10–25% is a [Hypothesis].

**4. Spending evidence.** Resellers win licence awards in my 2026 sample. [Verified: Contracts Finder]
- Generation Digital, "MIRO Licence Expansion": £152,064. Generation Digital is a G-Cloud reseller of Miro, Notion, Asana and Glean. [Verified: gend.co/blog/g-cloud-services-uk-public-sector, 2026-10-13]
- TribusIT, "Collaboration Software Licences": £191,215.
- Eficode UK, "Atlassian Licensing": £110,979.
- Softcat / SCC, ServiceNow licences: £645k–£1.03m.

TCS's G-Cloud 15 documents state that it holds reseller agreements with several SaaS providers. [Secondary: search snippet of the TCS G-15 pricing PDF] A ChannelWeb headline reports that "one in five resellers did business on G-Cloud". [Secondary: headline only; page 403]

**5. Competitors.** Large value-added resellers (Softcat, SCC, Computacenter, XMA) and specialist resellers (Generation Digital, Eficode, TribusIT). Foreign vendors' complaints about these are [Unknown].

**6. Entry strategy.** Large resellers ignore small, unknown foreign vendors. Offer those vendors an exclusive or semi-exclusive UK public-sector listing with no upfront fee, plus software automation of the paperwork (service definitions, pricing documents, security answers). This is credible only if vendors with real UK-public-sector fit can be signed.

**7. Acquisition mechanism.** Two-sided:
- **Vendor side:** direct outreach to foreign SaaS firms. Newcomer conversion is [Unknown].
- **Buyer side:** catalogue search plus the vendor's own UK leads. Same 14% caveat as E1.

**8. Capital and operability.**
- A UK Ltd, Cyber Essentials and insurance.
- No inventory, but reseller credit exposure: you pay the vendor and the government pays you, usually within 30 days.
- Israel-based ownership is feasible. A non-UK entity winning is evidenced by E1's examples.

**9. Labour dependence.** Medium. Each listing and each call-off needs admin, though AI can automate much of the documentation. Revenue scales with the number of vendors, not founder hours, once several vendors are listed.

**10. Unit economics.** [Hypothesis] One £50–150k licence deal a year at a 10–15% margin gives £5–22k of gross profit. Four to six such deals would be Track A. Track B needs a portfolio of dozens of vendors or a few large wins.

**11. Risks.**
- Vendors refusing to give margin.
- Every vendor sales cycle being 6–18 months.
- Reseller liability under the call-off contract.
- **Decisive unknown:** will 3 or more non-UK vendors with real UK public-sector demand sign up?

---

## E3. Revenue-share career-centre operator for small professional associations (outside the US)
**1. Concept.** Run white-label job boards for small and mid-size professional associations in the UK, Ireland, Australia, Canada or Israel. The association brings the audience and brand. You provide the software, seed the board with jobs (backfill), sell employer postings, and split the revenue.

**2. Paying customer and geography.** Employers hiring in a profession pay per posting. The association is the channel partner.

**3. Model and price.** Pay-per-post, about $150–400, plus bundles. Revenue is shared with the association (percentage [Unknown]).

**4. Spending evidence.**
- YM Careers (Momentive) claims more than 3,000 association career centres. [Anecdote/vendor claim, via search snippet]
- Naylor uses a revenue-share model with a $2,500 setup fee. [Secondary: Cavuno blog, verified page 2026-10-13]
- Niceboard claims AIA Colorado's board generates $50–100k a year [Anecdote/vendor claim]. My check of jobs.aiacolorado.org showed only about 14 live jobs by category count, so the claim is unverified and possibly stale.
- **Job-board software pricing** (Cavuno blog, verified page 2026-10-13):

  | Vendor | Monthly price |
  |---|---|
  | Cavuno | $39–105 |
  | JBoard | $119–849 |
  | Niceboard | $319–599 |

**5. Competitors.** YM Careers, Naylor, Web Scribble and SmartJobBoard dominate in the US, and association management software includes job boards. Cavuno's (competitor-written) post says the revenue-share model is costly to large associations and leaves them dependent on the vendor's sales performance [Secondary].

**6. Entry strategy.** Target non-US associations of 1,000–20,000 members that have no career centre or only a static "jobs" page. Offer zero setup cost, AI job backfill, and an automated employer-outreach engine. Credibility depends on whether those associations have employers willing to pay [Unknown].

**7. Acquisition and newcomer evidence.** The channel is outreach to association executives, of which there are thousands of enumerable associations. Newcomer outcomes are [Unknown]. The comparable channel economics show that niche boards often have to give basic listings away free: Conservation Job Board (500 live jobs) has free basic listings and a **$65** premium upgrade [Verified: conservationjobboard.com, 2026-10-13].

**8. Capital and operations.** Low, under $2k with off-the-shelf software or your own build. Israel operability is fine. Employer sales are the operations burden.

**9. Labour dependence.** Medium. Sales across associations can be automated, but each association relationship needs attention.

**10. Unit economics.** [Hypothesis] One association producing 10 paid posts a month at $200 gives $2,000 gross, and $1,000–1,400 after a 30–50% revenue share. Three to five healthy associations would be Track A. Track B needs a network of 20 or more.

**11. Risks.** Small associations' boards get very few paid posts; the AIA Colorado check suggests low volume. Incumbents are entrenched. LinkedIn and Indeed act as substitutes.

---

## E4. Seeker-paid job search with AI application tools in a non-English market
**1. Concept.** An aggregator of internships, apprenticeships and entry-level jobs for one language market (for example Germany's Ausbildung, Poland, Brazil, Italy or Spain). Free search, with a cheap Pro tier for AI CVs and cover letters and fit scoring. The model follows French Ton-piston.

**2. Paying customer and geography.** Students and early-career job seekers in a single non-English market.

**3. Model and price.** €9.99 a month, matching Ton-piston's Pro tier.

**4. Spending evidence.**
- **Ton-piston (FR), founded 2026-08-03.** [Verified: trustmrr.com/startup/ton-piston.md, Stripe-API verified, 2026-10-13]
  - $10,517 in revenue over the last 30 days and $22,065 all-time, after about 10 weeks.
  - Claims about 50,000 users.
- **Remote Rocketship.** A solo-built remote-job aggregator charging seekers $18 a month, reportedly earning about $6k a month [Secondary: Kardow article].
- **Hirevire** ($13k MRR) and **Rezi** ($249k MRR) show that adjacent career tools sell. [Verified: TrustMRR recruiting category, 2026-10-13]

**5. Competitors.** Indeed, StepStone, LinkedIn, national boards (Ausbildung.de, Azubiyo, Pracuj.pl) and generic AI CV tools. In 2026, Google is giving Google AI Pro/Plus free to students and apprentices for a year in Germany, which is a substitute threat. [Secondary: mydealz/borncity snippets]

**6. Entry strategy.** A language- and season-specific product (apprenticeship and internship seasons) in a market without a Ton-piston equivalent. Whether such a market exists is [Unknown]; my one German search found no seeker-paid AI application product, but absence of results is not absence of competitors.

**7. Acquisition and newcomer evidence.** Ton-piston is a genuine newcomer outcome, but its **founder has 51,582 X followers** [Verified: TrustMRR profile]. Its distribution was an existing audience plus TikTok/student virality [Hypothesis], which the founder does not have. Revenue also fell 4% over 30 days after the September peak. Paid acquisition cost is [Unknown].

**8. Capital and operations.** Low. Scraping job listings carries legal and terms-of-service risk (for example GDPR for EU personal data in postings, and site terms) [Unknown]. LLM costs are per user.

**9. Labour dependence.** Low. This is a product business.

**10. Unit economics.** [Hypothesis] At €10 a month, about 1,000 paying users gives about €10k MRR at 80% or more gross margin (LLM costs). Track B is possible at peak but highly seasonal, and student churn is structural.

**11. Risks.** No owned audience. Free AI substitutes. Seasonality. Scraping legality.

---

## E5. Vertical B2B newsletter and data digest funded by vendor sponsors (UK public-sector tech awards)
**1. Concept.** A free weekly email covering one buyer vertical: which UK councils, NHS trusts and fire services bought or renewed which software, for how much, and when contracts expire. It is generated automatically from the public Contracts Finder and G-Cloud data used in E1/E2. Revenue comes from vendor sponsorships, a job-board slot, and a paid alert tier. This differs from K13 (a Hebrew, subscription-only tender tool): it covers a different geography, is sponsor-funded, and is aimed at vendors.

**2. Paying customer.** UK GovTech vendors and resellers, the same people selling in E1/E2.

**3. Model and price.**
- Sponsorship slots. Vendor benchmarks: about $100–500 per slot at 1–10k subscribers, and B2B CPMs of $50–150. [Secondary: Dupple/Artha vendor guides via search; vendor-biased]
- Plus a paid tier at £20–50 a month [Hypothesis].

**4. Spending evidence.**
- Paid public-procurement intelligence already exists: TechMarketView PublicSectorViews is paywalled, and Tussell and Stotles are commercial. [Secondary: search results]
- The data itself is free: the Contracts Finder API returns award-level supplier, buyer and value fields [Verified, used above].
- beehiiv reports that 44.8% of commercial newsletters with more than 5k subscribers accept sponsors. [Secondary: Voxbooster citing beehiiv]
- **I could not measure sponsor sell-through for any newcomer newsletter** [Unknown].

**5. Competitors.** Tussell, Stotles, TechMarketView, UKAuthority and PublicTechnology. Free data dashboards are a substitute.

**6. Entry strategy.** Narrow vertical depth (for example "council housing and revenues software" only) plus a contract-renewal calendar that the incumbents' broad products do not surface for free. Moderately credible.

**7. Acquisition and newcomer evidence.**
- SEO from programmatic award pages, LinkedIn, and cross-promotion.
- Newcomer evidence comes from community media: Françaisalondres.com (FR-in-UK, founded 2018, 45k members) earns **$51,528 over 12 months / $4,804 over 30 days**. [Verified: trustmrr.com/startup/fran-aisalondres-com.md, 2026-10-13]
- That works out to about $1 per member per year after 8 years. Audience-monetised media is slow.

**8. Capital and operations.** Very low, and Israel operability is fine. The Contracts Finder API rate-limits heavy pulls (I hit failures after about 2,300 records per window). Allowed reuse is under the Open Government Licence [Hypothesis; confirm].

**9. Labour dependence.** Low once automated. Sponsor sales take founder time.

**10. Unit economics.** [Hypothesis] With 3,000 vendor subscribers, 4 sponsor slots a month at £300 is about £1.2k a month. Track A only after 12–24 months. It is mainly valuable as an acquisition engine for E1/E2.

**11. Risks.** A small audience ceiling. Incumbent data firms. Slow audience growth.

---

## E6. Language-community city media
**1. Concept.** A newsletter, site and classifieds for one language community in one city, for example Brazilians in Lisbon or Dublin, Poles in a German city, or Spanish speakers in Berlin. It is monetised by local-business ads, memberships and classifieds. This is not Israel-diaspora.

**2. Paying customer.** Local businesses targeting the community, and members.

**3. Model and price.** Françaisalondres charges £50 a year for readers and £250 a year for businesses [Verified: TrustMRR profile].

**4. Spending evidence.** Françaisalondres: $51.5k over 12 months and $189k all-time since 2018; revenue fell 2.3% over 30 days [Verified: TrustMRR, 2026-10-13]. Revenue paid outside Stripe may be uncounted.

**5. Competitors.** Facebook groups, which are free, and incumbent community sites in each city [Unknown per city].

**6. Entry strategy.** Pick a large, growing community with no strong media. Whether such gaps exist is [Unknown].

**7. Acquisition.** Facebook groups, SEO for practical "how to" queries, and events. The only evidence is one 8-year-old incumbent, so newcomer economics are [Unknown].

**8–9. Operations and labour.** Low capital, but content-heavy. AI can draft the content, but local credibility needs a human presence. Remote operation from Israel is weak.

**10. Unit economics.** At best about $3–4k a month of revenue after years. Weak Track A, no Track B.

**11. Risks.** A slow ramp and needing to be local. I list it for completeness; I rank it low.

---

## Killed or weak ideas (with evidence)
- **Employer-paid niche tech job boards.**
  - LaraJobs, a leading Laravel board, had 6 posts in the last 30 days and 26 live in total [Verified: larajobs.com plus RSS, 2026-10-13].
  - Vue Jobs' feed (1,142 items, 462 in September) is mostly aggregated listings, so post counts are not paid counts.
  - The dev-hiring market is depressed. Leaders make Track A at best, and newcomers face that market with no audience.
- **Employer-paid non-tech niche boards.** The category leader, Conservation Job Board, has to offer free basic listings, with a $65 premium [Verified]. Monetisation is thin.
- **Israeli government procurement (Mercava / exemptions).**
  - The data.gov.il exemptions dataset was last updated in 2021.
  - Of its software-related records from 2019–21, 447 of 530 were **sole-supplier exemptions (regulation 3(29))** spread across 108 suppliers and led by established vendors (SPL, Matrix, Sapiens, Elad, CyberArk). [Verified: data.gov.il CKAN datastore, 2026-10-13]
  - The newcomer path is closed unless you hold a unique product.
- **AppSumo launch deals.** Recent deals show 11–96 reviews. The model is lifetime deals, which creates a support liability with no recurring revenue. It is also a marketplace, the kind Phase 5 found has near-zero newcomer outcomes.
- **Indie "launch directories" and ad slots sold to makers** (TrustMRR "advertising platforms" category, 235 entries). Most are under $1k per 30 days and the model sells to other indie founders. Killed.
- **Generic recurring-commission affiliate/reseller programs** (HubSpot, GoHighLevel and similar). No public newcomer payout data; partner directories mostly show services firms, which means selling dev hours. Not pursued. The concrete reseller angle survives only as E2.
- **Associations' preferred-vendor programs.** Outcomes are not measurable from public data. This is folded into E3 via the career-centre model.

## Ranking
1. **E1 G-Cloud niche micro-SaaS.** Best measured channel: award-level spending, an SME share near 50% of 2026 awards, and non-UK winners. It also has the hardest measured newcomer barrier (14% of listed suppliers win anything).
2. **E2 G-Cloud reseller for non-UK SaaS.** Same channel, less product risk, more partner risk. Verified reseller wins of £110–190k licence deals.
3. **E4 Seeker-paid local-language job search plus AI.** A verified newcomer reached $10.5k per 30 days within about 10 weeks, but that was driven by the founder's audience.
4. **E3 Association career-centre operator.**
5. **E5 Public-sector award digest.** Worth more as a lead engine for E1/E2 than on its own.
6. **E6 Language-community city media.**

## Top picks for deep diligence and the decisive unverified assumption for each
- **E1.** *Does at least one narrow UK public-sector workflow exist where buyers are on renewal and would direct-award a lower-priced new entrant without references?*
  - Next desk step: pull a full 12 months of Contracts Finder G-Cloud awards (throttled) to find workflows with 10 or more awards a year under £50k and only 1–2 incumbents.
  - Also confirm G-Cloud 15 eligibility and insurance minimums for a newly formed UK Ltd, using the Find a Tender documents.
- **E2.** *Will non-UK SaaS vendors with UK public-sector demand grant a 10–25% reseller margin?*
  - Next desk step: count non-UK vendors already sold through resellers in the award data.
  - Check G-Cloud 15 Lot 2 listings for whether the vendor or the reseller is listed, and which foreign SaaS products are missing.
- **E4.** *Can a founder without an audience acquire job-seeker subscribers at a cost below roughly 3 months of revenue (about €30) in a market without a Ton-piston equivalent?*
  - Next desk step: list competitors in 3 candidate markets (DE, PL, BR) and look for verified-revenue comparables beyond Ton-piston.

## Sources (key)
- gov.uk G-Cloud spend CSV (to Dec 2018): https://assets.publishing.service.gov.uk/media/5c484b2ce5274a6e5ad27a46/g-cloud-spend-end-Dec2018.csv (accessed 2026-10-13)
- Contracts Finder OCDS API: https://www.contractsfinder.service.gov.uk/Published/Notices/OCDS/Search (accessed 2026-10-13)
- gov.uk G-Cloud 15 launch: https://www.gov.uk/government/news/g-cloud-relaunches-with-biggest-upgrade-in-its-history
- Stotles G-Cloud 14 report: https://www.stotles.com/reports/prepare-for-g-cloud-14
- Tussell 14% statistic (snippet only): https://www.computerweekly.com/news/252473749/G-Cloud-10-fails-to-generate-business-for-suppliers
- Generation Digital: https://www.gend.co/blog/g-cloud-services-uk-public-sector
- Companies House search: https://find-and-update.company-information.service.gov.uk/
- data.gov.il exemptions dataset: https://data.gov.il/dataset/exemptions
- TrustMRR: https://trustmrr.com/startup/ton-piston.md, https://trustmrr.com/startup/fran-aisalondres-com.md, https://trustmrr.com/category/recruiting, https://trustmrr.com/special-category/advertising-platforms
- LaraJobs: https://larajobs.com/ ; Conservation Job Board: https://www.conservationjobboard.com/
- Cavuno association job-board software: https://cavuno.com/blog/best-job-board-software-for-associations
- Kardow job-board examples: https://kardow.com/articles/job-board-examples

**WebSearch count: 8 / 8** (all logged as P6-E in research-notes/search-log.txt).
