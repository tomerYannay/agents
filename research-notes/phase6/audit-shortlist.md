# Phase 6 Evidence Audit: shortlist L1–L13 (independent auditor)

Date: 2026-10-13. Desk research only: no browser tools, no logins, no contact with anyone.
WebSearch: **5 of 10 used**, each logged as `P6-AUDIT`. Everything else came from WebFetch, curl and public APIs:
- WordPress.org plugin API
- Contracts Finder OCDS API
- Empire Flippers API
- Elegoo `products.json`
- SEC EDGAR
- gesetze-im-internet.de
- GCA (formerly CCS) framework documents
- TrustMRR Markdown pages
- Skool `__NEXT_DATA__` (2 groups spot-checked, plus agent A's saved sweep re-analysed)

Scratch files: `scratchpad/p6plus/audit-shortlist/`.

**Blocked sources:**
- computerweekly.com (403). The Tussell figure was verified on Tussell's own site instead.
- Contracts Finder HTML notice pages (403). The API worked.
- zap.co.il through curl (bot wall). WebFetch worked.
- Victorville CA (403).
- eSUN, Polymaker and Bambu where-to-buy pages (403).
- The Israeli customs tariff site (JavaScript only).

## Summary table

| ID | Verdict | Suggested penalty | One-line reason |
|---|---|---|---|
| L1 Elterngeld concierge | Partly supported | **12** | The paid category and its prices are verified. The test is older than claimed (Finanztest 1/2023). The test winner now sells **€24.95 software** with an English UI, and Elterngeldexperten serves English and French. RDG legality is unresolved. Free multilingual NGO help exists for the TR/AR/RU/UA segment. |
| L2 Spanish AI community | Partly supported | **12** | The Skool numbers replicate exactly from the saved data and 2 groups were re-fetched. Still an upper-bound trending sample. The channel is a co-host who has not been found. |
| L3 Operator-partner communities | Partly supported | **12** | The base rates replicate. The "lift from an operator" claim is untested. Drift towards agency work. |
| L4 Bulk filament (Israel) | Weak | **13** | The retail gap is verified. Self-import of a 10 kg pack lands near the proposed sale price. No buyer count, no Israeli bulk-supplier scan, duty unknown, capital above budget. |
| L5 First Israeli distributor | Weak | **14** | Only the reform is evidenced. No brand, no terms, no demand. |
| L6 Pay-per-call / lead sites | Partly supported, leaning weak | **13** | The "$213 median payout" is a minimum offered rate per ZIP row in a bid-coverage file, not realised earnings. The buyer prices cited as Lead Smart's site prices are contradicted by the site now. The Google rules and the LSA migration are verified and adverse. |
| L7 Backflow tester-pay platform | Partly supported | **12** | Fees are verified. But the main incumbent (BSI) charges utilities **$495–8,995/yr plus** $15.95–23.95 per report from testers. Tester-pay is not universal. BSI claims a US patent and is actively signing new cities. |
| L8 Cemetery software | Supported (facts), weak on channel | **12** | Cemify prices, team size and "profitable" claim verified. NY 1,700 verified. Channel unmeasured. |
| L9 Abandoned WP plugins | Partly supported | **13** | Plugin data verified. Taking over a slug needs the author's consent. Trademark owners are a listed reason for denial, and these slugs carry WooCommerce, PagSeguro and Correios names. Active Brazilian newcomers already serve the same niche (one reached 4k installs in 2 years). |
| L10 G-Cloud micro-SaaS | Partly supported; **timing contradicted** | **12** (plus speed-to-first-sale cut) | The award examples and the "86% of suppliers won nothing" figure are verified. But **G-Cloud 15 does not reopen to new suppliers until about 18 months after its Aug 2026 start (about Feb 2028)**. Insurance minimums are PI £1m, PL £1m, EL £5m. Lot 1b needs £50m/£20m, not "£75m". |
| L11 G-Cloud reseller | Weak | **13** | Same reopening problem. Reseller margins and vendor willingness unknown. |
| L12 Seeker-paid job search + AI | Partly supported | **13** | Ton-piston is verified (MRR $9,770, 936 subscriptions) but it is one outlier with an audience. The "founded" date is self-entered. |
| L13 Aged app acquisition | Weak | **13** | Capital is 5–25× the budget. Uplift has no data. Not re-verified beyond the agent's samples. |

**Cross-cutting finding.** Three of the four "direct" ideas (L1, L7, L10) have a load-bearing fact the discovery agent got wrong or incomplete, and each is checkable from a primary page:
- L1: the €24.95 software from the incumbent.
- L7: BSI's utility subscription and patent.
- L10: the reopening date.

The Red-Team should treat these as current blockers or major frictions, not open unknowns.

---

## L1 — Elterngeld / family-benefit concierge (Germany)

### Verified
- **Births:** 654,241 live births in 2025, the lowest since 1946, down from 677,117 in 2024 (−3.4%) [Verified: destatis.de/DE/Themen/Gesellschaft-Umwelt/Bevoelkerung/Geburten/_inhalt.html, 2026-10-13]. The share born to foreign mothers is still [Unknown]; the table exists but was not opened.
- **Finanztest test** (test.de/Elterngeldberatung-im-Test-5942423-0, page dated 01.02.2024) [Verified, 2026-10-13]:
  - 8 providers and 40 consultations.
  - Commercial providers: Einfach Elterngeld, Elterngeldexperten, Elterngeld.net, Elterngelden.
  - Non-profit providers: AWO, Caritas, Diakonie, pro familia.
  - Quotes: "Im Test überzeugen vor allem kommerzielle Anbieter"; specialist advice can be worth "Tausende Euro"; the test winner is a commercial firm. Grades ran from 1.6 to 3.2.
  - Commercial advice-only packages cost €120–149 as of January 2024.
- **Elterngeldexperten** [Verified: elterngeldexperten.de, 2026-10-13]:
  - €179 / €279 / €329 for both parents, one-time.
  - "über 25.000 Familien seit 2018" [vendor claim].
  - It is a GmbH (HRB 31603 Chemnitz) that calls itself "ein privates, unabhängiges Beratungsunternehmen und keine Behörde".
  - **Languages: German, English and French.**
- **Elterngeldhelden** [Verified: elterngeldhelden.de, 2026-10-13]:
  - €169 / €249 / €299, in German, English and Italian. No customer count.
  - Its AGB scope reads "Beratung in finanziellen Fragen … so wie die Erstellung der notwendigen Anträge".
- **Einfach Elterngeld GmbH** (HRB 36979 Dresden), the test winner. Its site cites "Note 1,6 (Stiftung Warentest)" and 735 ProvenExpert reviews at 4.92 [Verified: einfach-elterngeld.de, /software/infos, /beratung, 2026-10-13]:
  - **Self-service software for €24.95 one-time.** It fills in the Elterngeld and Kindergeld applications and has an English UI toggle.
  - Advice packages at €149 / €249 / €299.
  - Its AGB (version valid from 13.10.2026) states: "Wir vertreten Sie nicht gegenüber Behörden und geben keine Erklärungen in Ihrem Namen ab."
- **RDG text** [Verified: gesetze-im-internet.de/rdg/__2.html, __5.html, __10.html]:
  - §2(1): a legal service is any activity in concrete third-party matters "sobald sie eine rechtliche Prüfung des Einzelfalls erfordert".
  - §10: registered "Rentenberatung" covers pension and accident insurance, social compensation and other social insurance only where linked to a statutory pension. **There is no registration route covering Elterngeld (BEEG) advice.**
  - §5: ancillary legal services are allowed only as a side activity to another occupation.

### Contradicted or overstated
- **"Finanztest Jan 2024 tested commercial providers favourably"** is overstated. The downloadable test is from **Finanztest 1/2023** (fieldwork 2022). The February 2024 page adds updated prices. The evidence is about 3 years old.
- **"Only Elterngeldhelden offers English/Italian"** is contradicted. Elterngeldexperten offers English and French, and the test winner's software has an English UI.
- **The entry wedge "AI intake, calculator, cheaper check-my-own-application tier at about €99"** is undercut. The test winner already sells self-service form-filling software for **€24.95** and advice from €149.
- **"No TR/AR/RU/UA provider found"** holds for paid providers. But free multilingual help exists for exactly those groups: for example, ema gGmbH in Hannover gives multilingual benefits and application help with Arabic, Russian and Ukrainian staff; Flüchtlingsrat BW runs English parent advice; municipal FamilienServiceBüros exist [Secondary: search snippets, P6-AUDIT]. Elterngeldstellen must advise for free (§14 SGB I, cited by test.de).

### Legality (the RDG question)
- No court ruling or Abmahnung against Elterngeld advisers surfaced in one targeted WebSearch [P6-AUDIT log]. Absence is not clearance.
- The incumbents publish no RDG statement: none of the 3 sites or AGBs mention RDG or a lawyer.
- The structure the test winner uses looks like risk management: it does not represent clients before the authority, does not make declarations for them, sells software licences, and advises on "optimisation".
- Relevant background, not fetched this phase [Secondary/background]: the BGH "Smartlaw" decision (I ZR 113/20, 2021) held that a document-generator product is not a legal service.
- **Assessment:**
  - Calculation, optimisation and form-filling software is low risk.
  - Case-specific advice on contested points, such as foreign income or EU coordination under Regulation 883/2004, is precisely "rechtliche Prüfung des Einzelfalls". That is the planned premium segment.
  - Firms operate openly and Stiftung Warentest tested them without objection. That points to tolerance, not legality.
  - **Unresolved; needs a German lawyer's opinion before launch.** For a non-German founder's firm, the risk sits in the high-value cross-border cases.

### Unknowns that matter
- CAC and paid-search CPCs.
- The share of births to non-German-speaking parents.
- Willingness to pay among the TR/AR/RU/UA segment, given free NGO help and lower average incomes [Hypothesis].
- Adviser supply that speaks those languages.

### Verdict and penalty
**Partly supported. Penalty 12.**

Criterion concerns:
- Existing spending: about 3/5. The category is real, but volume is vendor-claimed.
- Defensibility: 1/5. The incumbent has software plus advice at €24.95–299 in English.
- Proven channel: should not exceed 2/5 (no CAC, no newcomer data).
- Capital/delivery: note the legal-opinion cost.

The best remaining wedge is narrow: Turkish, Arabic or Russian service for employed (not refugee) parents. That is a [Hypothesis] with no willingness-to-pay evidence.

---

## L2 — Spanish-language AI-agents community (co-host model)

### Verified
- **Replication.** I re-ran agent A's saved sweep (`scratchpad/p6plus/A/data/*.json`) with my own script, normalising yearly prices to monthly and excluding one-time prices. The headline figures **replicate exactly**:
  - Spanish "claude", new model-2 monthly groups: n=12, median 136 members, 8 at ≥$2k implied MRR.
  - English "claude code": n=28, median 48, 10 at ≥$2k.
- **Spot-checks** [Verified: skool.com/{slug}/about `__NEXT_DATA__`, 2026-10-13]:
  - "Agentic Engineers": 215 members, created 2026-05-06, 15 courses, **44 posts in 5 months, 1 member online**.
  - "Automatízate": 121 members, 111 posts, 0 online.

### Overstated or method caveats
- **The agent's generic analysis script (`an.py`) multiplies price × members for one-time and yearly prices too.** In the loose "all new paid" cut, this inflates the ≥$2k counts:
  - Spanish "claude": 14 naive against 12 normalised.
  - English hobby sweep: 162 against 126.
  - It also lets in absurd gate prices, such as "IA Builder Lab" at $9,999/month × 16 members.
  - **The figures quoted in the report use the correct model-2 monthly filter**, so the reported numbers stand. The loose top-25 lists in the script output should not be cited.
- **Implied MRR is an upper bound.** `totalMembers` includes owners, admins, trialists and comped members. Activity is low: 1 online member out of 215.
- The sample is the top ~60–90 "trending" results per keyword, so survivorship bias makes the true newcomer distribution worse.
- **n=12 is tiny.** The Spanish "claude" results are dominated by generic "make money with AI" groups rather than technical-builder communities.

### Unknowns that matter
- Churn and retention.
- A co-host with an audience. This is the whole channel, and no candidate has been identified.
- Revenue split terms.

### Verdict and penalty
**Partly supported. Penalty 12.**

Criterion concerns:
- Proven channel: about 2/5. The data proves that people *with* audiences fill groups. It does not show a faceless founder can.
- Founder labour: weekly live sessions mean high labour.
- Recurring revenue: credit only with a churn caveat.

---

## L3 — Operator-partner for hobby-expert paid communities

### Verified
The same replication applies. English new model-2 monthly groups: n=454, median 11 members, p75 38, 84 (18.5%) at ≥$2k. Dog vertical: 29 groups, median 16, 7 at ≥$2k.

### Overstated
- "1 in 3 launches succeed" with operator involvement is a [Hypothesis] above the visible 18.5%. The visible rate itself is an upper bound from a trending sample.
- Revenue-share economics depend on partners not leaving after success. There is no evidence either way.

### Verdict and penalty
**Partly supported. Penalty 12.**

Criterion concerns:
- Founder labour and delegation: should score low (each partner is a 3–6-month build, which is service drift).
- Defensibility: 1/5 (the partner owns the audience).

---

## L4 — Bulk filament for Israeli print farms and labs (+ DTF variant)

### Verified
- **Zap category** [Verified: WebFetch of zap.co.il/models.aspx?sog=c-3dprintersupplies, 2026-10-13]:
  - 487 products; no 5 kg or 10 kg packs listed.
  - Bambu PLA at 109–129 ₪.
  - The cheapest PLA is **Creality Hyper PLA at 84 ₪/kg** (Daily Sale, free shipping). The agent's floor of "96 ₪" is slightly overstated.
- **Elegoo 10 kg packs** [Verified: elegoo.com/products.json, 2026-10-13]: PLA $119.99, PLA+ $109.99, Rapid PLA+ $129.99. That is $11–13/kg before shipping.
- **Bambu price.** Bambu's "$11.19" is a conditional "after bulk sale" promotional price on the Asia-store page (agent B's saved HTML). It is not a standing price.

