# Phase 9: Copy-Resistant Positions

**Date:** 2026-10-13
**Branch:** `local-research-phase6-10`
**Working files:** `research-notes/phase9/`
- Six discovery reports (`agent-A.md` to `agent-F.md`)
- Leader re-check (`audit-leaders.md`)
- Shortlist (`shortlist.md`)
- Evidence audit (`audit-shortlist.md`)
- Red-team report (`redteam.md`)

The scoring script is `scratchpad/p6plus/P9-score/score.py`. It reproduces every total in §6.

---

## Bottom line

**The Phase 9 direction was largely falsified.**
- Phase 8 measured a copy window of about 6 months.
- Phase 9 asked whether a founder with about $2k could escape that window by holding something a follower can't copy quickly: a licence, a certification, a contract, exclusive supply, local network effects, or an Israel-specific advantage.

Evidence from public registries, certified-provider lists and contract data gives a consistent answer: **a moat this founder can obtain in 3–9 months for about $2k, a follower can obtain on the same timeline. Moats that actually block followers are out of reach on time, capital or prerequisites.**

| Kind of moat | What was measured |
|---|---|
| Cheap licences and approvals fill quickly | IRS 2290 e-file providers 64 → 149 in three tax years (36 state-named copycat brands); Israeli food importers 3,098 holders, about half recent; Israeli cosmetics responsible persons on the new EU route: 434 importers; EU IOSS intermediaries 1,394; Texas driving-safety courses 471; UK MTD VAT software 469; French e-invoicing platforms 155 + 12 pending. |
| Hard licences protect incumbents, not newcomers | 48 independent EU medical-device authorised representatives registered 2023–26: median **1** client; about 6.5% reached 15+, the same as the Phase 8 base rate. Of 1,160 Israeli device-registration holders, recent independents hold 0–3 registrations. |
| Contracts amplify existing businesses | First-time Texas DIR software holders: **10 of 23 sold $0 in FY2026, median $19.7k** (red team). Agent E's "47% sold $100k+" was driven by staffing firms. The sample counts only currently active contracts, so it is an upper bound. Truly exclusive deals (Israeli central tenders, ADA endorsements) went to incumbents only. |
| Local network effects take years and capital | About 250 local-marketplace entrants (2023–26) in 7 small markets: best entrant has 0–11 ratings vs incumbents with 400–42,661. Handyhand (DK) took 5–7 years plus acquisitions. Vinted now out-rates local incumbents in FI, RO, HR and GR. |
| Israel-specific edge is weaker than assumed | 314 Hebrew business apps released since 2024: median 0 Israeli ratings, only 1 with 100+. Israel-domestic ideas in the ledger have the same median score as the rest (43.5 vs 43.8), and all three of the best were cut after audits found incumbents late. |

**Agent F's falsification test, from outside our idea set:**
- **Empire Flippers listings mentioning a licence, contract or certification:** 1.3% of 2,854 listings. They earn about 3× the median profit but sell at the same or a lower multiple, so buyers don't pay for the moat.
- **Federal contract winners:** about 40% exit within 3 years, no better than the BLS survival rate for all new establishments.
- **Licence-heavy sectors:** 5-year survival is lower than in retail and food service.

**Best new idea:** an approved online boater-safety course, entering through language and price gaps (P1), at **44.7**. Every Phase 9 idea scores 25–45, so nothing enters the top cluster.

**Leader corrections:**
- **K8 Framer vertical kit: 52.0 → 50.4** (speed to first sale 4→3). The shortlist auditor dissented at 51.4.
- **H6, H1, M1 and H7: held.** The red team dissented on M1 at 48.6.

---

## 1. Methodology (unchanged)

**Frozen rubric, scored at criterion level:**

| Score | Criteria (step value) |
|---|---|
| CF | Spending ×5, Speed ×4, Capital ×4, Margin ×4, Labour ×3 |
| Scal | Depth ×3, Recurring ×4, Acquisition ×4, Leverage ×4, Defensibility ×3, Fit ×2 |
| Dist | Clarity ×4, Discoverability ×4, Proven ×6, First customers ×3, Beyond founder ×3 |

- Balanced = 0.4 CF + 0.4 Scal + 0.2 Dist. Adjusted = Balanced − penalty.
- Differences under about 5 points are noise.

