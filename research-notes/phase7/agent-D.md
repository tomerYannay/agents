# Phase 7 — Discovery Agent D: Niche software, OEM/embedded and white-label supply

Date: 2026-10-13 · WebSearch used: **8 of 8** (logged as P7-D) · All pages below accessed 2026-10-13 unless stated.

## Summary
I tested five ways a software product could be sold through companies that already own the customers:
- OEM components embedded by SaaS vendors;
- country compliance modules;
- licensed data feeds;
- white-label tools for agencies;
- tools bundled by banks.

Only one route has strong transaction evidence from a **small, recent** vendor and a visible gap. That route is a deep, single-platform integration API for a legacy desktop accounting product that has no web API, sold to SaaS vendors and fintechs at a price per connected company.

The proof case is **Conductor**, a QuickBooks Desktop API:
- $42,133 MRR and 271 active subscriptions, Stripe-verified on TrustMRR;
- founded July 2022, with a self-declared one-founder operation.

The UK equivalent, **Hyperext**, claims 2,400+ connected Sage 50 companies and lists five software vendors that resell it.

Sage 50 US and Sage 50 Canada each have a separate, Windows-only SDK. A Conductor-grade self-serve offer for them is not visible:
- Rutter offers Sage 50 only on enterprise contracts.
- Apideck lists Sage 50 as "on radar", not supported.

Country fiscal-compliance APIs (the Verifactu model) clearly pay, but are crowded and need local legal status. Germany's e-invoice APIs are commoditised. White-label tools for agencies and bank calculators have long-standing incumbents or no traction signal.

The Phase 6 lesson still applies: none of these channels hands a newcomer customers. What D1 gets from the vendors is **contracted multiplication**: once one SaaS vendor integrates, every one of its customers who connects becomes a billable unit without new selling.

---

## D1. Deep integration API for Sage 50 US/Canada (and possibly Sage 100): the "Conductor for Sage" (TOP)

1. **Concept.** A hosted, typed REST API (plus SDKs and an MCP server) that reads and writes Sage 50 US and Canada company files through a small Windows agent. It is sold to SaaS vendors and fintechs that must sync with customers still on desktop Sage.

2. **Paying customer and geography.**
   - Buyers: vertical SaaS (field service, construction, wholesale, e-commerce operations), spend-management fintechs, lenders and AI-agent startups in the US and Canada.
   - End users: SMBs on Sage 50 desktop.
   - The vendor pays, and often passes the cost through to its own customer.

3. **Model and price.** Free development and sandbox, then about $39–49 per connected company file per month, with volume discounts.
   - This copies Conductor's public model: $49 per company file per month, no platform fee, billed only for connections called in the past month [Verified: conductor.is and conductor.is/blog/conductor-vs-apideck].

4. **Spending evidence (transaction signals).**
   - **Conductor (QuickBooks Desktop):**
     - TrustMRR, Stripe-verified: MRR $42,133; last-30-days revenue $39,221; all-time revenue $476,137; 271 active subscriptions; founded July 2022, US.
     - The founder's message claims "Completely runs itself", "$350K ARR… growing 7% month-over-month", "Enterprise customers include Ramp" and "virtually no churn". These are vendor claims.
     - Source: [Verified: trustmrr.com/startup/conductor, data updated 2026-10-13].
     - The site claims "Syncing 1,600+ businesses" and shows logos of small SaaS companies such as PalletWiz, Model Wiz, Stak and Groundscale AI [Anecdote/vendor claim: conductor.is].
   - **Hyperext (Sage 50 UK & Ireland):**
     - Claims "2,400+ Sage companies connected" and "1M+ API requests per week".
     - Lists five resellers that are software vendors: Rekki, LiveCosts, UpTick, HireHop and PrintIQ. These are vendor claims, and no pricing is public.
     - It now also markets a "Sage 50 MCP" enquiry route.
     - Source: [Verified page / vendor claim: hyperext.com].
   - **Gap evidence:**
     - Rutter: "The Sage 50 integration is available only to customers with an enterprise contract", with approval and guided onboarding [Verified: docs.rutter.com/platforms/accounting/sage50].
     - Apideck lists Sage 50 and Sage 50 UK as "not yet supported / on radar" (page updated 2026-10-09). Its field guide says Sage 50 US, UK and Canada and Sage 100 have **no official web API** (local COM SDK or ODBC only), with a separate SDK per region [Verified: radar.apideck.com/blog/sage-integration-field-guide, updated 2026-07-14].
     - Supergood: Sage 50 is "version-locked", Windows-only, needs an interactive session and has no OAuth. US install base "materially smaller than QuickBooks Desktop" [Verified: supergood.ai/api-report-card/sage-50].
   - **Weak demand signal from end users:** a Zapier community thread has 5 requests for Sage 50 (2023–Feb 2025). Zapier does not support it [Verified: community.zapier.com thread 22481].