### Contradicted or weak
- **The kill test the agent set ("self-import of 10 kg lands under about 50 ₪/kg") is close to failing in the business's disfavour** [Hypothesis arithmetic]:
  - Starting point: $120 for 10 kg Elegoo.
  - VAT: +18%, because the order is above the $75 exemption.
  - Shipping: plus about $30–60 for 11–12 kg (shipping cost [Unknown]).
  - Result: about $172–202, or **53–62 ₪/kg** at 3.077 ₪/$.
  - The proposed sale price is 55–70 ₪/kg. **Print farms that already self-import gain little from switching.** The real gap exists only against Israeli 1 kg retail, which serious farms probably don't pay.
  - Whether Elegoo ships 10 kg packs to Israel is [Unknown]. Its shipping policy page did not mention Israel.
- **"No Israeli bulk supplier"** is unverified, not established:
  - Zap is a consumer price-comparison site and does not show B2B distributors.
  - Brand where-to-buy pages were blocked (403).
  - One English WebSearch for an Israeli eSUN, Polymaker or Bambu distributor returned nothing; the engine is US-only, so this is not proof.
  - CopyTech's private label (ALMA) shows at least one importer at scale.
- **Duty on HS 3916** is still [Unknown] (the customs site is JavaScript-only).
- **Buyer count** is [Unknown]. Capital for the first shipment (about $2.5–4k) is above budget.

