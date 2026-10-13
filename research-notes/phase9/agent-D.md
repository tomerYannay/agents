# Phase 9 — Discovery Agent D (Software moats beyond "first"), label P9-D

Date: 2026-10-13. WebSearch used: **6 / 6** (all logged in research-notes/search-log.txt under P9-D). Everything else came from WebFetch or curl of public pages, public CSV files, PDFs and Wayback snapshots. Raw files are in the scratchpad at p6plus/P9-D/data.

## Bottom line

I measured holder counts on 14 public lists of certified, approved or licensed software and course providers. The pattern is consistent:

- **Holder counts stay small** only when approval is a paid review of the content itself, repeated per jurisdiction and renewed periodically. Examples: NASBLA boating courses, CRA NETFILE, and Streamlined Sales Tax CSPs.
- **Holder counts explode** when approval is a technical test, a registration or a cheap licence:
  - **IRS Form 2290 ATS:** 64 providers in TY2023, 149 in TY2026. 36 of the 2026 providers are state-named doorway brands.
  - **Texas driving-safety course licences:** 471. Some are named "$25 – EASY – NO FINAL TEST".
  - **UK MTD VAT recognised software:** 469.
  - **French plateformes agréées:** 155 registered and 12 more pending.
  - **Croatian e-invoice intermediaries:** about 37.
  - **Texas trade CE providers:** 190 for electricians alone.

  In these categories certification is a ticket to entry, not a moat.

Only one position passed all three tests:
- it can be obtained within the founder's reach (just over budget);
- the holder count is small and stable;
- a recent newcomer measurably got in.

That position is **state- and NASBLA-approved online boater-safety courses** (D1). Everything else is either a measured kill or a moat that is real but out of reach.

### Holder-count table (the core measurement)