**Process:**
1. Six discovery agents.
2. A leader auditor.
3. An 11-item shortlist.
4. An independent evidence auditor and an independent red team, working in parallel.
5. Final scores are the mean of the two reviewers' scores (the Phase 8 rule).

**Calibration (not a rubric change):**
- Agent F proposed that Defensibility score at most 2 of 5 for any moat obtainable in under about 9 months, unless holder numbers are capped or the term is fixed.
- Both reviewers applied it independently, with stated exceptions. The auditor gave 3 to P5 (fixed-term awards) and P4 (a refusal rule protects the first registrant), and 4 to P10 (5–7 years). The red team exempted P4.
- It changed P1's Defensibility by at most one step.

**Searches:** 53 WebSearches, all logged.

| Agent | Searches |
|---|---|
| A, B, C, D, F | 6 each |
| E | 5 |
| Leader auditor | 4 |
| Shortlist auditor | 6 |
| Red team | 8 |

**Primary data sources:**
- data.gov.il registries (companies, brokers, contractors, CPAs, car dealers, food importers, payroll auditors)
- the Israeli Ministry of Health device (AMAR) and cosmetics registries (30,212 and 61,991 records)
- the EUDAMED API
- Texas DIR sales data, the Sourcewell award spreadsheet and Contracts Finder
- NASBLA fee and terms PDFs; state boater-course lists, current and on Wayback
- IRS, Texas, UK, French and Croatian certified-provider lists
- iTunes Search API, across IL, CZ, PT, GR, HU, DK, UK, FI, RO and HR
- the Empire Flippers public API; BLS business-survival tables
- nexxt-change listings; eCFR; Israeli regulations

**Blocked (none bypassed):**
- gov.il and isa.gov.il (403 or JavaScript-only)
- myfwc.com and californiaboatercard.com (403; Wayback used)
- the NASBLA approval portal (members only)
- Flippa API (login required)
- Trustindex history; Zap category redirects
- the Portugal tax authority list (JavaScript); the Transport Canada provider list (404)
- the HMRC software finder (form-driven)
- a scanned National Insurance tender PDF

**Boundaries kept:** no contact, purchases, sign-ups, browser use or deployment. No personal identifiers were sent. Personal fields in the registry pulls were not stored.

---

## 2. Research direction and why

Phase 8 found that the copy window is about 6 months, and that AI-built supply roughly tripled newcomer volume from 2024 to 2026. Ideas whose edge is "first to notice" decay before they pay back. Phase 9 tested the obvious response: find positions a fast follower cannot copy, which this founder can still obtain. Each agent had to show evidence of spending, evidence of the moat (holder counts and trends, time and cost to qualify), and outcomes for recent holders.

---

## 3. Discovery results by agent

**A: thin-market network effects and trust assets.**
- See the table above.
- Copying runs faster than the 6-month window: Israeli sublet apps drew about 10 entrants in 2025–26 (best 32 ratings, all free), and Czech tradesperson apps 56 since 2023.
- Buying liquidity is out of budget: the cheapest Empire Flippers listing is $51.5k, and listed marketplaces cost $240k+.
- Kills:
  - UK pet-microchip database: operators self-certify; incumbents formed AMDO and launched shared search on 30 Sep 2026.
  - Israeli second-hand fashion; P2P escrow (CarPay precedent appears defunct; needs a payment licence).
  - Breed-society registries; Tel Aviv sublets; seller tools for Vinted; aged seller accounts (breach platform terms).

**B: exclusive supply, rights and certifications.**
- Israel's 2023–25 "what's good for Europe" reforms turned most certification barriers into 48-hour or notify-only steps:
  - Class I device registration is free and confirmed within 48 hours.
  - 434 importers use the new EU cosmetics route.
  - 2,804 wireless-device models carry approvals that other importers can reuse.
- Class II device holders are few per category (breast pumps 16, light therapy 74), but only 47–49% of 2016–21 holders are still active. 19.7% of manufacturers already have 2+ Israeli holders.
- Household pesticides have about 25 holders and about 10 new registrations a year: the strongest moat measured, but with unknown time and cost.
- US FDA establishment registration costs $13,785 a year, 6.9× the budget.