5. **Competitors and what customers dislike.**
   - Codat supports Sage 50 (pricing not public; its pricing URL now returns 404).
   - Rutter: enterprise-only for Sage 50.
   - Supergood: generalist "API for hard software", pricing not public.
   - Apideck: €599/month floor, no Sage 50.
   - Hyperext covers UK only.
   - Conductor could extend to Sage. Its testimonials say older connector vendors DBSync and Commercient are harder to use.
   - What customers dislike is cost floors and enterprise gating for small SaaS vendors. Conductor's whole pitch against Apideck is "€599/month minimum vs $49 per active connection" [Verified: conductor-vs-apideck; written by an interested party].

6. **Entry strategy.** Copy Conductor's positioning (depth on one platform, self-serve, per-connection price, no minimum) for the two regions without a self-serve specialist: **Sage 50 US and Sage 50 Canada**. Treat Sage 100 as a later step.
   - Add an MCP server from day one, because AI-agent startups need write access to SMB books. Hyperext and Sikka already market MCP, which validates the demand direction.
   - Secondary borrowed channel: license the connector to unified-API vendors that list Sage 50 as "on radar" (Apideck) or gate it (Rutter) [Hypothesis: no evidence they buy connectors externally].

7. **Acquisition mechanism and channel evidence.**
   - **Developer search intent.** Typical queries: "Sage 50 API", "Sage 50 SDK REST", "sync X with Sage 50". Then comparison pages, which Conductor runs (vs Apideck), and docs SEO.
   - **Newcomer evidence.** Conductor's Product Hunt launch got 4 upvotes [Secondary: search snippet of producthunt/hunted.space]. Its Ahrefs domain rating is only 26 [TrustMRR]. So its traction did **not** come from launches or audience. It is consistent with search-intent pull from developers who have no alternative [Hypothesis on mechanism; acquisition cost Unknown].
   - **Multiplication.** Each integrated vendor adds billable files as its customers connect. Hyperext's five software resellers show the pattern.
   - **Caveats.** Conductor is one data point, and a successful one (survivor bias). The size of the Sage 50 US/CA market relative to QuickBooks Desktop is smaller, but by how much is Unknown.

8. **Capital, operations and operability.**
   - Capital: under $2k (Windows VMs with Sage 50 trial or licensed copies; Sage Developer Program membership — fee Unknown; the UK SDK requires a paid programme).
   - Ops: onboarding support for the agent on end-customer machines, and redeploying for each annual Sage version.
   - Fully remote, so it can be run from Israel.
   - Legal: SDK licence terms may restrict redistribution [Unknown; must be read before building].

9. **Labour dependence.** Medium. Revenue grows per connected file without new sales, but version breaks and Windows-agent support scale with the install base. Conductor claims it "runs itself" at about $40k MRR [vendor claim].

10. **Unit economics** [Hypothesis, owner profit].
    - Hosting plus support tooling is under $300/month.
    - At $45 per file, 80–120 active files gives about $3.3–5.1k/month owner profit (Track A).
    - Conductor's $42k MRR would require 900+ files at $45, or fewer with enterprise deals.
    - Track B is possible only if Sage 50 US/CA demand is a meaningful fraction of QuickBooks Desktop's [Unknown].
    - Time to traction: Conductor took about 3 years to reach $476k cumulative revenue.

11. **Risks and kill conditions.**
    - Sage ships a supported web API for Sage 50 US/CA.
    - Conductor, Rutter or Apideck adds self-serve Sage 50.
    - The SDK licence forbids hosted resale.
    - Small install base or decline: desktop users migrating to cloud.
    - Support load from a fragile COM/SDO stack.

---

## D2. Single-country fiscal and e-invoicing compliance API for vertical SaaS and POS (Verifactu model)

1. **Concept.** A JSON-in, compliant-record-out API that handles signing, chaining, QR codes, submission to the tax authority and representation forms for one country's mandate. Vertical SaaS and POS vendors embed it instead of building it.

2. **Customer.** Software vendors (salon, gym and booking software, POS, ERP) selling into the mandate country. This includes foreign SaaS entering that country.

3. **Model.** A subscription per taxpayer ID (NIF), which vendors pass through with a margin.
   - Verifacti publishes this logic, including tiered per-NIF pricing, a higher first-NIF price and "€2 per 1,000 extra invoices" above 3,000 per NIF per month.
   - Online signing of representation forms costs €2.90 [Verified: verifacti.com/preguntas-frecuentes].