| List (authority) | Holders now | Over time | What approval takes | Read |
|---|---|---|---|---|
| Texas TPWD online boater-ed courses | 6 brands (5 firms; Boat-Ed and iLearnToBoat share Kalkomey's support line) | 2014: 3 · 2018: 3 · 2020: 5 · 2022: 5 · 2025–26: 6 (Wayback) | NASBLA review ($4,500–5,500 for non-members) plus state review; full re-review every 3 years | **Moat holds** |
| NY State Parks online boater courses | 5 (Boat-Ed, Boat-Ed+, BOATERexam, BOATsmart, Recademics) | n/a | Same | Moat holds |
| California Boater Card approved courses | 16 (classroom and online) | n/a | NASBLA plus DBW review | Moat holds |
| CRA NETFILE (Canada T1) | 17 products | About 15 brands in 2018, about 17 in 2020, 2023 and 2026 (Wayback) | Annual CRA certification | Stable oligopoly; free leaders |
| eFileTexas certified EFSPs | 25 | 2016: 13 · 2019: 18 · 2022: 20 · 2024: 23 · 2026: 25 | Court/OCA EFSP certification | Moderate moat; about +1.2 a year |
| Streamlined Sales Tax CSPs | 6 (5 offering free service) | n/a | SSTGB certification, contract and liability | Strong moat, out of reach |
| Croatia information intermediaries (e-invoice) | about 37 (updated 7 Oct 2026) | Mandate began 2026 | Conformity certificate | Crowded within year 1 |
| France PA (e-invoicing) | 155 registered pending audit, plus 12 pending interop tests | Started 2024 | Dossier plus interop tests | Crowded; includes foreign firms (A-Cube IT, Ademico BE) |
| UK MTD VAT software | 469 results | n/a | HMRC recognition | No moat |
| IRS Form 2290 MeF ATS providers | 149 | 64 (TY2023) → 149 (TY2026); 0 → 36 state-named brands | IRS ATS test | Doorway-brand spam |
| Texas driving-safety providers (TDLR) | 471 current licences | n/a | TDLR licence | Spam names; no moat |
| TDLR CE providers | Electricians 190, A/C 79, tow 43, cosmetology 245 | Shared licence numbering reaches #2564 | TDLR approval | Crowded; national players (Jade Learning) |
| Israel ITA software / allocation lists; ISA open-finance licensees | **Blocked** (gov.il Cloudflare 403) / not found | n/a | n/a | Unmeasured; hand to Agent F |
| Portugal AT certified programs | **Not measured** (list page needs JavaScript) | n/a | n/a | n/a |

Sources:
- TPWD: tpwd.texas.gov/learning/boater_education/internet_courses.phtml and Wayback copies (2014-07-29, 2018-09-04, 2020-10-20, 2022-07-03, 2025-03-16).
- New York: parks.ny.gov/activities/boating/boating-education.
- California: DBW Nov-2025 commission PDF.
- CRA: canada.ca NETFILE certified-software page and Wayback (2018-02-22, 2020-04-13, 2023-04-13).
- eFileTexas: efiletexas.gov/service-providers.htm and Wayback (2016–2024).
- Streamlined Sales Tax: streamlinedsalestax.org CSP list.
- Croatia: porezna-uprava.gov.hr/hr/popis-informacijskih-posrednika/8019.
- France: impots.gouv.fr PA xlsx lists.
- UK: tax.service.gov.uk/making-tax-digital-software.
- IRS: irs.gov TY2023 and TY2026 2290 MeF provider pages.
- TDLR: dbproduction2 CSVs.

All accessed 2026-10-13.

---

## D1. Approval-gated online boater-safety course provider (NASBLA + per-state), entering on language, price and partner bundles — TOP

1. **Concept.** An interactive online course that legally satisfies a state's boater-education requirement. It issues the completion certificate the state accepts.

   The moat is the approval stack:
   - NASBLA conformity assessment against ANSI/NASBLA 100/103;
   - a separate review by each state agency, with state-specific content;
   - a full NASBLA re-review every 3 years.

   The certificate is sold to the boater; the software is the business.

2. **Paying customer and geography.**
   - Recreational boaters in US states with mandatory education, typically younger operators or, increasingly, all operators.
   - New York's Brianna's Law and California's all-ages Boater Card rule both took full effect on 1 Jan 2025.
   - Later expansion: Canadian PCOC (unmeasured).

3. **Model and price.**
   - One-off fee per student, often plus a state fee.
   - Texas provider fees [Verified: TPWD page, 2026-10-13]:
     - BoatUS $1;
     - Recademics $29.99 ($19.99 military);
     - BOATsmart $39.95;
     - BOATERexam $49.95;
     - Boat-Ed $54.95;
     - iLearnToBoat $74.95;
     - each plus a $10 state fee.
   - In 2018 Texas capped provider fees at $20 [Verified: Wayback 2018-09-04]. Prices have since risen to $30–75, so pricing power grew as the list stayed small.
   - The Boat-Ed+ bundle costs $79.95 including a year of the Wavve app [Anecdote: Boat-Ed blog, 2 Jul 2026].

4. **Spending evidence.**
   - **Kalkomey** (Boat-Ed, hunter-ed, ATV and snowmobile):
     - "trains and certifies nearly one million" people a year;
     - 360+ approved courses and 110+ agencies;
     - acquired by Macquarie Capital in June 2024 after Cove Hill (2020) [Verified: kalkomey.com release 24 Jun 2024; dallasinnovates.com 25 Jun 2024].
     - The serial PE ownership is a transaction signal.
   - **California** [Verified: DBW Nov-2025 PDF]:
     - 144,608 Boater Cards issued Aug 2024–Aug 2025, up 198% (the deadline spike);
     - 432,256 cumulative;
     - 16 approved courses.
     - The free DBW home-study route took about 10,700 graded exams, so most of the remaining ~134k CA completions came through other approved courses, most of them paid [Hypothesis on split].
   - **Washington:** 500,000 cumulative cards [Secondary: search snippet only].
   - Total paid market size: [Unknown].

5. **Competitors and dislikes.**
   - Kalkomey (Boat-Ed, iLearnToBoat; in every state and province);
   - BOATERexam;
   - BOATsmart (Canada-origin);
   - BoatUS Foundation (nonprofit, $1 in Texas, $8.99 Florida renter course);
   - state free home-study routes.

   Customer dislikes: not measured (no review dataset fetched). Incumbent prices of $55–75 for a 3–6 hour course suggest room on price.

6. **Entry strategy.** Concrete and evidenced in part:
   - **(a) Language.** In Texas, Spanish is offered only by Boat-Ed [Verified: TPWD page]. NASBLA terms explicitly cover certified translations [Verified: NASBLA Terms and Conditions PDF]. Spanish, and possibly Vietnamese or Chinese for California, is a defined gap.
   - **(b) Price.** Sit at $25–35, between the nonprofit $1 and Kalkomey's $55–75. This is what the newcomer Recademics did.
   - **(c) Revenue per account.** Completers are brand-new boat operators. Bundle partners (towing memberships, boat insurance, navigation apps) as Boat-Ed+ does with Wavve. This raises revenue per account and creates the "proprietary data accrued through operation" asset. Consent and privacy terms apply.

7. **Acquisition mechanism and evidence.**
   - **State agency lists.** Each state agency page lists every approved provider with price and link (verified for TX and NY). This is a high-intent, non-auction channel that only approved holders can use. That is the distribution half of the moat.
   - **Paid search.** DBW reports that Google search advertising "has proven to provide the best return on investment" for reaching boaters [Verified: DBW PDF]. That is the state's own outreach, not a provider's CAC.
   - **Newcomer outcome:**
     - Recademics LLC (Southlake TX, two co-founders) launched boating courses around 2023 [Anecdote: competitor's blog].
     - It is absent from the Texas list in July 2022 and present by March 2025 [Verified: Wayback], and is on the NY list [Verified].
     - It claims about 20 state approvals within about 3 years and press-releases each new state (NY, OR, KY, KS, NJ…) [Secondary: search P9-D #4].
     - Boat-Ed published a "Boat-Ed vs Recademics" page in July 2026, which is a sign the incumbent feels it.
     - Recademics' revenue, student counts and review counts: [Unknown]. Its free refresher course shows 136 students [Verified: recademics.com].
   - Acquisition cost per student: [Unknown]. This is the decisive gap.
   - P2P rental platforms are **not** a proven channel: Boatsetter only points renters to NASBLA and BoatUS, with no partner [Verified: boatsetter.com]. Getmyboat partners Mariners Learning only for captain courses [Secondary].

8. **Capital, operations, Israel operability, restrictions.**
   - NASBLA fees [Verified: NASBLA Fee_Structure.pdf]:
     - non-member: $4,500 timed internet course, or $5,500 interactive, with one state included;
     - $550 per additional state;
     - $300 extra for a custom question bank;
     - associate-member rates $3,150 / $3,850 / $385.
     - So the first state costs about $4.5–5.5k and ten states about $9.5–10.5k. **This exceeds the $2k budget; flagged.**
   - Ongoing obligations: full re-review every 3 years; annual student and certificate statistics reported to each state; certificates issued within 14 business days.
   - Some states add requirements:
     - Connecticut requires CT-specific materials and annual provider recertification [Verified: portal.ct.gov];
     - Minnesota uses "delegated provider" status.
   - **Foreign providers:** NASBLA defines "State" to include non-US jurisdictions, and BOATsmart is Canada-origin. A US LLC is probably advisable. Whether any state requires an in-state entity: [Unknown].
   - Delivery is pure software plus support.

9. **Labour dependence.**
   - Upfront: content and the approval dossier (3–9 months, founder-heavy).
   - After that: support, state reporting and renewals, which can be delegated.
   - Revenue scales per state without matching founder hours.
   - Strongly seasonal (spring and summer).

10. **Rough unit economics [Hypothesis].**
    - Assume $30 net per completion, about 5% payment and hosting costs, and CAC unknown.
    - At 3,000 paid completions a year in years 2–3 across 5–8 states: about $90k revenue, before ads and renewals.
    - **Track A** ($2–5k a month owner profit) is plausible if CAC is at most about $12.
    - **Track B** needs expansion: more states plus ATV, snowmobile and bowhunter courses (Recademics' path), plus partner bundles.
    - Revenue per account is low (under $50 one-off), which carries Phase 8's 0.37× trait. The protection is the state-list channel, which Phase 8 datasets did not contain.

11. **Main risks and kill conditions.**
    - **Demand drop after phase-ins:** the CA and NY spikes were deadline-driven, so steady state is only the new-boater flow.
    - **Free anchors:** BoatUS at $1, state home study.
    - **Kalkomey's agency relationships:** some state pages lead with Boat-Ed.
    - **Approval slippage:** NASBLA review time [Unknown].
    - **SEO dominance** by incumbents on "boating license [state]".
    - **Budget:** above $2k before any marketing.
    - **Kill test:** if the first state's paid-search CAC exceeds about $20, or if an approved newcomer cannot reach about 500 completions in its first full season.

**Ledger distinction:** not exam prep (Phase 2 licensure apps, P8 N2 study kits) and not German food hygiene (P8 N1). This is the issuing course itself, with a regulatory listing as the channel. It is not a regulatory deadline play: Texas has required the course since 1993-born operators, and the moat is the approval, not a date.

---

## D2. Spanish- and other-language boater-safety course as a stand-alone entrant (variant of D1, kept separate because the segment and channel differ)

- **Concept:** enter only where the state list lacks a non-English course. Texas lists one Spanish option, Boat-Ed at $54.95 [Verified]. Market through Spanish-language search and Hispanic angler and boater communities.
- **Moat:** the same approval stack, plus NASBLA's certified-translation requirement.
- **Spending:** within the D1 figures; Spanish share [Unknown].
- **Channel:** state list plus Spanish search. Newcomer evidence: none, so [Unknown].
- **Risk:** Kalkomey already has Spanish versions and can cut price. The segment may be too small per state.
- **Rank:** test it only as D1's entry wedge, not as a separate business.

## D3. Certified court e-filing service provider (EFSP), Texas first

- **Concept:** a certified EFSP that files into the Tyler-run eFileTexas system, bundled into a vertical legal workflow such as small debt-collection or eviction filers.
- **Spending:**
  - 25 certified EFSPs, including Clio and InfoTrack [Verified];
  - pricing anchors at free (State EFSP, iDocket) to $1 per filing (GreenFiling) [Verified: efiletexas.gov provider pages].
- **Moat:**
  - holders grew 13 (2016) → 25 (2026), about 1.2 net a year;
  - exits: One Legal, FilePilot, File & ServeXpress;
  - entrants 2024–26: Provana, LegalConnect, Rapid Legal, Clio, TXDocs.
  - Certification cost and time: [Unknown].
- **Newcomer outcomes:** [Unknown].
- **Economics:** the filing fee is commoditised at $0–1, so value must come from the workflow.
- **Entry strategy:** none credible beyond bundling into a vertical tool, which is a different product.
- **Rank:** low. Moderate moat, thin price, entrenched incumbents.

---

## Measured kills (certifications that are not moats, or moats out of reach)

1. **IRS ATS-approved niche e-file (2290 / 720 / 8849 / 94x).**
   - 2290 providers went from 64 to 149 in three tax years, including 36 state-named doorway brands [Verified].
   - The ATS test is cheap, so approval is no barrier.
   - Overlaps the Phase 2 trucking exclusion.
   - Becoming a transmitter also needs IRS e-file application eligibility. This was not verified for a non-US founder.
2. **Texas online driving-safety courses.** 471 TDLR licences, many with keyword-spam names [Verified: TDLR CSV]. Cheap licence, so no moat.
3. **State-approved trade CE (TDLR).** 190 electrician CE providers and 79 A/C, with national players such as Jade Learning [Verified]. No moat.
4. **Tax-authority certified invoicing and e-invoicing for end users.**
   - Holder counts: France 155+12 PAs, Croatia about 37 intermediaries within year 1, UK MTD VAT 469 [Verified].
   - Crowded and within the Phase 7 exclusion of single-country fiscal and e-invoicing APIs.
   - A different segment (end-user rather than API) does not change the count problem.
5. **CRA NETFILE consumer tax software.** A stable 17 brands since 2018 [Verified], with free leaders (Wealthsimple, CloudTax, StudioTax). Annual recertification of the full T1 is heavy, and price per return trends to $0.
6. **Streamlined Sales Tax CSP.**
   - Only 6 certified holders (Avalara, TaxCloud, Sovos, AccurateTax, Avior, plus Exactor which is inactive) [Verified]. This is a real moat, and states compensate CSPs.
   - But it means multi-state tax liability, audits and a rate/boundary engine. Capital is orders of magnitude above $2k.
7. **Israeli licensed open-finance (AIS) service and ITA-certified software lists.**
   - Could not measure: gov.il returns Cloudflare 403, and no licensee list surfaced (search #3).
   - The ISA capital and insurance directive has been in force since 22 May 2024 [Secondary: Shibolet snippet].
   - Handed to Agent F. Not evidence either way.
8. **App-store approval-gated categories** (CarPlay, Family Controls, loan apps), desk reasoning only:
   - CarPlay categories require being the actual operator (parking, EV charging);
   - Family Controls is a light gate, with hundreds of screen-time apps;
   - loan apps need a lender licence.
   - Unmeasured; dropped.
9. **P2P rental-platform renter certification (B2B wedge for D1).** Neither Boatsetter nor Getmyboat partners with a renter course [Verified / Secondary]. Florida's renter temporary course is BoatUS at $8.99. The channel is unproven, so dropped as an independent idea.

## Generalisable finding for the Research Director

Across 14 lists, **holder growth tracks approval cost per jurisdiction, not the existence of certification.**

- **Cheap, test-based approvals** that list holders on an official high-intent page attract doorway brands. Holders doubled within about 3 years (IRS 2290, TX DSC).
- **Content-reviewed, fee-bearing, per-state, periodically renewed approvals** stay at about 5–6 holders per state for a decade. Recademics shows a determined two-founder newcomer can still enter in about 3 years.

Phase 9 ideas that cite "certification" as the moat should show which of these two classes they belong to.

## Ranking

1. **D1 — approval-gated online boater-safety courses.** The only idea with a verified small, stable holder count, verified spending signals, and a verified newcomer entry.
2. **D2 — language-gap entry**, as D1's wedge only.
3. **D3 — Texas EFSP.** Weak.

Everything else was killed with measurements.

### Top picks for deep diligence and the decisive unverified assumption

- **D1.** Decisive assumption: a newly approved provider can acquire paying completions at a CAC of about $12 or less in at least one high-volume state, against Kalkomey's SEO and BoatUS's $1 anchor.

  Cheap desk checks, within the rules:
  - search-volume and CPC tools for "[state] boating license/course";
  - Recademics' review velocity on Google or Trustpilot;
  - state annual reports, since providers must report certificate counts to states every year, so states may publish provider shares;
  - NASBLA review turnaround;
  - whether any target state requires an in-state entity.

- **D2.** Decisive assumption: the Spanish-speaking share of certifications in Texas, Florida and California is large enough to support a standalone wedge.

- **D3.** Not recommended for diligence unless a vertical legal workflow is already in hand.

## Searches (6/6)

1. NASBLA approval process
2. Boater-card issuance counts
3. Israeli open-finance licensees
4. Recademics
5. Kalkomey ownership and scale
6. P2P rental-platform renter certification

Blocked or unavailable:
- gov.il (403);
- myfwc.com (403);
- californiaboatercard.com (403);
- Portugal AT list (needs JavaScript);
- Transport Canada provider list (404 at guessed URLs);
- the HMRC MTD ITSA finder (form-driven; not submitted).
