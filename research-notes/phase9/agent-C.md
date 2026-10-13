# Phase 9, Agent C (Traditional, offline and services): licences, registrations and acquired licence-holders

Agent label: P9-C. Date: 2026-10-13. WebSearch used: 6 of 6. Most evidence comes from public registers pulled directly: data.gov.il CKAN, the Israeli MOH registries API, the EUDAMED public API, Texas DSHS, nexxt-change.org, eCFR and the EC OSS report PDF. Scripts are in `scratchpad/p6plus/P9-C/scripts`; raw data is in `.../P9-C/data`.

## Headline finding: this moat type mostly fails the Phase 9 test for this founder

I measured nine registers. They fall into two groups.

**1. Barrier cheap enough for this founder (weeks to months, under about $2k).** Holder counts grow freely, so the status is not a moat:
- Israeli food-importer registrations: about half of the active ones carry the newest registration numbers.
- Israeli cosmetics "RP corporations": 68, mostly recent, many of them single shops.
- Texas online food-handler programmes: 63 holders, licence fee $600 for 2 years; 20 of the 63 hold licence numbers of 200 or above (the highest is 252).
- Certified payroll auditors: 2,029 registered.
- IOSS intermediaries: 1,394.

**2. Barrier meaningful** (an EU establishment plus a PRRC, or an Israeli QMS-certified entity). Here the status is real, but incumbents hold the mandates. Of 46 independent service ARs that entered EUDAMED in 2023–26, the median holds **1** non-EU manufacturer mandate. Only 3 reached 15 or more without a global brand or a spin-off from an incumbent. That is about 6.5%, almost exactly the Phase 8 base rate of 4–6%. Israeli manufacturers' EU mandates are concentrated: MedNet entities hold 179 and Obelis 64.

**Conclusion:**
- Licences obtainable in 3–9 months do not by themselves beat the 4–6% newcomer prior.
- Mandate-type statuses have high switching costs. That protects incumbents, not entrants.
- Only one idea, C1 (Israeli IRH), keeps a plausible Track A case, and it is modest.

---

## C1. Independent, flat-fee Israel Registration Holder (IRH) for foreign small and mid-size device makers, sold through global regulatory platforms

**1. Concept.**
- An Israeli company that holds AMAR (MOH medical-device) registrations on behalf of foreign manufacturers, independently of any distributor.
- It sells mainly as a white-label partner to multi-country registration platforms that do not cover Israel.

**2. Paying customer and geography.**
- Customers are foreign device and IVD makers with CE or FDA clearance (US, China, Germany, Korea and others) entering Israel.
- They are served from Israel. An IRH must be an Israeli citizen or an Israeli-established company [Secondary: meddeviceguide.com AMAR guide; Emergo IRH page, accessed 2026-10-13].

**3. Model and price.**
- The customer pays an annual IRH fee plus per-registration filing work.
- Vendor guide: "Annual IRH fees $3,000–$10,000"; total with consultant is $3–8k for Class I and $5–15k for Class II [Secondary/vendor: meddeviceguide.com/blog/israel-amar-medical-device-registration-guide, accessed 2026-10-13].
- Global platform benchmark: Pure Global charges from $2,000/yr for the EU, UK and CH, with a 3-year contract, and **does not list Israel** [Verified: pureglobal.com/services/pricing, 2026-10-13].

**4. Spending evidence (AMAR register, my pull of all 30,212 records via registries.health.gov.il/api/MedicalDevices, 2026-10-13).**
- The register holds 13,404 active registrations across 1,160 active registration holders (2,172 holders all-time).
- Origin of active registrations: US 3,721, China 2,047, Germany 1,806, Israel 1,047.
- Registration numbering runs chronologically. Each recent numbering band adds about 58–94 first-time holders, so this is a live and growing market.
- Independent regulatory IRHs exist and are paid:
  - "I.L Emergo Israel" holds 134 active registrations for 84 manufacturers.
  - "L.Sh. Marketing & Registration" holds 93 active registrations for 61 manufacturers.