4. **Spending evidence.**
   - **Verifacti:**
     - Started in 2024 by a two-founder team (Swellbike, Getxo).
     - Named SaaS customers with CTO/founder testimonials: Koibox, Boxify, Xolo and Mekavo [Verified: verifacti.com, /sobre-nosotros].
   - **fiskaly:**
     - Claims "over 1,900 customers" and "active in 1 million POS" across DE, AT, ES, IT, FR, PT, BE and SE.
     - Logos include SumUp, Shopify, Cloudbeds and eviivo [Vendor claim: fiskaly.com/signes/verifactu-for-international-pos].
   - B2Brouter, Quaderno, TeamSystem and Alegra also sell Verifactu APIs [Secondary: search P7-D #1; B2Brouter page verified, no prices].

5. **Competitors.**
   - Spain is saturated: fiskaly, B2Brouter (offers white-label and a startup programme at 100% discount), Verifacti, Quaderno and TeamSystem.
   - Poland: the Ministry of Finance gives free OpenAPI specs plus Java and .NET SDKs for KSeF 2.0, which weakens a paid wrapper [Secondary: search #2].
   - Germany: see the kill list.

6. **Entry strategy.** **None credible identified in this phase.** It would have to be a country whose mandate is in force or imminent and which has no developer-first API. I did not find one with my search budget.

7. **Acquisition.** Developer search plus mandate deadlines. In Spain the deadlines moved to 1 Jan 2027 (companies) and 1 Jul 2027 (self-employed) [Secondary: Holded snippet; sources conflict]. No forum evidence was found of global vendors (Fresha, Square and others) asking for third-party modules (search #6).

8. **Operations.** Often needs local legal standing. Verifacti submits as an AEAT "colaborador social" with its own representative certificate, which a non-Spanish solo founder cannot easily get. Compliance liability toward vendors' customers.

9. **Labour.** Low once built, but rule changes force rework.

10. **Economics.** Per-NIF pricing compounds with vendor growth, so in principle it suits Track B. [Hypothesis] Owner profit Unknown, and depends on finding an uncrowded country.

11. **Kill conditions.** Incumbents (fiskaly's 8 countries, Avalara/Sovos/Pagero) reach the country first; local-entity or certification requirements; deadline slippage, as happened with Verifactu.

---

## D3. Licensed niche data API embedded by other software (data-feed OEM)

1. **Concept.** A clean, normalised feed of hard-to-get data, sold per key to developers who build it into their products.

2. **Customer.** Developers, analysts and vertical apps, globally.

3. **Model.** Tiered monthly API plans.

4. **Spending evidence** (TrustMRR, Stripe-verified, accessed 2026-10-13):
   - **SoldComps** (eBay sold-price API): founded March 2025, Canada; MRR $21,591; 545 subscriptions; plans $0/9/29/79; domain rating 10. Its audience is mostly resellers, not OEM.
   - **BestTime** (venue foot-traffic API): MRR $9,283; 144 subscriptions; "team size 1 person; bootstrapped". The listing says founded May 2025, but the product is older (I believe it dates from about 2020 [Unknown]).
   - **fuelprice.io** (Australian fuel prices): founded August 2025; MRR $828; 12 subscriptions.
   - The dispersion is wide. Note that my TrustMRR sample came from revenue-sorted category pages, so it is an upper-biased sample, not a newcomer median.

5. **Competitors.** These are specific to whatever dataset is chosen.

6. **Entry.** This needs a dataset with clean rights and acute developer pain. SoldComps sells around eBay's API restrictions, which is a terms-of-service risk. I found no specific dataset in this phase, so: "none credible yet".

7. **Acquisition.** Developer search intent, as with D1. SoldComps reached $21.6k MRR in about 18 months with domain rating 10, which suggests search-intent pull without audience [Hypothesis]. This is newcomer evidence, but n=1 and survivor-selected.

8. **Operations.** Cheap. Legal exposure depends on the data source.

9. **Labour.** Low.

10. **Economics.** High margin. Track A is plausible if a dataset is found. Track B is rare.

11. **Kill conditions.** Data-rights takedown, or the source platform opening an official API.

**Note:** D3 is only partly "borrowed distribution". The buyer embeds the data, but there is no multiplication per end customer unless pricing is per seat or per call.

---

## D4. White-label Sage 50 / desktop-accounting connectors resold by vertical SaaS (the Hyperext reseller model)

- **Concept.** The channel variant of D1. Ready-made connectors (for example, job-management SaaS ↔ Sage 50 US) that the SaaS vendor resells under its own brand to its customer base.
- **Evidence.** Hyperext lists Rekki, LiveCosts, UpTick, HireHop and PrintIQ as resellers [vendor claim].
- **Why it might help.** It lets one vendor deal deliver many end customers without the vendor writing code, which is faster than D1's API sale for vendors with no engineers to spare.
- **Weaknesses.**
  - Each connector is part bespoke, which slides towards services.
  - It depends on D1's core being built.
- **Rating.** Treat it as D1's second channel, not an independent business.

---

## Ideas killed (with reasons)

| Idea | Evidence | Why killed |
|---|---|---|
| German XRechnung/ZUGFeRD generation API for software makers | rechnungsapi.de (Finbc GmbH, founded 2018) sells at €0 / €9.99 per month per 100 pages, white-label on request [Verified: rechnungsapi.de/pricing]. Factora sells the same; free open-source libraries and a free KoSIT validator exist. Mandate: issuance for >€800k turnover from 1 Jan 2027 [Secondary]. | Commoditised and cheap; no wedge. |
| On-premise practice-management bridges (dental/vet) for SaaS | Sikka ONE API: 400+ practice-management systems, 47,000+ practices, 100+ apps, MCP server [Vendor claim: sikkasoft.com] | Incumbent owns the category; other verticals untested. |
| White-label infrastructure for agencies | Tarkle on TrustMRR: $1.0M all-time but current MRR $500 with 1 subscription; Stripe key expired, data as of Aug 2026 | No current traction signal; agency channel crowded. |
| White-label financial calculators bundled by banks and credit unions | CalcXML "trusted by hundreds of financial institutions for over 30 years" [Verified: calcxml.com]; KJE/Dinkytown is a long-time incumbent | 30-year incumbents and slow bank procurement. |
| Country payroll/tax calculation engines for global HR vendors | Not researched (budget) | Liability and expertise depth, against large incumbents [Hypothesis]. |
| Accounting-firm-deployed client tools (B2B2B) | Overlaps ledger item "UK MTD white-label for accountants" (weak distribution) | Not materially different. |

## Ranking (my view)

| Rank | Idea | Rough fit |
|---|---|---|
| 1 | **D1 Sage 50 US/CA integration API** (with D4 as its reseller channel) | Track A likely if demand exists; Track B conditional |
| 2 | D3 Licensed niche data API | Needs a dataset; evidence n=2 |
| 3 | D2 Country fiscal API | Spends clearly, but no uncrowded country found; local standing barrier |
| 4 | D4 | Only as a D1 channel |

## Top picks for deep diligence and the decisive unverified assumption

1. **D1.**
   - **Decisive assumption:** enough US/Canadian SaaS vendors need **write** access to Sage 50 desktop, and will pay about $45 per file, to reach 100+ active files within 12–18 months. Equivalently, Sage 50 US/CA's integration demand is at least about 10–20% of QuickBooks Desktop's.
   - **Also verify:**
     - the Sage Developer Program terms (hosted resale allowed? fee?);
     - whether Conductor, Codat or Supergood already sells self-serve Sage 50 US;
     - Sage 50 US/CA install base and trend.
   - Cheap tests within the rules: search-volume tools for "Sage 50 API/SDK" queries; counting Sage 50 integration requests on public SaaS roadmaps and in the Sage developer community.
2. **D3.**
   - **Decisive assumption:** a dataset exists with (a) clean redistribution rights, (b) no official API and (c) developer search demand comparable to "eBay sold prices".
   - SoldComps' $21.6k MRR at domain rating 10 is the evidence that such pull exists.
3. **D2** only if a scan of upcoming 2026–2028 mandates finds a country with:
   - no fiskaly or local developer API;
   - no local-entity requirement for submission.
   - **Decisive assumption:** that such a country exists.

## Searches used: 8 / 8

The queries are logged in research-notes/search-log.txt under P7-D: Verifactu APIs; KSeF API; Sage 50 unified APIs; Sage 50 REST wrappers; XRechnung APIs; Verifactu vendor forums; Conductor acquisition; Sage 50 roadmap requests.

All other evidence came from WebFetch or curl of public pages: TrustMRR startup pages and category pages (developer-tools, fintech, saas, marketing), conductor.is, verifacti.com, b2brouter.net, rechnungsapi.de, hyperext.com, Apideck radar, Rutter docs, Supergood, fiskaly, Sikka, CalcXML and the Zapier community.

Not verified:
- Codat and Supergood pricing (404 or not public);
- Hyperext pricing;
- Conductor's acquisition channel (no disclosure);
- the Sage developer-programme fee;
- Sage 50 US/CA install base.
