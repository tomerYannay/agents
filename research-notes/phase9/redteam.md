# Phase 9 Red-Team Investor report (P9-REDTEAM), 2026-10-13

**Scope.** Why each of P1–P11 would fail *for this founder*. The founder is Israel-based, technical, part-time, has about $2k and wants to own a business. I also challenge the leader items: K8, H6, H1, M1 and H7. I worked independently of the evidence auditor and did not read its output.

**Searches and sources.**
- WebSearch: **8 of 8 used**, all logged as `P9-REDTEAM`. Topics:
  1. Boat-Ed vs Recademics
  2. California Boater Card after the phase-in
  3. Recademics reviews and student counts
  4. Israeli open-finance licence capital and holders
  5. Israel's EU adequacy status in 2025–26
  6. NASBLA review turnaround
  7. Israeli payroll-audit price (Hebrew)
  8. Israeli household-pesticide registration duration
- Primary pages fetched with curl, using a generic User-Agent:
  - Boat-Ed's "Boat-Ed vs Recademics" page (2 Jul 2026);
  - the TPWD Texas internet-course list (prices);
  - the DBW Nov-2025 Commission PDF (text extracted locally with zlib);
  - Trustindex's Recademics profile;
  - Pure Global's pricing page and its **/markets/israel** page;
  - the State Comptroller 2023 pest-control report (agricultural only; not useful);
  - Wayback CDX for recademics.com (no usable traction claims).
- **Re-analysis of Agent E's own DIR cohort file** (`P9-E/data/dir_newcomers.csv` and `scripts/dir.py`). This is the discovery agent's data, not the auditor's. My script is `scripts/dir_split.py`.
- **Blocked or failed:**
  - The Emergo IRH service URL returned 404 (a guessed URL).
  - Trustindex has no Wayback history, so I could not measure Recademics' review velocity over time.
  - Recademics' archived homepages carry no student counts.
  - No Hebrew price for payroll audits surfaced.
- Scratch: `scratchpad/p6plus/P9-redteam/{scripts,data}`. No browser, contact, sign-ups or purchases.

**Conventions.**
- Frozen rubric. Step values are CF 5/4/4/4/3, Scal 3/4/4/4/3/2, Dist 4/4/6/3/3.
- "Steps" are the 0–5 criterion scores in rubric order:
  - CF: spending, speed, capital, margins, independence.
  - Scal: depth, recurring, scalable acquisition, operating leverage, defensibility, founder fit.
  - Dist: clarity, discoverability, proven channel, first customers, growth beyond outreach.
- Scores are reproducible with `scripts/score.py`.

**Calibration guidance: applied, in a narrowed form.** I cap Defensibility at 2 for any moat the founder could obtain in under about 9 months, unless the holder count is capped or the award has a fixed term with limited holders. Evidence:
- Agent F's Part 2 shows no survival or multiple premium for obtainable moats.
- Agent C's EU AR cohort reached 15+ clients about 6.5% of the time, the same as the open-marketplace base rate.
- Agent D's IRS 2290 and TDLR lists flooded.

I do **not** let the cap *raise* anything. It binds only on P1, where Def would otherwise be 3, and costs 1.2 Adjusted points. Every other P-idea already scores Def ≤2 on its own evidence. P4 is the exception: its moat is not obtainable in under 9 months, so the cap does not apply and it gets Def 3.

---

## 0. Headline

1. **Nothing in Phase 9 reaches the board's top cluster.** The best is **P1, boater-safety courses, at 44.0**. The next is **P5, co-op contract SaaS, at 39.8**. Everything else lands at 21–34.
2. **Phase 9 verifies the direction's own falsification.** Every moat this founder can obtain in 3–9 months is one that a follower obtained on the same clock:
   - Recademics entered roughly 20 states in about 3 years.
   - Payroll auditors number 2,029.
   - The Israeli open-finance licence had about 8 holders by early 2023.

   Every moat that *is* scarce is out of budget or time:
   - P4 pesticides: timeline unknown, probably over 12 months.
   - P10 liquidity: 5–7 years and over $51k.
   - P6 and P5 contract vehicles: they need references first.