### Verdict and penalty
**Weak. Penalty 13.**

Criterion concerns:
- Existing spending: 1–2/5. Only shelf presence is shown.
- Margins: likely overstated if farms already self-import.
- Capital: flag over budget.

The DTF/sublimation variant is not evidenced beyond a single sublimation-paper price comparison.

---

## L5 — First authorised Israeli distributor (EU-compliance import track)

**Brief check.** The only evidence is that the reform exists [agent: barlaw.co.il client update, 13-Jul-2025; not re-opened, source URL not recorded in the report]. There is:
- no named brand,
- no MOQ or discount terms,
- no demand signal.

The SEC distributor gross-margin benchmarks (21–45%) come from scale distributors and do not transfer to a micro-importer.

### Verdict and penalty
**Weak. Penalty 14.** Spending evidence: 1/5. Speed to first sale: low, because brand negotiation is outside desk scope.

---

## L6 — Pay-per-call / exclusive lead sites in emergency home-service verticals

### Verified
- **Lead Smart's own newsroom** (leadsmartinc.com/news/press-google-lsa-lead-costs-rise-payout-data-september-2026) [Verified, 2026-10-13]:
  - Water damage $213.00 median / $507 high across 18,665 ZIPs; biohazard $210.50; fire $193.
  - **Method:** "from Lead Smart's public affiliate bid coverage tool, complete extract of 296,513 rows". The figures are described as **"minimum expected payouts"** that "exclude buyer-side reconciliations".
  - Claims "more than 10,000 registered affiliate publishers worldwide" and "$50 million … across Lead Smart and its predecessor businesses" [vendor].
  - A later extract (September 20, via a search snippet) put the water-damage median at **$189**.