- At $3–10k per manufacturer per year, Emergo's Israeli IRH book would be about $250–840k/yr [Hypothesis: vendor price range × my holder count].

**5. Competitors and complaints.**
- Competitors: Emergo by UL, L.Sh., Freyr (lists Israel registration), and distributors acting as IRH (the default).
- Emergo's own pitch names the pain points of distributor-held registrations: switching distributors, conflicts with a second distributor, sharing design files, and recall conflicts [Verified: emergobyul.com IRH page, 2026-10-13].
- Small consultancies have struggled: Arazy Group holds 11 active registrations (62 all-time), and Medicsense has 0 active (51 all-time).

**6. Entry strategy.**
- Target three gaps:
  - **Price:** flat, published pricing at the low end of $3–10k.
  - **Channel:** white-label IRH for global platforms that lack Israel, such as Pure Global's unpriced "additional markets", and for EU ARs whose clients ask about Israel.
  - **Software:** automated tracking of renewals and reference-approval expiries. AMAR will not register beyond the reference approval's validity, and renewals are due 4 months before expiry, so expiry tracking is a recurring operational job.
- The relevant "first" here is **Class I declaration volume since January 2024 plus the August 2023 import reform**. That is not a first-to-notice edge; the edge is the Israeli entity plus QMS plus AMAR track record.

**7. Acquisition and newcomer outcomes.**
- The channel is partner/white-label, which is the 3–6× channel class in Phase 8.
- Newcomer evidence is poor. Recent service-type entrants: BIOREG SERVICES has 2 active registrations, REGULOG PLUS 3, "Liran Consulting Services" 3.
- Among all 594 holders that first appear in the three most recent numbering eras, only 62 hold 5 or more active registrations and 12 hold 20 or more. Most of those 12 are renamed incumbents (Tzamal, Roche, Solventum, Teva).
- Partner-channel conversion is [Unknown]. No partner terms were checked.

**8. Capital, operations and legality.**
- Requirements:
  - An Israeli Ltd.
  - Likely ISO 9001 certification. Sources conflict: one calls it a legal requirement, another an expectation [Secondary, unverified; search 6]. Certification probably costs several thousand dollars and takes months, so it would likely exceed the $2k budget [Hypothesis].
  - Product-liability and recall exposure as holder.
  - Regulatory-affairs competence, which the founder lacks; he would hire or partner with an RA consultant.
- A business licence and presence in Israel are required (Freyr).
- Time to first sale is about 4–9 months.

**9. Labour.**
- The work is per-file regulatory work (dossier, AMAR portal, vigilance). It is delegable to an RA hire.
- Software can automate monitoring and renewals, but the dossier work scales with hours.
- **Flag: service labour.**

**10. Unit economics.**
- 20 manufacturers × $4k = $80k/yr revenue [Hypothesis].
- Minus a part-time RA contractor (about $30–40k) and insurance and QMS (about $10k), owner profit is about $2.5–3.5k/mo. That is Track A at roughly year 2.
- Track B would need around 150 or more manufacturers, nearly twice Emergo's 84. Unlikely.

**11. Risks.**
- Partners may not outsource Israel. Emergo and Freyr already cover it.
- An ISO 9001 or liability requirement could exceed the budget.
- The Israeli market is small.
- Newcomer IRH consultancies show 0–3 registrations.
- **Decisive unverified assumption:** whether one or more global registration platforms or EU ARs would white-label an Israeli IRH at $1.5–3k per client per year.

---

## C2. Software-leveraged certified payroll-audit practice (Israel)

**1. Concept.**
- A firm that employs ministry-certified wage inspectors ("bodek sachar musmach") to perform the mandatory payroll audits of cleaning, security and catering contractor workers.
- Founder-built software parses payslips and attendance and flags violations, so each certified auditor covers more workers.

**2. Customer.**
- Public bodies and other clients of licensed service contractors, and the contractors themselves, in Israel.
- Employers in security, cleaning and catering "are required to use the services of a certified wage inspector" [Secondary: bizportal.co.il/bizpoint-sponsored/news/article/805418, sponsored, 2026-10-13].
- Government tenders for these audits exist: Accountant General, and NII tender B(1006)2024. The NII tender is a 183-page scanned PDF I could not read [Verified existence only: btl.gov.il, 2026-10-13].