**C: licences and accredited statuses.**
- See the table above for holder counts.
- Kills:
  - Israeli notary: needs 10+ years as a lawyer; 7,735 active.
  - US customs broker: citizenship required (19 CFR 111.11).
  - Tour-guide refresher organisers: 38 organisers; median price ₪120.
  - EU product-safety (GPSR) responsible person and FDA US agent: no licence needed.
- Buying a German business that holds contracts: 47 of 240 nexxt-change listings ask €50k or less, but almost none hold contracts; property-management firms ask €250–500k.

**D: certified software.**
- Measured 14 public lists. **The moat depends on the per-jurisdiction cost and renewal of approval, not on certification as such:**
  - Cheap, test-based approvals fill quickly.
  - Paid, content-reviewed, per-state approvals stay small: Canadian NETFILE about 17 brands, stable since 2018; Streamlined Sales Tax certified providers 6; Texas court e-filing providers 13 → 25 over 10 years; Texas boater courses 3 → 6 over 12 years.
  - The auditor then found California boater courses grew 10 → 19 (2018–26), with doorway-named entrants.

**E: contracted distribution.**
- Texas DIR: $3.84B in FY2026 across 582 vendors.
- Sourcewell: about 1,060 contracts, median 6 awards per tender. Public Safety Software drew 80 proposals and made 39 awards; price is weighted 40%.
- Small foreign vendors do win (Carbyne, Compusult, Blinkay), but with products and references already in hand.
- Contract-vehicle resellers: Ondaro grew $248k → $4.66M on ServiceNow; SATRDE $429k → $1.03M on Zendesk.
- Israel's Nimbus tier-5 cloud marketplace is pass/fail with recurring rounds and no public spend data.
- Israeli central tenders all had a single, incumbent winner.

**F: Israel advantages, plus the falsification test.**
- 406,904 active Israeli companies, with about 17–18k new ones a year.
- Licences the founder could obtain are abundant: 24,984 real-estate brokers; 24,373 registered contractors (new registrations tripled 2015–23); 32,153 CPAs; 10,872 car dealers.
- The only scarce one found, radon testing (32 permits), has no current obligation behind it.
- Part of the earlier "Hebrew moat" was a measurement artefact: our search engine is US-only. Agent F recommends treating future Israel ideas as 1–3 points lower to allow for incumbents not yet found.

---

## 4. Shortlist (11)

| ID | Idea |
|---|---|
| P1 | Approved online boater-safety course (NASBLA plus states), entering through language and price gaps |
| P2 | Independent Israel Registration Holder for foreign medical-device makers, white-label via global platforms |
| P3 | Israeli registration holder for one niche Class II home-use device with exclusivity, sold DTC |
| P4 | Israeli household-pesticide registration for a foreign-registered product |
| P5 | Niche public-sector SaaS sold through cooperative contracts (Sourcewell, Texas DIR) |
| P6 | Texas DIR contract-vehicle reseller (Vertosoft model) |
| P7 | Israeli government cloud marketplace (Nimbus tier 5) listing |
| P8 | Open-finance bank-feed reconciliation for Israeli accounting firms (licensed provider) |
| P9 | Israeli back-office for EU/UK accountants, positioned on EU adequacy |
| P10 | Liquidity roll-up in one small-language local-marketplace vertical |
| P11 | Software-assisted payroll-audit firm (Israel) |

---

## 5. Adversarial review: findings

