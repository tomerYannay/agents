# Phase 6 — Discovery Agent D: direct-sold niche software/data to registry-enumerable buyers

Date: 2026-10-13 · WebSearch used: 8/8 (logged as P6-D) · WebFetch/curl used for primary pages: gov.uk Content/Search API + DVSA ODS file, iTunes Search API (GB), Companies House, NFDA, NY DOS, vendor sites (Cemify, PlotBox, Chronicle, TotalDrive, Gather, SwiftComply, BSI, Brycer, Syncta, FSP, Fahrschulcockpit, Reggora press release), city backflow pages.
Blocked or unavailable: Capterra, G2 and GetApp.de category pages returned 403, so review velocity could not be measured directly. The ATF FFL list returned 403 to both WebFetch and curl. The Queen Creek AZ page returned 403. The Yorktown NY VEPO page returned 404. The Washington DOH page returned 404, and syncta.com/pricing returned 404.

## Summary
The strongest lead is not a classic "SaaS for a profession". It is a business model that has already shown it works with small, enumerable buyers. The software is free to the local authority, and the licensed contractors who must file reports pay a fee per report. Backflow cross-connection programs at US and Canadian water utilities are the clearest case, with verified per-report fees of $7.50–$15.95 and secondary figures up to $35.95. Brycer's fire-inspection platform uses the same model and says it serves 2,000+ jurisdictions. Small cemeteries are the second-best segment: a 4-person, profitable, family-run vendor (Cemify) publishes $799–$1,899/year prices and says it has served "hundreds" of cemeteries. UK driving instructors are a real, countable market (42,401 ADIs). One incumbent claims 8,600 weekly instructor users, but I found no credible way in. Appraisal forms, microschools, FFL bound books, funeral homes and flight schools are killed (reasons at the end).

---

## 1. Backflow/cross-connection tracking for small water utilities, paid by testers per report (US/Canada)
**Concept.** A hosted tracking system for a utility's backflow assemblies. It sends annual test-due notices to property owners, gives certified testers a portal for test reports, flags overdue or failed assemblies, and produces the reports the state requires. The utility pays nothing or very little. Testers pay a filing fee for each report they submit.

**Paying customer + geography.** Formally, the contract is with municipal or district water utilities. The money comes from certified backflow testers (licensed contractors) and is ultimately passed on to property owners. US first, Canada second.

**Model / price.** Per-report filing fee. Verified market levels:
- Piqua, OH (BSI): $15.95 per report from 15 Feb 2024, after a no-fee onboarding window. [Verified: mycountylink.com/piqua-joins-the-bsi-online-backflow-community, article 16 Jan 2024, accessed 2026-10-13]
- Gig Harbor, WA (SwiftComply): $7.50 per passing test report. [Verified: gigharborwa.gov/856/Tester-Resources, accessed 2026-10-13]
- Other BSI cities: Queen Creek AZ $14.95, Wilton Manors FL $28, Plantation FL $35.95, Vancouver BC C$21. VEPO CrossConnex in Yorktown NY charged $15 from Feb 2024. [Secondary: search snippets of city pages; the primary pages were 403/404 or unreadable PDFs]

**Spending evidence (transaction signals).**
- SwiftComply says it is "trusted by 700+ organizations". It prices by utility subscription plus implementation, but backflow programs can choose a tester-pay model. [Verified: swiftcomply.com, accessed 2026-10-13; vendor claim]
- BSI says it has "75+ staff". Its clients range from towns with "less than 100 devices" to systems with tens of thousands. [Verified: backflow.com, accessed 2026-10-13; vendor claim]
- Small towns are still being converted from paper. Piqua (2024) and Yorktown (2024, secondary) are examples, so the market is not saturated even among smaller utilities.
- The fee is mandatory once a utility adopts a platform. Every certified tester working in that territory must pay it. That is a stronger transaction signal than a list price.
- Brycer/The Compliance Engine runs the same model for fire-system inspection reports: "Jurisdictions pay nothing", service providers pay a "per-system report fee", and it claims "over 2,000 Authorities Having Jurisdiction". [Verified: thecomplianceengine.com, accessed 2026-10-13; vendor claim]

