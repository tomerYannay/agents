# Phase 7 Red-Team Investor report (P7-REDTEAM), 2026-10-13

**Scope.** Why each of M1–M12 would fail for this founder. I also challenge the leader re-check (UK MTD, J1, H10) and H7's #1 position.

**Searches and sources.**
- WebSearch: **8 of 8 used**, all logged as `P7-REDTEAM`. One was wasted (Telarus foreign-advisor eligibility).
- WebFetch/curl was used on primary pages: conductor.is (home, sitemap, 2026 blog), Rutter and Codat Sage 50 docs, hyperext.com, Apideck's Sage field guide, enlyft.com technographics, Sage FY25 RNS (FCA NSM), the ZPP provider FAQ (full HTML, grepped), TEFA providers page and educator-credential policy, avetta.com/partner-program.
- Blocked: Sage NA partner-programme PDFs (developer.sage.com, 403), the GKV "Kriterien Kapitel 5" PDF (timeout), and the Odyssey vendor-requirements help page (403).
- Scratch: `scratchpad/p6plus/P7-redteam/{scripts,data}`. No browser, no contact, no sign-ups.

**Conventions.** All scores use the frozen rubric. Step values are CF 5/4/4/4/3, Scal 3/4/4/4/3/2, Dist 4/4/6/3/3. "Steps" lists the 0–5 scores in rubric order.

---

## 0. Headline

1. **M1 (Sage 50 API) is the only Phase 7 idea that earns a place in the #2–#12 cluster. It is overrated as a Track B idea.** I found no hard blocker, but its demand ceiling is structurally smaller than its proof case (Conductor) suggests:
   - **Sage's North America revenue is dominated by Intacct:** £461m of £997m US revenue in FY25 [Verified: Sage FY25 RNS, 19 Nov 2025].
   - **Intuit's QuickBooks Desktop ecosystem is about 15–35× larger by revenue.** Conductor cites $2.775B FY25 Desktop Ecosystem revenue, up 5% [Secondary: conductor.is/blog/quickbooks-desktop-api-in-2026, citing Intuit].
   - **Sage 50 US and Sage 50 Canada are "completely separate codebases"** [Verified: Apideck field guide]. "US/Canada" therefore means two products, not one.
   - **Conductor rides Intuit's free Web Connector, and Sage 50 has no equivalent** (see the M1 failure modes below).
   - My central estimate: a Conductor-equivalent for Sage 50 US+CA reaches about **10–20% of Conductor's MRR after a similar 3 years**. That is Track A, not Track B.
   - Rubric: **51.0 (range 48–53.5)**, in the noise band with UK MTD, H6 and K8. It does **not** displace H7.
2. **M3's decisive regulatory unknown is resolved in its favour, but the idea still falls.**
   - The ZPP provider FAQ states: "Kann ich einen Kurs, der in anderer Sprache und nicht in Deutsch durchgeführt wird, zur Prüfung einreichen? **Ja, Kurse können auch in einer anderen Sprache durchgeführt werden.**" Course documents must be submitted in German [Verified: zentrale-pruefstelle-praevention.de/faqs/anbieter/, fetched 2026-10-13].
   - Live online seminars count as Chapter 5 IKT courses.
   - The economics stay weak: one-off €75–150 refunds, a maximum of 2 courses a year, a mandatory qualified course leader the founder cannot be, and acquisition through migrant communities at unknown cost.
   - Rubric: about **41**.
3. **The services ideas (M8, M10, M12) hide their labour.** Two distribution claims were also over-read:
   - Avetta's "partner programme" lists only **24 partners** and publishes no lead sharing or referral terms [Verified: avetta.com/partner-program]. It is not a consultant lead channel.
   - M12's Shopify rev share is economically trivial for Israeli stores. 20% of a Basic plan is under $100 a year per store.
4. **Kill:** M4 (Texas ESA), M7 (presale merch). **Down sharply:** M5, M6, M11. **Not scorable as an opportunity until a dataset or task is named:** M2, M9.
5. **Leader corrections:**
   - UK MTD −3.4: **right**. One part is mildly double-counted; the range is 49.2–50.2.
   - J1 −2.4: **insufficient**. The Russian-gap weakness should also cut market depth, giving about 47.4.
   - H10 −1.2: **right**.
   - **H7 (56.6) remains defensible only as a nominal tie-leader.** Its newcomer data is from Phase 5 and has not been re-measured with 2026 data. Its 4-point lead is inside the noise band. Trimming it to 55–56 (the Phase 6 dissent) still leaves it #1.