| ID | Finding |
|---|---|
| **P1** | NASBLA fees are verified: $4,500 timed / $5,500 interactive (non-member), $550 per extra state, full re-review every 3 years. Three claims were refuted. **The holder count is not stable:** California rose 10 → 19 (2018–26). **The Spanish gap is Texas-only:** California's own course is free and NASBLA-approved in English and Spanish; New York lists two Spanish options; Texas already has Boat-Ed Spanish at $54.95. **A follower can license an approved course** (NASBLA terms §7). Recademics (two founders, from about 2023) shows real newcomer traction: 470 Trustindex reviews, now on the Texas and New York lists. Boat-Ed's July 2026 attack page advertises "$30–55", so the $25–35 band is contested. California cards: 37.7k (2022), 53.7k (2023), 82.2k (2024), then the 144.6k deadline spike; post-deadline demand is unmeasured. Capital before the first sale is about $7–12k (red team estimate). |
| **P2** | **The channel premise is false.** Pure Global sells Israeli registration through a local partner for a flat annual fee. The regulations put ISO 9001 on storage and transport (Reg. 20), not on the holder as such, but the contact person must be the holder's own employee (Reg. 21), and the law carries criminal and officer liability. Registry figures reproduce. |
| **P3** | The statute sets a 120-day decision deadline. Exclusivity is weak and capital is over budget. |
| **P4** | Every decision goes through a 6-member inter-ministerial committee with no deadline. The committee may refuse a product if a less-harmful one is already registered for the same use, so it protects the first registrant. Trial literature is accepted, so local trials are not explicitly required. Time and cost remain unknown. |
| **P5/P6** | The DIR, Sourcewell, Ondaro and SATRDE figures reproduce. The cohort counts only active contracts, so it is survivorship-biased. Software makers: median $19.7k, and 43% sold $0, including established firms (Teradata, Versaterm, Edmunds GovTech). The founder has no product or references. |
| **P8** | At least 7–8 open-finance licensees by 2023, and growing, so the licence is not capped. A May 2026 bill note mentions relief for foreign providers. Capital requirements are unknown. |
| **P11** | Since 2017, employers and service buyers relying on a certified auditor get 30–50% lower sanctions, a real demand driver. But there are 2,029 auditors, and new registrations are falling (525 in 2019, 83 in 2026), which suggests oversupply. No tender price was found. |

---

## 6. Phase 9 scoring (frozen rubric, criterion level; mean of the two reviewers)

| ID | Auditor steps (CF / Scal / Dist, pen) | Red-team steps (CF / Scal / Dist, pen) | **CF** | **Scal** | **Dist** | Balanced | Pen | **Adjusted** | Aud / RT |
|---|---|---|---|---|---|---|---|---|---|
| P1 Boater-safety course | 4,1,2,4,4 / 3,1,3,4,2,4 / 5,4,1,2,3, 12 | 4,1,1,4,4 / 3,1,3,4,2,2 / 5,4,2,2,4, 12 | 58.0 | 53.0 | 61.5 | 56.7 | 12 | **44.7** | 45.4 / 44.0 |
| P5 Co-op contract SaaS | 5,0,2,4,2 / 4,5,2,3,3,3 / 4,3,2,1,3, 13 | 4,0,2,4,2 / 4,5,2,3,2,2 / 3,2,1,0,3, 12 | 52.5 | 64.5 | 43.5 | 55.5 | 12.5 | **43.0** | 46.2 / 39.8 |
| P8 Open-finance bank feeds | 2,1,1,4,4 / 2,5,2,4,2,4 / 4,2,1,2,2, 13 | 1,0,1,4,4 / 2,5,2,4,2,4 / 4,2,0,2,2, 14 | 41.5 | 64.0 | 39.0 | 50.0 | 13.5 | **36.5** | 39.4 / 33.6 |
| P2 Israel registration holder | 3,2,3,3,2 / 2,4,2,2,2,2 / 4,2,1,1,2, 13 | 3,2,2,3,1 / 2,4,1,2,2,1 / 4,2,1,1,2, 13 | 49.5 | 45.0 | 39.0 | 45.6 | 13 | **32.6** | 35.2 / 30.0 |
| P11 Payroll-audit firm | 3,2,3,1,1 / 2,4,2,2,1,2 / 4,3,1,2,2, 13 | 3,2,3,2,1 / 2,4,2,2,0,3 / 4,3,1,2,2, 12 | 44.0 | 44.5 | 46.0 | 44.6 | 12.5 | **32.1** | 31.0 / 33.2 |
| P3 Device DTC with exclusivity | 2,2,1,3,3 / 2,1,3,3,2,2 / 3,2,1,2,3, 12 | 2,2,1,3,3 / 1,1,2,3,1,2 / 4,3,1,2,3, 13 | 43.0 | 39.0 | 45.0 | 41.8 | 12.5 | **29.3** | 31.0 / 27.6 |
| P4 Pesticide registration | 2,0,1,3,3 / 1,3,2,3,3,1 / 4,2,1,2,2, 12 | 2,0,1,3,3 / 1,3,2,3,3,1 / 4,2,1,2,2, 13 | 35.0 | 46.0 | 42.0 | 40.8 | 12.5 | **28.3** | 28.8 / 27.8 |
| P9 Adequacy back-office | 3,2,3,2,1 / 3,4,2,1,1,2 / 3,2,1,1,2, 13 | 3,3,3,2,1 / 3,4,1,1,0,2 / 3,1,0,1,1, 14 | 48.0 | 40.5 | 28.5 | 41.1 | 13.5 | **27.6** (kill) | 30.0 / 25.2 |
| P6 DIR reseller | 4,1,2,1,2 / 3,3,2,2,2,1 / 3,2,2,1,2, 13 | 4,1,1,1,1 / 3,3,1,2,1,0 / 3,1,2,0,1, 13 | 38.5 | 40.5 | 36.0 | 38.8 | 13 | **25.8** (kill) | 30.0 / 21.6 |
| P7 Nimbus listing | 1,1,3,4,3 / 2,4,1,3,1,4 / 3,1,0,1,1, 14 | 0,2,3,4,2 / 1,4,1,3,0,3 / 2,1,0,1,1, 14 | 44.0 | 45.0 | 20.0 | 39.6 | 14 | **25.6** (kill) | 28.4 / 22.8 |
| P10 Liquidity roll-up | 3,0,0,3,1 / 3,3,2,3,4,2 / 2,2,1,1,3, 13 | 3,0,0,3,1 / 2,3,1,3,2,2 / 3,2,0,1,2, 13 | 30.0 | 50.5 | 31.5 | 38.5 | 13 | **25.5** (kill) | 28.6 / 22.4 |