3. **New verified contradictions of shortlist claims:**
   - **P2: "Pure Global does not list Israel" is now false.** pureglobal.com/markets/israel ("AMAR Israel Medical Device Registration", last reviewed 24 Jul 2026) offers Israel with "in-country representation… for a market-specific flat annual fee" and describes the IRH role. Israel also appears in the pricing page's market list. The white-label gap P2 was built on has been closed by the platform itself.
   - **P1, language gap:** the Texas list already carries a **Spanish Boat-Ed course** ("Costo: $54.95 Provider fee + $10.00 State Fee") [Verified: TPWD page, 2026-10-13]. The wedge is price-on-Spanish, not an empty slot.
   - **P1, incumbent price response:** Boat-Ed's attack page now advertises "$30–$55 (varies by state)" and positions on "official course" status against Recademics [Verified: boat-ed.com, 2 Jul 2026]. The $25–35 band P1 wants is already contested from both sides: Recademics at $29.99 in Texas and Boat-Ed at $30 in some states.
4. **Survivorship in the contract-holder data is real and measurable.** Agent E's 2023–24 DIR "newcomer" cohort is built only from **currently active** contracts (`dir.py` reads `active.json`). Vendors whose 2023–24 contracts lapsed or were not renewed are missing, so "29% sold $0" is a floor. The headline 47% ≥$100k is also driven by **IT staffing firms**: 48 of 94 are staffing or DBITS vendors, with a median of $199.6k. **Software product makers, the P5 profile, number 23. Of these, 10 (43%) sold $0 and the median was $19.7k in FY2026.** That is after excluding the two resellers (Ondaro and SATRDE). The zero-sellers include established firms such as Teradata Government Systems, Versaterm and Edmunds GovTech.
5. **Leader calls:**
   - **K8: 50.4 is right**, not too harsh. The strict range is 49.8–50.4.
   - **H6: hold 52.2**, with a dissent range of 51.2–52.2.
   - **H1: hold 51.2.**
   - **M1: take the downside, 48.6** (penalty 13).
   - **H7: hold 55.4.** It is still overrated as a forecast but not mis-scored. No new Phase 9 evidence, and the calibration cap does not bind it.

---

## 1. Cross-cutting attacks