- **Google LSA → Google Ads migration** [Verified: support.google.com/google-ads/answer/17213585]:
  - August 2026: the first phase starts for select US categories.
  - Late 2026: broader groups.
  - 2027: non-US accounts.
  - Pay-per-valid-lead billing is kept.
- **Google Business Profile guidelines** [Verified: support.google.com/business/answer/3038177]:
  - A profile requires a location customers can visit, or a business that travels to customers.
  - Virtual offices and remote P.O. boxes are ineligible.
  - Lead-generation agents are named as ineligible in the practitioner context.
  - **Map-pack rank-and-rent for a non-existent business is a guideline violation.**
- **Angi Q2-2026 10-Q** [Verified: EDGAR re-fetched]: about 106,000 average monthly active pros. The −17% and −12% figures were not re-derived but are consistent with the agent.
- **Empire Flippers lead-gen listings** [Verified: api.empireflippers.com, re-pulled 2026-10-13]:
  - 26 listings: 25 sold, 1 for sale (96995, September 2026, $3,113/mo, 36×).
  - Only 4 were first listed in 2024 or later.
  - Small examples confirmed: 47115 ($712/mo, $13.5k), 48163 ($662, $15.9k), 88006 ($4,318, 27×).

### Contradicted or overstated
- **The "median publisher payouts" are not realised earnings.**
  - They are minimum offered rates per ZIP-service row in a bid-coverage file. The median is across ZIP rows, not across calls paid.
  - Water damage and biohazard are **CPL (qualified-lead) entries, not duration-gated calls**.
  - The figure moves ±10% within weeks ($213 → $189).
  - The announcements are serial paid press releases syndicated on "pr.*" news-site subdomains.
  - The Red-Team's CallScaler check found typical water-damage call payouts of $40–110.