The reviewers disagreed by more than 5 points only on P5 (46.2 vs 39.8) and P6 (30.0 vs 21.6). The mean absorbs this, and neither idea is near the cluster either way.

**Leader corrections (criterion steps):**

| Leader | Decision | Reviewers |
|---|---|---|
| K8 Framer kit | **52.0 → 50.4.** Speed 4→3: CF 84 → 80; Balanced 63.4; penalty 13. Evidence: no public sales counts; at most about 9–13% of 7,359 creators received a December-2025 payout; 2026 creators' median is 43 followers; new listings arrive at 2–3× the 2024–25 rate. | Leader auditor 50.4 and red team 50.4. Shortlist auditor dissents at 51.4 (first customers −1 instead). Applied 50.4 as the majority position; both readings are within noise. |
| H6 College-baseball API | **Hold 52.2.** NCAA.com and SIDEARM terms say noncommercial use only, but CFBD and Highlightly operate paid APIs openly. Same risk as priced in Phase 6. | All hold. Red-team dissent range 51.2–52.2. |
| H1 Meshtastic kits | **Hold 51.2.** Tindie, Etsy and Amazon were bot-blocked. Archived Tindie: about 90% of 2024–26 Meshtastic listings have 0 reviews (weak negative, wrong channel). Trigger: proven channel −1 → 50.0 if Amazon $300+ bundles prove weak. | All hold. The auditor notes its penalty of 7 is below the historical 9–14 band. |
| M1 Sage 50 API | **Hold 49.6.** The archived 2023 Sage NA programme covers Sage 50 US/CA ($350 + $250 a year). The only archived agreement text is "Medium Segment": it bars use for any third party's benefit and allows termination for convenience on 90 days' notice. | Leader auditor and shortlist auditor hold. Red team 48.6 (penalty 13, treating this as direct contradiction). No Sage 50-specific text exists, so not applied. |
| H7 Blender add-ons | **Hold 55.4.** | Red team: overrated as a forecast (2–5% per product) but not mis-scored. |

---

## 7. Finalists: deep dives

**Selection:** the top five by Adjusted score are P1, P5, P8, P2 and P11. The gap after P5 is 6.5 points, so P8, P2 and P11 are covered briefly. All scenario figures are **[Hypothesis]** model outputs.

### F1. Approved online boater-safety course (P1): 44.7

**Offer**
- A NASBLA-approved online course, approved state by state.
- Launch in one high-volume state, priced at $25–35.
- Spanish only where it is genuinely missing.
- Later add hunter, ATV and snowmobile courses, which is what Recademics did.

**Spending evidence**

