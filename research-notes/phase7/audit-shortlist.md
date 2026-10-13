# Phase 7 Evidence Audit of shortlist M1–M12 (P7-AUDIT), 2026-10-13

**Auditor:** independent Evidence Auditor.
**WebSearch:** 6 of 10 used, all logged as `P7-AUDIT` in `research-notes/search-log.txt`. The red team's parallel searches on the Sage SDK, the Sage install base and TSD eligibility were checked first and not repeated.
**Other evidence:** WebFetch, or curl with a generic User-Agent. The SEC request used `research-bot admin@example.com`. No personal identifiers were sent.
**Scratch files:** `scratchpad/p6plus/P7-audit/{data,scripts}`.
- `scripts/shopify_check.py` is an independent re-run of Agent E's data.
- `data/krit2026.txt` is the extracted text of the GKV/ZPP criteria dated 06.01.2026.

**Blocked sources (none bypassed):**
- developer.sage.com and sage.com partner pages: 403 to both curl and WebFetch.
- The gkv-spitzenverband.de PDF: timed out. A Wayback Machine copy captured 2026-03-11 was used instead.
- conductor.is/pricing: 404. Prices were taken from the homepage.
- The ChannelDive Avant article could not be re-opened. The agent's saved copy (`P7-F/data/cad.html`) is a 0-byte file.

## Summary table

| ID | Verdict | Suggested penalty | One-line reason |
|---|---|---|---|
| M1 Sage 50 US/CA API | **Partly supported** | **11** | Conductor's data reproduces exactly, and no self-serve US/CA Sage 50 API exists. But the demand evidence for Sage 50 US/CA is thin, the Sage terms are not public, and two new threats appeared: Apideck lists Sage 50 as "Upcoming", and Conductor is for sale. |
| M2 Data API | **Weak** | **13** | The comparable businesses are real but misread. SoldComps' revenue is a recent spike, its data is scraped, and it sells through Apify and RapidAPI. BestTime is not a newcomer. No dataset has been identified. |
| M3 §20 prevention courses | **Partly supported** | **11** | The 2026 criteria are silent on course language, which neither confirms nor blocks the wedge. The course-leader qualification, the 48-hour expert-reply rule and the 1-year evaluation are now verified. Newcomer outcomes are unmeasured. |
| M4 Texas ESA (TEFA) programme | Weak to partly supported | 12 | Programme scale is verified. Newcomer vendor outcomes and foreign-owner eligibility are unknown. The $30k IEP figure is not on the Comptroller page. |
| M5 Kids'-art fundraisers | Weak | 13 | School shares are verified (US and UK). Whether the target country is free of providers is still unchecked; the UK has at least four providers. |
| M6 Souvenir wholesale | Weak | 13 | Faire is unmeasurable, print-on-demand margins fail at keystone wholesale, and the incumbent markets "hand-drawn by humans". |
| M7 Creator presales | Weak | 13 | The sample of products showing sales counts is biased (6 of 53 pages). No segment Makeship leaves unserved has been shown. |
| M8 Contractor prequalification | Weak | 13 | Spending is forced, but the platform ships its own AI adviser and the one newcomer has no traction. Consultant leads are unmeasured. |
| M9 Pharmacy co-op partner | Weak | 14 | The intake process is verified, but no gap has been identified and funded vendors give tools away free. |
| M10 Technology advisor (TSD agent) | Market supported; newcomer case weak | 12 | The 10-K figures reproduce. Foreign-advisor eligibility is unknown after two searches. The 12–22% commission figure is unverified. |
| M11 Payments-residual agent | Unsupported | 14 | No residual split, newcomer or adoption data. |
| M12 Shopify partner studio (Israel) | **Supported** (measurement), with caveats | **10** | Every directory statistic replicates exactly. Revenue-share terms are verified. The base is listed partners only, and the success cases are concentrated in Brazil. |

---

## M1. Sage 50 US/Canada integration API (most important)

### Verified
- **Conductor's TrustMRR listing** [Verified: trustmrr.com/startup/conductor; Stripe API key; MRR synced 2026-10-13 08:25]:
  - MRR $42,133; last 30 days $39,221; all-time $476,137; 271 active subscriptions;
  - founded 2022-07-31; US; 95% profit margin; `cofounders: []`; domain rating 26.
  - **All match the agent's figures.**