**3. Price.** Per worker or per audit: [Unknown]. I found no price sheet.

**4. Spending and holder evidence (data.gov.il, 2026-10-13).**
- 2,029 certified wage inspectors are registered.
- New registrations by year: 2018: 181, 2019: 525, 2020: 341, 2021: 241, 2022: 221, 2023: 198, 2024: 121, 2025: 118, 2026 YTD: 83. Inflow is falling.
- The auditable base is 2,065 valid "service contractor" licences plus 1,929 manpower-contractor licences (Labour Ministry register, 8,100 rows).

**5. Competitors.** Accounting and payroll firms (BDO and others) with certified staff. 2,029 holders against about 2,000 service contractors suggests heavy supply [Hypothesis].

**6. Entry strategy.** Win public tenders on price, using software leverage to cut the hours per audited worker. This is credible only if tenders are price-weighted.

**7. Acquisition.** Public tenders (mr.gov.il) and direct sales to municipalities. Tender win rates for newcomers: [Unknown].

**8. Operations.**
- The founder cannot sign audits himself. Certification requires a course and exam plus background requirements [Unknown detail; kolzchut 403].
- He would employ certified auditors. There is no capital beyond software.

**9. Labour.** Service labour, flagged. Software only raises auditor productivity.

**10. Economics.** [Unknown] without a price per audit. Track A is possible only with a tender win.

**11. Risks and decisive assumption.** The decisive assumption is that tender prices per audited worker leave margin after auditor wages. The oversupply of certified auditors suggests price pressure.

---

## C3. US multi-state accredited online certificate courses (Texas food handler as the test case)

The ledger has N1 (German food-hygiene certificate, killed) and "licensure exam-prep apps" (Phase 2). This is materially different: a US state-licensed issuing right, not exam prep or an unregulated German employer briefing.

**1. Concept.** Obtain the state licence to issue mandatory certificates online (Texas DSHS food handler; later TABC seller-server and Illinois or California equivalents), and sell automated courses.

**2. Customer.** US food-service employees and employers. Texas requires many food employees to complete an accredited course within 30 days of hire [Verified: dshs.texas.gov licensing-food-handler-training-programs, 2026-10-13].

**3. Price.** $10.00 plus $0.99 processing at StateFoodSafety [Verified: statefoodsafety.com/food-handler/texas, 2026-10-13].

**4. Barrier and holder count.**
- Licence: $600 per 2-year licence for each programme; submit a curriculum and a sample certificate [Verified: 25 TAC §229.178 via law.cornell.edu, 2026-10-13].
- 63 online licensees are listed.
- Licence numbers run to 252, and 20 of the 63 online holders hold numbers of 200 or above. Entry continues [Verified: DSHS online programs list, 2026-10-13].

**5. Competitors.** StateFoodSafety, ServSafe (National Restaurant Association), American Safety Council, 360-style aggregators, and TABC Pronto.

**6. Entry strategy.** None credible on the licence alone. A $600 licence is no moat. The only angles would be enterprise-group billing or language versions, and incumbents already offer Spanish, Mandarin and Vietnamese.

**7. Acquisition.** SEO and Google Ads against entrenched players. CAC is [Unknown]. At $10 a certificate, any paid-click cost above about $2–3 eats the margin [Hypothesis].

**8–9.** Fully automatable, and a fit for the founder. US entity and payments are straightforward.

**10.** Owner profit is [Unknown]. Track A would require ranking organically in a mature SERP.

**11.** This is a commodity with a cheap licence. **Rank: low.** Kept only as a contrast case for the "cheap licence = no moat" finding.

---

## C4. EU MDR/IVDR Authorised Representative for Israeli (and other non-EU) medtech from an EU entity with a contracted PRRC

**1. Concept.** Set up an EU entity (for example an Estonian OÜ), contract a qualified PRRC, and act as the EU AR for non-EU makers, with an Israeli-founder angle.