| Fact | Status |
|---|---|
| California cards: 37.7k (2022), 53.7k (2023), 82.2k (2024), 144.6k (Aug 2024–Aug 2025 deadline spike) | [Verified: state data via Agent D and auditor] |
| Kalkomey (Boat-Ed) trains about 1M people a year across courses; acquired by Macquarie in 2024 | [Secondary] |
| Texas price list ranges from $1 to $74.95 | [Verified] |

**Competition**
- Boat-Ed, BOATsmart!, BOATERexam, iLearnToBoat, BoatUS ($1 in Texas), state-run free courses (California), and Recademics.

**Moat:** real but modest.
- Approval costs $4.5–10k, needs content review, and is renewed every 3 years.
- Holder counts still grow (California 10 → 19).
- Followers can license approved content.

**Channel**
- State agency lists show every approved provider. Only holders can be listed there.
- Search ads against Kalkomey's SEO.
- Acquisition cost per student is [Unknown].

**Capital and labour**
- About $7–12k before the first sale: NASBLA review, state fees, course production, and an LMS. That is **3.5–6× the $2k budget**.
- After approval, labour is low: support plus annual state reporting.

**Economics**

| Scenario | Students per year | Owner profit |
|---|---|---|
| Downside | 1–2k | Barely covers re-review costs, about $0–500/month |
| Base (two states, 24 months) | 10–20k at about $15 net | **about $2–4k/month**, seasonal |
| Upside (multi-state, multi-course portfolio like Recademics) | — | $10k+/month; needs a team |

**Decisive assumption:** a newly approved provider wins paying students at about $12 or less acquisition cost per student in one state, against Kalkomey's SEO and $1 or free anchors.

**Track fit:** A, and only after a capital step-up.

### F2. Niche public-sector SaaS sold through cooperative contracts (P5): 43.0

**Offer:** a narrow local-government workflow product, bid into a Sourcewell or DIR category re-solicitation once there are 1–3 pilot customers.

**Evidence**
- Small and foreign vendors are awarded; awards are uncapped, price is weighted 40%, and the lowest awardee scored about 700 of 1,000.
- First-time software holders: median $19.7k a year, and 43% sold $0.

**Capital and time**
- The product build fits the founder's skills.
- Pilots need US local-government sales, which runs 0–3 hours of time-zone overlap from Israel.
- Horizon 2–4 years.

**Economics**

| Scenario | Owner profit |
|---|---|
| Downside | Award won, $0 sales (43% of software holders) |
| Base (year 3–4) | $20–80k a year in contract sales, **about $1.5–5k/month** |
| Upside (Veoci-like) | $700k a year in sales |

**Decisive assumption:** the founder can land 1–3 paid local-government pilots remotely before a category re-solicits.

**Track fit:** B in principle; too slow for Track A.

### F3–F5, in brief

**P8, open-finance bank feeds for Israeli accounting firms (36.5)**
- Recurring and software-native, with high founder fit.
- But the licence is not capped (7–8+ holders and growing), its capital requirement is unknown, and Israeli B2B app newcomers have median 0 ratings.
- Kill test: the Israel Securities Authority licence capital and insurance requirements. Kill if more than $50k.

**P2, Israel Registration Holder (32.6)**
- Real spending: $3–10k per manufacturer per year; Emergo holds 84 manufacturers.
- But the white-label gap is closed (Pure Global covers Israel), it is service labour, and it carries criminal and officer liability.
- Recent independents hold 0–3 registrations.

**P11, payroll-audit firm (32.1)**
- Demand is driven by sanctions relief, but the 2,029 certified auditors suggest oversupply, and it is service labour.
- Price per audit is unknown.

---

## 8. Cumulative leaderboard (all phases; * = corrected in Phases 5–9)