- **New: Conductor is listed for sale.** First listed 2026-03-06. The asking price was $1.0M in Dec 2025 and **$1.25M from 2026-06-03**. There are 24 offers, and TrustMRR shows a "multiple" of 2.66. [Verified: same page's embedded data]
  - The founder's seller message ("$350K ARR today, growing 7% MoM") is **stale**. The current Stripe run-rate is about $505k ARR, and MRR grew 8.9% in the last 30 days.
- **Conductor's pricing and scope** [Verified: conductor.is homepage, 2026-10-13]:
  - $49 per company file per month; free for development; enterprise volume pricing.
  - "Syncing 1,600+ businesses" (vendor claim).
  - **QuickBooks Desktop and Enterprise only.** No Sage, Xero or "coming soon" items on the site or in the docs index.
- **Rutter:** "The Sage 50 integration is available only to customers with an enterprise contract", with a desktop connector and guided onboarding. The page names no regions. [Verified: docs.rutter.com/platforms/accounting/sage50]
- **Codat:** the connector is "Sage 50 Accounts (UK & Ireland)" only. The overview lists "Sage 50 (UK)". [Verified: docs.codat.io/integrations/accounting/sage50/accounting-sage50/ and /overview/]
  - **Correction:** the agent wrote "Codat supports Sage 50". In fact Codat has **no US/CA coverage**. This strengthens the gap claim.
- **Merge:** its accounting list has no Sage 50, Sage 100 or QuickBooks Desktop. [Verified: docs.merge.dev accounting overview]
- **Hyperext:** "the only real-time REST API built specifically for Sage 50 UK & Ireland", with 2,400+ companies, 1M+ requests a week, 95 endpoints and an MCP server. These are vendor claims, and there is no public pricing. **UK & Ireland only.** [Verified: hyperext.com]
- **Sage 50 Cloud** is "Sage 50 as you know it, hosted on a virtual machine". It is UK only at launch, and third-party integrations are not supported at launch. [Verified: hyperext.com news post, about Aug 2026]
  - It is not a threat to US/CA. It is a medium-term risk for the UK analogue.
- **Supergood report card:** no REST API, the Windows-only COM library (SDO) is version-locked, and access is "gated behind Sage Developer Program approval; documentation, certification, and support are paywalled".
  - "In the U.S. it is materially smaller than QuickBooks Desktop in installed base" (no figure given).
  - The page's "A+" grade contradicts its own text, so treat it as auto-generated. Supergood sells custom "Get an API" builds, so it is a potential bespoke competitor.
  - [Verified: supergood.ai/api-report-card/sage-50]
- **Developer-ecosystem health (US).** A Sage 50 US development partner since 2007 posted "Why developers are abandoning Sage 50 U.S.":
  - Sage 50 US runs on .NET 4.7 (end of support) and is 32-bit only;
  - the API is painful (re-authorisation on every change);
  - ISV apps in the marketplace are declining;
  - his "no change" follow-up was about 6 months ago, and no Sage staff replied.
  - [Verified: communityhub.sage.com/us/sage50_us/f/software-development-kit-sdk/252074] This cuts both ways: little competition, but a shrinking ecosystem.
- **Demand signals (all anecdotal):**
  - Zapier thread: 4 "+1"s plus the original post, Mar 2023 to Feb 2025. Zapier does not support Sage 50cloud. [Verified: community.zapier.com thread 22481]
  - A Canadian construction SaaS founder asked Sage for a developer licence to integrate with Sage 50 CA as a "cash-strapped startup". The Sage-side reply: there is a yearly fee, and there are no test copies unless enrolled. [Verified: communityhub.sage.com/ca/sage_50 thread 227809, about 2+ years old]
  - In a vendor scan, field-service tools mostly integrate with QuickBooks only: Field Promax with QBD/QBO, Jobber with QBO only. One (FieldCentral HindSite) syncs QBD, QBO and Sage 50. [Secondary: search P7-AUDIT #2 snippets]

### Contradicted, overstated or needing correction
1. **"$49 per company file" does not explain the revenue.** 271 subscriptions at $42k MRR is about $155 average per subscription. Subscriptions are therefore vendor accounts, not files; billable files are about 860 at list price, or fewer with enterprise deals. This matters for M1's Track A arithmetic: "80–120 files" means perhaps only **10–30 paying vendors**. Each one is a B2B developer sale.
2. **"Solo founder."** The page shows no cofounders and no team size. It is consistent with a solo founder but not proven. "Completely runs itself" is a seller's claim made while the business is listed for sale.
3. **"Codat supports Sage 50"** should read "UK & Ireland only".
4. **"Apideck: on radar".** Apideck's integration page now says "**Upcoming** Sage 50 Accounting API integration… Request access when this integration launches". The region is not stated. [Verified: apideck.com/integrations/sage-50, 2026-10-13] This is a stronger competitive signal than "on radar".
5. **The traction mechanism** ("search-intent pull, not launches") is still a hypothesis. TrustMRR lists no marketing channels for Conductor.

### Unknowns that matter
- **Sage programme terms.** Verified only in outline: application and approval, a programme agreement, sign-up plus annual fees, and no test copies without enrolment. [Secondary: Sage NA Tech Partner Program PDF via search snippet; the PDF itself is 403; community posts]
  - The fee amount is unknown. A 2020-era post says $350 first year and $250 renewal (stale).
  - **Whether the agreement allows a hosted third-party API resold to other vendors is not public.** This remains a potential hard blocker.
- **Sage 50 US/CA installed base.** No official split exists. (The red team's search found only vendor-derived global figures.)
- Whether Apideck's "Upcoming" covers US/CA, and its timing.
- Whether a buyer of Conductor would extend it to Sage 50.

### Weakest load-bearing assumption, tested
"Sage 50 US/CA integration demand is at least about 10–20% of QuickBooks Desktop's."

- The evidence points **below** that range. US Sage 50 is "materially smaller", developers report leaving the SDK, a sample of SaaS vendors integrate with QuickBooks and skip Sage 50, and public request counts are single-digit.
- Not disproven: there is no market-size figure.
- Implication: Track A needs about 10–30 paying vendors (see correction 1). That is plausible but slow; Conductor took about 3 years. Track B on US/CA alone is doubtful.

### Rubric concerns
- **Spending evidence.** Conductor is a strong and verified analogue, but for a different, larger platform. Credit 3/5, not 4–5.
- **Proven channel.** n=1 and survivor-selected, and the mechanism is unknown. At most 2/5 under the Phase 5–6 standard.
- **Defensibility.** Apideck "Upcoming", Rutter enterprise and the for-sale Conductor could all add Sage 50 US/CA quickly. 1–2/5.
- **Speed to first sale.** Slow: a developer B2B sale, a Windows agent, Sage enrolment first. 2/5.
- **Labour.** Windows-agent support and the annual version lock add labour. 2–3/5.
- **Penalty 11.** The core numbers are verified, but the gating terms and the size of demand are unknown.

---

## M2. Licensed niche data API

### Verified (TrustMRR, Stripe, 2026-10-13)
- **SoldComps:** founded 2025-03-28; Canada; MRR $21,591; 545 subscriptions; DR 10; not for sale.
- **BestTime** (slug `private-location-intelligence-api-platform`): MRR $9,283; 144 subscriptions; team size "1"; bootstrapped.
- **fuelprice.io:** founded 2025-08; MRR $828; 12 subscriptions; DR 29.

### Overstated
1. **SoldComps "reached $21.6k MRR in about 18 months".** All-time revenue is only **$49,013**, and MRR grew 40.7% in the last 30 days. Most of the revenue is from the last few months, so this is a **recent spike**, not a steady ramp, and durability is unknown.
2. **"Search-intent pull without audience".** SoldComps' footer says it is "Also on Apify Actor [and] RapidAPI". It distributes partly through API marketplaces, which Phase 5 showed rarely pay newcomers. Its footer also says "Data sourced from publicly avail[able]…", i.e. **scraped eBay data**, so the terms-of-service risk is concrete. [Verified: sold-comps.com]
3. **BestTime as newcomer evidence.** "Founded May 2025" contradicts DR 45 and all-time revenue of $133.7k. It is an older product, and it is **for sale (asking $599k)**. It is not newcomer evidence.

### Unknowns and weakest assumption
- There is no candidate dataset with clean rights. The comparable businesses that succeed (SoldComps, eBay) depend on data they have no right to resell.
- Weakest assumption: a dataset exists that is legally resellable *and* has no official API. That is untested.

### Rubric concerns and penalty
- Distribution should not be credited: the channel is a marketplace plus search, n=1.
- Defensibility: 1.
- **Penalty 13.**

---

## M3. §20 SGB V certified online prevention courses, foreign-language wedge

### Verified
**From the GKV "Kriterien zur Zertifizierung von Kursangeboten…" (Stand 06.01.2026, Chapter 5)** [Wayback copy 2026-03-11 of the gkv-spitzenverband.de PDF; text in `data/krit2026.txt`]:

- **Language.**
  - The document contains **no rule on course language**. The only matches for "Sprach" are "Rücksprache", and "deutsch" appears only in DGE references.
  - The ZPP FAQ explicitly allows foreign languages only for **Chapter 7** digital offers, with a translator's confirmation.
  - For Chapter 7 the FAQ also says "Leichte Sprache"/Gebärdensprache are "aktuell keine Verpflichtung". [Verified: zentrale-pruefstelle-praevention.de/faqs/anbieter/]
  - **So for Chapter 5 IKT courses the rules are silent. They neither prohibit nor permit a foreign language. The agent's statement is accurate.**
- **IKT courses need a real course leader with a guideline-conformant qualification.** The qualification is a state-recognised professional or university qualification, with documented competences.
  - Foreign degrees need a German equivalence recognition (Gleichstellungsanerkennung) plus a certified translation.
  - Exception: EU-acquired Bachelor/Master degrees in "Psychology" and "Sport Science" need none.
  - Implication: a Russian-, Ukrainian-, Turkish- or Arabic-speaking EU psychology or sport-science graduate could qualify without recognition. That is relevant to the wedge.
- **Online-course rules:**
  - 8–12 units of 45–90 minutes;
  - a **communication quota of at least 24 minutes per participant**;
  - **expert answers within 48 hours**;
  - modules unlock sequentially;
  - **100% completion required for reimbursement** (80% for live seminars);
  - a full test account must be provided;
  - movement and relaxation content needs video or audio, not text only (FAQ);
  - certification for **1 year only**, then an evaluation to extend by 2 years.
- **Provider location.** The FAQ says only that a mismatch between course venue and provider seat "ist unerheblich" (courses are searched by postcode). No seat-in-Germany rule was found in the criteria. Treat this as not blocked, but it is not an explicit permission for a provider based outside the EU.
- **ISO 27001 (ISMS).** It applies to Chapter 7 digital offers (deadline 01.01.2025), not to Chapter 5 IKT courses. This keeps Chapter 5 cheaper. [Verified: ZPP FAQ]
- **Insurer coverage.** The cooperating insurers are all Ersatzkassen, most BKKs, 11 AOKs, several IKKs, Knappschaft and SVLFG. [Verified: ZPP FAQ]
- **Market statistics:**
  - about 115,000 certified offers, almost 65,000 providers, about 45,000 certified in 2025, and about 1.9M insured people supported in 2024 [Verified: vdek PR 2026-01-21];
  - "73% Präsenz / 27% online" refers to **courses**, not participants [Verified: zm-online 2025-11-27]. The agent's "about 500k online participations" is therefore a hypothesis, as the agent flagged.

### Not verified
- "€243M on individual prevention courses in 2025": only a snippet; the zm-online article gives only €686M for all prevention.
- "TK up to €100": from the agent's secondary source; not re-opened.

### Weakest assumption, tested
- The language question is still not resolved, but it is **less likely to be a hard blocker** than feared, because the rules are silent rather than prohibiting it.
- The real load-bearing unknowns are now:
  1. whether ZPP reviewers accept non-German Stundenverlaufspläne (lesson plans) and course materials without the Chapter 7-style translator route, which the founder can only learn by applying;
  2. **whether insurers' course search lets foreign-language speakers find the course** (the search is by postcode and topic, not by language);
  3. CAC.
- The 24 minutes per participant plus 48-hour expert replies make delivery labour scale with volume, which caps operating leverage.

### Rubric concerns
- Independence from founder labour, and leverage: no higher than 3, because of the communication quota and qualified-expert replies.
- Proven channel: the database listing is a directory with no newcomer data, so 1–2.
- **Penalty 11.**

---

## M4. Texas TEFA ESA-funded programme for IEP students

- **Verified:**
  - "nearly 73,000" accounts funded on 1 July;
  - ">54,000 approved products and services from nearly 2,400 vendors";
  - vendors "will not be charged fees to list, buy or sell";
  - homeschool award $2,000.
  - [Verified: comptroller.texas.gov PR 2026-06-30]
- **Vendors "must have the right to transact business in Texas".** Online and out-of-state providers are allowed "if the provider applies and is accepted". [Verified: educationfreedom.texas.gov/providers-vendors]
- **Not on the Comptroller page:** the "up to $30,000" IEP amount. It stays [Secondary: Outschool page].
- **Arizona concentration** (Amazon about two-thirds; Outschool $12M of $30M): ABC15, not re-opened.
- **Unknowns:** newcomer vendor order distribution (decisive), foreign-owned LLC eligibility, background-check rules.
- **Penalty 12.**

## M5. Children's-artwork keepsake fundraisers in an unserved country

- **Verified:**
  - Square 1 Art: "Standard profit is 33% (with the possibility to make up to 38%)" (qualifications apply), with the profit check 10–14 days after completion. It makes **no school-count claim on that page.** [Verified: square1art.com/plan-a-fundraiser]
  - My Child's Art 20% (agent-verified PTA listing).
- **New:**
  - The UK has at least four providers: a search also surfaced **School Fund Prints** on pta.co.uk.
  - A German-language search returned only UK/US results, so German, Dutch and Israeli competition is still **unknown, not absent**.
- **Weakest assumption** (no provider in the target country, and ≥20% parent participation): completely untested.
- **Penalty 13.**

## M6. Per-location souvenir lines (wholesale)

- Lantern Press SKU count and Printful base costs were agent-verified; not re-run.
- Faire is blocked (403), so newcomer wholesale traction cannot be measured.
- Print-on-demand economics fail at keystone, so short-run inventory is needed. That pushes against the $2k budget and the Israel logistics constraint.
- **Penalty 13.** Agent B's own conclusion stands.

## M7. Creator presale merch

- The Makeship MOQs were verified by the agent.
- The sold counts (215–1,098) come from 6 of 53 pages, an upward-biased sample.
- Creator acquisition is founder outbound against an incumbent that now signs large licensed IP.
- **Penalty 13.**

## M8. Contractor prequalification service

- Contractor counts come from one inconsistent third-party page.
- "$5k/yr consultants" is PrequalPilot's marketing claim.
- Avetta's own AI "Safety Advisor" is verified.
- The only AI newcomer shows 6 Product Hunt views.
- Not re-opened.
- **Penalty 13.** Directory listings are not credited as a channel.

## M9. Pharmacy co-op preferred partner

- **AAP intake re-verified:** form; "allow us up to two weeks"; call; "formalized proposal"; agreement. **No fees** are stated on the page, and no member count is given there.
- No uncovered task has been identified, and Nimble is free to IPC members.
- **Penalty 14.**

## M10. US technology advisor under a technology services distributor (TSD)

- **Verified** [ScanSource 10-K FY2026; sec.gov/Archives/edgar/data/918965/000091896526000044/scsc-20260630.htm]:
  - Intelisys net billings "approximately $2.88 billion, an increase of 3.2%";
  - Intelisys & Advisory net sales $101.13M (+3.1%; **+2.3% excluding acquisitions**);
  - gross margin 98.6%; operating income $28.6M;
  - contracts with "more than 200" carriers and cloud providers.
- **Corrections:**
  - The segment includes **Advisory** (end-user consulting, Resourcive acquired Aug 2024), so it is not pure Intelisys.
  - Net sales are about 3.5% of billings: the TSD books net revenue, and advisor commissions sit outside it.
  - Organic growth is 2.3%.
- **Telarus:** "no upfront fees to become a Telarus advisor"; apply via a form, contact within 1 business day [Verified: telarus.com/become-advisor]. **No eligibility, residency or W-9 rule is published.** My search and the red team's search both failed to find foreign-advisor terms, so this stays [Unknown].
- **Not re-verified:**
  - Avant's commission-advance programme (ChannelDive): the URL was not recorded and the agent's saved file is empty, so treat it as [Secondary].
  - "12–22% commissions": snippet only.
- **Weakest assumption:** that a remote, non-US newcomer closes deals in the first 12 months. There is no data on it.
- **Penalty 12.**

## M11. Payments-residual agent for small vertical-software vendors

- No split data, no newcomer data and no adoption data.
- The broker's attrition table is a vendor claim.
- The risk of unpaid integration work is unmitigated.
- **Penalty 14.**

---

## M12. Israeli Shopify launch/migration partner studio (with Brazil/Türkiye and Odoo variants)

### Replication
I ran my own script, `P7-audit/scripts/shopify_check.py`, on Agent E's saved `*_prof.json`. All 507 profiles parsed with no errors.

| Check | Result |
|---|---|
| Listed partners | IL 38 / PL 40 / BR 57 / MX 82 / TR 68 / DE 222 = 507 ✔ |
| Zero-review share | IL 47%, PL 60%, BR 46%, MX 39%, TR 44%, DE 53% ✔ |
| Partners since 2024 | n=89; 60 with zero reviews (67%) ✔; median 0 ✔; 8 with ≥10 lifetime ✔; 9 with ≥5 in the last 12 months ✔ |
| Same, by country | IL 1/5, PL 1/13, BR **5/16**, MX 0/6, TR 2/20, DE 0/29 ✔ |
| Registered tier | 225 (44%) ✔. Registered-tier newcomers: 55, of which 34 have zero and 6 have ≥5 in 12 months ✔ |
| Partners since before 2020 | 155; median 3; 39% zero ✔ |
| Reviews in last 12 months, Israel | ≥59 ✔ |

The newcomer success list matches. The IL case, "SEDER Studio", is handle `jonathan-siag`: Select tier, 41 reviews, 9 in the last 12 months.

**Revenue-share terms re-verified** [help.shopify.com/en/partners/help-support/faq/earnings, 2026-10-13]:
- From 10 Aug 2026: 20% of base subscription plus 0.1% of net eligible online GMV, for 4 years.
- Plans: Basic, Grow, Advanced and Plus. Starter and Lite are excluded.
- B2B is excluded; GMV is capped at $100M a year.
- Before that date: 20% perpetual for Basic, Grow and Advanced, with no GMV share.
- The share cannot be split. Launch Partner status cannot be transferred without Shopify's consent.
- **Condition:** the partner must have **built the development store and transferred it**. Plus co-sell deals need a statement of work (SOW) before close.

### Overstated or caveats
1. **The denominator is listed partners only.** Registered-tier listing is discretionary ("a limited number"). The "1 in 7" rate (9 of 60 outside Germany) applies to newcomers who were **already admitted** to the directory, not to all new partners. The founder's real odds start with an unknown listing probability.
2. **Concentration.** Brazil supplies 5 of the 9 newcomer successes. The Israel figure is n=5 with 1 success. Treat the Israel-specific rate as unknown.
3. **A review is not a job of known size.** Israeli listed starting prices have a median of $150. Average job value in Israel: [Unknown].
4. **The revenue share only applies to stores the partner builds and transfers.** Re-platforming an existing Shopify merchant earns nothing. On Basic (about $39/month), 20% is about $94 a year. The 0.1% GMV share matters only for larger stores. The agent's figure of about $150–400 a year per store is optimistic for typical Israeli small and medium merchants [Hypothesis].
5. **Re-registration.** The agent's own caveat stands: some 2024 "newcomers" are re-registered agencies. I did not check company founding dates.

### Weakest assumption
A new Registered-tier Israeli partner gets listed and reaches 2+ jobs a month at ≥$2k each within 12 months. Untested: the listing rule, Israeli job values, and SEDER's prior client book are all unknown.

### Rubric concerns
- **Proven channel.** This is the best-measured newcomer channel in Phases 5–7, and it deserves real credit (3/5) for a market like Brazil. For Israel specifically, 2–3.
- **Labour and leverage.** This is a services business. Leverage is no higher than 2–3, and it is close to the ledger's L3 "agency drift" exclusion. The Director must rule on whether it is a repackage.
- **Recurring.** The annuity is real but small for small stores: 2/5.
- **Penalty 10.** The evidence is strong and replicated; the remaining risk is in interpretation.

---

## Opinion on the Phase 7 leader re-check (audit-leaders.md)

- **UK MTD (52.6 → 49.2).**
  - I spot-checked the core fact on rossmartin.co.uk: 570k signed up, 436k first updates by 7 Aug 2026, 864k in scope, penalty points from 6 Apr 2027, £30k threshold from Apr 2027. It reproduces.
  - The defensibility cut (−3) and the proven-channel cut (−6) are justified.
  - **The penalty rise from 10 to 11 partly double-counts.** The same evidence (Outbooks, QX, the Sage agent, ANNA) already drives the defensibility cut. I recommend **penalty 10 → 50.2**.
  - The difference is inside the noise band either way.
- **J1 memoir books (51.0 → 48.6).**
  - Reasonable. MyStories' added voice, QR codes and 10 languages, plus a Hebrew UI test flag, justify defensibility −1.
  - The proven-channel cut applies the Phase 5–6 standard consistently.
  - Correctly, the auditor did not also cut market depth for the weaker Russian gap.
- **H10 ketubot (50.6 → 49.4).**
  - The direction is defensible. But the cut rests on one newcomer (Love Letters) plus snippets, because Etsy was blocked. It is weak evidence for a 6-point move.
  - I would accept it only because Phase 3's credit was itself incumbent evidence. The cut reverses an over-credit; it is not a new negative finding.
- **General.**
  - The baselines are reconstructions that reproduce the totals, so only the deltas are meaningful, and the auditor said so.
  - All three end at about 48.6–50.2. That is inside the ±5 noise band of the M-candidates, so the board stays flat.

## Cross-cutting notes for rescoring
- **Two of the "small vendor" comparables are for sale:** Conductor at $1.25M and BestTime at $599k. Sellers' self-descriptions ("runs itself", "solo") should be treated as sale marketing. Listing for sale also means Conductor could gain a well-capitalised owner who adds Sage.
- **The TrustMRR comparables' "founded" dates are self-entered.** Check all-time revenue against MRR before calling a business a newcomer (SoldComps, BestTime).
- **M1 and M12 are the only candidates whose core numbers replicated from primary data.** M3's regulatory question moved from "possibly blocked" to "silent, so test by applying".
- **Searches used: 6 of 10** (P7-AUDIT).

### Sources (accessed 2026-10-13 unless noted)
- trustmrr.com/startup/{conductor, soldcomps, fuelprice-io, private-location-intelligence-api-platform} · conductor.is · docs.conductor.is
- docs.rutter.com/platforms/accounting/sage50 · docs.codat.io/integrations/accounting/sage50/accounting-sage50/ and /overview/ · docs.merge.dev (accounting overview)
- apideck.com/integrations/sage-50 · apideck.com/integrations/quickbooks-desktop · hyperext.com · hyperext.com/sage-50-news/sage-50-cloud-what-we-learned-from-sages-pre-launch-webinar/ · supergood.ai/api-report-card/sage-50
- communityhub.sage.com threads 252074 (US SDK) and 227809 (CA developer licence) · community.zapier.com thread 22481 · sold-comps.com
- gkv-spitzenverband.de "Kriterien … Kapitel 5 Stand 06.01.2026" (Wayback 2026-03-11) · zentrale-pruefstelle-praevention.de/faqs/anbieter/ · vdek.com PR 2026-01-21 · zm-online.de 2025-11-27
- comptroller.texas.gov PR 2026-06-30 · educationfreedom.texas.gov/providers-vendors · square1art.com/plan-a-fundraiser · rxaap.com/become-a-preferred-partner
- sec.gov ScanSource 10-K FY2026 · telarus.com/become-advisor · help.shopify.com/en/partners/help-support/faq/earnings · rossmartin.co.uk/sme-tax-news/9073
- Blocked: developer.sage.com and sage.com partner pages (403); gkv-spitzenverband.de (timeout); conductor.is/pricing (404); the ChannelDive Avant article (not re-located).