| Attack | Evidence | Who it hurts most |
|---|---|---|
| **Moat realism: a follower gets it on the same clock** | Agent F Part 2: CSIS found about 40% of new federal contract entrants exit within 3 years. BLS shows licence-heavy sectors do not survive longer. EF moated listings sell at 24.5–30× vs 28–31× for other listings. Recademics shows a two-founder US team reaching about 20 state approvals in about 3 years. | P1, P2, P3, P8, P11 |
| **Capital beyond $2k** | P1: NASBLA $4,500–5,500 plus $550 per extra state, plus a US LLC and an ad test, so about $7–12k before season one [Hypothesis on the total]. P3: ISO 9001 plus a 100-unit MOQ at $3–6k. P4: dossier and possible trials [Unknown]. P5: US entity, insurance certificates, TX-RAMP and a HUB plan. P10: EF floor $51.5k. P6: pass-through credit exposure. Tnufa (F9-1) is unconfirmed, deep-tech biased, and does not fund consumer courses or service firms [Hypothesis]. | P1, P3, P4, P5, P6, P10 |
| **Service-labour drift** | P2 is per-file regulatory work done by an RA hire, and the founder carries holder liability. P9 is bookkeeping labour at Israeli wages against India and the Philippines. P11 needs certified auditors on payroll; the founder cannot sign audits. None of the three grows faster than headcount. | P2, P9, P11 |
| **Incumbents respond** | Kalkomey (Macquarie-owned since Jun 2024, about 1M trained a year) published a named attack page on the one newcomer within about 3 years of its entry, and prices from $30. Pure Global added Israel. Emergo and Freyr hold the IRH book. Carahsoft and Vertosoft carry vendors with traction. Bookkeeping vendors and licensed aggregators (Finbot: 18 IL apps since 2024) can add bank feeds natively. | P1, P2, P6, P8 |
| **Demand decay** | California issued 144,608 cards in Aug 2024–Aug 2025, up 198%. That implies about 48.5k in the prior year and 31,339 in Aug 2021–Aug 2022 [Verified: DBW Nov-2025 PDF; prior-year figure derived]. The all-ages phase-in completed on **1 Jan 2025**, and the card is $10 for life. Steady state is new boaters plus late compliers, shared among 16 approved courses including a free DBW course. New York's Brianna's Law completed in 2025 too. No 2026 issuance data surfaced (search #2). | P1 |
| **Survivorship** | DIR: see headline 4. Sourcewell's 49% award rate (39 of 80) means "holders" are pre-selected firms. Handyhand and Vendora are the survivors of about 250 sub-scale entrants measured by Agent A. EF moat listings are 36 of 2,854. | P5, P6, P10 |
| **Israel market size** | 406,904 active companies. 290 independent 2024+ Hebrew business apps have a median of 0 Israeli ratings. AMAR has about 1,160 active holders, with about 58–94 new holders per numbering band, most of them distributors holding their own registrations. There are 2,153 licensed exterminators and 32,153 active CPAs. Track B from Israel-only demand needs $300+ per account, and only P8's and P11's B2B buyers plausibly pay that. | P2, P3, P4, P7, P8, P11 |

---

## 2. Per-idea red team

### P1. Approved online boater-safety course (NASBLA plus states), entering through Spanish and a $25–35 price
**What I checked:**
- **TPWD Texas list** [Verified, 2026-10-13]:

  | Provider | Provider fee |
  |---|---|
  | BoatUS | $1.00 |
  | Recademics | $29.99 |
  | BOATsmart | $39.95 |
  | BOATERexam | $49.95 |
  | Boat-Ed (English) | $54.95 |
  | **Boat-Ed (Spanish)** | **$54.95** |
  | iLearnToBoat | $74.95 |

  Each also carries the $10 state fee.
- **Boat-Ed attack page** (2 Jul 2026) [Verified]:
  - "Boat-Ed courses range from $30–$55 depending on the state";
  - Recademics "$39.95";
  - frames Recademics as lacking "direct state agency relationships";
  - "If your state requires its official course, Boat-Ed is the established, trusted answer."
- **Recademics traction:**
  - Trustindex shows **4.9 from 470 reviews**, collected from Google and Trustindex, with active automated invitations [Verified: trustindex.io, 2026-10-13].
  - About 25 dated entries on page 1 cover 9 Sep–11 Oct 2026. Most mention **hunter** education, not boating.
  - This is a real newcomer outcome, but its growth is coming from Kalkomey's other core line, by a US-based two-founder team working full time.
- **DBW:** 16 approved CA courses; "Google search advertising… has proven to provide the best return on investment" [Verified: DBW Nov-2025 PDF]. That is the state's own outreach, not a provider's CAC.
- **NASBLA turnaround:** not published. Reviews are processed "in order received". One Canadian re-review ran from Dec 2024 to about mid-2025 [Secondary: search #6].

**Top 3 failure modes:**
1. **The wedge is already occupied from both sides.**
   - Recademics took the "modern, cheap, video" slot at $29.99 in about 20 states and is now the one Kalkomey attacks.
   - Kalkomey can price at $30 and already sells Spanish.
   - A third challenger arrives about 3 years behind Recademics, without US presence, with no boating domain, and with Spanish as its wedge. The founder does not write Spanish.
2. **Capital and time to first dollar.**
   - About $7–12k before the first paid completion [Hypothesis].
   - Course build plus NASBLA review plus state review is about 6–12 months. Missing the spring 2027 window pushes the first real season to 2028.
   - Recurring revenue is zero (a lifetime card), so every completion is a new acquisition.
3. **Demand decay plus the free anchor.**
   - The CA and NY deadline cohorts are already served. Steady state is unmeasured.
   - BoatUS at $1 and state free courses cap price for the price-sensitive segment P1 targets.
   - Kalkomey owns "boating license [state]" SEO.

**Moat realism:**
- The approval stack is real. Texas went from 3 to 6 holders in 12 years.
- But it is obtainable by any funded follower in the same 6–12 months for about $5–10k.
- It does not stop Kalkomey's price response.
- **Defensibility capped at 2 under the calibration guidance.** It would be 3 without the cap, which adds +1.2 → 45.2.

**Hard blockers:** none verified. Whether any target state requires an in-state entity is [Unknown].

**Verdict:** **Viable with conditions.** It is the best of Phase 9, but well below the cluster.
- Steps: CF 4,1,1,4,4 = 56 · Scal 3,1,3,4,2,2 = 51 · Dist 5,4,2,2,4 = 66 → Balanced 56.0, penalty 12 → **44.0**.
- **Decisive assumption:** a new approved provider acquires paid completions at a CAC of about $12 or less in one high-volume state, against Boat-Ed at $30–55, Recademics at $29.99 and BoatUS at $1.
- **Cheapest desk check:** find state annual boater-education reports that break certificates down by provider (TPWD, NY Parks, Oregon Marine Board). Providers must report counts, so some states publish shares. **Kill if Recademics' share after 2–3 seasons in any state is under about 5% of online completions.** That would mean even the best-executed newcomer is marginal.

### P2. Independent Israel Registration Holder (IRH), white-label through global platforms; portfolio-of-DTC-brands variant
**What I checked:** pureglobal.com/markets/israel [Verified, last reviewed 24 Jul 2026]:
- "AMAR Israel Medical Device Registration";
- "local representation, all for a market-specific flat annual fee… Includes dossier submission, in-country representation…";
- it explains the IRH role.

Israel also appears in the pricing page's market list. **The shortlist claim that Pure Global does not list Israel is contradicted.**

**Top 3 failure modes:**
1. **The channel premise is gone or already filled.** The platform the idea was to white-label for now sells Israel itself. It either has an Israeli IRH partner already or will choose an established one (Emergo is the obvious one). Recent independents hold 0–3 registrations [Agent C].
2. **Service labour plus liability with no domain.**
   - The founder is not a regulatory-affairs professional, so he needs an RA contractor at about $30–40k a year [Agent C, Hypothesis].
   - The IRH carries vigilance and recall duties.
   - ISO 9001 may be required (sources conflict).
   - Revenue scales with files, not software.
3. **Small, captured market.** About 58–94 new holders per numbering band. Most are distributors holding their own registrations. Emergo (84 manufacturers) and L.Sh. (61) set the reference book size. Track B would need about 150 manufacturers, nearly twice Emergo's 84.

**DTC-portfolio variant (B3):** Class I registration is free and arrives in 48 hours, so the recurring fee has nothing scarce to charge for.

**Verdict:** **Kill.**
- Steps: CF 3,2,2,3,1 = 46 · Scal 2,4,1,2,2,1 = 42 · Dist 4,2,1,1,2 = 39 → 43.0, penalty 13 → **30.0**.
- **Decisive assumption:** a global platform or EU AR outsources its Israel IRH role to a new independent at $1.5–3k per client per year.
- **Cheapest desk check:** pull the MoH registry API for holders whose manufacturers are Pure Global, Freyr or Asphalion clients, or search holder names for "Pure Global". If the platform's Israeli IRH already appears as a holder, kill.

### P3. Israeli fast-track holder for one niche Class II/IIa home device with exclusivity, sold DTC in Hebrew
**Top 3 failure modes:**
1. **Exclusivity is weak.**
   - 33% of Chinese manufacturers already have 2+ Israeli holders [Agent B, Verified].
   - The fast track takes 2–4 months, so a copier holding a different manufacturer's near-identical device enters in a single season.
   - AliExpress personal imports leak demand.
2. **Capital.** ISO 9001, a 100-unit MOQ and Hebrew Meta ads exceed $2k before the first sale.
3. **No demand or newcomer evidence.**
   - Zap listings are not sales.
   - 47–49% of 2016–21 holders no longer hold any registration, and the median recent holder has 1.
   - Israeli medical-device DTC CAC is [Unknown].

**Verdict:** **Kill for this founder.** It is e-commerce with a thin regulatory moat, and nothing in it uses his software edge.
- Steps: CF 2,2,1,3,3 = 43 · Scal 1,1,2,3,1,2 = 34 · Dist 4,3,1,2,3 = 49 → 40.6, penalty 13 → **27.6**.
- **Decisive assumption:** 60+ units a month at a CAC under ₪200 for one device.
- **Cheapest desk check:** use Meta Ad Library (IL) to count active Hebrew advertisers for wearable breast pumps and LED masks. **Kill if ≥3 run fresh creatives.**

### P4. Israeli household-pesticide registration for a foreign-registered product, sold to 2,153 exterminators
**What I checked (search #8):**
- No household-track duration was published.
- The 1994 regulations give the Minister 6 months just to accept or refuse the request.
- The agricultural analogue needs about 2 years of testing plus a field trial [Secondary].
- The Comptroller's 2023 pest-control report covers only the agricultural committee, so it was not useful.

**Top 3 failure modes:**
1. **Time and capital are unknown and probably fatal.** At least 6 months to a decision, likely more than 12. A dossier from a foreign maker, plus possible local efficacy data. Nothing is earned meanwhile.
2. **The founder brings no edge.** It needs chemistry, regulatory work and B2B distribution to exterminators. Software is irrelevant.
3. **Small market, unknown spend.** 2,153 licensed exterminators. Incumbents SANO (24 registrations) and Rimi (22) can match or undercut a single product.

**Moat:** genuinely scarce (about 25 holders, about 10 new a year). This is the one idea where the calibration cap does not apply, so Def is 3. Scarcity exists because it is slow, which is exactly why the founder cannot get it in 3–9 months.

**Verdict:** **Kill for this founder.**
- Steps: CF 2,0,1,3,3 = 35 · Scal 1,3,2,3,3,1 = 46 · Dist 4,2,1,2,2 = 42 → 40.8, penalty 13 → **27.8**.
- **Decisive assumption:** registration within 9 months, with no local trials, for under $2k of dossier cost.
- **Cheapest desk check:** compare registration dates with first-import or EPA/BPR dates for 5 recent entries (numbers 678–689) in the data.gov.il `domestic_pesticides` dataset. **Kill if the median lag is over 12 months.**

### P5. Niche public-sector SaaS sold through cooperative contracts (Sourcewell, Texas DIR)
**What I checked:** re-analysis of Agent E's DIR file [Verified: data.texas.gov derived, 2026-10-13]:
- The cohort is drawn from **active contracts only**, so lapsed 2023–24 awardees are absent.
- Split by profile:

  | Segment | n | $0 in FY2026 | ≥$100k | Median FY2026 sales |
  |---|---|---|---|---|
  | All newcomers | 94 | 27 | 44 | $82.7k |
  | Staffing/DBITS | 48 | 8 | 29 | $199.6k |
  | **Software makers** | **23** | **10** | **7** | **$19.7k** |

- Among the software makers above $100k: Salty Cloud $3.3M, Veoci $703k (founded long before), Document Logistix $470k (an established UK firm).
- Small makers: Mongoose $80k, 3Di $48k, Transact Campus $38k, Saltus $31k, Validas $20k, Trusted Driver $10k.

**Top 3 failure modes:**
1. **The contract amplifies demand; it does not create it.** For the profile P5 needs, the median DIR software maker sold about $20k in FY2026, and 43% sold nothing, even though they arrived with products and references. A founder arriving with neither scores out: Sourcewell weights "Marketplace Success" and "Ability to Sell and Deliver".
2. **Timing and capital.**
   - A product plus 1–3 pilot agencies first, then a solicitation window that may be years away. That is 2–4 years to meaningful revenue.
   - Insurance certificates, TX-RAMP, a HUB plan and a US entity.
3. **Founder fit.** US local-government selling from Israel with 0–3 hours of overlap, plus implementation labour. The 49% award rate means about 39 competitors per category until re-solicitation.

**Verdict:** **Weak.** It is the only Track B route in Phase 9, and it is slow.
- Steps: CF 4,0,2,4,2 = 50 · Scal 4,5,2,3,2,2 = 62 · Dist 3,2,1,0,3 = 35 → 51.8, penalty 12 → **39.8**.
- **Decisive assumption:** a vendor with 1–3 pilots can score into a Sourcewell or DIR award band and then sell beyond about $20k a year through it.
- **Cheapest desk check:** pull Sourcewell Proposal Evaluation PDFs for 5–10 software solicitations. Record the lowest awarded score and whether any awardee had fewer than 5 public customers. **Kill if none did.**

### P6. Holding a DIR vehicle and reselling small vendors' SaaS (Vertosoft model)
**Top 3 failure modes:**
1. **The winners rode one blockbuster brand plus relationships.** Ondaro had ServiceNow; SATRDE had Zendesk; Precision Task Group is a Workday partner. Small vendors without a vehicle are the leftovers Carahsoft and Vertosoft declined, the same adverse selection that killed L11.
2. **Margin and credit.** A 3–8% reseller margin [Hypothesis]. Pass-through credit exposure. Some DIR contracts bar designated resellers. You need $1M+ of vehicle sales for Track A.
3. **No path to the vehicle.** A DIR contract needs a response to a solicitation, references and a HUB plan. The founder has none of these, and no US public-sector relationships.

**Verdict:** **Kill.**
- Steps: CF 4,1,1,1,1 = 35 · Scal 3,3,1,2,1,0 = 36 · Dist 3,1,2,0,1 = 31 → 34.6, penalty 13 → **21.6**.
- **Decisive assumption:** an unknown holder can sign a brand that sells over $1M a year that Carahsoft and Vertosoft do not already carry.
- **Cheapest desk check:** in DIR VSR data, list the brands of every reseller first active in 2023–24. **Kill if all brands with sales over $250k were already carried by Carahsoft, Vertosoft or SHI.**

### P7. Nimbus tier-5 listing (Israeli government cloud marketplace)
**Top 3 failure modes:**
1. **No spending evidence, and the listing is pass/fail.** "All services which were found to meet the parameters" win. That is the G-Cloud structure, where 86% of suppliers earn nothing.
2. **No product.** It is a channel looking for an offer. Ministries buy from Israeli incumbents, who all qualify equally.
3. **Israel's public-sector market is small and slow.** AWS/GCP marketplace listing plus security scoring take the founder's time with no buyer in view.

**Verdict:** **Kill.**
- Steps: CF 0,2,3,4,2 = 42 · Scal 1,4,1,3,0,3 = 41 · Dist 2,1,0,1,1 = 18 → 36.8, penalty 14 → **22.8**.
- **Decisive assumption:** ministries buy tier-5 SaaS from small listers.
- **Cheapest desk check:** search mr.gov.il storefront purchase notices for "נימבוס" plus "שכבה 5" orders. **Kill if no small-vendor orders appear.**

### P8. Israeli open-finance bank-feed reconciliation for accounting firms (licensed information-service provider)
**What I checked (search #4):**
- The ISA had issued about **8** open-banking licences by early 2023: RiseUp was the first AISP in Sep 2022, and Summa was described as the 7th.
- A separate 2024 payments law applies to payment initiation.
- Equity and insurance directives exist, but no amounts were found [Secondary: legalink, barlaw, gkh-law snippets].

**Top 3 failure modes:**
1. **The licence is either out of reach or no moat.** The licence route needs equity, insurance and law-firm support [Unknown amounts; Hypothesis: well over $2k]. The licensee-API route is open to every Israeli developer. The holder count of about 8 and growing means it is not capped.
2. **The platforms own the integration.** Hashavshevet, Rivhit, iCount and Morning, and the licensed aggregators (Finbot: 18 IL apps since 2024), can add bank feeds natively. The founder would be a feature on someone else's roadmap.
3. **Israeli B2B newcomer outcomes are about zero.** Hebrew business apps have a median of 0 ratings. Agent F's −1 to −3 prior applies for undiscovered incumbents.

**Verdict:** **Weak.** Kill if licence capital exceeds about $10k.
- Steps: CF 1,0,1,4,4 = 37 · Scal 2,5,2,4,2,4 = 64 · Dist 4,2,0,2,2 = 36 → 47.6, penalty 14 → **33.6**.
- **Decisive assumption:** the licence, or a licensee's resale API, is obtainable for under $10k within 9 months, and fewer than about 10 non-bank holders serve accountants.
- **Cheapest desk check:** run the ISA licensee list through a Wayback snapshot of isa.gov.il (gov.il returns 403 live), then read the bookkeeping vendors' feature pages for "חיבור לבנק" / "התאמות בנקים". **Kill if 2 or more of the top 4 already have automatic bank feeds.**

### P9. Israeli back-office for EU/UK accountants on EU adequacy
**What I checked (search #5):**
- No 2025–26 change was found.
- Access Now, EDRi and 9 NGOs asked the Commission to reconsider after the Jan 2024 reconfirmation.
- The 2011 decision lets EU DPAs suspend flows [Secondary].

**Top 3 failure modes:**
1. **Adequacy is not a moat.** Every Israeli firm has it, EU-located outsourcers have it better, and SCCs are boilerplate for Indian vendors [Agent F's own judgement]. It is also politically contestable.
2. **Labour arbitrage runs the wrong way.** Israeli bookkeeping wages are well above India and the Philippines. The founder would be running a staffing business in a craft he does not practise, in German or Dutch, which he does not speak.
3. **No channel.** Outbound to accountants, with no newcomer data.

**Verdict:** **Kill.**
- Steps: CF 3,3,3,2,1 = 50 · Scal 3,4,1,1,0,2 = 37 · Dist 3,1,0,1,1 = 22 → 39.2, penalty 14 → **25.2**.
- **Decisive assumption:** EU firms pay a premium for "no SCC/TIA paperwork".
- **Cheapest desk check:** read the service pages of 10 Indian offshore accounting vendors that sell to the UK and EU. **Kill if most already advertise GDPR/SCC handling as included.**

### P10. Liquidity roll-up in one small-language local-marketplace vertical
**Top 3 failure modes:**
1. **The comparables are survivors.** Handyhand took 5–7 years and bought rivals. Of about 250 2023–26 entrants measured, none reached 1% of its incumbent's rating base.
2. **Capital.** The EF floor is $51.5k. The only affordable targets have 0–30 ratings, so buying ten of them buys almost nothing.
3. **Cross-border override.** Vinted out-rates local incumbents in FI, RO, HR, CZ and GR. Liquidity in Israel sits in Facebook and WhatsApp groups that cannot be bought.

**Verdict:** **Kill.**
- Steps: CF 3,0,0,3,1 = 30 · Scal 2,3,1,3,2,2 = 44 · Dist 3,2,0,1,2 = 29 → 35.4, penalty 13 → **22.4**.
- **Decisive assumption:** a mid-scale local player (100–500 ratings) sells for $10–20k and its users stay.
- **Cheapest desk check:** check Flippa or Acquire public listing pages (not the API, which returns 401) for marketplace listings under $25k in small-language markets. **Kill if there are none with over 100 active providers.**

### P11. Software-assisted payroll-audit firm employing certified auditors (Israel)
**What I checked (search #7):**
- No price was found.
- The 2017 regulations give **30% (employer) / 50% (service buyer) sanction reductions** for relying on a certified auditor. That is a real demand driver [Secondary: chamber.org.il].
- The State Comptroller's 2023 audit of 5 municipalities found widespread violations.

**Top 3 failure modes:**
1. **The licence is abundant and the founder cannot hold it.** There are 2,029 certified auditors against about 2,065 service-contractor plus 1,929 manpower licences. Falling inflow (83 in 2026) reflects market saturation, not a cap.
2. **Service labour and price pressure.** Revenue equals auditor hours. Public tenders are price-weighted, and BDO-type firms already bid.
3. **Israel-only, tender-paced.** No newcomer win rates. The software edge (payslip parsing) is copyable by incumbents' own staff tools.

**Verdict:** **Weak.** Track A at best, and only as a services firm.
- Steps: CF 3,2,3,2,1 = 46 · Scal 2,4,2,2,0,3 = 44 · Dist 4,3,1,2,2 = 46 → 45.2, penalty 12 → **33.2**.
- **Decisive assumption:** the tender price per audited worker exceeds auditor cost by enough for software leverage to matter.
- **Cheapest desk check:** download 2–3 municipal tender result notices or protocols ("פרוטוקול ועדת מכרזים בדיקת שכר") that publish winning prices. **Kill if the winning price is under about ₪15 per worker per month** [Hypothesis threshold].

---

## 3. Leader challenges

### K8 Framer kit: **50.4 is right** (strict 49.8)
- The auditor's speed cut (4→3, CF 84→80) prices a fact that is genuinely new to K8. Unlike H7, where "79% get ≥1 sale" was measured, K8 has **no** evidence of a fast first sale, and the bounds point against it:
  - at most 9–13% of creators paid in a month;
  - median followers among 2026 creators is 43;
  - 1 featured item in about 290 sampled;
  - supply up 2–3×.
- **Not too harsh:** CF 80 still assumes near-zero capital and is the joint-highest CF in the cluster.
- **Possibly lenient:** adding first customers −1 as well gives 49.8. I do **not** press for it. Phase 8 rejected the same double cut for H7, and the board should treat both alike. The penalty stays at 13, because no sales counts exist to contradict the assumption directly.
- **Calibration:** non-binding. A marketplace kit's defensibility is already ≤1 under any split that yields Scal 56 [Hypothesis: back-solved].

### H6 College-baseball API: **hold 52.2** (dissent range 51.2–52.2)
- The SIDEARM terms ("personal, noncommercial use") remove the school-site fallback. Every primary source is now under noncommercial terms, and stats.ncaa.org and StatBroadcast block automated clients.
- The red-team reading is that "lawfully sell" is now contradicted at the contract level across *all* sources, which would justify penalty 14 → 51.2.
- I hold at 52.2 for two reasons:
  - CFBD (commercial use permitted, 3,600+ patrons) and Highlightly operate openly on public facts;
  - facts are not copyrightable.
- **The trigger to cut** is any enforcement against a stats API, or a C&D on a sportsdataverse repository.

### H1 Meshtastic kits: **hold 51.2**
- Tindie, the archived evidence, is a weak negative on a channel H1 never planned to use. The 12 Tindie listings at $150+ have 0–1 reviews each.
- But Dist 71 is now the **least-evidenced high score on the board**. No conversion has been measured at $300+ anywhere.
- I support the auditor's trigger: if Amazon $300+ Meshtastic bundles have under about 20 ratings, cut proven channel −1 → 50.0. A pre-emptive cut of first customers −1 (→ 50.6) is defensible, but I do not apply it because it rests on a different channel.

### M1 Sage 50 API: **take the downside, 48.6** (penalty 12→13)
- New this phase, verified by the auditor: the Aug-2023 NA programme explicitly covers **Sage 50 US/CA** and requires signing "the Developer Partner Program Agreement". The only NA agreement on record:
  - licenses development "in connection with Developer's efforts to sell end user licenses";
  - bars use "for the benefit of any third party";
  - allows termination for convenience on 90 days' notice.
- M1's paying customer *is* a third-party vendor. A single programme with a single agreement whose stated purpose excludes that customer is as close to direct contradiction as desk research can reach without signing. So this meets the penalty rule.
- I do not re-propose Phase 8's defensibility 1→0. The 90-day clause is the same platform risk already priced.

### H7 Blender add-ons: **hold 55.4**; overrated as a forecast, not mis-scored
- Phase 9 adds no H7-specific evidence. The Phase 8 dissent (54.8, first customers −1) was rejected as double counting, and nothing new re-opens it.
- **Calibration:** non-binding. Scal 58 is reachable only with defensibility 0–1 under any plausible split, for example depth 3, recurring 1, acquisition 3, leverage 5, fit 5 [Hypothesis: back-solved, because per-criterion scores were never published].
- The board must keep carrying the caveat: H7's CF 80 rewards a cheap start, and per product it is a 2–5% lottery.
- Phase 9's main contribution to H7 is indirect. No "moat" idea came within 10 points of it, because every moat this founder can afford is copyable and every scarce one is unaffordable.

---

## 4. Recommended ranking

| Idea | CF | Scal | Dist | Pen | Adj | Verdict |
|---|---|---|---|---|---|---|
| P1 Boater-safety courses | 56 | 51 | 66 | 12 | **44.0** | Viable with conditions |
| P5 Co-op contract SaaS | 50 | 62 | 35 | 12 | **39.8** | Weak |
| P8 Open-finance bank feeds | 37 | 64 | 36 | 14 | **33.6** | Weak |
| P11 Payroll-audit firm | 46 | 44 | 46 | 12 | **33.2** | Weak |
| P2 Independent IRH | 46 | 42 | 39 | 13 | **30.0** | Kill |
| P4 Household-pesticide registration | 35 | 46 | 42 | 13 | **27.8** | Kill (for this founder) |
| P3 Device exclusivity DTC | 43 | 34 | 49 | 13 | **27.6** | Kill (for this founder) |
| P9 Adequacy back-office | 50 | 37 | 22 | 14 | **25.2** | Kill |
| P7 Nimbus tier 5 | 42 | 41 | 18 | 14 | **22.8** | Kill |
| P10 Liquidity roll-up | 30 | 44 | 29 | 13 | **22.4** | Kill |
| P6 DIR reseller | 35 | 36 | 31 | 13 | **21.6** | Kill |

**Leaders:** H7 55.4 · H6 52.2 · H1 51.2 · K8 50.4 · **M1 48.6**.

**Tracks:**
- **Track A:** P1 only, conditional on the provider-share check and a capital source above $2k.
- **Track B:** P5 only, on a 2–4 year horizon, and only after a product with references exists. It is an amplifier, not a starter.

**Cheapest information:**
- P1: state provider-share reports (free).
- P2: a holder-name scan of the MoH registry for platform partners (free; likely closes the idea).
- P5: Sourcewell lowest-awarded-score profiles (free).

**Verified contradictions of shortlist claims:**
- P2: Pure Global now sells Israel.
- P1: the Spanish slot is already filled (Boat-Ed Spanish, Texas); Boat-Ed prices from $30.
- P5: the 47% ≥$100k figure is driven by staffing firms and drawn from active contracts only. Software makers' median is $19.7k, with 43% at $0.

**Sources:**
- [Boat-Ed vs Recademics](https://www.boat-ed.com/blog/boat-ed-vs-recademics/)
- [TPWD internet courses](https://tpwd.texas.gov/learning/boater_education/internet_courses.phtml)
- [DBW Nov-2025 Commission PDF](https://dbw.parks.ca.gov/pages/28702/files/2025%20DBW%20Commission%20Boating%20Education%20and%20Outreach%20Program%20Summaries_v2.pdf)
- [Trustindex: Recademics](https://www.trustindex.io/reviews/recademics.com)
- [Pure Global: Israel](https://www.pureglobal.com/markets/israel) · [Pure Global pricing](https://www.pureglobal.com/services/pricing)
- [NASBLA course approval](https://www.nasbla.org/education/nasbla-course-approval)
- [legalink: open banking in Israel](https://www.legalink.net/en/publications/newsletters/open-banking-is-taking-off-in-israel/3157/) · [barlaw.co.il/08mm](https://barlaw.co.il/08mm)
- [Pearl Cohen: adequacy renewal](https://www.pearlcohen.com/eu-renews-israels-data-protection-adequacy-recognition/)
- [chamber.org.il: certified wage inspector regulations](https://www.chamber.org.il/serviceslobby/legal/1856/79616/)
- [gov.il pesticides service (search snippet only)](https://www.gov.il/en/service/pesticides-approval-licensing-import-new)
- Agent E's DIR data via data.texas.gov (re-analysed)
- All accessed 2026-10-13.
