# Phase 8 — Discovery Agent F (contrarian, negative space, emerging)

Date: 2026-10-13. Search label: P8-F. **WebSearch used: 7 of 7** (all logged in `research-notes/search-log.txt`). Everything else came from WebFetch or curl of public pages and public APIs: the NuGet search and registration APIs, the npm registry and downloads APIs, Apideck's public radar and country pages (34 country pages pulled), unified.to's integration index and pricing, Codat docs, Rutter, Chift, Agave, Supergood, TrustMRR (Conductor), Tally, CONTPAQi, H-ERP (Hashavshevet), ClearTax, AR Software / GitHub, and the Shopify community. Scripts and downloads are in the scratchpad under `p6plus/P8-F/`.

## Headline (read first)

1. **The Conductor pattern generalises only weakly. It is also being copied fast.**
   - **The new finding:** at least **three QuickBooks Desktop API clones launched in 2026**, all after Conductor's revenue became publicly visible:
     - Nxus (npm SDK created 2026-04-10).
     - TenkeyBridge (2026-09-11).
     - Desktop Accounting API (2026-10-06). It **copies Conductor's price exactly**: $49 per active company file per month, no minimum.
     - All three: [Verified: npm registry; desktopaccountingapi.com/pricing, 2026-10-13].
   - **Their pull so far:**

     | SDK | npm downloads, last month |
     |---|---|
     | Conductor's `conductor-node` | **53,125** |
     | Desktop Accounting API (SDK + MCP package) | 1,636 + 1,640 |
     | TenkeyBridge (client + MCP) | 687 + 629 |
     | nxus-qbd | 282 |

     [Verified: api.npmjs.org, 2026-10-13]
   - **What that means:** the Phase 5 lesson (AI-built supply floods any visible opportunity) now applies to integration APIs too. A newcomer's advantage in a "missing-capability" niche lasts only until the niche's revenue is visible. The niche is not a durable negative space.
   - **The same threat applies to M1.** "Desktop Accounting API" is a generic, multi-product name. It could add Sage 50 next [Hypothesis].
2. **Most closed or legacy systems with many business users are already covered, gated or vendor-integrated.** Only a few non-English desktop accounting systems remain without any self-serve per-connection API. The strongest:
   - **CONTPAQi (Mexico):** claims 1.2M user companies [vendor claim]. No official API was found. Apideck has it only "on radar".
     - A one-person Mexican developer, AR Software, already sells a CONTPAQi Comercial API licence at **$720/year per RFC** (Mexican taxpayer ID) [Verified: GitHub README].
     - Its sales volume is [Unknown].
   - **TallyPrime (India, GCC):** claims 2.7M businesses, 65k of them in the UAE [vendor claim]. It has no cloud API, Zapier or Make support [Secondary: aiaccountant.com].
     - Unified.to covers it, but with a **$750/month minimum** [Verified]. Apideck has it "on radar".
     - But big Indian vendors (ClearTax, Vyapar) build their own Tally connectors, and Tally is modernising itself (it is going after UAE e-invoicing provider accreditation).
   - **Elsewhere:**
     - **Japan (Yayoi, PCA, OBIC, TKC) and Korea (Douzone):** uncovered, but the language makes them infeasible for this founder.
     - **South Africa (Sage Pastel / Evolution):** uncovered, English-speaking, but evidence is thin.
     - **Europe:** largely covered by Chift (€10.5M Series A) and by unified.to / Apideck (DATEV, EBP, Cegid, Lexware Office).
     - **Construction on-prem ERPs:** Sage has named hh2 its single authorised integration platform, and Sage's developer licence key is needed on every request.
     - **Dental/vet:** already excluded in the ledger.
3. **Negative space, where newcomers actually outperform.** Across about 30 channels measured in Phases 5–7, plus this phase's data, newcomers did relatively well in exactly three situations:
   - (a) **A capability searched for by developers with no self-serve supplier** (Conductor). The window is temporary.
   - (b) **Mid-size non-English service markets.** In the Shopify Partner Directory, 5 of 16 Brazilian newcomers had 5+ reviews in 12 months, against 0 of 29 in Germany.
   - (c) **Buyers sitting below an incumbent's minimum price.** Apideck's minimum is €599/month, unified.to's $750/month, Rutter is enterprise-only, and Conductor wins small SaaS at $49 per connection.
   - **Non-software:** the only model with *measured* newcomer outperformance is **services sold through a directory in a mid-size, non-English market** (Brazil). The "below-the-minimum" non-software analogue (a low-MOQ broker, K6) was already tested and scored 43.0.