---

## 1. Per-idea red team

### M1. Sage 50 US/Canada integration API ("Conductor for Sage")

**What I checked:**
- **Conductor's platform scope:** QuickBooks Desktop and Enterprise only. There is no roadmap mention of Sage. Its sitemap is 100% QBD SEO content (about 20 "QuickBooks Desktop to X / API / Web Connector" articles) [Verified: conductor.is, conductor.is/sitemap.xml]. Its acquisition looks like **long-tail developer SEO on a large keyword universe**. That universe is much smaller for Sage 50 US.
- **Conductor's mechanism:** "Conductor builds on the built-in QuickBooks Web Connector rather than requiring a custom Windows agent". The blog says this matters for hosted-desktop providers such as Rightworks, where third-party installs are hard [Verified: conductor.is/blog/quickbooks-desktop-api-in-2026].
  - Sage 50 US and Canada have no Web Connector equivalent. Integration goes through the COM SDO, and "the SDK is free but requires an ISV/development-partner application"; Sage 100 is "gated by Sage's Technical Partner Program" [Verified: radar.apideck.com/blog/sage-integration-field-guide].
  - Supergood: Windows-only, version-locked, needs an interactive session [Verified by Agent D].
  - So a Sage clone carries **more** ops per connected file than Conductor does, not the same.
- **Competitor coverage:**
  - Codat's Sage 50 connector is UK & Ireland only [Verified: docs.codat.io Sage 50 page].
  - Rutter's Sage 50 is enterprise-contract only; the region is not stated [Verified: docs.rutter.com].
  - Hyperext is UK & Ireland only, claims "15 years" of Sage expertise and no Sage partner status, and lists "end of Sage SData" in its news [Verified: hyperext.com].
  - **Zynk (UK iPaaS) lists Sage 50 US and Sage 50 CA connectors** [Secondary: search snippets of zynk.com/integrations/sage-50-ca and the US page, 2023 edition listed].
  - Sagify (Shopify ↔ Sage 50 CA) said US support was "in progress" [Secondary: forum snippet].
  - So the gap is **self-serve developer API with public pricing**, not "no connector exists".
- **Size proxies (all imperfect):**
  - Enlyft technographics, a web-footprint-biased sample [Verified pages, undated]:

    | Product | Companies in dataset | US share | Canada share |
    |---|---|---|---|
    | Sage 50 | 25,402 | 36% | 13% (UK 35%) |
    | QBD Pro | 16,552 | 84% | 7% |
    | QBD Enterprise | 15,032 | 84% | 7% |

    That gives about 12.4k Sage 50 US+CA against about 28.7k QBD Pro+Enterprise in North America (Premier excluded). This is an **upper-bound ratio of about 0.4**.
  - Revenue proxy: Sage US £997m, of which Intacct is £461m. The remaining ~£536m covers Sage 50 US, 100, 300, X3, construction, HR and Fyle. Canada is £141m in total. Management says only that North America saw "continued growth in Sage 200 and Sage 50" [Verified: FCA NSM RNS 0746I].
  - Sage 50 US+CA revenue is plausibly £100–200m [Hypothesis], against about $2.8B for the QBD ecosystem. That is a **ratio of about 0.05–0.1** before adjusting for ARPU.
  - There was no 2025 Sage 50 US desktop release [Secondary: third-party guide], and Sage retired Sage Business Cloud Accounting in the US at the end of 2024 [Secondary: reseller blog]. Both point to Sage putting little into the US small-business tier.