- **"Buyer prices HVAC $135–225, roofing $155–295 on Lead Smart's site" is contradicted now.**
  - leadsmartinc.com/pay-per-call lists roofing **$120**, HVAC **$100**, plumbing $100, electrician $50.
  - /hvac says "$100 per qualified call".
  - **Water damage, restoration and biohazard are not on Lead Smart's buyer price list.**
  - So the "networks keep 60–80%" inference becomes about 60% for HVAC ($38.50 against $100). The emergency-vertical spread is unverifiable.
- **Angi "Network" service requests −38%** (third-party sites) is a negative signal for affiliate lead sites, not a positive one.
- **EF exit multiples** come from survivors listed 2015–2022. The flow has nearly stopped, so they are no newcomer evidence.

### Unknowns that matter
- Time to first call for a new organic site in 2026, with AI Overviews and LSA/PMax above the organic results.
- Actual payable call volume.
- Network acceptance terms for traffic sources.

### Verdict and penalty
**Partly supported, leaning Weak. Penalty 13.**

Criterion concerns:
- Proven channel: ≤2/5. No newcomer data; the platform is moving against the channel.
- Speed to first sale: low (4–12+ months).
- Margins: should use about $40–110 per call, not $213.

---

## L7 — Backflow compliance platform, testers pay per report (+ FOG/septic variant)

### Verified
- **Gig Harbor WA:** "currently using SwiftComply (c3swift.com)"; "$7.50 per passing test fee to submit a passing test report" [Verified: gigharborwa.gov/856/Tester-Resources, 2026-10-13]. A search snippet said $5.00; the page says $7.50.
- **Piqua OH:** BSI Online, "$15.95 per test report submitted", from 15 Feb 2024 after a no-fee window. Article dated 16 Jan 2024 [Verified: mycountylink.com]. The article does not say who pays; BSI's pricing page says testers pay.
- **BSI public pricing** [Verified: backflow.com/sales/, 2026-10-13]:

  | Plan | Utility pays (US) | Tester pays per report |
  |---|---|---|
  | Standard | $495/yr | $15.95 |
  | Premium | $1,495/yr | $18.95 |
  | Elite | $4,495/yr | $20.95 |
  | Diamond | $8,995/yr | $23.95 |

  - A one-time implementation fee applies on top.
  - Canada: C$595–9,995/yr, with tester fees of C$23.95–30.95.
  - "75+ trained employees". Clients range from "less than 100 devices" to tens of thousands.
- **BSI patent claim** [Verified page; vendor claim]: backflow.com/patent says "The ONLY US Patented Backflow Software Solution" and "we hold the US Patent for the concept". The patent number and claims were not identified.
- **BSI is actively signing new cities.** Its page sitemap has 2024–2026 onboarding and registration pages for Pompano, Northglenn, Carrollton, Rosenberg, Durham, Buffalo Grove, Johnston, Flower Mound, Akron, Palos Heights, South Holland, Westminster and Hillsborough, plus Texas, Colorado and North Carolina lunch-and-learns.
- **Brycer / The Compliance Engine** [Verified: thecomplianceengine.com]: "Jurisdictions pay nothing to implement or maintain the system"; "per-system report fee"; "over 2,000 AHJs" [vendor]. This is the fire-inspection analogue.
- **Yakima WA uses Tokay, and the city pays** [Verified: yakimawa.gov Guidelines PDF, version 2/01/22]: "Currently the city pays any fees associated with submittals, however these fees may be passed onto the tester in the future."
- **Utility sample (9 programmes, from 1 search plus fetches):**
  - BSI: 5 (Piqua, Wilton Manors $28, Queen Creek $14.95 on a 2014 page, Round Rock, New Westminster BC).
  - SwiftComply: 3 (Gig Harbor $7.50, Victorville, Park City).
  - Tokay: 1 (Yakima, city pays).
  - Victorville says there is no charge for SwiftComply submissions [Secondary: snippet; page 403].
  - **Tester-pay is common but not universal. At least 2 of the 9 do not charge testers.**

### Contradicted or overstated
- **"Free to utility, testers pay" is presented as the incumbent model. For BSI it is a hybrid:** the utility pays a subscription and testers pay per report.
  - The proposed entry ("no cost to the utility, lower tester fee $7–10") saves a small utility only **$495/yr** against BSI Standard. SwiftComply already charges testers $7.50.
  - **The price wedge is thin on both sides.**