| Rank | Opportunity | Phase | Adjusted |
|---|---|---|---|
| 1 | Blender/VRChat add-ons (H7) | 3 | 55.4* |
| 2 | College-baseball data API (H6) | 3 | 52.2* |
| 3 | Meshtastic family kits (H1) | 3 | 51.2* |
| 4= | monday.com Israeli invoicing app | 1 | 50.8* |
| 4= | Apify Actors (J7) | 4 | 50.8* |
| 6 | Hebrew tender + receivership intelligence (K13) | 5 | 50.6* |
| 7 | **Framer vertical kit (K8)** | 5 | **50.4*** (was 52.0) |
| 8 | UK MTD prep for accountants | 2 | 50.2* |
| 9 | Israeli allocation verification | 1 | 49.8 |
| 10 | Sage 50 US/CA integration API (M1) | 7 | 49.6* |
| 11= | Ketubot (H10) | 3 | 49.4* |
| 11= | Spanish Holy Land box (H8) | 3 | 49.4 |
| 11= | Non-US availability alerts (H5) | 3 | 49.4 |
| 14 | Pay-per-call emergency lead sites (L6) | 6 | 48.8 |
| 15 | Hebrew/Russian memoir books (J1) | 4 | 48.6* |
| 16= | Hebrew personalised kids' books (J2) | 4 | 48.2 |
| 16= | Judaica STL (H4) | 3 | 48.2 |
| 18= | WooCommerce Merchant Center monitor (N12) | 8 | 48.0 |
| 18= | MT5 prop-rule utility (J9) | 4 | 48.0 |
| 20 | Remote b'nai mitzvah (H9) | 3 | 47.8 |

**Cross-phase verdict**
- The board is flatter than ever: #2–#20 span 47.8–52.2.
- The best Phase 9 idea (44.7) would rank about #30.
- The ideas that score well do so through cheap, fast starts (high CF), not through defensibility.
- Agent F's caution that Israel-domestic leaders (monday.com app, K13, allocation verification, J1, J2) may be overstated by 1–3 points is **noted but not applied**, because the rule requires named criterion evidence. The cross-phase report will flag it as an uncertainty.

---

## 9. Three most promising Phase 9 discoveries

1. **Fastest cash flow:** none of the Phase 9 ideas is fast. The fastest is P1 after approval, but that needs $7–12k first.
2. **Most scalable: P5 co-op contract SaaS.** Contracts run 4+3 years and awards are uncapped, but the evidence says contracts amplify an existing product. The real prerequisite is a product with references.
3. **Best risk-adjusted: P1 boater-safety course.** It has the highest score, a verified newcomer precedent (Recademics), and a measurable moat. Its decisive assumption (acquisition cost per student) is testable once the course is approved.

**The most valuable Phase 9 output is the negative result:** the cumulative research should stop searching for moats a $2k founder can buy. This changes what Phase 10 should do.

---

## 10. Research limitations

- **Survivor data:** contract cohorts count only active holders. Empire Flippers listings with moats are n=36. Registry age bands are inferred from number order.
- **Blocked Israeli government sources** (gov.il): the Israel Tax Authority list, open-banking licensees, the medical-tourism register and the payroll tender PDF.
- **Unknowns:**
  - boater acquisition cost per student and post-deadline demand;
  - pesticide registration time and cost;
  - open-finance licence capital;
  - payroll-audit prices;
  - Tnufa grant terms (conflicting guides; the site blocked fetching).
- **Calibration:** applying the Defensibility guidance moved P1 by at most 1.2 points and did not change any rank.

---

## 11. Phase 10 direction (decided after this phase)

Phases 5–9 converged on three measured facts:
1. **Newcomer success is about 4–6% per attempt** in every dataset measured.
2. **Followers arrive within about 6 months**, and cheap moats don't stop them.
3. **Winners without an audience over-index on high price per account** ($300+/month: 5.1× lift), **small teams** (4.4×) and **paid or partner channels** (3–6×).

Defensibility and novelty have failed as levers. Phase 10 will target the measured winning traits directly.

**Phase 10: "high-ticket B2B with paid acquisition, where unit economics survive copying".** Each agent looks for offers priced at $300+ per account per month (or one-off equivalents of $1,500+). The offers must be sold through search ads, paid social or partner channels with evidence of newcomer winners, and must have unit economics that work even if copied:
- a CAC-to-LTV ratio that is measurable before scaling;
- delivery the founder can automate or delegate.

Each agent must:
- name the paid keyword or audience and show evidence of advertiser competition, e.g. the Google Ads Transparency Center and Meta Ad Library, both public;
- report newcomer outcomes;
- state the cheapest test with an explicit kill threshold.

**Leader re-check (final):**
- Run the cheapest decisive desk checks still open for the top five: H7, H6, H1, the monday.com app and J7.
- Apply Agent F's Israel-incumbent caution only where named evidence exists.