- **Why QuickBooks Desktop integration demand is larger (answering the brief's question):**
  1. A far larger installed base, concentrated in the operations-heavy US verticals that vertical SaaS sells to (construction, field service, wholesale). Conductor names exactly these.
  2. Big fintech pull: Ramp is a Conductor customer [vendor claim]. US spend-management and lending fintechs prioritise QBD because their customers are on it.
  3. Intuit's Web Connector makes a hosted API feasible without a custom agent, including on Rightworks-hosted files.

  Sage 50 US lacks (3) and is weaker on (1) and (2). Canada is the relative bright spot: Sage 50 is "the primary legacy desktop solution for Canadian small businesses". But it is a separate codebase, and Canada is about 1/7 of Sage's North America revenue.
- **Can incumbents add it quickly?**
  - **Rutter already has a connector.** Moving Sage 50 from enterprise-gated to self-serve is a pricing decision, not engineering.
  - **Zynk** already owns US/CA SDO connectors and could expose an API.
  - **Hyperext** knows the Sage 50 domain, but US and Canada are different codebases, so it would take months, not days.
  - **Conductor** would need a new Windows agent stack (no Web Connector). That is a 3–6-month project for a small team [Hypothesis], and nothing suggests it plans to.
  - The **most likely fast follower is Rutter**, if the founder proves volume. Rutter's gating itself is a demand signal: a well-funded unified-API vendor chose not to make Sage 50 self-serve. That suggests low volume and/or high support cost [Inference].

**Top 3 failure modes:**
1. **Demand ceiling.** If Sage 50 US+CA integration demand is about 10–20% of QBD's, a 3-year Conductor-equivalent is about $4–8k MRR [Hypothesis]: Track A after a long ramp, never Track B. Developer search volume for "Sage 50 API" is small. Conductor's SEO engine needed a large keyword universe.
2. **Ops and support per file are higher than Conductor's.** There is no Web Connector, so a custom Windows agent must run beside a licensed Sage 50 install, with SDO calls that may need an interactive session. Sage-hosted and Rightworks-hosted users may not allow agent installs. Annual SDK version breaks are 2× (US and CA). This is the "runs itself" claim failing for Sage [Hypothesis grounded in the verified mechanism difference].
3. **Gatekeeping and platform risk.**
   - The partner application and fees: the Tech Partner Program "must pay sign-up and annual renewal fees" [Secondary: snippet of the Sage NA Tech Partner Program PDF, Mar 2025; PDF 403]. The amount and the redistribution terms are unknown.
   - Sage could gate or price the SDK out, or ship its own Copilot or agents and platform APIs. Sage is "introducing intelligent AI agents" across Sage 50 [Verified: RNS]. That weakens the "MCP for AI startups" angle.
   - Rutter can de-gate at any time.

**Hard blockers:** none verified. The SDK is accessible after a partner application [Verified: Apideck; a community post says it is a free download with a Sage ID tied to a Sage 50 US licence].

**Unverified concerns:**
- the partner fee and hosted-resale terms;
- Israel-based ISV eligibility;
- whether SDO works headless or as a service;
- whether a Sage 50 US customer base big enough for 100 files within 18 months exists;
- Rutter's actual Sage 50 regions and price.

**Verdict:** **Hold** (best of Phase 7, but not "strong").

**Adjusted:** **51.0, range 48–53.5.**
- Steps: CF 3,1,4,5,3 = 64 · Scal 2,5,2,4,2,5 = 66 · Dist 4,3,2,2,3 = 55 → Balanced 63.0, penalty 12.
- The upper end (53.6) needs speed 2 and penalty 11. That is only justified if the SDK terms are confirmed permissive.

**Cheapest later validation (no contact):** an integration-page census.
- Scrape the public "integrations" pages of about 200 US/Canadian vertical SaaS products (construction, field service, wholesale/distribution, property, nonprofit).
- Compute the ratio of vendors listing Sage 50 US or CA to vendors listing QuickBooks Desktop.
- **A ratio of at least 0.2 keeps Track A alive. A ratio of at most 0.08 kills it.**
- Add a free keyword-volume check of "Sage 50 API/SDK" against "QuickBooks Desktop API".

---

### M2. Licensed niche data API (dataset TBD)

**Top 3 failure modes:**
1. **No dataset means no opportunity.** Every economic claim is about a dataset not yet found.
2. **Data rights.**
   - Datasets with clean redistribution rights and no official API are rare.
   - SoldComps (the proof case) lives on top of eBay data. That is a terms-of-service and takedown exposure, not a model to copy.
3. **Survivor-biased evidence.** TrustMRR revenue-sorted pages (SoldComps $21.6k, BestTime $9.3k) are the top of the distribution. fuelprice.io at $828 MRR is closer to the newcomer median, and that median is unknown. This is the Apify pattern (median new Actor: 1 user).

**Hard blockers:** none, because there is nothing concrete to block.

**Unverified:** everything material.

**Verdict:** **Down**. Do not rank it alongside named ideas. Keep it as a method for later phases.

**Adjusted:** **42–46** if forced.
- Steps CF 1,2,4,5,4 = 61 · Scal 2,5,2,5,1,5 = 67 · Dist 1,3,2,2,3 = 43 → Balanced 59.8, penalty 14 → 45.8.
- The rubric over-rewards margin and leverage for an unnamed product, so treat 45.8 as a ceiling.

**Cheapest validation:** desk-scan public-domain or open-licensed datasets (government open data under OGL or CC-BY, with no official API) against developer search demand. Choose one only if both conditions hold.

---

### M3. Germany §20 SGB V online prevention courses in Russian/Ukrainian/Turkish/Arabic

**What I checked (ZPP FAQ, full text, verified 2026-10-13):**
- **Language:**
  - Courses may be run in another language ("Ja, Kurse können auch in einer anderen Sprache durchgeführt werden").
  - "Der Titel, die Kursdetails und alle Unterlagen müssen auf Deutsch zur Prüfung vorliegen", and the language must be stated in the description.
  - Chapter 7 digital offers in foreign languages need a translator's confirmation.
  - **Agent A's decisive unknown is answered: permitted.** The FAQ answer is general rather than IKT-specific. I infer it applies to Chapter 5 IKT courses as well [Inference].
- **IKT format:**
  - 8–12 units of 45–90 minutes; module gating; mandatory reactive exchange with the course leader.
  - Written-only content is not enough: exercises must be demonstrated.
  - One-year recognition, then a mandatory effect evaluation to extend to 3 years.
  - "Online-Seminare werden weiterhin als IKT-Angebote in Kapitel 5 eingeordnet" if they run on fixed dates.
- **Course leaders:** every course leader needs a recognised qualification and an "Einweisung" into the concept.
- **ISO 27001:** an ISMS certified under ISO 27001 (and ISO 27018 for cloud) is required for **Chapter 7 "digitale Angebote"**. It is "nicht delegierbar". The FAQ does not apply it to Chapter 5 IKT, which only needs a signed data-protection declaration. **Staying in Chapter 5 is therefore essential.** Chapter 7 would mean ISO 27001 certification (well above $2k) plus a study.

**Top 3 failure modes:**
1. **Unit economics are one-off and capped.**
   - About €75–150 refunded, at most 2 courses a year per person.
   - There is no recurring revenue; each participant must be re-acquired.
   - Insurers reimburse after the fact, so the participant pays upfront and files a claim. That is friction for exactly the low-German-proficiency target group.
2. **The labour sits with a qualified, foreign-language course leader the founder cannot be.**
   - The leader needs a German-recognised qualification and is mandatory for reactive exchange, or for every session if live.
   - Live webinars are labour-bound. Self-paced IKT still needs leader responses at scale.
   - Recruiting a Russian- or Turkish-speaking physiotherapist or sports scientist whose degree ZPP accepts is the real gate [Hypothesis: foreign-degree recognition unverified].
3. **Acquisition into migrant communities is unmeasured and probably expensive.**
   - Prevention-course take-up skews to German-speaking, educated women [Hypothesis; not verified this phase].
   - Competitors use free-gift incentives (FitnessRAUM €49 goodie; medizen bottle).
   - The ZPP database gives discoverability only to people who already search for a course, in German.

**Hard blockers:** none (language now verified permitted).

**Unverified concerns:**
- whether individual Krankenkassen subsidise foreign-language online courses;
- recognition of foreign qualifications for course leaders;
- passing the 1-year evaluation;
- the size of the target insured groups;
- invoicing and VAT from Israel.

**Verdict:** **Down** on economics, despite the regulatory "Up". The blocker is gone, but this is a low-ARPU, non-recurring, labour-attached course business.

**Adjusted:** **~41, range 39–44.**
- Steps CF 4,2,3,3,3 = 61 · Scal 2,2,2,3,1,2 = 41 · Dist 4,3,2,2,3 = 55 → Balanced 51.8, penalty 11 (lowered, because the key unknown is now verified).
- Agent A's 49–52 assumed open languages but did not price in recurring = 2/5 and founder fit = 2/5.

**Cheapest validation:** query one or two insurers' public course-search tools (or the ZPP-fed databases) for online courses tagged Russisch/Türkisch/Arabisch/Ukrainisch. Count the existing supply. Absence would support the wedge; presence would kill it.

---

### M4. Texas Education Freedom Account (ESA) online IEP programme

**What I checked:**
- **TEFA educator credential policy (7 Jul 2026)** [Verified: educationfreedom.texas.gov/newsupdates/educator-credential-policy]:
  - Each lead educator must be a current or retired employee of an accredited school or higher-education institution, or hold a "relevant license or accreditation". Examples: a teaching licence, Orton-Gillingham certification, a related degree.
  - The lead educator must be "continuously present during instruction".
  - Other staff "must meet the same **fingerprint background check** requirements as the lead educator".
- **Vendor eligibility:**
  - "Approved providers and vendors must have the right to transact business in Texas." Online and out-of-state providers only "if the provider applies for approval and is accepted" [Verified: TEFA providers page].
  - An Odyssey help page reportedly requires a **US-based business entity** registered with the Texas SOS [Secondary: search snippet; page 403].

**Top 3 failure modes:**
1. **It is a US tutoring agency with credentialed, fingerprinted staff.** The founder's software skill is incidental. Margin is the tutor spread.
2. **Discovery is a 54k-product catalogue that concentrates on giants.** Arizona: Amazon about 2/3 of marketplace spend; Outschool $12M of $30M online.
3. **Policy and audit risk.** ESA is politically contested, there was an Arizona audit controversy, and IEP funds come with heavy documentation.

**Hard blockers (verified):**
- fingerprint-checked, credentialed lead educator continuously present;
- Texas business registration.

These are fatal for a solo Israel-based founder without a US entity and US staff. **Unverified:** foreign ownership of the US LLC; Odyssey payment terms.

**Verdict:** **Kill.**

**Adjusted:** **29.4, range 28–34.** Steps CF 4,1,3,2,1 = 47 · Scal 3,3,1,2,1,1 = 38 · Dist 4,2,1,2,2 = 42 → Balanced 42.4, penalty 13.

**Cheapest validation (if ever revived):** request the Arizona or Texas per-vendor payment dataset behind the ABC15 story through public-records portals. That shows the share of spend going to vendors outside the top 20.

---

### M5. Children's-artwork keepsake fundraisers in an unserved country

**Top 3 failure modes:**
1. **"Unserved country" is unverified.**
   - Competitors in DE/NL/Nordics were not searched in local languages.
   - Israel adds Ministry of Education limits on commercial activity in schools [Hypothesis, unverified].
2. **Each campaign needs local-language, in-person coordination with schools.** The founder has neither the language nor a presence in DE/NL, so it depends on an ambassador network that does not exist. Seasonality is extreme (Q4).
3. **Thin unit economics on POD.**
   - About €7–8 owner gross per order. A 300-pupil school yields about €650 per campaign.
   - Track A needs about 50–60 campaigns a year, which means school-by-school selling: the Phase 6 failure mode.

**Hard blockers:** none verified. **Concerns:** GDPR for pupils' names and artwork; school-commerce rules; a local POD partner.

**Verdict:** **Down.**

**Adjusted:** **35.0, range 33–38.** Steps CF 3,2,4,3,2 = 57 · Scal 2,2,2,3,1,1 = 39 · Dist 4,2,2,2,2 = 48 → Balanced 48.0, penalty 13.

**Cheapest validation:** native-language desk search plus the PTA/Elternbeirat supplier directories of one target country, to list existing providers.

---

### M6. Per-location souvenir/print lines wholesale

**Top 3 failure modes:**
1. **Margins.**
   - Keystone pricing plus Faire's 15–25% leaves cents per unit on POD (verified by Agent B).
   - Short-run inventory per town design means capital and dead stock across hundreds of SKUs.
2. **Positioning against the incumbent.**
   - Lantern Press (≥10,750 SKUs) markets "Hand-drawn by humans".
   - AI-assisted art is a negative with this buyer, which removes the founder's only edge.
3. **Faire newcomer reality is unmeasurable (403), and logistics from Israel are poor.** Case packs, freight and reorders all need a destination-country printer and 3PL.

**Hard blockers:** none verified. **Concerns:** Faire's eligibility for Israel-based brands; place-name and park trademarks.

**Verdict:** **Down → effectively Kill.**

**Adjusted:** **32.6, range 31–36.** Steps CF 3,2,2,2,2 = 45 · Scal 3,3,2,3,1,1 = 46 · Dist 4,3,1,2,2 = 46 → Balanced 45.6, penalty 13.

**Cheapest validation:** get short-run unit quotes for stickers and magnets in the US and UK from public price calculators. If stickers cost more than $0.80 or magnets more than $1.50, it is dead.

---

### M7. Presale merch for creators and small game studios

**Top 3 failure modes:**
1. **Acquisition is founder outbound to creators against Makeship**, which pays out $16M+ and now signs licensed big IP.
2. **Per-campaign project-management labour and failure costs.** Samples cost $300–800 each, a failed MOQ burns them, and factory delays bring refunds and chargebacks.
3. **No recurring revenue and no defensibility.** Every campaign is a new sale.

**Hard blockers:** none. **Concerns:** IP licensing; China QC from Israel; creators defecting.

**Verdict:** **Kill.**

**Adjusted:** **25.6, range 24–30.** Steps CF 3,2,2,3,1 = 46 · Scal 3,1,1,2,1,1 = 30 · Dist 3,2,2,1,2 = 41 → Balanced 38.6, penalty 13.

**Cheapest validation:** parse Makeship's catalogue for language and category coverage. This only matters if a segment is clearly unserved.

---

### M8. Contractor prequalification compliance (ISNetworld/Avetta)

**What I checked:**
- Avetta's partner page has two types, "Services Partner" and "Technology Alliance Partner", with **24 partners listed**. It shows no requirements, fees, referral commissions or lead sharing [Verified: avetta.com/partner-program].
- **The claimed borrowed channel, Avetta's consultant directory, is a small curated logo wall, not a lead engine.**

**Top 3 failure modes:**
1. **No channel.** Avetta's partner list is tiny and curated, and the broker route is a hypothesis. Acquisition falls back to founder cold outreach to US/Canadian contractors from Israel.
2. **Services drift and liability.**
   - Safety programmes, questionnaire answers and document upkeep are bespoke per client and per hiring client.
   - A mistake costs the client its approval.
   - The founder becomes a compliance consultant selling hours. AI drafting lowers cost but not accountability.
3. **The platforms automate the job.** Avetta's AI "Safety Advisor" ships inside the platform contractors already pay for. The AI newcomer PrequalPilot has 6 PH views and is in private beta.

**Hard blockers:** none verified. **Concerns:** OSHA/provincial expertise; whether platforms restrict third parties submitting on a contractor's behalf; E&O insurance.

**Verdict:** **Down.**

**Adjusted:** **37.2, range 35–40.** Steps CF 3,3,5,3,1 = 62 · Scal 3,4,1,2,1,2 = 44 · Dist 4,2,1,2,1 = 39 → Balanced 50.2, penalty 13.

**Cheapest validation:** count ISN/Avetta consultants publicly listed (Avetta's 24 plus ISN's equivalent, plus Google Maps "ISNetworld consultant") and their review counts. If established consultants show low review velocity, the market is thin.

---

### M9. Preferred-partner software for independent pharmacies via co-ops

**Top 3 failure modes:**
1. **No product.** No uncovered monthly-paid task has been identified.
2. **Gatekeepers give software away or build it.** Nimble is free to IPC members; EPIC has PharmCAP; AAP has SmartSync and ProfitAmp.
3. **An endorsement still sells one pharmacy at a time.** Liberty's AAP page is a demo form. HIPAA/BAA obligations and US healthcare credibility are needed. Paid marketing packages may be pay-to-play.

**Hard blockers:** none verified (nothing concrete). **Concerns:** HIPAA; co-op package prices.

**Verdict:** **Down / not an opportunity yet.**

**Adjusted:** **38.0, range 35–40.** Steps CF 2,1,3,4,3 = 51 · Scal 3,5,2,4,1,2 = 60 · Dist 2,3,1,1,3 = 38 → Balanced 52.0, penalty 14.

**Cheapest validation:** inventory the preferred-partner categories of AAP, IPC, EPIC and RxPOA from public pages to find a task class none of them covers.

---

### M10. US technology advisor under a TSD (Telarus/Avant/Intelisys) with sub-agents

**Top 3 failure modes:**
1. **It is pure B2B telecom and cloud selling** with 3–9-month cycles, against thousands of incumbent advisors and suppliers' direct teams. The founder's comparative advantage (building software) is barely used. Founder fit is the worst on the list.
2. **No newcomer evidence, and the channel is mature.**
   - Intelisys billings grew +3.2% [Verified 10-K].
   - "Apply in 5 minutes, no upfront costs" implies a long tail of inactive advisors.
   - Avant's commission advances show residuals are bankable for **established** advisors, not that newcomers close deals.
3. **Eligibility and control.**
   - Foreign-advisor eligibility is unknown (my search was wasted). A US LLC is probably needed.
   - Suppliers can cut commissions or claw them back.
   - Sub-agent recruitment is itself a second sales job.

**Hard blockers:** none verified. **Concerns:** whether a TSD accepts an Israel-resident or Israeli-owned US LLC; commission clawbacks; assignment of residuals.

**Verdict:** **Down.** Keep it as a Track B "residual asset" thought experiment only.

**Adjusted:** **42.0, range 39–44.** Steps CF 4,1,5,4,2 = 66 · Scal 4,5,1,3,2,1 = 56 · Dist 3,1,1,1,2 = 31 → Balanced 55.0, penalty 13.

**Cheapest validation:** find publicly posted TSD sub-agent or partner agreements (some appear in court filings and SEC exhibits) and read the eligibility, assignment and clawback clauses.

---

### M11. Payments-residual agent placing embedded payments into small vertical-software vendors

**Top 3 failure modes:**
1. **Disintermediated by design.** Self-serve embedded-payments platforms pay ISVs directly, leaving no room for a referring agent: Stripe Connect, and payfac-as-a-service vendors such as Finix and Rainforest [Hypothesis from memory].
2. **Unpaid integration work.** The founder writes code for free in hope of residuals, which is "selling dev hours" without the invoice.
3. **Residual splits and agent terms are unknown, and adoption inside an ISV's merchant base is often far below 100%.**

**Hard blockers:** none verified. **Concerns:** ISO agent agreements requiring a US entity; residual assignment needing ISO consent.

**Verdict:** **Down.**

**Adjusted:** **35.0, range 32–38.** Steps CF 2,1,4,3,2 = 48 · Scal 3,5,1,3,2,3 = 57 · Dist 3,2,1,1,2 = 35 → Balanced 49.0, penalty 14.

**Cheapest validation:** scan the pricing pages of about 100 vertical SaaS in one niche to measure how many lack native payments. If 80% or more already embed payments, kill it.

---

### M12. Israeli Shopify launch/migration studio plus Shopify rev share

**Top 3 failure modes:**
1. **It is an agency.** Revenue equals packages delivered; contractors still need founder sales, QA and client handling. That is ledger L3 "agency drift" plus the Phase 5 "fixed-scope builds via expert directories" exclusion, under a better-measured channel.
2. **The annuity is small.**
   - 20% of a Basic subscription is under $100 a year per store, for 4 years.
   - 0.1% of GMV matters only for stores above roughly $300k a year, and few Israeli SMB stores reach that.
   - The "Track A borderline in year 2–3" estimate depends mostly on labour.
3. **Market and listing.**
   - Israel has about 12k live Shopify stores and 38 listed partners, with the top 3 taking 46% of recent reviews.
   - Wix is strong locally.
   - Registered-tier listing is discretionary ("a limited number"), so the first 5–10 clients must come from outside the channel.
   - The measured newcomer success rate is about 1 in 7 at best (9 of 89 post-2024 partners have ≥5 reviews in 12 months; Israel 1 of 5).

**Hard blockers:** none. **Concerns:**
- Shopify changing the rev share again (it already went from perpetual to 4 years in 2026);
- whether successful "newcomers" were really re-registered agencies with existing client books;
- the founder's stated dislike of service work.

**Verdict:** **Hold as a Track A cash bridge only; Down for a "business" mandate.** It has the best measured channel of Phase 7, attached to the least desirable model.

**Adjusted:** **41.8, range 40–45.** Steps CF 4,3,5,3,1 = 67 · Scal 1,2,2,2,1,3 = 36 · Dist 4,3,3,2,2 = 58 → Balanced 52.8, penalty 11 (measured channel data).

**Cheapest validation:** for SEDER Studio and the other 8 successful newcomers, compare `partnerSince` against company founding and prior web presence (Wayback and company registry). This tells whether *genuinely new* firms got the flow.

---

## 2. Leader re-check corrections: are they fair?

| Leader | Auditor | My view | Range |
|---|---|---|---|
| **UK MTD prep** 52.6 → 49.2 | Defensibility −3, proven channel −6, penalty 10→11 | **Right in direction and size.** The proven-channel cut matches H6, H1, K8 and H10. The defensibility cut to 0 is consistent with the Phase 3 allocation-verification precedent. Penalty +1 and defensibility 0 both cite the same evidence (Outbooks, QX, Sage's agent), so penalty +1 is partly double-counted. Against that, speed to first sale at 3/5 is generous: the first quarterly cycle passed, practices have locked their 2026-27 workflows, and there are no penalty points until Apr 2027. Speed 3→2 would be −4 CF (−1.6 Adjusted). The two effects roughly cancel. | **48.5–50.2; 49.2 acceptable** |
| **J1 memoir books** 51.0 → 48.6 | Defensibility −3, proven channel −6, penalty held | **Insufficient.** The auditor found the **Russian gap largely gone**: Russian is LTR, and both MyStories and Storyworth accept and print other-language text. It deliberately did not cut market depth "to avoid stacking". That is not stacking: defensibility covers competitor entry into the remaining Hebrew niche, while depth covers the size of the addressable segment, which has roughly halved because Russian was half the J1 concept. Depth 3→2 gives Scal 49, Balanced 58.4, **Adjusted 47.4**. The Hebrew window is also visibly closing (live code flag `test-heb=1`), which a stricter reviewer could put in the penalty (11→12, 46.4). I would not, because defensibility already covers it. | **46.4–48.6; recommend 47.4** |
| **H10 ketubot** 50.6 → 49.4 | Proven channel −6 | **Right.** It applies the same incumbent-vs-newcomer standard. The one checkable 2024 entrant shows no traction. Not raising the penalty for blocked Etsy data is correct, since that would double-count. One caveat: if Etsy newcomer velocity is later measured as near-zero, proven channel should fall again (2→1), to about 48.2. | **48.2–49.4; 49.4 now** |

None of the three corrections is unfair. Only J1's is too light.

---

## 3. Is H7 (Blender add-ons, 56.6) still defensible as nominal #1?

**Yes, but only as "first among ties", for three reasons:**
1. It is the only leader whose channel was measured on **newcomers with unit sales**: curated picks 11 of 12 at ≥10 sales; a 1,900-sale breakout; median under 10 sales in 2–3 months. Every other leader has now been cut for lacking exactly that.
2. Nothing in Phase 7 contradicts it. Phase 7 did not test it.
3. Applying the Phase 6 red-team dissent (first customers −1, penalty 12→13) gives about 55.0. That is still above M1's 51.0 and every corrected leader (≤52.2).

**Caveats the report must carry:**
- The H7 newcomer data dates from Phase 5. Supply was then growing about 2.5× (about 385 new add-ons a month).
- The 2026 MCP-registry flood (Agent F: about 3,900 new servers in Sep 2026) shows how fast AI-built supply can swamp a marketplace.
- A **2026 re-measurement of Superhive newcomer sales** is the cheapest leader check left.
- If the median newcomer is now under 5 sales, H7 drops to about 53 and the board has no leader at all.

**Range: 54.5–56.6.**

---

## 4. Rankings

**Red-team Adjusted (midpoints), compared with the corrected cumulative board:** H7 54.5–56.6 · H6 52.2 · K8 52.0 · **M1 51.0** · H1 51.2 · UK MTD 49.2 · H10 49.4 · J1 47.4 (recommended).

### Track A ($2–5k/month owner profit, realistic within 12–24 months)

| Rank | Idea | Why |
|---|---|---|
| 1 | **M1** Sage 50 API | Most plausible product-shaped Track A: 80–120 files at $45. Slow ramp (Conductor took 3 years). |
| 2 | **M12** IL Shopify studio | Fastest cash and best-measured channel, but it is labour. |
| 3 | **M3** §20 courses in foreign languages | Regulator gate open; needs a qualified co-founder or trainer and community acquisition. |
| 4 | **M10** TSD advisor | Slow first cash, poor fit. |
| 5 | **M8** Prequalification compliance | Service with no channel. |

Then M2 (if a dataset appears), M9, M5, M11, M6, M4, M7.

### Track B ($10–30k+/month)

| Rank | Idea | Condition |
|---|---|---|
| 1 | **M1** | Only if extended into a *portfolio* of legacy-desktop APIs (Sage 50 US + CA + Sage 100, then other gated desktop ERPs). That is a multi-year Track B, and still conditional on the census ratio. |
| 2 | **M10** | Residual compounding plus sub-agents is the one model where income decouples from hours, but founder fit and eligibility are poor. |
| 3 | **M2** | Only with a dataset. |

Everything else is structurally capped at Track A or below.

### Risk-adjusted (expected value per unit of founder time and capital)

H7 still sits above every Phase 7 idea. Within Phase 7: **M1** (51) > **M12** (41.8) ≈ **M10** (42.0) > **M3** (40.8) > M9 (38) > M8 (37.2) > M2 (≤45.8 on paper, but discounted to this position because no dataset is named) > M5 (35) = M11 (35) > M6 (32.6) > M4 (29.4) > M7 (25.6).

**Kill:** M4, M7. **Effectively kill:** M6.

### For deep diligence

1. **M1:** run the integration-page census and keyword-volume check first. It is decisive and costs nothing.
2. **M12:** only as a cash-bridge option; run the newcomer-authenticity check.
3. **M3:** only if a qualified, Russian- or Turkish-speaking course leader can be found on revenue share; run the existing-supply count.

**WebSearch used: 8 of 8** (`P7-REDTEAM`; one wasted on TSD eligibility). No hard blocker was found for M1. The verified hard blockers are confined to M4: credentialed, fingerprint-checked lead educators continuously present, plus a Texas business registration.
