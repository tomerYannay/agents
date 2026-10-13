# Phase 7: Borrowed, Contracted and Inherited Distribution

**Date:** 2026-10-13
**Branch:** `local-research-phase6-10`
**Working files:** `research-notes/phase7/` holds the six agent reports, the leader re-check, the shortlist audit, the red-team report and the shortlist.

---

## Bottom line

**One Phase 7 idea reaches the top cluster: a self-serve integration API for Sage 50 US/Canada desktop accounting (M1), at 52.0.**
- It ties for #3 on the cumulative board, within noise of everything from #2 to #12.
- It is modelled on Conductor, a solo-founder QuickBooks Desktop API. Conductor's figures, Stripe-verified on TrustMRR, are:
  - $42,133 MRR
  - $476k all-time revenue
  - 271 subscriptions
  - founded July 2022

  Its Product Hunt launch got 4 upvotes. That makes it the first verified newcomer success in seven phases that did not depend on bringing an audience.
- **No self-serve Sage 50 US/Canada API was found.**
  - Codat and Hyperext cover the UK and Ireland only.
  - Rutter sells Sage 50 only on enterprise contracts.
  - Merge has none.
  - Apideck lists Sage 50 as "upcoming" without saying which region.
- **But the market is much smaller than QuickBooks Desktop's, and a fast follower could close the gap.**
  - Sage's US revenue is mostly Sage Intacct.
  - Sage 50 US and Canada are separate codebases.
  - The SDK is 32-bit, .NET 4.7, and gated behind a developer-partner programme whose resale terms are not public.
  - The red team's central estimate is 10–20% of Conductor's MRR after three years: Track A, not Track B.

**The direction "borrow someone else's distribution" mostly failed on evidence.** Agents measured or checked about 20 partner channels:
- employer perks portals
- school-voucher marketplaces
- insurer prevention catalogues
- HSA/FSA checkout
- Faire
- creator merch
- co-ops and buying groups
- franchisor supplier programmes
- telecom-advisor distributors
- payments agents
- Shopify and Odoo partner directories
- Pax8
- MCP and AI-agent registries

In each case either:
- the channel owner already builds the product itself;
- spending concentrates on giants (in the Arizona school-voucher marketplace, Amazon took about two-thirds of spend); or
- the channel gives a newcomer an application form, not sales.

The one channel with measured newcomer flow, the Shopify Partner Directory in mid-size markets, sends work to **service** firms. Of 89 partners that joined in 2024 or later in six markets, 67% have zero client reviews and 9 have five or more in the last 12 months. Germany: 0 of 29. Brazil: 5 of 16.

**Leader corrections continued:**

| Leader | Was | Now |
|---|---|---|
| UK MTD prep | 52.6 | **50.2** |
| J1 memoir books | 51.0 | **48.6** |
| H10 ketubot | 50.6 | **49.4** |

