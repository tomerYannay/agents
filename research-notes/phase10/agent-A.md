# Phase 10 — Agent A (Consumer/Prosumer): high-ticket done-for-you services for individuals via paid search/social

Agent label: P10-A. Date: 2026-10-13. WebSearches used: **6 of 6** (logged in `research-notes/search-log.txt`). WebFetch/curl used for primary pages and public endpoints (uncapped).

## Method notes and channel-measurement limits (read first)

- **Google Ads Transparency Center (GATC).** The page is a JavaScript app; a plain fetch returns only the shell. The page's own unauthenticated suggestion endpoint (`/anji/_/rpc/SearchService/SearchSuggestions`, no login, no CAPTCHA) returns the **verified advertiser name, country of verification and an ad-count range**. I used it for ~55 advertiser lookups [Verified: adstransparency.google.com suggestion endpoint, 2026-10-13]. A second batch of ~30 generic terms (e.g. "expat tax", "pet transport", "probate services") hit **HTTP 429**; I stopped rather than retry aggressively, so generic-term density is **[Unknown]**. Caveats: the ad count is an advertiser-level total across formats with no time window stated. It is **not** keyword-level competition. Domains returned without a named advertiser are ambiguous.
- **Meta Ad Library.** This returns a JavaScript bot-verification challenge (`__rd_verify` POST and reload). I did not bypass it. Meta advertiser density is **[Unknown]** for every idea.
- **Published CPC.** LocaliQ/WordStream "2026" search benchmarks, last updated 1 June 2026 [Verified: https://localiq.com/blog/search-advertising-benchmarks/, accessed 2026-10-13]:

  | Category | CPC | CVR | CPL |
  |---|---|---|---|
  | All-industry | $5.42 | 8.18% | $66.69 |
  | Attorneys & Legal | $9.87 | 5.55% | $131.63 |
  | Career & Employment | $5.81 | 3.05% | $67.36 |
  | Finance & Insurance | $3.39 | 2.64% | $74.44 |
  | Business Services | $5.87 | 4.85% | $93.69 |
  | Animals & Pets | $4.06 | 16.22% | $31.50 |
  | Personal Services | $7.17 | 12.34% | $54.60 |
  | Travel | $2.14 | 5.83% | $44.70 |

  No published source gives **keyword-level** CPC for probate, expat tax, NIW or pet relocation. Web Tonic (Sept 2026) states explicitly that no report breaks immigration out of the legal category [Verified: webtonic.io/blog/immigration-law-google-ads-statistics]. Keyword CPCs are therefore [Unknown]. The category numbers are proxies.
- **Copying model.** No public source quantifies how CPC changes when N more bidders enter. In every "+3 followers" case below I use a stated [Hypothesis]: CPC +50% and close rate −20%, because buyers compare more quotes. Agent E's channel data should replace this if it has anything better.
- **Newcomer data.** TrustMRR (local P8-D sample, no re-crawl) is software-skewed and holds almost no high-ticket human-delivered services. Empire Flippers' public listings API (1,175 for-sale and sold listings pulled) yields only n=1 comparables.

---

## A1. Reverse recruiting ("we run your job search") for US mid/senior professionals — RANK 1

1. **Concept.** A productised done-for-you job search: resume rebuild, then offshore applier contractors submitting 50–100 tailored applications a week, recruiter outreach and a weekly report. Sold per month with a minimum term.
2. **Customer and geography.** US white-collar job seekers in the $100k+ salary band. Explicitly **excludes New York** and, pending verification, **California**, the **UK** and the **EU** (see item 8).
3. **Model and price.** About $1,200–1,500 a month, 3-month minimum (≈$3,600–4,500 one-off equivalent). An optional success fee follows the incumbents' model.
4. **Spending evidence.**
   - Reverse Recruiting Agency charges $1,500 a month plus 10% of first-year salary. It reports 45 clients helped plus 25 active, an average of 863 applications per client and 12.7 weeks to an offer [Verified: fortune.com/2026/03/25/reverse-recruiting-agency-job-search-ai-applications-cost, accessed 2026-10-13; figures are company claims]. Implied run-rate ≈ $37.5k a month from active clients alone [Hypothesis: 25 × $1,500].
   - Seven priced providers, from F1Jobs at $349/mo (6-month minimum, $2,094–2,994 total) to iCareerSolutions at $1,595–5,995/mo, Career Agents at $999 / $5,950 / $14,999, and Find My Profession at $3,000/mo or $1,500 + 8% [Verified: f1jobs.io/resources/blog/reverse-recruiting-cost-2026-what-companies-actually-charge, article dated 2026-07-18; vendor-authored]. No provider discloses client counts beyond RRA.
5. **Competitors and dislikes.**
   - GATC: JOBHIRE AI LIMITED (Cyprus) 53 ads; Find My Profession Inc 4 ads; Lets Eat Grandma 6 [Verified: GATC endpoint, 2026-10-13]. Advertiser density is moderate, not saturated.
   - Dislikes: no job guarantee, spray-and-pray quality, refunds. These are [Hypothesis]; reviews were not read.
6. **Entry strategy.** A segment with urgency and high willingness to pay: **H-1B holders in the 60-day post-layoff grace period**, and laid-off US tech/product staff. Price at about $1,200/mo, under the $1,500 incumbents. Credible but thin: F1Jobs already targets visa candidates at the low end. There is no durable differentiation beyond execution and reviews.
7. **Acquisition.**
   - Google Search: "reverse recruiter", "job search service", "hire someone to apply to jobs". Category CPC $5.81, CVR 3.05%, CPL $67.36 [Verified: LocaliQ].
   - Meta: layoff- and job-seeker interest audiences, density [Unknown: Ad Library blocked].
   - Newcomer outcomes: in the TrustMRR job/resume subset (n=183, mostly software), median 30-day revenue is $0, 14 have ≥$1k and 5 (2.7%) have ≥$3k [Verified: local P8-D parsed.json]. These are low-ticket tools, not services. No newcomer data exists for reverse-recruiting services [Unknown].
8. **Ops and legal.**
   - Delivery: VA appliers (≈10–15 h/week per client), one resume writer, one account manager, plus software the founder builds for tracking and tailoring. Israel-operable; no capital.
   - **Legal:** New York GBL §171(2)(a) defines an employment agency as anyone who "for a fee, procures or attempts to procure employment … for persons seeking employment", and §171(2)(c) extends this to paid vocational counsellors who represent they can procure employment [Verified: nysenate.gov/legislation/laws/GBS/171, 2026-10-13]. NY clients therefore need a licence; exclude them.
   - California Civil Code §1812.500+ (employment agency / job listing service bonding) could not be fetched (403) [Unknown].
   - The UK Employment Agencies Act 1973 bars charging work-seekers fees for finding work [Unverified this session]. Exclude the UK.
   - Automated mass applying breaches LinkedIn terms, so applications must be human-submitted.
9. **Labour.** Delegable. VA cost scales linearly per client; founder hours go to QA, systems and ads.
10. **Unit economics** [Hypothesis unless noted].

    | Item | Base case | +3 followers |
    |---|---|---|
    | CPL | $67 [Verified category] | ~$100 |
    | Close rate | 10% | 8% |
    | CAC | ≈ $670 | ≈ $1,260 |
    | Revenue per client | $3,600 (3 × $1,200) | |
    | Delivery | VA ~$500/mo × 3 = $1,500, resume $150, AM/tools $300 | |
    | Contribution per client | ≈ $980 | ≈ $390 |

    - Track A ($3k/mo) needs about 3–4 new clients a month at base economics. Track B needs 30+ concurrent clients and a hired operations lead.
    - Copying compresses margin hard. Survival depends on refund rate and term length, not CPC.
11. **Risks / kill.** Refund and chargeback rate on "no job" outcomes. Regulatory creep (more states treating this as an employment agency; FTC scrutiny of outcome claims). Zero barriers: copy window ≪ 6 months. Price ladder pressure from $349/mo players.

**Cheapest test (describe only).** $1,200 of Google Search over 3 weeks on the 3 keyword clusters, US excluding NY/CA. Landing page offers a $150 paid "search audit", credited to month 1. **Kill if** fewer than 6 paid audits, CPL above $120, or fewer than 2 audits convert to a paid month within 14 days.

---

## A2. Complex-case US expat tax catch-up and exit desk (non-Israel "accidental Americans") — RANK 2

1. **Concept.** A fixed-price Streamlined Foreign Offshore package for **complex** cases, i.e. foreign mutual funds (PFIC/8621), foreign corporations (5471) and foreign trusts/pensions. Plus a **renunciation-readiness bundle** (5-year compliance + Form 8854). Prepared by contracted US Enrolled Agents.
2. **Customer and geography.** US citizens by birth or descent living in Canada, the UK, the EU and Australia. **Israel deliberately excluded** under the brief's diaspora caution; the ledger's "olim foreign-asset disclosure" is a different, Israel-domestic item.
3. **Model and price.** $1,900–3,500 one-off, priced by form count. Simple cases are referred out or sent to cheaper players.
4. **Spending evidence.**
   - Greenback: Streamlined package $1,750 (3 returns + 6 FBARs); 8621 $185–275; 5471 $280–665; consultations $250–1,000/hr. Claims "15,000+ expats" and "71,000+ returns" [Verified: greenbacktaxservices.com/pricing, 2026-10-13].
   - MyExpatTaxes: Streamlining $875, Exit Bundle $1,175, Trustpilot 4,000+ reviews [Verified: myexpattaxes.com/pricing, 2026-10-13].
   - IRS IR-2016-137: 48,000 taxpayers used Streamlined procedures, filing 96,000+ returns [Verified: irs.gov newsroom, 2016-10-21]. No current count exists.
   - **Demand catalyst:** the Certificate of Loss of Nationality fee was cut from $2,350 to $450, effective 13 April 2026 (Federal Register 2026-04931). The tax side is unchanged and still requires 5-year compliance and Form 8854 [Verified: taxesforexpats.com/articles/expatriation/us-citizenship-renunciation-fee-cut.html, updated 2026-08-28]. Renunciation volume after the cut is [Unknown].
5. **Competitors.**
   - GATC: Taxes for Expats 100–200 ads; Expat Tax Professionals LLC 55; Bright!Tax 32. Greenback, MyExpatTaxes, Expat Tax Online and Online Taxman appear as domains only [Verified: GATC, 2026-10-13].
   - Customer dislikes are [Unknown]; reviews were not read.
   - The key structural fact is **price compression**. A simple Streamlined package sells for $875 at a large, review-rich player, so the $1,500 floor holds only for complex, form-heavy cases.
6. **Entry strategy.** Complexity-priced, non-US-resident focus. Lead with keyword clusters such as "PFIC Canada mutual funds US citizen" and "accidental American renounce taxes", plus a software intake that auto-scopes forms and prices instantly (founder fit). This is credible but narrow, and incumbents already sell every form à la carte.
7. **Acquisition.**
   - Google Search, geo-targeted to CA/UK/AU/EU.
   - CPC: Finance & Insurance $3.39 / CPL $74.44; Business Services $5.87 / CPL $93.69 [Verified: LocaliQ]. Keyword-level CPC [Unknown].
   - Newcomer outcomes for new expat-tax firms [Unknown]. In TrustMRR "tax" (n=20), median 30-day revenue is $4.
8. **Ops and legal.**
   - Preparers need a PTIN. Representation before the IRS requires an EA, CPA or attorney (Circular 230). Disclosure and use of return information need IRC §7216 consents.
   - Whether non-US firms can e-file Streamlined submissions is [Unknown].
   - Contract EAs are plentiful. Israel-operable. No capital. Professional liability insurance is needed; cost [Unknown].
9. **Labour.** Delegable to EAs. The founder owns intake software, QA and ads. Highly seasonal (April, June and October peaks).
10. **Unit economics** [Hypothesis].

    | Item | Base case | +3 followers |
    |---|---|---|
    | CPC (assumed) | $6 | $9 |
    | Lead CVR | 5% | 5% |
    | CPL | $120 | $180 |
    | Close rate | 20% | 16% |
    | CAC | $600 | $1,125 |
    | Price | $2,200 | |
    | EA fee + software/insurance | ~$800 + $150 | |
    | Contribution per case | ≈ $650 | ≈ $125 |

    Track A needs about 5 cases a month at base. Track B needs a firm-level operation; incumbents show it exists (Greenback 71k returns).
11. **Risks / kill.** Price compression from $875 software-plus-review players. Incumbents bid on the same terms. Liability for mistakes on penalty-relief certifications. Seasonality.

**Cheapest test.** $1,000 over 4 weeks (best run in a Feb–Apr or Sept–Oct peak) on complex-case and renunciation clusters, CA/UK/AU geo. Use a $150 paid scoping call credited to the package. **Kill if** CPL exceeds $150, fewer than 4 paid scoping calls, or the median scoped quote is below $1,500.

---

## A3. International pet relocation coordination (non-US origin lanes) via IPATA partners — RANK 3

1. **Concept.** A coordinator brand that sells door-to-door international pet moves (documents, vet timeline, airline booking, customs) and subcontracts physical custody to registered partner agents at origin and destination.
2. **Customer and geography.** Relocating families and expats. Start with lanes such as UK/EU → US/Canada and US → EU.
3. **Model and price.** One-off, $4,000–10,000 per move.
4. **Spending evidence.**
   - Starwood's May 2026 report: single pet $4–6k+, multi-pet $6–9k+, complex/AU-NZ $10k+ [Secondary: search summary of Starwood report via PR distribution; vendor claim, page not opened].
   - Starwood's own cost page lists Economy, Business and Premium tiers with airfare, customs, USDA endorsement and boarding bundled, but shows no prices without the estimator [Verified: starwoodpet.com/international-pet-relocation-costs, 2026-10-13].
   - No volume claims found.
5. **Competitors.**
   - GATC: Airpet Animal Transport (AU) 200–300 ads; Air Animal (US) 25; PET Relocation Thailand 26; Puppy Travel (PE) 21; Furry Pets (AE) 20; Fetch Pets (AE) 19; Panama Pet Relocation 18; Elite Pet Relocation (CY) 10; Pawsome Friends (GB) 9; Happy Tails Travel (US) 8 [Verified: GATC, 2026-10-13].
   - Pattern: many small, single-country advertisers with low ad counts. That fragmentation is consistent with a newcomer being able to buy into a lane.
   - Happy Tails Travel has been in business since 1995, is an IPATA member since 1996, and is a USDA Class H intermediate handler [Verified: happytailstravel.com].
6. **Entry strategy.** Lane-specific landing pages, instant itemised quote software (founder fit) against "call for quote" incumbents, plus a status-tracking portal. Credible as execution; there is no moat.
7. **Acquisition.**
   - Google Search: "pet relocation [country]", "ship dog to [country]".
   - Category Animals & Pets: CPC $4.06, CPL $31.50 [Verified: LocaliQ]. This is a vet-heavy proxy, so real quote-request CPL is likely higher [Hypothesis].
   - Cheap clicks relative to a $5k ticket are this idea's main structural advantage.
   - Newcomer outcomes [Unknown].
8. **Ops and legal.**
   - USDA registration (9 CFR 2.25) is needed for anyone taking custody in US commerce. It is free with a 3-year validity [Secondary: search summary; APHIS not opened].
   - **IPATA membership** costs $1,000 to apply plus $1,275 a year, needs **2 reference letters from IPATA members** and an IATA LAR-certified staff member, and requires US members to be USDA-registered/licensed [Verified: ipata.org/active-members, 2026-10-13]. A newcomer can subcontract to members without joining.
   - Big operational risks: animal injury or death, airline cargo embargoes (summer heat, breed bans), and the need for working capital to prepay airfare.
   - Israel operability: coordination is remote, but time-zone coverage is needed.
9. **Labour.** Coordination time per move is significant (weeks of document chasing) [Hypothesis ~8–15 h/move]. It is delegable to trained coordinators. More ops-intensive than A1 or A2.
10. **Unit economics** [Hypothesis].

    | Item | Base case | +3 followers |
    |---|---|---|
    | CPC | ~$4 | ~$6 |
    | Quote CVR | 6% | 6% |
    | CPL | ≈ $70 | ≈ $100 |
    | Close rate | 15% | 12% |
    | CAC | ≈ $470 | ≈ $840 |
    | Price | $5,500 | |
    | Pass-through (cargo airfare, vet, crate, partner fees) | ~$4,000 | |
    | Gross margin | ~$1,500 | |
    | Coordinator labour | ~$300 | |
    | Contribution per move | ≈ $730 | ≈ $360 |

    Low CPC relative to ticket helps, but the actual gross-margin percentage is the decisive [Unknown].
11. **Risks / kill.** A pet-death incident is reputationally fatal for a review-dependent newcomer. Cash-flow exposure on prepaid airfare. Strong seasonality. Partner reliability.

**Cheapest test.** Agree desk partner pricing with 2 IPATA agents on one lane (desk-only, from published quote forms). Spend $800 over 4 weeks on lane keywords, with a quote form and a $250 refundable booking deposit. **Kill if** fewer than 15 quote requests, no deposits, or partner cost leaves under $800 gross margin per move.

---

## A4. Self-petition employment green cards (EB-2 NIW / EB-1A / O-1) through an attorney-partnered or Arizona-ABS structure — RANK 4

1. **Concept.** A productised petition factory for researchers and engineers: evidence-gathering software, recommendation-letter drafting workflow, contract paralegals. A licensed attorney signs and advises.
2. **Customer and geography.** Global STEM professionals.
3. **Model and price.** $5,000–12,000 flat [Unknown: Manifest publishes no prices; Boundless shows unlabelled figures].
4. **Spending evidence.**
   - Manifest Law: "technology-enabled immigration law firm", 4,000 clients served; structure includes **Manifest Legal Services LLC, an Arizona ABS** [Verified: manifestlaw.com, 2026-10-13].
   - Boundless: 100k+ helped; advertising law firm is **Boundless Legal LLC, licensed by the Arizona Supreme Court** [Verified: boundless.com, 2026-10-13].
   - The Arizona Supreme Court issued 10+ ABS approval orders in 2026, including **Crimson Talent Immigration LLC (Feb 2026)** and Newland Chase Legal (Jun 2026). Each requires a compliance lawyer and semi-annual audits [Secondary: search summary of azcourts.gov admin orders; azcourts ABS page returned 403].
5. **Competitors.** GATC: Boundless Immigration Inc 100–200 ads; SimpleCitizen 100–200; Manifest (domain) [Verified: GATC]. Legal-category CPC is the highest of all: $9.87 / CPL $131.63 [Verified: LocaliQ].
6. **Entry strategy.** A sub-niche (e.g. EB-2 NIW for one profession) with software-driven evidence assembly. Per Phase 9, an ABS licence is a moat a follower can also obtain (10+ approvals in H1 2026 alone), so defensibility is ≤2.
7. **Acquisition.** Search and Meta. Keyword CPC [Unknown]. Newcomer outcomes [Unknown].
8. **Legal.** Immigration advice and petition preparation are the practice of law. Non-lawyers cannot advise or share fees with lawyers (ABA Model Rule 5.4) except via Arizona ABS (or the Utah sandbox). The founder cannot run this without either a US immigration attorney as legal owner/partner or an ABS licence. Time and cost exceed the $2k budget [Hypothesis]. This is the remit's "immigration may need a licence" case: **yes, it does**.
9. **Labour.** Delegable to paralegals plus attorney review. Attorney hours are the bottleneck.
10. **Unit economics** [Hypothesis]. At $8,000 price, $250 CPL and 15% close, CAC ≈ $1,700. Attorney plus paralegal ≈ $3,000. Contribution ≈ $3,300. With followers, CAC ≈ $3,000 and contribution ≈ $2,000. The economics are robust; the binding constraint is legal structure and capital.
11. **Risks.** Licensing and structure. Policy volatility (USCIS adjudication trends, fees). Malpractice. Over budget.

**Cheapest test.** Not runnable at $2k without an attorney partner. The desk step is to price an ABS application and compliance-lawyer retainer. **Kill if** structure cost exceeds $15k or no attorney partner accepts a per-case fee under 40% of price.

---

## A5. UK full estate administration front-end with an SRA-regulated partner firm (Farewill model) — RANK 5

1. **Concept.** A consumer brand and software intake for full estate administration, with reserved legal work delivered by a partner SRA-regulated firm.
2. **Customer and geography.** Executors in England & Wales.
3. **Price.**
   - Full administration from £2,730, with examples of £4,882–11,182 (Octopus Legacy, delivered by SRA-authorised Octopus Legal Services, SRA ID 8007668) [Verified: octopuslegacy.com/probate, 2026-10-13].
   - Farewill: grant-only from £895; full service "from £1,500" in the FAQ vs "from £2,750" in the listing. "Farewill Ltd is not a law firm"; services are delivered by an unnamed third-party SRA-regulated firm [Verified: farewill.com/probate, 2026-10-13].
   - Grant-only (£585–895) is **below** the remit floor; only full administration qualifies.
4. **Competition.** GATC: **Octopus Legacy Ltd 1,000–2,000 ads**; Farewill 45; UK Probate Ltd 15; Probate Tech 13; Kings Court Trust 13 + 10 [Verified: GATC]. A heavily funded incumbent is outspending everyone.
5. **Entry strategy.** None credible for an Israel-based newcomer. Bereavement buyers favour trusted local brands, and Octopus is both cheaper on grant-only and outspends on ads.
6. **Legal.** Grant applications are reserved legal activities, so delivery must sit with an authorised firm, and the front-end's margin is a negotiated marketing/referral fee [Unknown].
7. **Unit economics.** Keyword CPC [Unknown]; legal-category CPL is $131.63. Front-end margin [Unknown]. **Status: weak; listed for completeness.**

---

## A6. Spain/Portugal relocation-visa packages (DNV / non-lucrative / D7) via local lawyers — RANK 6

- **Evidence.** Lexidy (Barcelona/Madrid/Málaga) claims 7k–10k+ clients and 45+ lawyers, with fixed-price proposals but no published prices [Verified: lexidy.com, 2026-10-13]. GATC: LEXIDY LAW BOUTIQUE S.L.P. 100–200 ads; Global Citizen Solutions (PT) 63 [Verified: GATC]. In TrustMRR, "Get Brazil Visa" (founded Dec 2025) had $3,167 30-day revenue via SEO, a newcomer n=1 in an adjacent visa niche [Verified: local P8-D data].
- **Legal.** In Portugal, legal acts by non-lawyers are restricted ("procuradoria ilícita", Law 49/2004) [Unverified this session], so the model must be a lawyer partnership with a referral or marketing fee.
- **Entry.** None credible. A dense, lawyer-led field, prices undisclosed, and policy volatility.
- **Status:** weak.

---

## Killed ideas

| Idea | Why killed |
|---|---|
| Credential evaluation (WES-type) | Ticket far below $1,500; evaluator membership gatekept. |
| Medical-bill advocacy / insurance appeals | Ticket is typically contingency on modest savings, so below the floor [Hypothesis]; Claimable (31 GATC ads) is already productised at low price. |
| SSDI / VA claims representation | VA forbids charging by unaccredited agents. SSDI fees are capped and paid via SSA to qualified reps. A US presence is effectively required. |
| Credit repair / student-loan document prep | Advance-fee bans (CROA/TSR) defeat paid-ads economics. |
| Online uncontested-divorce documents | Below ticket. The EF #83697 comparable ($38.1k rev/mo, $14.2k net, 39% margin, since 2021) has been listed since April 2025 and is still unsold, a weak signal. |
| Italian/German citizenship by descent | Repackage of ledger J3. |
| Executive resume writing alone | Folded into A1; standalone tickets are usually below $1,500 [Unknown, not verified]. |
| Renunciation-only service | Folded into A2. The fee cut is a timing edge that incumbents are already publishing on (Greenback, MyExpatTaxes, Taxes for Expats all have 2026 articles). |

Other Empire Flippers notes:
- EF #40293 (2014–15) was an AdWords-only US business-licence filing service. It made $14.2k/mo, and profit fell when the seller cut ad spend. It is old n=1 evidence that paid-search-only document services can run, and that they depend on continuous spend.
- EF #62527 ($78k/mo, 60 Philippine contractors, 25% margin) shows contractor-delivered "access to specialists" services exist at scale, but its margin is thin.

---

## Ranking, deep-diligence picks and decisive unknowns

1. **A1 Reverse recruiting (US ex-NY/CA).** Strongest transaction signals among new-ish entrants (RRA: 70 clients at $1,500/mo, Fortune 2026; 7 priced providers). Moderate GATC density, fully delegable, no capital. **Decisive unverified assumption:** a refund/chargeback rate under ~15% and an average paid term of ≥3 months. Without both, contribution is ≤$400 per client under copying.
2. **A2 Complex-case expat catch-up and exit desk.** Strongest spending evidence (Greenback 71k returns; MyExpatTaxes 4k+ reviews; IRS 48k Streamlined filers by 2016) plus a 2026 catalyst. **Decisive assumption:** enough paid demand at ≥$1,500 for *complex* cases when MyExpatTaxes sells simple Streamlined at $875, i.e. median scoped quote ≥$1,500 at CPL ≤$150.
3. **A3 Pet relocation coordination.** The best CPC-to-ticket ratio in the set (category CPL $31.50 vs a $4–10k ticket) and a fragmented advertiser field. **Decisive assumption:** gross margin after pass-through of ≥$1,200 per move via subcontracted IPATA partners. This is [Unknown], and ops/liability risk is the highest of the three.

A4 has robust economics but is licence- and capital-blocked for this founder (immigration practice requires an attorney or Arizona ABS). A5 and A6 have no credible entry.

Cross-cutting finding: in all three top ideas the "+3 followers" case roughly halves to quarters contribution per sale under my [Hypothesis] CPC/close-rate shock. None has a moat. Survival rests on operational quality (refunds, reviews, gross margin), not on channel access.

**WebSearch count: 6 / 6.**