4. **Recommendation.**
   - Treat Conductor-type APIs as a **portfolio of short first-mover windows**, not one durable business.
   - **CONTPAQi** is the best new window: no unified-API coverage, an incumbent selling a licence rather than a hosted API, and a large installed base.
   - The decisive unknowns are: does any SaaS or fintech pay for CONTPAQi write access at about $40–50 per company, and do CONTPAQi's SDK terms allow a hosted resale?
   - Because cloning is fast, **keep revenue unpublished** (no TrustMRR) and build defensibility from things AI cannot clone in weeks: signed partner agreements, the installed agent base, local-language support, and tax-format know-how (CFDI).

---

## Part 1. Does the Conductor pattern generalise? System-by-system census

**Method.**
1. Took Apideck's public country pages for 34 countries (the "notable local systems not yet supported" lists). This works as a systematic negative-space dataset, because Apideck writes these pages to capture developer search demand.
2. Cross-checked coverage against Codat docs, Rutter's integrations page, unified.to's index (grepped from HTML), Chift's homepage and Agave.
3. Used **NuGet and npm package downloads** of community wrappers as a rough proxy for developer integration demand.
   - Calibration point: Conductor's SDK gets 53k downloads a month at $42k MRR.
   - Download counts include CI and bot traffic, so they show order of magnitude only.

### 1a. Coverage matrix (accounting / ERP; ✔ = live connector; ✘ = not listed)