**Buyer count.** EPA counts "over 148,000 public water systems". [Verified: epa.gov/dwreginfo/information-about-public-water-systems, updated 2026-03-16] Roughly 50,000 of these are community systems [Secondary/approximate; I could not pull the SDWIS split]. Every one is enumerable from SDWIS with operator contact details. Not all run cross-connection programs; the count of addressable programs is [Unknown].

**Competitors + what customers dislike.** Competitors are BSI Online, SwiftComply (formerly C3), VEPO CrossConnex, Tokay, XC2 and Syncta (Watts, tester-side). Contractors resent the fees, and fees of $28–$36 per report in Florida look high next to $7.50 in Gig Harbor. I could not open independent reviews: Capterra was blocked, and Syncta has only 14 reviews [Secondary].

**Entry strategy.** Target small systems (roughly 300–5,000 assemblies) that still run on paper or spreadsheets. Offer:
- no cost to the utility;
- a lower tester fee ($7–10);
- state-specific report forms;
- a 60-day no-fee onboarding window, as BSI used in Piqua;
- AI-assisted import of the utility's existing paper/Excel assembly records, which is the real switching barrier.

Start with one or two states whose rural water association runs vendor exhibits. This is a price and segment play, not a technology play. [Hypothesis]

**Acquisition mechanism.** Direct mail and email to cross-connection program managers and small-system operators, built from SDWIS. Exhibit or sponsor at state rural-water and AWWA-section events. Reference sales from neighbouring towns. Evidence that the channel works for new entrants: VEPO is a smaller vendor that won Yorktown in 2024 [Secondary]. I found no data on cost of acquisition or sales cycle [Unknown]. Municipal adoption often needs a council or board vote. A zero-cost contract may avoid formal tendering in some places [Hypothesis].

**Capital/ops/Israel.**
- Software capital is low.
- Ops include mailed notices to property owners. BSI's site has a "Mail" service. This can be automated with print-and-mail APIs at about $1 per letter [Hypothesis].
- Municipal contracts will likely require a US entity, cyber/general liability insurance (cost [Unknown]; may exceed the $2k budget), and data-security questionnaires.
- Selling from Israel is workable by email, but on-site training is expected [Hypothesis].
- Water-utility data is critical infrastructure in some states, so security reviews are a risk.

**Labour dependence.** Onboarding each utility (data import, mapping forms) is founder- or contractor-heavy. Once a utility is live, revenue recurs every year without additional founder hours, because annual tests are mandatory.

**Rough unit economics [Hypothesis].**
- A town with 1,500 assemblies at $9 per test gives about $13.5k/yr.
- Mailing and payment costs are about $3–4 per assembly, leaving about $8k/yr contribution per utility.
- 10 utilities is about $6.5k/month (Track A). 40 utilities is about $27k/month (Track B).
- Sales cycles are probably 6–18 months, so first revenue is slow.

**Risks / kill criteria.**
- Utilities may prefer incumbents' references.
- Testers may lobby against new fees; small towns often charge nothing today.
- Liability if an overdue assembly causes contamination.
- Procurement or security requirements a foreign solo vendor cannot meet.
- SwiftComply or BSI could simply match the low fee.

---

## 2. Same contractor-pay filing model for un-platformed local programs (FOG/grease interceptor, septic O&M, other mandated inspections)
**Concept.** Clone the model from #1 for other local inspection programs where licensed contractors must file periodic reports with a county or city. Candidates are grease-trap pump-outs reported by haulers, septic operation-and-maintenance reports by licensed septic service providers, and possibly other periodic certifications. Choose whichever program has no dominant platform in a given state.

**Paying customer.** Licensed haulers or septic contractors pay per filing. The authority adopts the system at no or low cost. US.

**Spending evidence.**
- The model is proven at scale by Brycer (2,000+ AHJs, contractor-pay) [Verified vendor claim].
- SwiftComply sells FOG and Pretreatment modules [Verified: swiftcomply.com].
- Per-filing fee levels for FOG and septic programs are [Unknown]. I ran out of searches before checking them.

**Competitors.** SwiftComply (FOG), Brycer (fire), and county-built portals. Others are [Unknown].

**Entry strategy.** Pick one state where a statute requires periodic septic O&M reporting and counties still take paper. Then sell county by county. [Hypothesis; needs verification of which states and what fees]

