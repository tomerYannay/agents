# Phase 7 — Discovery Agent C (Traditional / offline): "one contract → many units"

Agent: P7-C · Date: 2026-10-13 · WebSearches used: **8 of 8** (logged as `P7-C` in research-notes/search-log.txt) · All other evidence was gathered by WebFetch or curl of public pages. No browser, no sign-ups, no contact.

## 0. Headline findings (read first)

1. **The gates are real, documented and open to unknown suppliers, but they admit you to a pitch, not to sales.** The clearest public newcomer entry points found:
   - **Do it Best** (hardware/LBM co-op, which now also serves True Value stores): a vendor questionnaire, then an invitation to one of two **Open Buying Days** a year. Each is a 30-minute meeting with a merchandise manager and requires a **$300 non-refundable donation** to the Do it Best Foundation. [Verified: https://www.doitbestonline.com/become-a-vendor/, accessed 2026-10-13]
   - **AAP** (American Associated Pharmacies, an independent-pharmacy co-op): web form, a reply within about 2 weeks, a call, then a "formalized proposal". Partners also buy marketing packages that reach ">3,300 pharmacies through email". [Verified: https://www.rxaap.com/become-a-preferred-partner/ and /preferred-partner-media-kit/, 2026-10-13]

   No source anywhere gave the share of applicants accepted, or what a newly admitted small vendor sells afterwards. Newcomer outcomes are **[Unknown]** for every channel in this report.
2. **Channel owners increasingly build or own the software themselves.** This is the most important pattern for a software founder:
   - SIAA, the largest US independent insurance-agency alliance, has its own BI platform, AgencyIQ, plus bundled "Tech Stack" options.
   - EPIC Pharmacies runs its own compliance product, PharmCAP.
   - AAP sells its own SmartSync and ProfitAmp tools.
   - Mishkei HaKibbutzim, the kibbutz movement's former national purchasing organisation (279 kibbutzim are members), owns Mekomi-net, a community, payments and emergency-module platform. It has now made the Mekomi app **free**.
   - Avetta, the contractor-prequalification platform, ships its own AI "Safety Advisor".
   - Do it Best runs a Dallas Tech Center and a "Retail Innovation Lab", and partners with Paycor/Paychex, CareerPlug and Epicor.

   Sources: [Verified: siaa.com technology page; epicrx.com; rxaap.com; mishkei.co.il/about, /mekominet; mekome.net; avetta.com/plans; doitbestonline.com news 2026-09-15 and 2026-09-23; all accessed 2026-10-13]
3. **Channel partners we could identify are established or funded vendors, and price pressure goes to zero for members.**
   - Nimble (pharmacy app, acquired by Swoop) is offered to Independent Pharmacy Cooperative (IPC) members "at no cost". [Verified: chaindrugreview.com, 2026-06-17]
   - Liberty Software is one of the large pharmacy-management-system vendors. [Verified: info.libertysoftware.com/aap-member-demorequest]
   - Paycor (part of Paychex) is a Do it Best partner.
   - The smallest admitted vendor found is RxConnexion, a "preferred vendor" of RxPOA (Pharmacy Owner Alliance) with an undisclosed size. [Verified: chaindrugreview.com, 2025-07-25]
4. **The FDD route is blocked to scripted desk research.** FDDs are franchise disclosure documents, filed with state regulators. All four state/NASAA portals were blocked:
   - Wisconsin DFI: Cloudflare challenge.
   - California DFPI docqnet: the search page sits behind a Cloudflare challenge.
   - Minnesota CARDS: 403.
   - NASAA EFD: 403.

   Franchimp and Vetted.biz were also Cloudflare-blocked, and FDDHub is a JS app. SEC EDGAR full-text search worked, but only returned large franchisors and a few small issuers. No Item 8 (supplier rebate) or Item 11 (technology) figures were extracted, so every franchise statement below is [Secondary] or [Hypothesis]. **The decisive FDD reading has to be done by a human with a normal browser** (not bypassing anything; the portals are public to humans).

Net: Phase 7's "borrowed distribution" thesis holds in the sense that these channels **do** aggregate thousands of buyers behind one gatekeeper. In traditional sectors, though, the gatekeeper:
- favours suppliers with scale and references;
- extracts a discount, rebate or marketing fee;
- and increasingly competes in software itself.

The founder's best shot here is not "software for franchisees" in general. It is a **narrow, physical-world or compliance-forced product** where the gatekeeper has no in-house alternative.

---

## 1. Opportunities

### C1. Preferred-partner niche tool for independent pharmacies via co-ops/PSAOs
1. **Concept:** A narrow workflow or revenue tool for US independent pharmacies, sold through one or more buying co-ops or PSAOs (pharmacy services administrative organisations: AAP, IPC, EPIC, RxPOA, Legacy) as an endorsed "preferred partner". The member discount is funded by the vendor.
2. **Customer/geo:** US independent community pharmacies. The co-op is the gate; the pharmacy pays.
3. **Model/price:** Per-pharmacy SaaS or per-transaction pricing. A price of $79–199/month is a **[Hypothesis]**. The co-op takes a discount for members and/or sells marketing packages; terms are [Unknown].
4. **Spending evidence:**
   - AAP's email list reaches 3,300+ pharmacies. [Verified, 2026-10-13]
   - IPC "reaches over a third of the independent pharmacy market". "Hundreds" of IPC members already use Nimble, which "filled hundreds of thousands of prescriptions in 2026". [Verified: chaindrugreview.com, 2026-06-17; vendor/co-op claims]
   - Legacy Pharmacy Group gives its 550+ pharmacies access to PrimeRx. [Search snippet only]
   - These show co-ops do push software to members. Spending per member on a given tool is [Unknown].
5. **Competitors:**
   - Pharmacy management system vendors (Liberty, PrimeRx, PioneerRx, EnlivenHealth).
   - Funded apps (Nimble/Swoop, free to IPC members).
   - The co-ops' own tools (EPIC PharmCAP, AAP SmartSync/ProfitAmp).
   - Customer dislikes: not researched (searches exhausted). [Unknown]
6. **Entry strategy:** Only credible if the tool fills a gap the PMS vendors and co-op tools don't cover. Examples would be a single new pharmacist-billable clinical service, or a state-specific compliance task. **No specific gap was verified**, so this is currently "none verified".
7. **Acquisition and newcomer evidence:**
   - AAP's intake is public: form, about 2-week reply, call, proposal, agreement. [Verified]
   - RxConnexion (size unknown) reached RxPOA preferred-vendor status in 2025. [Verified]
   - Admission rate, and what follows admission, are [Unknown].
   - Liberty's AAP landing page offers only a demo form, so even large partners still have to sell one pharmacy at a time.
8. **Ops/legal:** Any PHI makes HIPAA/BAA obligations apply. US healthcare credibility is needed. Delivery is remote, so it can run from Israel. Capital stays low unless the co-op requires paid marketing packages; their prices are [Unknown] (the media kit is a publuu flipbook and was not parsed).
9. **Labour:** Once endorsed, the co-op's email and events channel can run without the founder. Each pharmacy still needs onboarding.
10. **Unit economics [Hypothesis]:** 40 pharmacies × $129 × ~85% after co-op discount ≈ $4.4k/month gross, minus hosting and support. That is Track A only if 40 pharmacies convert. Track B needs several co-ops.
11. **Risks:**
    - The co-op builds or bundles the tool itself, or a funded vendor gives it away free (the Nimble precedent).
    - HIPAA liability.
    - A long sales cycle even after endorsement.

### C2. Contractor prequalification / approved-vendor compliance, sold through the platforms' partner programmes or insurance brokers
1. **Concept:** A productised, AI-assisted service, with software around it, that gets small contractors onto large buyers' approved-vendor lists and keeps them there. This covers:
   - safety-programme writing;
   - ISN's RAVS safety questionnaire answers;
   - certificate-of-insurance tracking;
   - document renewals.

   Distribution is borrowed through **Avetta's Partner Program** (it has a "Consulting" partner category) and/or commercial insurance brokers who already own contractor relationships.
2. **Customer/geo:** US and Canadian specialty contractors with 5–75 staff that must be ISNetworld/Avetta-compliant to keep industrial, energy or utility clients.
3. **Model/price:** Annual retainer. PrequalPilot's post claims consultants charge **$150–300/hour or about $5,000/year** [Anecdote/vendor claim: producthunt.com/p/prequalpilot, accessed 2026-10-13]. Its own founding price is $299/year. Contractors already pay the platforms: one Capterra reviewer reports a **$2,400** Avetta connection charge [search snippet, unverified].
4. **Spending evidence (forced spending):**
   - ISNetworld: 680–850 hiring clients and 75–85k contractors.
   - Avetta: 450+ hiring clients and 125k contractors.

   [Secondary: deltawye.com comparison "as of 2025"; figures inconsistent within the page]. Consultant revenue is [Unknown].
5. **Competitors:**
   - Many safety/compliance consultants. Avetta lists consulting partners by region. [Verified: avetta.com/partner-program]
   - AI newcomers such as PrequalPilot.
   - The platforms' own AI: Avetta "Safety Advisor", sold as "OSHA-trained AI guidance". [Verified: avetta.com/plans]
   - Dislikes: ISNetworld is rated 2.7/5 by 37 Capterra users [search snippet], which suggests contractor pain with the platforms.
6. **Entry strategy:** A narrow trade (e.g. electrical or industrial-painting subcontractors in one province or state), a lower price than human consultants, done-for-you rather than DIY. This is credible but **not differentiated from PrequalPilot**.
7. **Acquisition and newcomer evidence:**
   - The one AI newcomer found, PrequalPilot, shows **6 views** on Product Hunt after about 6 months and is in "private beta, 10 spots remaining". [Verified, 2026-10-13]
   - That is weak evidence the DIY-tool route sells.
   - Avetta's partner directory proves consultants are listed. How many leads it hands them is [Unknown].
8. **Ops/legal:** Remote delivery is possible. Safety programmes must meet OSHA or provincial rules, and a mistake costs the client its approval, so liability is real. Some RAVS questions are signed off by the contractor; the founder would act as a preparer.
9. **Labour:** Mixed. It starts as a service, and AI drafting plus templates per trade could lift margins. It risks becoming "selling hours", which the founder wants to avoid.
10. **Unit economics [Hypothesis]:** 25 clients × $2,000/year ≈ $4.2k/month at roughly 60–70% margin once templated. That fits Track A. Track B would need broker or platform distribution.
11. **Risks:**
    - The platforms automate the service away (Avetta's AI is already here).
    - No proof the partner directory produces leads.
    - Liability for safety documents.

### C3. Franchisor-mandated operations module for emerging franchise systems (20–200 units)
1. **Concept:** Sign the franchisor once. Get written into the operations manual and FDD as the required or approved tool for one job, and bill per unit monthly. Example jobs: brand-standards audits, local-marketing approvals, or state-specific licensing/inspection tracking for service franchises.
2. **Customer/geo:** US franchisors. Payment is by the franchisor (tech fee pass-through) or directly by franchisees.
3. **Model/price:** Per location per month. The franchisor may take a rebate: one commentator gives "3% of franchisee purchases from a technology vendor" as an example. [Secondary: thelawdept.com, via search snippet]
4. **Spending evidence:**
   - Item 8 must disclose required suppliers and franchisor revenue from them. Item 6/11 disclose technology fees. Rebates are "often" received. [Secondary: thelawdept.com, heritagelawwi.com, franchiselawsolutions.com via snippets]
   - The IFA 2022 Legal Symposium paper confirms the franchisor "normally will retain sole discretion for approving new suppliers", and that franchisees may request approval of a new supplier. [Verified: franchise.org PDF text extracted, accessed 2026-10-13]
   - **No per-unit tech-fee figures were verified**, because the FDD portals were blocked.
5. **Competitors:** Not verified in this phase. Known franchise software categories include FranConnect, Naranga and FranchiseBlast-type tools. [Unknown in detail; treat as crowded]. Franchisee pushback on required vendors is rising: a Zarco 2026 piece is titled "required vendors… supply-chain squeeze" (403 when fetched; title only).
6. **Entry strategy:** Pick one vertical (e.g. home-services or kids-education franchisors) where state rules create a tracking job general franchise software ignores. **None verified.**
7. **Acquisition:** One contract → N units is the core appeal. The franchisor will want pilots and field tests first. [Secondary] Newcomer outcomes: [Unknown]. The likely route is franchise-industry events (IFA, Franchise Expo) and franchise consultants. Their productivity for a new vendor is [Unknown].
8. **Ops/legal:** Remote. FDD disclosure means the franchisor's counsel must approve. Franchisee data and privacy obligations apply.
9. **Labour:** Good once signed. Rollout and support are per system, not per unit.
10. **Unit economics [Hypothesis]:** 2 franchisors × 80 units × $39/month ≈ $6.2k/month at about 85% margin. That reaches the top of Track A, and Track B with 5–8 systems.
11. **Risks:**
    - Long, reference-driven franchisor sales cycles, the same failure mode as G-Cloud in Phase 6.
    - A franchisee revolt against mandated tech fees.
    - The franchisor switches vendors at FDD renewal.

### C4. Specialty product line pitched at hardware/LBM co-op Open Buying Days
1. **Concept:** A founder-designed specialty SKU family (e.g. a tech-enabled or niche hardware item) pitched to Do it Best at an Open Buying Day. Acceptance puts it in a catalogue that thousands of member stores order from (the co-op holds about 67,000 warehouse-stocked items).
2. **Customer/geo:** The co-op buys centrally; members reorder. US, plus Do it Best's international membership.
3. **Model:** Wholesale to the co-op's warehouse, or drop-ship programmes. Margins after co-op terms are [Unknown].
4. **Spending evidence:**
   - "Billions in annual sales"; "thousands of independent home improvement businesses"; 67,000+ stocked items. [Verified: doitbestonline.com, 2026-10-13]
   - Open Buying Day: twice yearly, $300 donation, 30-minute meeting; the next one was 2026-06-24. [Verified]
5. **Competitors:** Every hardware manufacturer. Ace, and Orgill as a distributor, have similar gates (Ace was Cloudflare-blocked; Orgill's vendor page returned 404).
6. **Entry strategy:** Only with a genuinely differentiated product. **This overlaps Agent B's physical/wholesale lane**, so it is listed for completeness.
7. **Acquisition/newcomer:** The pitch slot is cheap ($300) and documented. Acceptance rates and sell-through for new vendors are [Unknown]. Item setup and EDI requirements are [Unknown] (they sit behind the vendor portal).
8. **Ops:** Inventory, US warehousing, product liability insurance, and EDI. Capital likely exceeds $2k (**flag**). Running it from Israel requires a 3PL.
9. **Labour:** Good once listed (reorders), but inventory risk is high.
10. **Unit economics:** [Unknown].
11. **Risks:** Capital, inventory, slow-moving stock, and co-op deductions.

### C5. Tech partner to independent insurance-agency alliances (SIAA TechFinder and similar)
1. **Concept:** A narrow tool for independent P&C agencies, listed in SIAA's **TechFinder** portal ("vetted" tools with "Tech Discounts") and in equivalent programmes run by other alliances and state Big "I" associations.
2. **Customer/geo:** US independent agencies. SIAA has 49 master agencies and $18.1B written premium. [Verified: siaa.com/about-siaa/the-siaa-model, 2026-10-13]
3. **Model:** Per-agency SaaS with a member discount. The alliance's fee from vendors is [Unknown]. Minnesota Big I runs a paid "Power in Partners" vendor membership [snippet; page fetch failed].
4. **Spending evidence:**
   - Agencies pay alliances sign-up and monthly fees and often must use a specified AMS (agency management system). [Verified: IA Magazine, 2025-09-01]
   - SIAA claims its Tech Stack saves members "up to 55%". [Verified page; vendor claim]
5. **Competitors:**
   - SIAA's own AgencyIQ, which already covers BI, predictive analytics, coverage gaps and sentiment, and is included in membership.
   - AMS and comparative-rater vendors (Applied runs an Alliance Partner Program).
   - Website and mobile-app partners.
6. **Entry strategy:** None credible found. The obvious AI/analytics wedge is already taken in-house.
7. **Acquisition:** A TechFinder listing is a directory. Under the methodology, directory listings are not credited as a channel without newcomer data, and none was found.
8–11. Remote and low capital. Phase 1 already excluded insurance commission reconciliation. **Weak; kept only to document the pattern.**

### C6. Veterinary management-group / buying-group preferred partner
1. **Concept:** Sell a practice tool or specialty consumable to independent vet hospitals through VMG's purchasing programme (about 60 preferred partners) or similar groups.
2. **Customer:** US independent veterinary practices. VMG peer groups have 18–22 practices each; total membership is [Unknown].
3. **Model:** Partners fund the group. VMG reports **$1.5M+ "in meeting sponsorship support"** and **$230M+ "rebates and upfront savings from top six partners"**. Visible partner logos: Antech, Elanco, Merck Animal Health, FedEx, Scrubin. [Verified: myvmg.com/membership/purchasing-program, counter values in page source, accessed 2026-10-13]
4. **Evidence:** Real money flows, but it is dominated by pharma, diagnostics and nutrition majors. A Strategic Opportunities Committee selects partners for "long-term" relationships.
5. **Entry strategy:** None credible for a solo founder. The pay-to-play is sponsorship plus rebates at a scale far above $2k.
6–11. Killed on capital and incumbency. It stays on the list only because the programme's economics are now quantified.

---

## 2. Israeli channels examined

- **Mishkei HaKibbutzim** (משקי הקיבוצים):
  - An agricultural cooperative society founded in 1996. It was the national purchasing organisation of the kibbutz movement from 2003 and is now a holding group. **284 members, of which 279 are kibbutzim.** [Verified: mishkei.co.il/about, 2026-10-13]
  - It runs joint purchasing (רכש משותף), leasing, insurance, communications, energy and a consumer card (Meshekard).
  - It owns **Mekomi-net**: messaging app, digital ballot, community site, emergency-squad (Tzachi) module, service calls, forms, real-time personal finance, cash-register interfaces, payment clearing, and a regional-council messaging and 106-hotline interface. **Mekomi is now free for all.** [Verified: mishkei.co.il/mekominet; mekome.net]
  - It runs agricultural-security analytics with G1 and "Bayit BaKibbutz" (construction).
  - **Verdict:** the channel owner already supplies the software a technical founder would sell. The only opening is as a module/OEM supplier to Mekomi-net, which is Agent D's lane, with no evidence they buy outside. **Killed for C.**
- **Mashcal** (Israeli Municipal Economic Corp., owned by the local and regional government centres):
  - Runs framework tenders for local authorities, a franchisee (זכיינים) pool joined by email, a "rapid price-quote procedure", IT/cyber framework tenders, and the MIC innovation centre.
  - MIC lists about **491 solutions** (29 + 49 + 24 + 30 + 34 + 98 + 105 + 38 + 17 + 46 + 21 Beta Zone). [Verified: mashcal.co.il, mic.org.il, 2026-10-13]
  - The ledger excludes "Israeli government procurement". Mashcal is the municipal variant, but it is still tender-based, scale-favouring and directory-like. **Killed** (not materially different).
- **Histadrut / workers' committees:** consumer perks channel, so this is Agent A's lane. Not examined.
- **Health-fund supplier lists:** not examined (searches exhausted). Likely tender/registration-based like the government channel. [Unknown]

---

## 3. Ideas killed and why

| Idea | Why killed |
|---|---|
| Kibbutz software via Mishkei | The channel owner's own Mekomi-net covers it, and the app is now free |
| Mashcal/MIC municipal supply | Ledger exclusion (Israeli procurement); ~491-solution directory; tenders favour scale |
| DSO / dental GPO vendor | No public vendor-approval or fee data (1 search wasted). DSOs centralise procurement under MSAs (management services agreements); ADSO industry membership is pay-to-play (fees not seen) |
| Vet buying groups (C6) | Partners are pharma/diagnostics majors; sponsorship-funded; capital far above $2k |
| SIAA/agency-alliance tech (C5) | In-house AgencyIQ plus bundled Tech Stack; the TechFinder listing is a directory |
| Insurer claims/repair vendor networks | Physical field services (TPA contractor networks); not a solo-technical fit; not pursued |
| Generic "software for franchisees" | Franchisors hold sole discretion; franchisee tech-fee backlash; FDD evidence unobtainable by script |
| Do it Best/Ace tech partnerships | Partners are Paycor/Paychex, Epicor and CareerPlug, and the co-op runs its own tech centre. Only the merchandise route (C4) is open to newcomers |

---

## 4. Ranking, top picks, decisive assumptions

Ranking, all with weak evidence. Expected scores sit in the low-to-mid 40s, below the board's #2–#12 cluster.

1. **C2 Contractor prequalification compliance via Avetta partner programme / brokers.** It is the only channel where the buyer's spending is **forced** (no approval means no work), the customer base is large (about 200k contractor accounts across two platforms), and the gatekeeper runs a public partner directory for consultants. Against it: the platform's own AI and a stalled AI newcomer.
2. **C1 Pharmacy co-op preferred partner.** It has a documented intake process, real precedents of software endorsed to thousands of pharmacies, and gatekeepers that actively look for partners. Against it: free funded competitors, co-op in-house tools, and no gap verified.
3. **C3 Franchisor-mandated module.** It has the best "one contract → N units" economics, but zero verified figures this phase, and the sales cycle looks like G-Cloud's.
4. C4 Co-op Open Buying Day (physical; flag to Agent B).
5. C5 Agency alliances.
6. C6 Vet groups.

**Top 2–3 for deep diligence and the decisive unverified assumption for each:**
- **C2:** Does Avetta's consulting-partner directory, or any broker partnership, produce paying contractor clients for a **new** consultant? And will contractors pay about $2k/year when Avetta bundles an AI "Safety Advisor"? Test: read Avetta/ISN partner-programme terms in full, count consulting partners per region, and sample them for size and age. Ideally find any public statement of partner-sourced leads.
- **C1:** Is there one pharmacist task, not covered by PMS vendors or co-op tools, that pharmacies pay for monthly, and will AAP/IPC endorse an unknown vendor without a paid marketing package? Test: obtain the AAP media-kit price list (flipbook), inventory the co-ops' preferred-partner categories, and find any partner under 3 years old.
- **C3:** Do emerging franchisors' FDDs show per-unit technology fees for tools from small vendors (under 20 staff), and how often do vendors change between FDD years? Test: a human pulls 20 FDDs (Item 8 and Item 11) from the California DFPI or Wisconsin DFI portals in a normal browser and tabulates required tech vendors, fees and rebates.

**Search count:** 8 / 8 WebSearches (3 effectively wasted: the two FDD explainer searches and the DSO search).

**Access notes:**
- Blocked (not bypassed): WI DFI, CA DFPI docqnet search, MN CARDS, NASAA EFD, Franchimp, Vetted.biz, Ace Hardware corporate, IPC/PSAORx sites, zarcolaw.com, heritagelawwi.com, businesswire.com.
- The AAP partner list requires login, so it was not accessed.
- One process note: an early SEC EDGAR full-text-search request was sent with the user's email in the User-Agent header. That was an error on my part; later requests used a generic header.