| System (market) | User-base evidence | Official/public API | Unified-API coverage | Self-serve per-connection API? | Developer-demand proxy | Legal / gating | Verdict |
|---|---|---|---|---|---|---|---|
| QuickBooks Desktop (US) | ~4M users [Secondary, P7 log] | qbXML SDK, Web Connector | Codat ✔, Rutter ✔, Apideck ✔, unified.to ✔ | **Yes: Conductor + ≥3 2026 clones at $49** | QbSync NuGet 232k; conductor-node 53k/month | Intuit SDK open | **Saturating** |
| Sage 50 US/CA | P7: smaller than QBD | 32-bit SDK via Sage developer partner programme (DPP) | Rutter (enterprise), Apideck "upcoming" | No | Nothing visible on npm/NuGet for the US edition | DPP resale terms unknown | **M1: in ledger, not resubmitted** |
| Sage 50 UK/IE | — | SData discontinued | Codat ✔, Chift ✔ | Hyperext (vendor-claimed 2,400 cos.) | CData.Sage50UK 27k | — | Covered |
| Sage 100 / 300 (US) | Mid-market ERP | Sage 100 ODBC/BOI; 300 Views | unified.to lists Sage 100; Apideck radar | Not found | — | DPP | Partly covered; M1 lists Sage 100 as an extension |
| Sage 300 CRE, Foundation, Vista, ComputerEase (US construction) | — | Sage 300 CRE Web API runs on IIS on the customer's server; DPP licence key needed per request [Secondary: Nango docs snippet] | Nango connector; Agave pivoted to contractor fin-ops, and its ERP connectors now show "coming soon" [Verified: useagave.com] | Not found | — | **hh2 named Sage's "single authorised integration platform" for Sage CRE** [Secondary: snippet; hh2.com unreachable] | **Gated: kill** |
| Microsoft Dynamics GP | Large, but retiring | eConnect | CData drivers | — | VSToolsSDK 55k, CData 52k | Microsoft partner channel | Migration market crowded with Microsoft partners: kill |
| **TallyPrime / ERP 9 (India, GCC, Africa)** | "Nearly 2.7M businesses" [Verified: tallysolutions.com/integration; vendor claim]; "over 65,000 UAE businesses" [Verified: Tally MENA page] | XML/JSON over HTTP on local port 9000; ODBC is read-only; no cloud API, webhooks, Zapier or Make [Secondary: aiaccountant.com] | **unified.to ✔ ("New"), $750/month minimum** [Verified]; Apideck radar; Codat ✘; Rutter ✘ | **No self-serve per-connection offer found** (2 searches) | TallyConnector (OSS) 23.7k NuGet; CData.Tally 13.7k; 6+ npm Tally clients/relays created Sep–Oct 2026, e.g. `tally-local-server`, a "cloud relay" agent | TDL needs a Tally Developer licence; plain XML does not [Secondary] | **Open window, but a crowded indie field and low willingness to pay: candidate** |
| Busy, Marg, Vyapar (India) | — | Desktop | Apideck radar | — | — | — | Same economics as Tally, smaller: skip |
| **CONTPAQi (Mexico)** | "1.2 Millones de Empresas Usuarias" [Verified: contpaqi.com; vendor claim] | Windows SDK only; no public REST/cloud API found [Secondary: search] | Apideck radar only; unified.to ✘; Codat ✘; Rutter ✘ | **Partial: AR Software sells a self-hosted "CONTPAQi Comercial API" licence at $720/year per RFC** (not open source; 15 GitHub stars) [Verified: GitHub README] | ARSoftware SDK 10.2k NuGet; 134 CONTPAQi packages on NuGet (most are CONTPAQi's own abandoned 2015 "Nube" packages) | SDK terms [Unknown] | **Best open window: candidate** |
| Aspel (Mexico) | "Popular" [Apideck] | Desktop | Apideck radar | Not found | No NuGet packages | [Unknown] | Bundle with CONTPAQi |
| Hashavshevet (Israel) | "50K+ customers" [Apideck radar page] | **Official H-CONNECT API, plus software-house support** [Verified: h-erp.co.il] | Apideck radar | Vendor route exists | No NuGet packages | Vendor-controlled | Not a gap; also drifts toward an Israeli niche: kill |
| Priority (Israel) | — | Official REST/OData API [Hypothesis: not verified this phase] | Apideck radar | — | — | — | Not a gap |
| DATEV (DE) | "2.5M+ businesses" [Apideck] | Certified marketplace APIs | unified.to ✔, Apideck (DATEV Unternehmen Online ✔), Chift logo | Aggregators cover it | FluiTec.DatevSharp 22.6k | Certification | Covered: kill |
| EBP, Cegid Quadra (FR) | — | — | unified.to ✔ (EBP Compta, Cegid Quadra), Chift | Aggregators | — | — | Covered: kill |
| Lexware (DE) | — | Lexware Office has an API | unified.to ✔, Apideck ✔ (Lexware Office) | — | — | — | Covered (cloud); desktop editions not checked |
| Yayoi, PCA, OBIC, TKC (JP); Douzone (KR) | Large [Unknown] | Closed/desktop | Apideck radar; freee and MoneyForward have APIs | — | No NuGet packages for Yayoi | — | **Language barrier for founder and customers: kill** |
| Sage Pastel Partner / Sage 200 Evolution (ZA) | "Traditional market leader" [Apideck] | Evolution SDK on NuGet from Sage (61.5k downloads; last release 2019) | Apideck lists 8 unsupported SA systems; Codat ✘ | Not found (no search spent) | 61.5k Evolution SDK | Sage SA terms [Unknown] | **English-speaking window: weak candidate** |
| Reckon Accounts (AU) | — | Desktop is QuickBooks-derived (qbXML-like) [Hypothesis] | Apideck radar | — | — | — | Conductor-class players could add it cheaply: skip |
| Subiekt, Optima, Symfonia (PL) | — | InsERT Sfera (paid SDK) | Apideck radar | BaseLinker-type local connectors exist for e-commerce [Hypothesis] | — | — | Polish language: skip |
| Contasol, Contaplus / Sage 50 ES, a3 (ES) | — | Desktop | Apideck radar | — | The "merlos" Sage 50 ES packages (1M+ downloads) belong to one Spanish software house, not an API vendor | — | Possible Spanish add-on to CONTPAQi later |
| Exact Globe, AccountView (NL) | — | On-prem | Apideck radar | — | — | — | Dutch: skip |

### 1b. Non-accounting closed systems (checked against existing unified APIs or the ledger)

| Category | Status | Source |
|---|---|---|
| Dental / vet PMS (Dentrix, Eaglesoft, Cornerstone) | Ledger-excluded (P7, "dental/vet PMS bridges"); Sikka and NexHealth exist | Ledger |
| Construction ERP | hh2 authorised by Sage; Agave moved to selling contractors directly | See above |
| Property management (Yardi Voyager, MRI, Entrata, RealPage) | Supergood grades Yardi, MRI and Entrata **F** and RealPage D. All are closed, with paid interface programmes. Specialist unified APIs exist [Hypothesis: Propexo, not verified this phase] | [Verified: supergood.ai/api-report-card] |
| Auto dealer DMS (CDK) | Graded F. Historically litigated against third-party data access [Secondary: general knowledge, not re-verified]. **Legal kill** | Supergood |
| Restaurant POS (Toast F, older on-prem POS) | Partner-gated | Supergood |
| Insurance agency management (Applied Epic, F) | Partner-gated | Supergood |
| Field service (ServiceTitan, D) | Partner-gated, with a large partner programme | Supergood |

**Generalist competitor.** Supergood ("API for hard software") has graded **1,496 platforms** [Verified: supergood.ai]. It builds APIs for exactly these closed systems, but sells them enterprise-style; its pricing is not public. Nango covers long-tail auth for systems that have some API.

### 1c. What the census says about the pattern

- **The Conductor conditions are rare in combination:**
  - a large installed base;
  - small, English-speaking SaaS buyers who search for the capability;
  - a vendor SDK that permits third-party use;
  - no aggregator below about $500/month;
  - a target market the founder can support.
- **US/UK systems** fail on coverage (QBD, Sage 50 UK, Dynamics GP) or on gating (Sage CRE, CDK, Yardi).
- **Continental Europe** fails on aggregators (Chift, unified.to).
- **Japan and Korea** fail on language.
- **What remains:** Mexico (CONTPAQi, Aspel), India and GCC (Tally family), and South Africa (Pastel / Evolution). In all three regions the paying SaaS developer typically has lower willingness to pay than Conductor's US customers [Hypothesis].
- **The copying test is the most important new fact.** Conductor's niche drew three priced clones in about six months. Tally drew six or more indie npm clients and cloud relays in September–October 2026 alone. AI-assisted builders now find and fill these gaps quickly. A new entrant should expect a first-mover window of months, not years.

---

## Part 2. Negative space: where do newcomers outperform?

### 2a. Base rates assembled from Phases 5–7, plus this phase

| Channel / model | Newcomer outcome | Source phase |
|---|---|---|
| Apify Actors | Median new Actor: 1 monthly user; 0 of the Actors under 3 months reached 100+ users (n=390) | P5 |
| Superhive add-ons | Typical <10 sales in the first 2–3 months | P5 |
| JetBrains paid plugins | 10–133 downloads | P5 |
| Wix / WooCommerce apps | Most have 0 reviews | P5 |
| CodeCanyon modules | 1–16 lifetime sales | P5 |
| Skool paid groups | Median 11 members (n=454) | P6 |
| UK G-Cloud | 86% of suppliers earned nothing | P6 |
| Israeli invoicing apps on Wix/Shopify | 0–16 reviews | P6 |
| ~20 borrowed-distribution channels | Application form, no sales data | P7 |
| **Shopify Partner Directory, 2024+ joiners** | 9 of 89 (10%) had 5+ reviews in 12 months. **Brazil 5/16 (31%)**, Germany 0/29, Israel 1/5 | P7 |
| **WP.org fork in Brazil (Infixs)** | ~4k installs in about 2 years | P6 |
| **TrustMRR audience-free API (Conductor)** | $42k MRR, 271 subscriptions, 4 Product Hunt upvotes. The founder claims 7% month-on-month growth [Verified figures; growth is a founder claim] | P7, re-checked P8 |
| **2026 QBD-API clones (this phase)** | 3 priced entrants within ~6 months. Combined SDK downloads are about 5–9% of Conductor's, and part of that may be launch-week noise | P8 |

### 2b. Where newcomers outperform

1. **Below the minimum price of incumbents.**
   - Conductor's own pitch is "€599/month minimum vs $49 per connection" (against Apideck). Unified.to's floor is $750/month. Rutter sells Sage 50 only on enterprise terms.
   - Small vendors with 1–10 end customers cannot pay those floors, so they go to whoever sells per connection.
   - **This is the most robust mechanism found.** It explains Conductor, and Hyperext's resale to small vendors.
2. **Capabilities developers search for and nobody sells self-serve.** Real, but short-lived (see the clone finding above).
3. **Mid-size, non-English service markets** (Brazil, in two separate datasets). The advantage plausibly comes from less entrenched local agency competition and fast platform growth [Hypothesis on cause].
4. **Non-English software negative space.**
   - Apideck's country pages list 5–19 unsupported local systems per country.
   - The densest gaps are Japan, France, the Netherlands, Germany, the UK and South Africa. But in France and Germany Chift and unified.to fill much of Apideck's gap.
   - The genuinely uncovered systems are concentrated in **Mexico, India, South Africa, Japan and Korea**.

### 2c. Is there a non-software model with the same property?

- **Measured:** only one. Directory-sourced services in a mid-size non-English market (Brazil Shopify partners, 31% newcomer success).
- **"Below-the-minimum" physical supply:** the Israeli low-minimum packaging broker (K6, 43.0) and similar ideas were already tested. Their newcomer data showed no advantage.
- **Implementation services for closed systems:** CONTPAQi and Tally each run large certified-distributor and partner networks. A newcomer there competes with established local partners. There is no newcomer data.
- **Conclusion:** I found no non-software model with Conductor-like, audience-free scalability. The Brazil services finding is real, but it means labour-bound revenue (Track A at best). It is listed below as F8-5 for completeness.

---

## Opportunities (5)

### F8-1. CONTPAQi (+ Aspel) self-serve integration API: "Conductor for Mexico" (TOP)

1. **Concept.**
   - A hosted REST API (plus MCP) that gives SaaS vendors and fintechs read/write access to their customers' CONTPAQi Comercial and Contabilidad companies.
   - Delivered through a small Windows agent beside CONTPAQi. Customers onboard themselves.
   - Docs in English and Spanish, with CFDI-aware objects.
2. **Paying customer and geography.**
   - Mexican SaaS: e-commerce and marketplace connectors, POS, payroll, expense, B2B ordering.
   - US and international SaaS and fintechs selling into Mexico: SME lenders and spend-management tools.
   - Possibly accounting firms automating client books [Hypothesis].
3. **Model.** Per connected RFC (Mexican taxpayer ID) per month, about $35–49 with no minimum; volume deals.
   - AR Software's price anchor is $720/year per RFC (= $60/month) for a self-hosted licence [Verified: github.com/AndresRamos/ARSoftware.Contpaqi.Comercial.Api, 2026-10-13].
4. **Spending evidence.**
   - **Installed base:** 1.2M user companies [Verified page, vendor claim: contpaqi.com].
   - **An incumbent charges for this exact capability** (AR Software licence, plus courses and consulting). It is a one-person operation with 72 GitHub followers. Unit sales are **[Unknown]**.
   - **Developer activity:** the AR Software SDK has 10.2k NuGet downloads, with releases through Aug 2026 [Verified: nuget.org].
   - **Merchant demand:** a Shopify community thread (May 2023) confirms no native Shopify–CONTPAQi integration exists [Verified]. It is a single anecdote.
   - **Paid vendor demand:** no priced commercial connector surfaced in two searches [Secondary]. **Paid demand from vendors is [Unknown].**
5. **Competitors and what customers dislike.**
   - **AR Software:** self-hosted, licence-based, Spanish-only, sold through courses and consulting. There is no hosted multi-tenant onboarding [Verified README].
   - **Apideck:** "on radar" only [Verified].
   - **Supergood:** enterprise, generalist.
   - **In-house builds** by larger Mexican vendors.
   - **CONTPAQi itself** could ship cloud APIs. Its 2015 "Nube" NuGet packages were abandoned [Verified: nuget registration].
6. **Entry strategy.**
   - The only hosted, multi-tenant, English-documented, per-connection option.
   - Price below AR Software's effective $60/month.
   - Target US and international buyers who cannot evaluate Spanish-only Windows SDKs.
   - Bundle Aspel later.
7. **Acquisition mechanism.**
   - Developer search ("CONTPAQi API", "integración CONTPAQi") with docs SEO, and comparison pages against AR Software and Apideck.
   - Outreach to the vendors listed on Mexican SaaS integration pages.
   - The channel evidence is Conductor's audience-free pull (one case). Apideck's radar pages show aggregators think this keyword set is worth capturing.
   - CAC [Unknown]. Newcomer outcomes in Mexico [Unknown].
8. **Capital, delivery and constraints.**
   - Under $2k: Windows VM, CONTPAQi licences or a demo, hosting.
   - Fully remote from Israel.
   - **Unknown:** CONTPAQi SDK licence terms for hosted third-party use, and whether a distributor agreement is needed.
   - **Support burden:** Spanish-language end-customer installs (a contractor in Mexico could handle these).
9. **Labour.** Medium. Revenue grows per connection. Agent and version support grows with the installed base and is partly delegable.
10. **Unit economics [Hypothesis].** About 85% gross margin.

    | Scenario | Connected RFCs | Owner profit |
    |---|---|---|
    | Downside | 10 | ~$300/month |
    | Base (18–24 months) | 60–120 at $40 | **~$2–4k/month** (Track A) |
    | Upside (CONTPAQi + Aspel + Spain later) | 400+ | ~$12–15k/month (Track B, unproven) |

11. **Risks.**
    - Little paid vendor demand (the main risk).
    - CONTPAQi ships its own API or restricts SDK use.
    - Clones within months once visible.
    - Mexican buyers' lower willingness to pay.
    - Spanish support load.

**Decisive assumption:** at least about 30 software vendors or fintechs need programmatic CONTPAQi write access and will pay about $40 per company per month, and CONTPAQi's SDK terms permit a hosted service. **Cheapest desk test:** count how many Mexican SaaS, POS, e-commerce and fintech integration pages list CONTPAQi, compared with Alegra or Bind (both of which have APIs).

### F8-2. TallyPrime per-company cloud API for vendors outside India and for small Indian SaaS

1. **Concept.** A self-serve REST API (plus MCP) over customers' Tally companies through a local agent, priced per company with no minimum. It sells below unified.to's $750/month floor and Apideck's.
2. **Customers.**
   - International fintechs and SaaS selling into India, the GCC and East Africa.
   - Small Indian SaaS that cannot afford to build in-house. A production connector is estimated at 3–6 months and ₹6–20 lakh [Secondary: aiaccountant.com, an interested vendor].
3. **Model.** $15–49 per company per month, with an India tier [Hypothesis].
4. **Spending evidence.**
   - **Installed base:** 2.7M businesses; 65k in the UAE [Verified pages; vendor claims].
   - **Build cost** (the money vendors save by buying): above.
   - **The capability sells:** unified.to lists TallyPrime as "New", behind a $750/month minimum [Verified]. CData sells Tally drivers [Verified: NuGet].
   - **Willingness to pay per connection: [Unknown].**
5. **Competitors.**
   - Unified.to (floor $750).
   - CData drivers (per developer).
   - Open-source TallyConnector (23.7k downloads).
   - At least 6 indie npm Tally clients and relays created Sep–Oct 2026, including a "cloud relay" agent [Verified: npm].
   - In-house connectors at large vendors (ClearTax uses its own agent on the Tally machine) [Verified: cleartax.com/ae].
   - Tally itself, which is pursuing UAE e-invoicing provider (ASP) accreditation and is modernising (TallyPrime 7.1) [Verified: Tally MENA page].
6. **Entry strategy.** USD-priced, English-first, compliance-grade security (no exposed port 9000), aimed at foreign buyers. Indian price competition makes the domestic segment hard.
7. **Acquisition.** Developer search ("Tally API", "TallyPrime REST API"). Apideck's radar pages and unified.to already compete for these keywords. CAC [Unknown].
8. **Ops.** Under $2k; remote. The XML interface needs no Tally licence, but TDL customisation does [Secondary].
9. **Labour.** Medium.
10. **Economics [Hypothesis].**

    | Scenario | Owner profit |
    |---|---|
    | Downside | $0–500/month (indie and open-source price pressure) |
    | Base | $1.5–3k/month |
    | Upside | Larger only if global fintech demand is real |

11. **Risks.** Crowding is already visible. Indian willingness to pay is low. Tally may ship an official cloud API. Big buyers build in-house.

**Decisive assumption:** enough non-Indian or well-funded buyers want hosted Tally access at a USD price, given open-source alternatives. **Kill signal:** an indie Tally relay launches with public per-company pricing before any test.

### F8-3. White-label on-prem connector supplier to unified-API aggregators ("arms dealer" to the radar lists)

1. **Concept.** Instead of fighting aggregators for developer search, build Windows agents for systems the aggregators list as "on radar" and license them B2B: CONTPAQi, Aspel, Tally, Busy, Pastel, Sage 200 Evolution, Contasol. The model resembles Hyperext's resale arrangements.
2. **Customers.** Unified-API vendors: Apideck lists 5–19 unsupported systems per country [Verified: apideck.com country pages]. Also Chift (which already offers a "local agent option" [Verified]), unified.to, Merge and Codat.
3. **Model.** Per-connection revenue share or a licence fee.
4. **Spending evidence.**
   - Aggregators publish demand-capture pages for these systems [Verified].
   - Chift raised €10.5M and sells to Revolut, Qonto and Pennylane [Verified: chift.eu logos/claims].
   - **No evidence that aggregators buy rather than build [Unknown].**
5. **Competitors.** The aggregators' own engineering teams, and Supergood.
6. **Entry.** Be first with a working, tested agent for one radar system (CONTPAQi), then pitch it.
7. **Acquisition.** Direct business development with about 10 named companies. The founder must sell, which is not audience-free but is a short list.
8. **Ops.** Low capital; remote.
9. **Labour.** Revenue follows the partner's growth.
10. **Economics [Hypothesis].**

    | Scenario | Outcome |
    |---|---|
    | Downside | 0 deals |
    | Base | 1–2 partners at $1–3k/month each |
    | Upside | Acquisition by an aggregator |

11. **Risks.** Concentration on one or two buyers. Aggregators prefer to own core connectors.

**Decisive assumption:** at least one aggregator will license or revenue-share a third-party agent instead of building it.

This pairs naturally with F8-1: sell direct first, then license.

### F8-4. Sage Pastel Partner / Sage 200 Evolution API (South Africa)

1. **Concept.** The Conductor model for the South African Sage desktop products, in an English-speaking market.
2. **Customers.** SA fintech lenders, payroll and e-commerce SaaS.
3. **Model.** Per company per month.
4. **Evidence.**
   - Apideck lists Pastel, Sage 50cloud Pastel and Sage 200 Evolution as unsupported [Verified].
   - Sage's own Evolution SDK on NuGet has 61.5k downloads, last released 2019 [Verified].
   - The installed base and paid demand are **[Unknown]**. No search was spent.
5. **Competitors.** Unknown. Sage SA business partners and local integrators are likely [Hypothesis].
6. **Entry.** As F8-1.
7. **Acquisition.** Developer search. CAC [Unknown].
8. **Ops.** Sage SA developer terms [Unknown]. This is the same Sage partner-programme gating risk as M1.
9. **Labour.** Medium.
10. **Economics [Hypothesis].** Track A at best.
11. **Risks.** Sage gating; small market; currency.

**Decisive assumption:** Sage SA's SDK licence permits a hosted resale API. **Status:** a pattern candidate needing one search plus a terms check. Ranked below F8-1 and F8-2 because the evidence is thin.

### F8-5. Brazil Shopify launch/migration studio run through Brazilian contractors (non-software negative space)

1. **Concept.** Fixed-price Shopify launches and migrations in Brazil, delivered by Brazilian freelancers, with the founder as operator. It also collects Shopify's revenue share on the stores it builds.
2. **Why this is not M12 or the Germany exclusion.** Brazil is where Phase 7 measured the *highest* newcomer success: 5 of 16 newcomers with 5+ reviews in 12 months, against Germany 0/29 and Israel 1/5. The audit, however, notes that Brazil supplies 5 of the 9 successes in the entire sample, the denominator counts only listed partners, and some "newcomers" may be re-registered agencies.
3. **Model.** Per-project fees plus revenue share.
4. **Evidence.** Measured directory flow [Verified in P7 audit]. Project prices in Brazil [Unknown].
5. **Competitors.** Local agencies; Tiendanube and Nuvemshop partners (Tiendanube partner is ledger-excluded as a channel).
6. **Entry.** English and Portuguese delivery for cross-border brands entering Brazil [Hypothesis].
7. **Acquisition.** The Shopify Partner Directory (measured). Getting listed is discretionary.
8. **Ops.** No capital. Portuguese needed via contractors. A foreign-run agency is legally feasible [Unknown].
9. **Labour.** High (services). Margin depends on contractor arbitrage.
10. **Economics [Hypothesis].** $1–3k/month owner profit (Track A; Track C).
11. **Risks.** Listing denied. Brazilian project prices too low after contractor costs. The founder has no local presence.

**Decisive assumption:** a foreign-operated studio gets listed and wins 2 or more Brazilian projects a month at prices that clear contractor cost by 40% or more.

---

## Killed ideas (and why)

| Idea | Why killed |
|---|---|
| QBD API (another Conductor) | Three priced clones in 2026 at an identical $49. Saturating [Verified: npm, pricing page] |
| Construction ERP API (Sage 300 CRE, Foundation, Vista) | hh2 is Sage's authorised platform; Sage developer licence key required on each request; Nango and Agave present |
| DATEV, EBP, Cegid, Lexware Office APIs | Covered by unified.to, Apideck and Chift [Verified] |
| Hashavshevet / Priority APIs | Official H-CONNECT and Priority APIs exist; also an Israeli-niche drift [Verified: h-erp.co.il] |
| Tally ↔ UAE e-invoicing connector | Tally is going after provider (ASP) accreditation itself; ClearTax already ships a Tally connector; also a compliance-deadline drift [Verified: Tally MENA page, cleartax.com/ae] |
| Yayoi, PCA, TKC, Douzone APIs | Japanese and Korean language barrier for docs, support and sales |
| Auto DMS (CDK, Reynolds) | Legal hostility; Supergood grade F |
| Yardi, MRI, Entrata, RealPage | Partner-gated (grade F/D); specialist aggregators |
| Dynamics GP data/migration | Retirement is served by the Microsoft partner channel; "platform-shutdown migration" is ledger-excluded (P3) |
| Reckon Accounts (AU) | Small; incumbents with qbXML-style stacks could add it cheaply [Hypothesis] |
| Dental/vet PMS bridges | Ledger-excluded (P7) |

---

## Ranking, deep-diligence picks, decisive assumptions

**Ranking:** F8-1 CONTPAQi API > F8-3 Aggregator connector supplier > F8-2 Tally API > F8-5 Brazil Shopify studio > F8-4 Pastel / Evolution API.

**Top 3 for deep diligence:**

1. **F8-1 CONTPAQi API.**
   - *Decisive assumption:* ≥30 vendors or fintechs will pay about $40 per RFC per month, and CONTPAQi's SDK terms allow hosted third-party use.
   - *Desk tests:*
     - count CONTPAQi mentions on Mexican SaaS integration pages (vs Alegra or Bind);
     - read the CONTPAQi SDK licence;
     - look for AR Software sales signals.
2. **F8-3 Aggregator connector supplier.**
   - *Decisive assumption:* an aggregator licenses or revenue-shares a third-party agent rather than building it.
   - *Desk test:* look for public precedents (partner connectors in Apideck, Chift or Codat docs credited to third parties; Hyperext's reseller list).
3. **F8-2 Tally API.**
   - *Decisive assumption:* foreign or funded buyers pay a USD per-company price despite open-source and indie alternatives.
   - *Desk test:* track the 2026 indie Tally relays for public pricing and paying users, and count non-Indian SaaS listing Tally integrations.

**Cross-cutting implications for the Director:**
- **M1 should be re-scored for clone risk.** The QBD niche drew three copies in about six months, and "Desktop Accounting API" could extend to Sage 50.
- **Any Conductor-type entry should avoid publishing revenue** (no TrustMRR listing).
- **Defensibility** should come from things AI cannot clone in weeks: partner agreements, the installed agent base, local language and tax-format know-how.

**WebSearch count: 7 of 7.**