**Acquisition.** Buyers can be listed from county environmental-health department registries and state licensed septic-contractor lists. Channel evidence is [Unknown].

**Ops/Israel/labour/economics.** As in #1, but with smaller volumes per authority. [Hypothesis]

**Risks.** Many programs may be too small to sustain fees. Counties may build their own portals. This idea rests on analogy, not observed fees.

---

## 3. Low-cost records + mapping software for small cemeteries (US first; UK/AU/NZ second)
**Concept.** Self-serve plot records, a searchable public burial map, deed templates and plot sales for small religious, township and nonprofit cemeteries. Setup would use AI-assisted transcription of handwritten burial ledgers and map tracing from aerial imagery to cut the costly digitization step.

**Paying customer.** Small cemetery associations, township boards, churches and dioceses. US first.

**Model / price.** Annual subscription plus a one-time digitization fee. Cemify, the comparable small vendor, charges $799, $1,299 or $1,899 per year, plus setup quoted case by case. [Verified: cemify.com/pricing, accessed 2026-10-13]

**Spending evidence / newcomer proof.**
- Cemify describes itself as a "four-person, family-run, profitable, and fully independent company". It says it has worked with "hundreds of cemeteries" over "8 years" (so started about 2018) and has never raised prices on existing customers. [Verified page; the customer count is a vendor claim]
- Chronicle has served cemeteries "since 2016" (founder-led, Australian) [Verified: chronicle.rip/about]. It also won an ICCFA supplier award in 2022 [vendor claim].
- PlotBox claims "over 2,000 facilities" and 130+ staff [Verified: plotbox.com, vendor claim]. It raised £5m in June 2023 [Secondary: Business Post / Irish News].
- Taken together, a 4-person vendor can be profitable in this niche, and at least two vendors founded since 2014 scaled.

**Buyer count.** New York State's Division of Cemeteries oversees "approximately 1,700 not-for-profit cemeteries" and publishes lists by county. [Verified: dos.ny.gov/cemeteries, accessed 2026-10-13] Other states' registries (township cemeteries in OH and MI, for example) are [Unknown] but plausibly public. Nationwide counts are [Unknown].

**Competitors + dislikes.** Competitors are PlotBox, Chronicle, Cemify, CIMS, CemSites (site blocked) and spreadsheets. PlotBox and Chronicle show no public prices ("tailored quote"), which suggests enterprise-style pricing that small boards dislike [Hypothesis]. I could not check complaint data (Capterra 403).

**Entry strategy.** Compete on the expensive step, digitization, rather than on software. Offer a fixed-price setup (for example, ledger scans uploaded and transcribed, then a plot map traced from public aerial imagery) for small cemeteries under about 2,000 plots, plus a subscription below Cemify's (for example, $400–600/yr). This is a credible but thin edge; Cemify already sits near the bottom of the market. [Hypothesis]

**Acquisition mechanism.** Postal mail and email to the NY DOS list, then other states' lists. Exhibit at state cemetery associations and township-association vendor directories. Referrals from monument dealers. Evidence that the channel produces sales for new entrants is [Unknown]; Cemify's "hundreds" over 8 years suggests slow, steady direct acquisition.

**Capital/ops/Israel.** Low capital. Digitization is labour, but it can be delegated or done with AI plus a reviewer. Selling remotely to volunteer boards works [Hypothesis]. Site visits are not required if the cemetery supplies scans and photos.

**Labour dependence.** Each new cemetery needs setup labour. Subscriptions then recur. AI transcription of handwritten ledgers decides whether revenue can grow faster than hours. Phase 5's K11 found old-handwriting transcription weak as a stand-alone product, but here it is only an internal cost reducer.

**Rough unit economics [Hypothesis].**
- Setup around $500–1,500 with about 4–10 hours of reviewer time.
- Subscription $500/yr at about 90% margin.
- 150 cemeteries comes to about $6k/month gross, so Track A.
- Track B would need around 500+ customers or a move up-market, which is unlikely solo.

**Risks.** Small boards have tiny budgets and are slow to decide. The vendors with free or low-cost tiers are Cemify-like in price already. Mapping errors carry reputational risk. The market may be lumpy and seasonal.