**2–3. Price.** About $2k/yr flat at tech-enabled players (Pure Global, 3-year contracts) [Verified, 2026-10-13]. Buyer-guide estimates are $6k–22k over 3 years [Secondary].

**4. Holder evidence (EUDAMED API, full pull of 3,003 AR actors, 2026-10-13).**
- 2,657 are active.
- Registrations by year: 2020: 65, 2021: 1,160, 2022: 596, 2023: 308, 2024: 292, 2025: 283, 2026: 299. That is about 290 new ARs a year, many of them captive subsidiaries.
- I identified 105 service-type ARs by name. They hold 3,739 current non-EU mandates. The leaders are Emergo (964), Obelis (586), MedNet (529 plus about 145 in sister entities) and Advena (517).

**5. Newcomer outcomes (the decisive data).**
- Of the 48 service ARs registered 2023–2026, median current mandates = 1.
- 2024 cohort: 8 of 14 have zero. 2026 cohort: 5 of 7 have zero.
- Only Javitech (61), Casus (42) and Transmed (15) reached 15 or more without a global brand or incumbent parent. Freyr (20) and Advena SRL (31) are incumbents' new entities.
- RegulatoryOne OÜ, an Estonian entrant from June 2025, has 0 mandates.
- **Israeli makers are already captured.** 284 IL mandates sit with service ARs, mostly MedNet (179) and Obelis (64), plus Arazy (18). No Israeli-founder gap is visible.

**6. Entry strategy.** None credible. The price floor is already about $2k/yr, and switching costs (re-labelling, technical file transfer) favour incumbents.

**7–9.**
- The PRRC requirement means hiring.
- The AR carries joint and several liability for defective devices under MDR Art. 11(5). The insurance cost of that liability is [Unknown].
- Service labour.

**10.** Track A only after about 30 or more mandates. Newcomer data says the median is 1.

**11. Rank: low.** Kept because it shows that a real licence-type moat protects incumbents, not entrants.

---

## C5. IOSS intermediary for non-EU e-commerce sellers

This is not the excluded "EU €3 duty classification" idea. It is the VAT-intermediary licence, not customs classification.

- **Spending and holders** [Verified: EC "Report on the Application of the VAT E-commerce Package for 2025", 31 Aug 2026, PDF text extracted]:
  - IOSS traders: 8,654 (2022), 10,200, 12,087, 12,799, then 13,733 (2025). Growth slowed to +7%.
  - Intermediaries: 876, 996, 1,231, 1,349, then 1,394. Growth slowed to +3%.
  - IOSS VAT: €7.7bn (+22%).
- About 10 traders per intermediary, and mature players exist (Avalara and others).
- The intermediary is jointly liable for VAT, and some states require guarantees [Unknown per state].
- **Labour:** monthly returns are automatable, which fits the founder.
- **Moat:** EU establishment plus a tax-authority registration. Holder growth is slowing because demand growth is slowing, not because entry is hard.
- **Newcomer outcomes:** [Unknown].
- **Rank: low.** A crowded commodity with liability.

---

## C6. Buying a small business that already holds contracts or licences (German listing data)

This is close to the Phase 6 exclusion "buying offline businesses with seller financing". I tested it only to supply the listing data the brief asked for.

**Data (nexxt-change.org, the German public succession exchange, 2026-10-13).**
- 6,453 active sale listings.
- I parsed 240 of the newest. Asking-price bands:
  - not published: 87
  - up to €50k: 47
  - €50–250k: 48
  - €250–500k: 24
  - €500k–2.5M: 26
  - over €2.5M: 7
- Only revenue bands are published, **no profit figures**. Sub-€50k listings are mostly salons, shops, shell GmbHs and small e-commerce. Licence or contract holders under €50k were rare: one forklift-training provider and a franchise licence. An AÜG temporary-staffing GmbH asks €250–500k.

**Contract-holder test, property management ("Hausverwaltung").**
- 9 relevant listings out of 130 search hits.
- Examples: 650 units at €50–250k asking; 709 units and 800 units at €250–500k (revenue band €250–500k); 1,300 units at €500k–2.5M.
- So management contracts trade at about 1× revenue, roughly €300–600 per unit.