**Why:**
- **UK MTD prep:** offshore outsourcers (Outbooks, QX) and AI tools (Sage's MTD agent, ANNA) already sell this work, and the landlords' association already offers statement upload.
- **J1 memoir books:** MyHeritage's MyStories now has voice recording, AI editing, QR codes and 10 languages, with a Hebrew site version in testing.
- **H10 ketubot:** no sign of traction for the one newcomer that could be checked.

**After Phase 7, every leader from Phases 1–5 except H7 has been checked against newcomer outcomes, and every one was lowered.** H7 (56.6) is nominally #1. The next 13 ideas sit between 48.6 and 52.2.

---

## 1. Research methodology

**Unchanged:**
- Six discovery agents (A–F).
- A parallel leader re-check auditor.
- A shortlist of 12, then an independent Evidence Auditor and an independent Red-Team Investor.
- Rescoring with the frozen rubric, published at criterion level.
- No changes to weights, criteria, formula or penalty range.

**Search use (73 WebSearches, all logged in `research-notes/search-log.txt`):**

| Role | Searches |
|---|---|
| Discovery agents | 8 each, except F with 9 log lines (one over its cap of 8, or one duplicate log line; I could not tell which) |
| Leader auditor | 10 |
| Shortlist auditor | 6 |
| Red team | 8 |

**Primary and public data used:**
- TrustMRR Stripe-verified revenue pages
- the Shopify Partner Directory (507 partner profiles, scripted)
- the Odoo partner directory (4,443 partners)
- the Odoo App Store
- the MCP Registry (13,953+ servers, with listing dates)
- the Printful catalogue API
- the Makeship product pages
- the ScanSource 10-K
- Sage FY25 results
- Texas Comptroller and Arizona ESA pages
- ZPP/GKV certification criteria (the 2026 edition, via a Wayback copy)
- the Shopify partner revenue-share FAQ
- rossmartin.co.uk MTD statistics
- MyHeritage MyStories page source

**Blocked:**
- Faire (including robots.txt)
- Sage developer and partner PDFs
- the GKV criteria PDF (live copy timed out)
- US state franchise-disclosure databases (Cloudflare or 403)
- Channel Futures
- MANA's members-only PDF
- the Odyssey vendor page
- Etsy, The Knot, Trustpilot
- the Xero App Store
- Tiendanube's directory

Nothing was bypassed.

**Process incident (disclosed):**
- Agent C sent one read-only SEC EDGAR request with the user's email address in the User-Agent header. EDGAR asks automated clients to identify themselves, which is probably why.
- No other personal data was sent.
- The shared brief now forbids personal identifiers in any request header, URL or payload.
- I searched the saved scripts and found no other occurrence. I cannot fully rule out the same pattern in Phase 6's EDGAR requests, because inline commands leave no files.

**Boundaries kept:** no browser or signed-in account, nobody contacted, no purchases, sign-ups, builds or deployments.

---

## 2. Research direction and why

**Phase 6 had shown** that on 11 channels newcomers without an audience or references get close to nothing. Acquisition, not product, is the constraint.

**Phase 7 therefore asked:** where can a founder *borrow* distribution from someone who already owns the customer?

| Agent | Phase 7 assignment |
|---|---|
| A Consumer | Consumer offers sold through employers, insurers, banks, schools, clinics; revenue share with creators |
| B Physical | Wholesale to retailers; private label for audience owners; gifting; institutional channels |
| C Traditional | Franchisors, buying groups and co-ops, insurer networks, kibbutz and municipal purchasing |
| D Software | OEM, embedded and white-label software sold to vendors who own customers; localisation modules |
| E Distribution | Partner programmes, distributor line cards, referral deals, measured for newcomers |
| F Contrarian | Commission agencies, reverse licensing, AI-agent buying as a channel |

A parallel auditor re-checked UK MTD prep, J1 and H10.

---

## 3. Research universe (about 45 ideas)

| Agent | Viable ideas (key evidence) | Killed (reason) |
|---|---|---|
| **A** | **German insurer-reimbursed online prevention courses in Russian, Ukrainian, Turkish or Arabic** (about 1.9M insured used courses in 2024; certification free; medizen €149, 1,788 reviews) · **Texas school-voucher-funded programme for children with special-education plans** (73k+ accounts; 54k products from about 2,400 vendors) · Israel's Ministry of Education Gefen programme catalogue · HSA/FSA eligibility · Perks portals | Library e-resources · Bank and card offers · Telco bundles · Germany's prescribed health apps (DiGA, capital) · Japan's furusato nozei · Student discounts · Israeli meal and perks networks · Employee spending accounts · Building creator-branded apps for a revenue share (App Store: 0–293 ratings) |
| **B** | **Children's-artwork fundraisers through schools** (Square 1 Art pays schools 33–38%) · **Souvenir lines for each location, sold wholesale** (Lantern Press has 10,750+ SKUs) · **Presale merch for creators** (Makeship minimum runs of 200–500) · Corporate gifting · Pet memorials · Club merch | A generic print-on-demand brand on Faire (print-on-demand cost makes keystone wholesale impossible) · US school spirit wear · UK school-art fundraisers (crowded) · Plush-only Makeship clone · Practitioner supplements · Trade shows · Israeli corporate gifts · Paper goods |
| **C** | **Contractor prequalification (ISNetworld/Avetta)** · **Pharmacy co-op preferred partner** · Franchisor operations tool · Do it Best Open Buying Day · Insurance-agency alliances · Vet groups | Kibbutz software (Mishkei owns a free platform) · Mashcal municipal supply · Dental support organisations · Insurer claims networks · Franchisee software · Co-op technology partners |
| **D** | **Sage 50 US/CA integration API** (Conductor analogue) · **Licensed niche data API** (SoldComps $21.6k MRR) · Single-country fiscal API (Verifacti; fiskaly 1,900+ customers) | German e-invoice API (€9.99, open source) · Dental/vet practice-system bridges (Sikka) · White-label tools for agencies · Bank calculators (CalcXML) · Tools for accounting firms (overlaps UK MTD) |
| **E** | **Israeli Shopify launch-and-migration studio** (Shopify's new revenue share of 20% of subscription plus 0.1% of sales for 4 years) · Brazil and Türkiye variants · Odoo entry-tier vertical partner · Tiendanube partner · Pax8 tool | Odoo App Store modules (88–92% have zero purchases) · Israeli Odoo compliance (Layline) · Telarus supplier · Buying Shopify revenue-share books · Accountant referral deals · Shopify partner in Germany (0 of 29) |
| **F** | **US technology advisor under a master agent** (Intelisys $2.88B billings) · **Payments-residual agent** · Buying residual books · Reverse licensing · UK/EU commission agent | Classic US manufacturer's rep · Selling through Instant Checkout (pulled back; about 30 Shopify merchants) · Master licence of foreign SaaS · Art licensing · Buying dormant brands · Being a supplier to AI agents (MCP Registry new listings rose from 56 in Jan 2026 to 3,911 in Sep 2026) |

**Market-level facts established:**
- **Partner directories behave like gated marketplaces.** About two-thirds of new Shopify partners got no client reviews; about 10–15% got steady work, and only in less-saturated markets. Older paid Odoo App Store listings: 88–92% have zero purchases.
- **Channel owners build their own software.** The pharmacy co-ops (AAP, EPIC), the insurance-agency alliance SIAA (AgencyIQ), Mishkei HaKibbutzim (Mekomi), Avetta (AI adviser) and Do it Best all do.
- **Voucher and benefit money concentrates on giants.** Arizona ESA marketplace: Amazon about two-thirds; Outschool $12M of $30M online.
- **AI-agent commerce isn't yet a channel for small suppliers.** OpenAI pulled Instant Checkout back into apps in March 2026. MCP Registry supply is flooding.
- **Telecom/IT technology advisory is a large, high-margin market.** Intelisys: $2.88B billings, segment gross margin 98.6% (ScanSource 10-K). It publishes nothing on what new advisors earn.

---

## 4. Shortlist (12)

| # | Business | Paying customer | Spending evidence | Main competition | Differentiation | Acquisition | Capital | Main risk |
|---|---|---|---|---|---|---|---|---|
| M1 | Sage 50 US/CA integration API | SaaS vendors and fintechs needing Sage 50 data | Conductor (QuickBooks Desktop) $42k MRR, verified | Rutter (enterprise), Zynk connectors (snippet), possible Apideck | Self-serve, priced per company | Developer search, docs, reseller vendors | Low (SDK fee) | Small market; Sage terms; Windows agent support |
| M2 | Licensed niche data API (dataset not yet chosen) | Developers | SoldComps, BestTime | Varies | Varies | Developer search, API marketplaces | Low | No clean-rights dataset identified |
| M3 | Prevention courses in foreign languages (Germany) | Insured migrants, refunded by insurers | 1.9M participants in 2024 | 115k certified offers | Language | Insurer database, community | Low | Course-leader labour; one-off refunds |
| M4 | Texas voucher-funded programme for children with special-education plans | Families paying from voucher accounts | 73k+ accounts | Outschool, Amazon, tutors | Specialised programme | Voucher marketplace | Medium | **Credentialed lead educator rule** |
| M5 | Children's-art fundraisers through schools (new country) | Parents, via schools | Square 1 Art (US) | UK providers; target country unknown | First in country | School outreach | Medium | School rules; uptake |
| M6 | Souvenir lines for each location, sold wholesale | Gift shops, museums | Lantern Press | Lantern Press, local artists | — | Faire, sales reps | Medium | Thin margins; AI art stigma |
| M7 | Presale merch for creators | Creators' fans | Makeship | Makeship (licensed IP) | Underserved niche | Creator outreach | Low | Winning creators |
| M8 | Contractor prequalification service | Small contractors | Must pay to keep working | Consultants; Avetta's AI | — | Avetta directory (24 partners, no lead terms) | Low | Services; no channel |
| M9 | Pharmacy co-op preferred partner | Independent pharmacies | Co-op intake | Co-op tools; free funded apps | None identified | Co-op endorsement | Low | No task identified |
| M10 | US technology advisor under a master agent | SMBs buying telecom, cloud, security | Intelisys 10-K | 4,000+ advisors (Telarus, 2022) | One vertical | Founder selling, sub-agents | Low | No US relationships; eligibility |
| M11 | Payments-residual agent | Vertical-software vendors | Processor residuals | Stripe Connect pays vendors directly | — | Outreach | Low | Cut out by payments platforms |
| M12 | Israeli Shopify launch-and-migration studio | Israeli merchants | Measured newcomer client reviews | SEDER Studio and others | Hebrew, fixed price, contractors | Shopify Partner Directory | Low | Agency labour; directory listing is discretionary |

---

## 5. Adversarial review

### New candidates

| Idea | What held up | What was contradicted or weakened | Hard blocker? | Effect |
|---|---|---|---|---|
| **M1** | Conductor's revenue figures replicate exactly. No self-serve Sage 50 US/CA API exists. Codat and Hyperext are UK/Ireland only. Rutter is enterprise-only. Merge has none. | **The market is small:** Sage US revenue is mostly Intacct (£461m of £997m); QuickBooks Desktop's ecosystem is far larger ($2.775B in Intuit FY25 revenue, as cited by Conductor). **Two products:** Sage 50 US and Canada are separate codebases. **No equivalent of Intuit's Web Connector**, so a Windows agent is needed on each customer machine. The SDK is gated (a developer programme with fees), 32-bit and .NET 4.7; a long-time partner says developers are leaving it. **Resale terms are not public.** Conductor is listed for sale (asking $1.25M), so a buyer could add Sage. Apideck shows Sage 50 as "upcoming". **Unit correction:** Conductor's 271 subscriptions average about $155, so they are vendor accounts, not company files. Track A therefore means about 10–30 paying software vendors. Demand signals are thin (4 "+1"s on Zapier). | **Possible:** Sage resale terms | Hold; top of Phase 7, Track A only |
| M2 | SoldComps and BestTime revenue verified | SoldComps' revenue is a recent spike (all-time $49k). It scrapes eBay and sells through Apify and RapidAPI, so it isn't "search pull without an audience". BestTime isn't a newcomer and is for sale. No dataset named. | — | Down |
| M3 | Certification criteria verified. The provider's location doesn't matter. EU psychology and sport-science degrees are recognised. | The language rule for online courses is not addressed in the criteria (the FAQ allows other languages for courses, and the red team reads that as covering this format). 100% completion is required for a refund. Each participant needs 24 minutes of communication and experts must reply within 48 hours. Refunds are one-off (€75–150, at most 2 a year). | No | Down |
| M4 | Texas figures verified | **The 7 Jul 2026 educator policy requires a credentialed, fingerprinted lead educator continuously present.** Vendors must be registered to transact business in Texas. Spending concentrates on Amazon and Outschool (Arizona data). | **Yes** | **Kill** |
| M5 | Square 1 Art's school share verified | A fourth UK provider exists. Competition in Germany, the Netherlands and Israel is unknown. | No | Down |
| M6 | Lantern Press catalogue verified | Print-on-demand cost can't support keystone wholesale. "Hand-drawn by humans" is part of the category's positioning. | Margin | **Kill** |
| M7 | Makeship terms verified | Makeship is moving to licensed IP. Winning creators is unproven. | — | **Kill** |
| M8 | Contractors must comply | Avetta's partner page lists 24 partners and gives no lead terms. Avetta ships its own AI adviser. The AI newcomer is still in beta. | — | Down |
| M9 | AAP intake verified | No uncovered monthly task. Co-ops sell their own tools. | — | Down |
| M10 | 10-K figures replicate | The segment includes advisory. Organic growth is 2.3%. No newcomer earnings data. Eligibility for non-US advisors unknown. | Possibly eligibility | Down |
| M11 | — | Stripe Connect and similar pay the vendor directly. Splits unknown. | — | Down |
| M12 | Directory statistics replicate (Israel 1/5, Poland 1/13, Brazil 5/16, Mexico 0/6, Türkiye 2/20, Germany 0/29). Revenue-share terms verified. | It is a services business. The revenue share is only about $94 a year per Basic store and applies only to stores the partner builds. Entry-tier listing is discretionary. The Israeli rate rests on 5 partners. | No | Hold as a cash bridge only |

### Leader re-check: decisions

| Leader | Criterion changes adopted | CF / Scal / Dist | Balanced | Penalty | Adjusted |
|---|---|---|---|---|---|
| UK MTD prep | Defensibility −1 (−3), Proven channel −1 (−6) | 61 / 63 / 53 | 60.2 | **10 (kept)** | **50.2** (was 52.6) |
| J1 memoir books | Defensibility −1 (−3), Proven channel −1 (−6) | 68 / 52 / 58 | 59.6 | 11 | **48.6** (was 51.0) |
| H10 ketubot | Proven channel −1 (−6) | 76 / 47 / 61 | 61.4 | 12 | **49.4** (was 50.6) |

**How the disagreements were resolved:**
- **UK MTD penalty:** the leader auditor proposed raising it from 10 to 11 (49.2). The shortlist auditor called that double counting, since the same evidence already cut defensibility, and the red team said the two roughly cancel. I kept the penalty at 10, consistent with Phase 6's rule: raise the penalty only when the decisive assumption is directly contradicted.
- **J1:** the red team argued market depth should also drop (to 47.4), because the Russian-speaking segment is largely served. The other two reviewers accepted 48.6. I adopted 48.6 and record the dissent.
- **Baselines:** the Phase 2–4 reports never published criterion scores for these three ideas. The auditor rebuilt baselines that reproduce the published totals, and only the changes are recommendations.

**H7 (56.6):**
- Both reviewers consider it defensible as nominal #1, but only as "first among a tie".
- It is the only leader whose channel was measured on newcomer unit sales.
- Its newcomer data dates from Phase 5 (2025–26 listings). Re-measuring it is the cheapest remaining leader check. The red team estimates that if the median newcomer now sells under 5 copies, H7 falls to about 53.

---

## 6. Phase 7 scoring (frozen rubric, criterion level)

Step values per criterion:

| Score | Step value |
|---|---|
| Cash flow | Spending ×5 · Speed ×4 · Capital ×4 · Margin ×4 · Labour independence ×3 |
| Scalability | Depth ×3 · Recurring ×4 · Acquisition ×4 · Leverage ×4 · Defensibility ×3 · Founder fit ×2 |
| Distribution | Clarity ×4 · Discoverability ×4 · Proven channel ×6 · First customers ×3 · Beyond founder ×3 |

| ID | CF steps | **CF** | Scal steps | **Scal** | Dist steps | **Dist** | Balanced | Penalty | **Adjusted** |
|---|---|---|---|---|---|---|---|---|---|
| M1 Sage 50 US/CA API | 3,2,4,5,3 | 68 | 2,5,2,4,1,5 | 63 | 4,3,2,2,4 | 58 | 64.0 | 12 | **52.0** |
| M2 Licensed data API | 2,2,4,4,4 | 62 | 2,5,2,4,1,5 | 63 | 2,2,1,2,3 | 37 | 57.4 | 13 | **44.4** |
| M12 Israeli Shopify studio | 4,3,5,3,1 | 67 | 2,2,2,2,1,3 | 39 | 4,3,3,2,2 | 58 | 54.0 | 10 | **44.0** |
| M10 US technology advisor | 4,1,5,5,1 | 67 | 5,5,1,2,2,1 | 55 | 3,2,1,1,2 | 35 | 55.8 | 12 | **43.8** |
| M3 Foreign-language prevention courses | 4,2,4,3,2 | 62 | 3,1,2,2,2,1 | 37 | 4,3,2,2,3 | 55 | 50.6 | 11 | **39.6** |
| M9 Pharmacy co-op partner | 2,1,4,4,3 | 55 | 3,5,2,3,1,3 | 58 | 3,3,1,1,3 | 42 | 53.6 | 14 | **39.6** |
| M8 Contractor prequalification | 3,3,5,3,1 | 62 | 4,4,1,2,1,2 | 47 | 4,2,1,2,1 | 39 | 51.4 | 13 | **38.4** |
| M5 School art fundraisers | 3,2,3,3,2 | 53 | 3,2,2,3,1,1 | 42 | 4,3,2,1,2 | 49 | 47.8 | 13 | **34.8** |
| M4 Texas voucher programme | 4,1,2,3,1 | 47 | 3,3,2,2,1,1 | 42 | 4,3,1,1,2 | 43 | 44.2 | 12 | **32.2** (kill: hard blocker) |
| M11 Payments-residual agent | 3,1,5,4,2 | 61 | 3,5,1,2,0,2 | 45 | 2,1,0,1,1 | 18 | 46.0 | 14 | **32.0** |
| M6 Souvenir wholesale | 3,2,2,2,2 | 45 | 2,3,1,3,1,1 | 39 | 4,2,1,1,2 | 39 | 41.4 | 13 | **28.4** (kill) |
| M7 Creator presale merch | 3,2,3,2,2 | 49 | 2,1,1,2,0,1 | 24 | 3,1,1,1,1 | 28 | 34.8 | 13 | **21.8** (kill) |

**Key judgement calls:**
- **M1:**
  - Spending evidence is 3/5: a strong analogue on a larger platform, not direct Sage 50 US spending.
  - Defensibility is 1/5, because Rutter could open its connector, Apideck has one "upcoming", and Conductor's buyer could add Sage.
  - Penalty is 12, not 11: the Sage resale terms could be a hard blocker and the market size is unmeasured.
  - The red team's range was 48–53.5 (central 51); the auditor suggested penalty 11.
- **M12:** proven channel is 3/5, the highest Phase 7 value, because newcomer flow was measured. Labour independence is 1/5 and recurring revenue 2/5, because it is agency work.
- **M10:** depth and recurring revenue are 5/5, but proven channel is 1/5 and founder fit 1/5.

**Comparison with the red team's independent ranges:**
- M1 52.0 vs 48–53.5 (inside).
- M12 44.0 vs 41.8; M10 43.8 vs 42.0; M3 39.6 vs 40.8; M8 38.4 vs 37.2.
- M2 44.4 vs ≤45.8; M5 34.8 vs 35.0; M11 32.0 vs 35.0.
- M4 32.2 vs 29.4 (killed either way).

---

## 7. Five finalists: deep dives

**Selection:** the top five by score are M1, M2, M12, M10 and M3. M2 is kept as a pattern finalist (an infrastructure API sold to developers) even though no dataset is named. It shares M1's channel logic and was the other Phase 7 idea with verified newcomer revenue.

### F1. Sage 50 US/Canada integration API (M1): 52.0

- **Offer:**
  - A hosted REST API giving SaaS vendors and fintechs read/write access to their customers' Sage 50 company files.
  - Delivered through a small Windows connector installed beside Sage 50, with the vendor's customer onboarding themselves.
  - Priced per connected company, about $45–49/month, matching Conductor.
  - Start with Sage 50 US only, then Canada (a separate codebase), then Sage 100.
- **Customers:** vertical SaaS for construction, field service, property management, distribution and payroll whose own customers keep their books in Sage 50; plus payments and lending fintechs.
- **Spending evidence:**

  | Fact | Status |
  |---|---|
  | Conductor (QuickBooks Desktop): $42,133 MRR, 271 subscriptions (about $155 each), $476k all-time, founded July 2022, no cofounders listed | **[Verified: TrustMRR, Stripe-connected]** |
  | Conductor pricing $49 per company file | [Verified: conductor.is] |
  | Hyperext claims 2,400+ Sage 50 UK companies and 5 reseller vendors | [Vendor claim] |
  | Customers pay for Sage 50 US/CA access specifically | **[Unknown]** |

- **Competition:**
  - Rutter (enterprise-only Sage 50).
  - Zynk (Sage 50 US/CA connectors, snippet only).
  - Apideck ("upcoming").
  - Codat and Hyperext (UK/Ireland only).
  - Vendors building directly on the SDK.
- **Entry strategy:** be the only self-serve, documented, transparently priced option, discoverable through developer searches for "Sage 50 API".
- **Acquisition:**
  - Developer search and docs SEO, the channel Conductor appears to use (domain rating 26, 4 Product Hunt upvotes).
  - Listing on unified-API comparison pages.
  - Reseller deals with vendors, Hyperext-style.
  - CAC [Unknown].
- **Startup capital:**
  - Sage developer programme fee (a 2020 post says about $350 the first year; current fee [Unknown]).
  - A Windows test machine with Sage 50 licences, obtained through the developer programme.
  - Hosting.
  - Under $2k plausible.
- **Unit economics [Hypothesis]:** about 85–90% gross margin after hosting and support tooling. Each vendor account brings 1–10 connected companies.

  | Scenario | Paying vendors | Connected companies | Owner profit |
  |---|---|---|---|
  | Downside | 3 | 15 | ~$500/mo; Sage terms or support burden end it |
  | Base (18–24 months) | 15–25 | 80–150 | **~$3.5–6k/mo** |
  | Upside (Sage 50 US + CA + Sage 100 portfolio) | — | 400+ | **~$15–20k/mo** (depends on market size) |

- **Labour:**
  - Build: 2–4 months part-time.
  - Then support for a Windows agent across Sage versions, which is ongoing and partly delegable.
- **Key assumptions:**
  1. Sage's developer terms allow a hosted API resold to third-party vendors.
  2. Enough vendors need Sage 50 US/CA access. The red team's cheapest test is to count how many of about 200 vertical-SaaS integration pages list Sage 50 versus QuickBooks Desktop: a ratio of 0.2 or more keeps it alive, 0.08 or less kills it.
  3. No unified-API vendor opens a cheap self-serve tier first.

### F2. Licensed niche data API (M2): 44.4

- **Offer:** an API over a dataset with clean resale rights (public-domain government data, licensed feeds or the founder's own collected data) that developers embed in products.
- **Evidence:**
  - SoldComps (eBay sold prices): $21.6k MRR, founded March 2025, but only $49k all-time. It is a recent spike, it scrapes eBay, and it sells through Apify and RapidAPI.
  - BestTime: $9.3k MRR solo. It is not a newcomer (domain rating 45, $134k all-time) and is for sale at $599k.
  - fuelprice.io: $828 MRR.
  - Revenue-sorted sampling biases all of these upward.
- **Status:** a pattern, not an opportunity, until a dataset is named.
  - Phase 6 showed H6 (sports data) is already served.
  - Phase 5 showed Apify newcomers earn about nothing.

**Economics [Hypothesis]:**

| Scenario | Owner profit |
|---|---|
| Downside | $0 |
| Base | $1–3k/mo after 12–18 months |
| Upside | SoldComps-like, $10–20k/mo |

**Key assumption:** a dataset exists that developers search for, can be resold legally, and isn't already sold cheaply.

### F3. Israeli Shopify launch-and-migration studio (M12): 44.0

- **Offer:** fixed-price Hebrew store launches and migrations (from Wix, WooCommerce and Konimbo) delivered by contractors, collecting Shopify's revenue share on stores the studio builds.
- **Evidence:**
  - **The best-measured channel in Phase 7.** Of new partners (joined 2024+) in six markets, 9 of 89 reached five or more client reviews in 12 months.
  - In Israel, 1 of 5 did (SEDER Studio, 41 reviews).
  - Revenue share verified: 20% of subscription plus 0.1% of online GMV for 4 years, from 10 Aug 2026.
  - On a Basic store that is about $94 a year.
- **Competition:** existing Israeli Shopify partners and Wix/Konimbo agencies.

**Economics [Hypothesis]:** average job about $2k; contractor cost about 50%.

| Scenario | Jobs/mo | Owner profit |
|---|---|---|
| Downside | 0–1 | — |
| Base | 3 | **~$3k/mo** |
| Upside | 8 | ~$7–8k/mo, a small agency |

- **Labour:** sales, QA and account management stay with the founder. This is a services business, the model the founder wants to avoid, so it fits only as a **cash bridge**.
- **Key assumption:** an entry-tier Israeli partner gets listed and reaches 2 or more paid jobs a month within 12 months.

### F4. US technology advisor under a master agent (M10): 43.8

- **Offer:** become a sub-agent of a master agent (Telarus, Intelisys or Avant) focused on one vertical, selling connectivity, UCaaS, cloud and security. The founder earns monthly residual commissions (12–22% of the monthly invoice, snippet) and recruits referral sub-agents.
- **Evidence:**
  - Intelisys: $2.88B billings, segment net sales $101.1M at 98.6% gross margin [Verified: ScanSource 10-K, Aug 2026].
  - Residual books trade at 3–30× monthly residuals [Broker claim].
  - **No data on new advisors' earnings.** Eligibility for non-US residents is unknown.

**Economics [Hypothesis]:** residuals compound, since each $1k/month customer at a 15% commission is $150/month.

| Scenario | Customers | Owner profit |
|---|---|---|
| Downside | 0 closes in 12 months | — |
| Base | 25 by year 3 | **~$3.75k/mo** |
| Upside | Sub-agent network | $15k+/mo |

- **Labour:** heavy early founder selling of US telecom deals without a US network. Poor founder fit.
- **Key assumption:** a new advisor without US references closes deals in year 1, and a foreign-owned founder can be appointed.

### F5. German insurer-reimbursed online prevention courses in non-German languages (M3): 39.6

- **Offer:** certified 8–12-unit online courses (stress, back health, nutrition) delivered live in Russian, Ukrainian, Turkish or Arabic by qualified course leaders on revenue share. Insurers refund participants €75–150.
- **Evidence:**
  - About 1.9M insured used courses in 2024.
  - Certification criteria verified (2026 edition).
  - The provider's location doesn't matter.
  - The ZPP FAQ: "Kurse können auch in einer anderen Sprache durchgeführt werden" (courses may also be held in another language).
  - 115k certified offers from 65k providers.
  - Each course needs 100% completion for a refund, 24 minutes of communication per participant, and expert replies within 48 hours.

**Economics [Hypothesis]:** €120 average price; course leader 40% (€48); platform and payment about €10.

| Scenario | Participants/mo | Owner profit |
|---|---|---|
| Base | 60 | ~€3.7k/mo gross |

That needs acquiring about 700 participants a year with unmeasured CAC.

- **Labour:** delivery is the course leader's; the founder handles certification, scheduling and acquisition.
- **Key assumptions:** migrant communities find and complete courses at an acquisition cost under about €40, and a qualified course leader who speaks the language can be recruited.

---

## 8. Cumulative leaderboard (all phases; * = corrected in Phases 5–7)

| Rank | Opportunity | Phase | Adjusted |
|---|---|---|---|
| 1 | Blender/VRChat add-ons (H7) | 3 | **56.6*** |
| 2 | College-baseball data API (H6) | 3 | 52.2* |
| 3= | **Sage 50 US/CA integration API (M1)** | **7** | **52.0** |
| 3= | Framer vertical kit (K8) | 5 | 52.0* |
| 5 | Meshtastic family kits (H1) | 3 | 51.2* |
| 6= | monday.com Israeli invoicing app | 1 | 50.8* |
| 6= | Apify Actors (J7) | 4 | 50.8* |
| 8 | Hebrew tender + receivership intelligence (K13) | 5 | 50.6* |
| 9 | UK MTD prep for accountants | 2 | **50.2*** (was 52.6) |
| 10 | Israeli allocation verification | 1 | 49.8 |
| 11= | Ketubot (H10) | 3 | **49.4*** (was 50.6) |
| 11= | Spanish Holy Land box (H8) | 3 | 49.4 |
| 11= | Non-US availability alerts (H5) | 3 | 49.4 |
| 14 | Pay-per-call emergency lead sites (L6) | 6 | 48.8 |
| 15 | Hebrew/Russian memoir books (J1) | 4 | **48.6*** (was 51.0) |
| … | J2 48.2 · H4 48.2 · J9 48.0 · H9 47.8 · K12 47.6 · L2 46.6 · L10 46.2 · … · **M2 44.4** · **M12 44.0** · **M10 43.8** | | |

**Cross-phase verdict:**
- The board stays flat: #2–#15 span 48.6–52.2.
- **M1 is the most significant Phase 7 addition.** It isn't higher than the cluster, but it is the first top-cluster idea whose analogue is a **verified newcomer success without an audience**. Every other leader's channel evidence is either an incumbent or has now been corrected down.
- H7 is still nominal #1 by 4.4 points, within the noise band.

---

## 9. Three most promising Phase 7 discoveries

1. **Fastest cash flow: Israeli Shopify launch-and-migration studio (M12), as a cash bridge only.** It has paid jobs from the first month and measured newcomer flow in the channel.
   - *Key assumption:* an entry-tier Israeli partner gets listed and wins 2 or more paid jobs a month within 12 months.
   - It is a services business and should not be confused with a scalable one.
2. **Most scalable: Sage 50 US/Canada integration API (M1),** extendable into a portfolio of desktop accounting APIs (Sage 50 US, Sage 50 CA, Sage 100, possibly others) with recurring per-company billing and high margin.
   - *Key assumption:* Sage's terms allow a hosted resale API, and Sage 50 integration demand is at least about 20% of QuickBooks Desktop's on vertical-SaaS integration pages.
3. **Best risk-adjusted: also the Sage 50 API (M1).** It has the highest Phase 7 score, the only verified audience-free analogue, under $2k capital, and kill criteria testable at desk level (the integration-page census and Sage's terms).
   - *Runner-up:* the Shopify studio (M12), for its measured channel.

---

## 10. Research limitations

- **Unverified load-bearing facts:**
  - **M1:** Sage's resale terms and fees; the Sage 50 US/CA installed base.
  - **M10:** foreign-advisor eligibility and new-advisor earnings.
  - **M3:** whether the online-course language rule allows non-German courses, and acquisition cost.
  - **M12:** whether entry-tier partners get listed.
  - Every idea: no measured CAC.
- **Blocked sources:** Faire, Sage developer PDFs, US state franchise-disclosure databases, the live GKV criteria PDF, Channel Futures, Etsy, Trustpilot and the Xero App Store.
- **Sampling biases:**
  - TrustMRR category pages are revenue-sorted, which favours winners.
  - The Shopify directory sample includes only listed partners.
  - Makeship sold counts appear on 6 of 53 pages.
  - Two Hebrew searches returned English results, because the search engine is US-only.
- **Scoring caveats:**
  - Phase 2–4 leader baselines were reconstructed to reproduce published totals.
  - The rubric still favours low-capital digital ideas.
  - Penalties ranged 10–14.

---

## 11. Phase 8 direction (decided after this phase)

Phases 5–7 measured newcomer outcomes on about 30 channels. The only verified newcomer success without an audience came from a pattern rather than a channel: **a developer searching for a missing capability** (Conductor).

Phase 8 will stop guessing channels and instead **reverse-engineer verified recent newcomer winners**. Each agent mines a dataset of recent entrants whose outcomes can be verified:
- TrustMRR verified revenue
- App Store ratings by release date
- Flippa and Empire Flippers businesses under 3 years old with verified profit
- hardware crowdfunding results
- company registries combined with outcome signals

The agents will ask which **replicable patterns** let a newcomer without an audience reach $2k+/month. The agents will also cover non-software categories, to avoid a software bias.

The leader re-check will re-measure H7's newcomer sales on Superhive for 2026, the last unmeasured leader assumption.