---

## 4. UK driving-instructor (ADI) business app, with a 2026 rule-change angle
**Concept.** Diary, pupil progress, payments and tax tracking for self-employed UK ADIs. New hook: since 12 May 2026, only learners can book or manage car tests (instructors cannot), and changes are limited to 2. Instructors now need to coordinate pupils' test dates and readiness using their ADI reference number.

**Paying customer.** Self-employed ADIs and small multi-car schools in Great Britain.

**Model / price.** Subscription. TotalDrive is "from only £18 per month" [Verified: totaldrive.co.uk, accessed 2026-10-13]. Learnr/Passly is £14.99/month per instructor. It switched from zero commission to a 1.5% payment fee in July 2026 and ran a LAUNCH50 promotion. [Secondary: pricingsaas.com/companies/learnrdriver, tracking dated Jul–Aug 2026]

**Spending evidence.**
- ADIs on register: 42,401 in FY2024/25, up from 38,839 in FY2021/22, with 3,261 new registrations in FY2024/25. [Verified: DVSA ins0101.ods via gov.uk statistical data set "Driving instructor and motorcycle instructor register data", updated 2026-06-25]
- TotalDrive claims "over 8,600 driving instructors use the app every week" and 211,000+ pupils [Verified page; vendor claim]. At £18/month that implies roughly £150k/month revenue if all of them pay [Hypothesis, upper bound]. Total Drive Software Ltd was incorporated on 2 Sept 2020 [Verified: Companies House 12853994]. The iOS app dates from 2018 and has 251 GB ratings.
- Newer entrants on the GB App Store: Driving Instructor Lessons (ZINTELLI, released 2023, 86 ratings), MyDriveTime (2022, 69), Rated Driving (2021, 86). [Verified: iTunes Search API, country=gb, 2026-10-13] These show modest traction for newcomers. Ratings are a weak proxy for paying instructors.

**Rule change.** Instructors can no longer book or manage tests, unofficial booking-search services are banned (since 12 May 2026), and tests can only be moved to the 3 nearest centres (since 9 Jun 2026). [Verified: gov.uk/guidance/changes-to-driving-test-booking-rules-in-2026, updated 2026-06-19]

**Competitors + dislikes.** TotalDrive, Passly/Learnr, MyDriveTime, Pocket Instructor, and school-run free apps such as LIDT. Complaint data could not be checked (no review-site access).

**Entry strategy.** None credible on core diary features: TotalDrive holds about 20% of the register and newcomers are already fighting on price. A possible wedge is HMRC-recognised MTD for Income Tax quarterly submission built in for ADIs crossing the £30k threshold in April 2027. Whether TotalDrive's "income and expense tracking... for Making Tax Digital" already submits to HMRC is [Unknown]. This overlaps the Phase 2 MTD idea, though with a different channel and segment.

**Acquisition.** ADI Facebook groups, the DIA, MSA GB and ADINJC associations, and referrals from pupils' apps. The register itself is search-only (find-an-instructor), not a downloadable list [Hypothesis]. Newcomer cost of acquisition is [Unknown].

**Ops/Israel.** Fine to run remotely. HMRC MTD recognition takes a process [Unknown effort].

**Labour.** Low after build; app support only.

**Economics [Hypothesis].** 400 paying ADIs at £12 is about £4.8k/month gross, so Track A at best. Track B is unrealistic without displacing TotalDrive.

**Risks.** A low-price, crowded market with a dominant incumbent. ADI fear of switching diaries mid-season.

---

## 5. German driving-school administration under a usage-based fee (DACH)
**Concept.** Cloud administration for Fahrschulen (scheduling, contracts, payments, theory content), priced as a percentage of pupil payments instead of a publisher subscription.

**Evidence.**
- Fahrschulcockpit, a newcomer, sells "Keine Abos. Keine Wartungsverträge. Keine Verlagsbindung" ("no subscriptions, no maintenance contracts, no publisher lock-in") [Verified: fahrschulcockpit.de, accessed 2026-10-13]. A reviewer says the fee is capped at 1% of pupil payments, about €3,800/yr for 100 pupils [Secondary: ki-syndikat.de via snippet].
- Other competitors are WINDRIVE, YOU-DRIVE, Fahrstundenplaner and fahrschule.live, which have few reviews [Secondary].
- The official count of German driving schools and Fahrschulcockpit's customer count are both [Unknown].