- **The patent claim adds IP risk to a direct copy of the model.** Its scope is [Unknown] and needs a freedom-to-operate check.
- **"Small towns are still on paper, so not saturated"** is supported. But the evidence shows the leading incumbent with 75+ staff actively winning those same towns, including small ones.

### Unknowns that matter
- How many of about 50k community water systems run formal cross-connection programmes.
- Sales-cycle length.
- Whether a zero-cost agreement avoids procurement.
- Insurance and US-entity requirements.
- The patent's claims.

### Verdict and penalty
**Partly supported. Penalty 12.**

Criterion concerns:
- Existing spending: 4/5 (mandatory fees verified).
- Defensibility: 1/5 (patent plus incumbents with matching or lower fees).
- Speed to first sale: 1/5.
- First customers: hard (municipal vote, references).

The FOG/septic variant has no fee evidence: penalty 14 if scored separately.

---

## L8 — Low-cost cemetery records and mapping software

### Verified
- **Cemify** [Verified: cemify.com/pricing, 2026-10-13]:
  - $799 / $1,299 / $1,899 per year; setup quoted case by case; a records-only setup takes $100 off.
  - "We are a four-person team", "hundreds of cemeteries", "8 years of operation", "profitable, fully independent, and family-run".
- **New York:** NY DOS oversees "approximately 1,700 not-for-profit cemeteries" and publishes "Find a Cemetery By County" [Verified: dos.ny.gov/cemeteries].

### Overstated
"A 4-person vendor is profitable" is a vendor self-description. "Hundreds over 8 years" means slow acquisition: dozens per year at best.

### Unknown
Channel conversion and review velocity (Capterra was blocked).

### Verdict and penalty
**Supported on the facts, weak on the channel. Penalty 12.** Proven channel ≤2/5. Market depth is small for Track B.

---

## L9 — Take over abandoned high-install WordPress plugins (Brazil first)

### Verified
- **The three Brazil plugins** [Verified: api.wordpress.org plugin_information, 2026-10-13]:

  | Plugin | Installs | Last updated | Ratings | Contributors |
  |---|---|---|---|---|
  | `woocommerce-extra-checkout-fields-for-brazil` | 60,000 | 2024-02-17 (tested to WP 6.4) | 96 (515) | Claudio Sanches only |
  | `woocommerce-correios` | 20,000 | 2025-01-25 | 98 (868) | Claudio Sanches, rodrigoprior, matheuscl |
  | `woocommerce-pagseguro` | 10,000 | 2020-08-10 | 98 (914) | — |

- **Adoption rules** [Verified: developer.wordpress.org/plugins/wordpress-org/take-over-an-existing-plugin/]:
  - The adopter "must attempt to contact the original developer".
  - If the developer denies the request, the Plugins Team honours that and asks for a fork.
  - If the developer is unresponsive for 30 days, the team decides case by case "based on … your history in the directory".
  - "Larger plugins (100k users or more) are also less likely to be adopted."
  - **Trademark-owning companies are a listed reason for denial.**
  - Adopters must keep the original purpose.
- **Newer competitors and newcomer outcomes in the same niche** [Verified: WP.org API]:

  | Plugin | Added | Installs | Ratings | Notes |
  |---|---|---|---|---|
  | `infixs-correios-automatico` | 2024-10-21 | **4,000** | 90 | Mentions a pro tier; updated 2026-10-10 |
  | `virtuaria-correios` | 2024-05 | 500 | — | |
  | `pagbank-connect` | 2024-01 | 3,000 | — | |
  | `brazilian-checkout-toolkit-for-woocommerce` | 2026-01 | 100 | — | |

  Also present: Melhor Envio (10,000), PagBank official (3,000), and several linknacional plugins.

### Contradicted or overstated
- **"Value is the slug; transfer price a few hundred to a few thousand"** is unsupported. Transfer is consent-based, and plugin names containing WooCommerce, PagSeguro or Correios trademarks face a stated denial ground.
- **Correios has 3 contributors and a January 2025 update**, so it is not clearly abandoned.
- **The stale-plugin demand is already being captured by maintained newcomers.** That helps the newcomer-outcome evidence: a fork-style newcomer reached 4k installs in about 2 years. But it weakens the "under-served" claim.

### Unknowns
- Author willingness to transfer.
- Paid conversion: there is no Brazil-specific pro-plugin sales data.
- Infixs pro revenue.

### Verdict and penalty
**Partly supported. Penalty 13.**

Criterion concerns:
- Defensibility: 1/5.
- Existing spending: 1–2/5 (no paid-tier transactions found).
- Distribution: credit the newcomer install data (Infixs) for discoverability, not for purchases.