**Verdict: killed on capital.** It needs 25–250× the $2k budget plus on-site management in Germany. Israeli listing data (Yad2 and similar) was not attempted because of blocking risk; data.gov.il medical-tourism XLSX downloads returned 403.

---

## Killed ideas (with evidence)

| Idea | Kill reason (evidence) |
|---|---|
| Israeli notary | Needs 10 or more years as a lawyer. 7,735 active notaries [Verified: data.gov.il "notary" dataset, 2026-10-13] |
| US customs broker licence | Individual broker must be a US citizen; a corporation needs a licensed officer [Verified: 19 CFR 111.11 via eCFR API, 2026-10-13] |
| Israeli food-importer registration as a moat | 3,098 valid registrations. About 1,574 (51%) carry registration numbers of 15,000 or above (the newest bands, max 18,998), so entry is easy. Only 1 "trusted importer" [Verified: data.gov.il fcs-importers, 2026-10-13] |
| Israeli cosmetics RP / "responsible representative" | 68 "RP corporations" (most with recent IDs, including single nail shops) and 525 responsible representatives. Self-serve status, no moat [Verified: registries.health.gov.il CosmeticsBusinesses API, 2026-10-13] |
| Tour-guide refresher-course organiser (Israel) | 38 organisers, about 460 courses a year, median price ₪120, about 20–25 courses per organiser. 13 new organisers since 2024–25. Tiny and effectively capped [Verified: data.gov.il training-courses 2024–27] |
| EU GPSR responsible person / FDA US agent | No licence, so anyone with an address qualifies. Commodity [Hypothesis; not measured] |
| Certified/sworn translation | Ledger exclusion (Phase 2). Israel has no sworn-translator status; the notary route is above |
| Israeli medical-tourism agent registration | Register XLSX blocked (403). Overlaps the dental-tourism and inbound-tourism exclusions |
| Working-at-heights training centre (Israel) | Could not locate the approved-centre list or prices (search 2 returned nothing relevant). Unmeasured, not scored |

---

## Ranking, deep-diligence picks and decisive assumptions

1. **C1 Independent Israel Registration Holder (partner/white-label channel).** This is the only idea with a measurable paying base: 84 manufacturers at Emergo Israel and 61 at L.Sh. Its barrier (an Israeli entity, likely ISO 9001, AMAR competence) cannot be cloned in weeks by foreigners. It is weak on newcomer outcomes (0–3 registrations) and is Track A at best.
   - **Decisive unverified assumption:** global registration platforms or EU ARs will white-label an Israeli IRH at $1.5–3k per client per year. Secondary check: whether ISO 9001 is legally mandatory for the IRH.
2. **C2 Software-leveraged payroll-audit practice.** This is a real mandatory task, but price and tender economics are unknown and the 2,029 certified holders suggest oversupply.
   - **Decisive assumption:** tender price per audited worker exceeds auditor cost by enough for software leverage to create a margin.
3. **C3 US accredited online certificates.** Fully automatable, but the licence is no moat ($600, 63 holders, steady entry) and the price is $10.99.
   - **Decisive assumption:** organic ranking or employer-group deals can be won without paid clicks.
4. C5 IOSS intermediary, low.
5. C4 EU AR, low. Measured newcomer median of 1 mandate.
6. C6 acquisition of contract holders. Killed on capital.

**Top picks for deep diligence:** C1 only. C2 is worth a single price check of a public payroll-audit tender. I do not recommend a third.

**Message to the Research Director.** In category C, the Phase 9 thesis ("obtainable licences beat the 4–6% prior") is largely falsified:
- Where this founder can get the status, so can everyone. The counts of food importers, cosmetics RPs, Texas programmes and payroll auditors keep rising.
- Where the status is hard, as with the EU AR, the 2023–26 entrant cohort shows a median of 1 client and about 6.5% reaching 15 or more clients, which is the same as the open-marketplace base rate.

WebSearch count: **6** (all logged in search-log.txt).