**Entry strategy.** None credible for an Israel-based non-German speaker. Incumbents are tied to theory-content publishers, and sales depend on German trust and support. I list it because it is the clearest sign of a disliked incumbent model being attacked by a newcomer.

**Economics.** €2–4k/yr per school; Track A/B only if language and support are solved. **Risk.** Language, plus publisher content lock-in.

---

## Killed ideas (and why)
- **US appraisal forms software (UAD 3.6).** There is a real forced switch (GSE deadline 2 Nov 2026), and the buyers are enumerable via the ASC registry. But Reggora launched GSE-verified forms software free on any transaction, with no per-report fees [Verified: newswire.com press release, 7 Jul 2026]. Only about 5 vendors were verified by July 2026 [Secondary]. Price floor is zero and certification is heavy.
- **Microschool/ESA administration.** Many cheap entrants have 0 Capterra reviews (BYEDU $349/yr, MicroCampus $24/month) [Secondary]. There is no registry of microschools, and the "75,000 microschools" figure is an advocacy estimate.
- **FFL electronic bound book.** The ATF licensee list blocked automated access (403). FastBound starts at $9/month [Verified: fastbound.com/pricing] and has been in the market since 2010. Payment-processor and reputational risk for firearms.
- **US funeral-home case management.** 15,401 US funeral homes (NFDA, updated 29 Sep 2025) [Verified]. But the market is crowded: Gather claims "thousands", and SRS, Ionic, Passare, Directors Assistant, Osiris, FrontRunner and Tukios compete. No wedge found.
- **Flight-school scheduling.** Flight Schedule Pro claims 1,100 schools, universities and clubs [Verified: flightschedulepro.com/pricing]. Flight Circle covers the low end ("thousands of users"). Small N, with two entrenched tiers.
- **Tester-side backflow app.** Syncta (Watts) has only 14 Capterra reviews from $29/month [Secondary], and C3Backflow has 0. Thin spend, because the utility's chosen platform decides tester tools. Folded into #1.
- **Registry-derived "new licensee" lead feeds sold to vendors** (for example, the 3,261 new ADIs per year). There is no evidence vendors buy such feeds; general data brokers already cover it [Hypothesis only].

---

## Ranking
1. **#1 Backflow tracking with tester-pay fees.** Strongest transaction evidence: mandatory per-report fees paid by contractors, verified at two cities and seen in several more. Utilities are enumerable, and small towns were still converting in 2024. Track B is plausible. Weaknesses are the municipal sales cycle and US entity/insurance needs.
2. **#3 Small-cemetery records + mapping.** Verified buyer list (1,700 in NY alone) and a verified profitable 4-person vendor with public prices. Track A; the wedge is cost of digitization.
3. **#2 Contractor-pay filing for FOG/septic programs.** Same mechanics as #1, but fee and adoption evidence are [Unknown].
4. **#4 UK ADI app.** Real market (42k), but no credible entry.
5. **#5 German Fahrschule.** Real disruption, wrong founder fit.

## Top for deep diligence, with the decisive unverified assumption
- **#1 Backflow.** Decisive assumption: small utilities (under about 5k assemblies) will adopt a new foreign-owned solo vendor at zero cost, within a 6–12 month cycle, without a formal RFP or insurance and security demands that exceed the budget. Secondary check: count how many SDWIS systems in two target states run cross-connection programs, and what share already use BSI or SwiftComply. Public city pages naming their vendor can be counted.
- **#3 Cemeteries.** Decisive assumption: AI-assisted ledger transcription plus map tracing can cut setup to under about 6 reviewer-hours per small cemetery. Also, that direct mail to state registries converts at a rate that makes $500/yr subscriptions pay back (CAC [Unknown]).
- **#2 FOG/septic.** Decisive assumption: identify at least one state where periodic contractor reports are legally required and counties still take paper, and confirm fee levels at existing platforms.

WebSearch count: 8 of 8 (all logged in research-notes/search-log.txt as P6-D).