---

## L10 — G-Cloud 15 micro-SaaS for a narrow UK public-sector workflow

### Verified
- **Award examples, re-queried independently** from the Contracts Finder OCDS Search API by exact timestamp window [Verified, 2026-10-13]:

  | Award | Value | Supplier (scale) | Buyer | Notes |
  |---|---|---|---|---|
  | Registrar Booking System | £14,304 | Stopford (SME) | Lincolnshire CC | Contract 2026-02-01 to 2027-01-31 |
  | Low Income Family Tracker | £50,900 | Policy in Practice (SME) | Wirral | Contract 2025-10 to 2026-10 |
  | MIRO Licence Expansion | £152,064 | Generation Digital (SME) | GBE-Nuclear | 2-year term |
  | Growth Chart Software | £43,088 | Harlow Printing (SME) | United Lincolnshire NHS | |

  Other examples, read from agent E's saved records:
  - "Dental Max-course" £16,500 is a **licence renewal** over 15 months.
  - "TfGM Cycle Training" £44,120 runs for **3 years** (about £14.7k/yr); the buyer has "offered this service … for a number of years".
- **Tussell figure on Tussell's own site** [Verified: tussell.com/insights/how-to-win-more-business-through-g-cloud-v1, 2026-10-13]: "86% of suppliers on G-Cloud 10 did not earn any revenue through the framework in 2018". This matches the agent's 14% winners. It is **2018 data**.
- **G-Cloud 15 framework** [Verified: gca.gov.uk/agreements/RM1557.15, and the RM1557.15 supplier guide and Framework Award Form downloaded from assets.gca.gov.uk]:
  - Open framework, starting 6 Aug 2026.
  - **"This framework will re-open after 18 months and again at 36 months … allow new suppliers to bid to join."**
  - The award form reads: "Initial Framework Contract Period of 18 months. Framework to be opened at the end of the Initial Framework Contract Period."
  - The framework "tests a Supplier's economic and financial standing as part of the framework application process".
  - Cyber Essentials (Call-Off Schedule 27) is optional per call-off.
- **Insurance** [Verified: Joint Schedule 3 Annex, RM1557.15]:
  - Lots 1a, 2a, 2b and 3: **professional indemnity £1m, public liability £1m, employer's liability £5m**.
  - Lot 1b: PI £50m, PL £20m, EL £5m.
- **Supplier liability cap** for Lots 2a, 2b and 3: the greater of £500k or 125% of the estimated yearly charges [Framework Award Form].

### Contradicted or overstated
- **"New suppliers can join during an 18-month reopening window"** reads as if joining is possible now. The GCA page and supplier guide say **the framework reopens after 18 months (about February 2028)**. The gov.uk press line ("during an 18-month re-opening window after launch") is ambiguous, but the framework documents are explicit.
  - **A new supplier cannot list on G-Cloud 15 until about Feb 2028**, and the first award would come later still.
  - That turns "time to first sale 6–18 months" into **roughly 18–30+ months**.
  - Selling below threshold without a framework (direct small-value contracts) is possible but is a different channel, with no evidence here.
- **"Lot 1b needs £75m insurance"** is contradicted: it is £50m PI and £20m PL. This is irrelevant if Lot 2b is used.
- **The award examples are mostly renewals or continuations of incumbents.** That supports the "references and incumbency" barrier more than the "small awards are winnable" reading. Values are multi-year totals, so annual values are lower than the headline figures.
- **Non-UK eligibility:** the documents I read state no UK-establishment requirement. Non-UK winners (Freshworks Inc, Sayari Labs Inc) appear in the awards. Israel is a WTO GPA party, which under the Procurement Act 2023 should make it a treaty-state supplier [Secondary/background, not verified this phase]. A UK Ltd still makes sense. A newly formed company must pass the economic and financial standing test; its criteria were not found.

### Verdict and penalty
**Partly supported, with a timing blocker. Penalty 12.**

Criterion concerns:
- **Speed to first sale: 0–1/5.** The framework is closed to new suppliers until about Feb 2028.
- Proven channel: 2/5 at most (86% of listed suppliers won nothing; winners are 10+ years old).
- Insurance cost (PI, PL and £5m EL) is likely about £1–3k/yr [Hypothesis]. Check this against the $2k budget.

---

## L11 — G-Cloud reseller for non-UK SaaS vendors

### Verified
Generation Digital won the £152,064 Miro award (re-queried, as above). Reseller wins exist.

### Problems
- The same **reopening constraint** applies (about Feb 2028).
- Reseller margin, vendor willingness and credit exposure are all [Unknown].
- The large VARs (Softcat, SCC) already serve vendors that have demand.

### Verdict and penalty
**Weak. Penalty 13.** Speed to first sale: 0–1/5. Spending evidence credits reseller awards but not this business's margin.

---

## L12 — Seeker-paid local-language job search with AI tools

### Verified
Ton-piston [Verified: trustmrr.com/startup/ton-piston.md, Stripe API, synced 2026-10-13]:
- Revenue: $10,517 in the last 30 days, $22,065 all-time.
- **Current MRR $9,770; 936 active subscriptions.**
- Last-30-day revenue −4.0%; MRR growth +54.4%.
- Founder has 51,582 X followers.
- About 50,000 users (estimated; founder-entered).

### Overstated
- "Founded 2026-08-03" is self-entered. The free "Piston" search engine may predate the Pro launch, so "10 weeks from zero" is not established.
- It is a single, audience-driven example, not a newcomer base rate.
- Remote Rocketship's "~$6k/mo" is secondary only.

### Verdict and penalty
**Partly supported. Penalty 13.** Proven channel: 1–2/5 for a founder with no audience. Recurring revenue is credible but seasonal.

---

## L13 — Acquire and modernise aged mobile apps

### Brief check
- Not re-fetched; Flippa's public search pages show only about 30 results per query.
- The agent's figures rest on samples of about 30 visible listings. The quoted profits (for example, the Quran app at $544/mo) are **seller claims**; "Data Verified" means a connected revenue source, not an audit.
- **No uplift data exists.** Capital of $6–25k per asset is above the $2k budget.

### Verdict and penalty
**Weak. Penalty 13.** Capital feasibility: 0–1/5. Existing spending: credit app revenue only as seller-claimed.

---

## Opinion on the leader re-check corrections (audit-leaders.md)

I agree with the direction of all five and with most of the magnitudes. My positions:

- **H6 (57.2 → 51.6): agree with the cut; the magnitude double-counts.**
  - The CFBD patron curve, the peer ceiling of 30–450 members, Highlightly's $0–7.99 API, the free daily sportsdataverse pipeline and the NCAA terms are all strong, directly measured evidence.
  - But "first customers −1" and "defensibility −1" both penalise the same fact (free equivalent data exists).
  - Dropping one of them gives about **52.2**, still with penalty 13 for the NCAA-terms contradiction, which I accept.
- **H1 (54.6 → 51.2): agree with proven channel −1; the rest double-counts.**
  - The penalty +1 and defensibility −1 both rest on one fact ("2-packs now exist").
  - A plain RAK 2-pack is not the pre-paired family kit, so the original differentiator is only partly contradicted.
  - Keep penalty 6 and take defensibility −1: about **52.2**.
- **monday.com app (52.0 → 50.8): agree.**
  - Removing platform-wide install and case-study credit is exactly the Phase 5 rule.
  - Shopify and Wix traction for Morning and iCount (0–16 reviews) is a fair proxy.
- **K13 (53.6 → 52.6 or 50.6): agree with defensibility −2 and first customers −1. Disagree with the spending +1.**
  - Ifat shipping receivership coverage and AI summaries, free through 2026, verifiably removes both planned differentiators.
  - The spending +1 rests on a subscription *structure* with no Ifat prices and a Kones list price of ₪249. Under hard lesson 4, a listed price is not proof of buyers.
  - Adopt **50.6**.
- **K8 (hold 53.2): agree with holding; make the conditional mandatory.**
  - There is no new measurable data, so holding is right.
  - The board keeper should confirm from the Phase 5 notes whether the $6.5M payout figure was credited in Distribution. If it was, apply the −1 (about 52.0), as the auditor proposes, since Phase 5's own rule forbids that credit.

**Net effect:** H7 (56.6) becomes the sole leader by about 4 points, which is within noise. The 50–53 cluster tightens further, which reinforces the Director's point that no candidate stands out.

---

## Decisive unverified items handed to Red-Team / rescoring

- **L1:** A German lawyer's RDG view on case-specific cross-border Elterngeld advice by a non-lawyer company. Willingness to pay in the TR/AR/RU segment, given free NGO help and €24.95 incumbent software.
- **L4:** Landed cost of a self-imported 10 kg pack to Israel (shipping and duty). A list of Israeli B2B filament importers.
- **L6:** Realised payable calls and payout for a new site, not offered rates.
- **L7:** Scope of BSI's patent. The share of programmes using tester-pay. Utility procurement for zero-cost agreements.
- **L9:** Author consent and the trademark-denial risk for `woocommerce-*` slugs. Paid conversion for Brazilian pro plugins.
- **L10/L11:** Confirm the G-Cloud 15 first reopening date (about Feb 2028) and the economic-standing criteria for a newly formed Ltd. Find a non-framework direct-award route for small values.

WebSearch count: 5 / 10 (P6-AUDIT).
