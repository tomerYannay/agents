# Phase 9 Evidence Audit of shortlist P1–P11 (P9-AUDIT), 2026-10-13

**Auditor:** independent Evidence Auditor (P9-AUDIT). I worked independently of the red team and did not read its output.

**WebSearch:** 6 of 8 used, each logged as `P9-AUDIT` in `research-notes/search-log.txt`:
1. California Boater Card issuance in 2026 (P1)
2. Israel AMAR registration-holder pricing at global platforms (P2)
3. MoEP household-pesticide registration and efficacy trials (P4)
4. ISA financial-information-service licensees (P8)
5. Municipal wage-inspection tender prices, in Hebrew (P11)
6. Central (Accountant General) wage-inspection tender, in Hebrew (P11)

**Primary sources re-opened.** I used WebFetch, or curl/Python with a generic `research-bot` User-Agent. No personal identifiers were sent.

| Source | What was checked |
|---|---|
| NASBLA `Fee_Structure.pdf` and `Terms_and_Conditions.pdf` (higherlogicdownload S3) | Fees, 3-year re-review, third-party content licensing, reporting |
| tpwd.texas.gov internet_courses page | Texas provider list, prices, Spanish offering |
| parks.ny.gov boating-education page | New York online provider list and Spanish flags |
| dbw.parks.ca.gov pages 28734, 29183 and 30826 | California free state course in English and Spanish |
| DBW "2024 California Boater Card Program Report" (PDF, April 2025) | Cards issued per year 2018–2024; 16 courses; Spanish course |
| californiaboatercard.com/courses/ via Wayback | 9 snapshots, 2018-07 to 2026-08: approved-provider count over time |
| recademics.com and its California launch post | State pages; student counts |
| boatus.org/courses | Free boater-safety course |
| he.wikisource.org transcriptions of statutes | Medical Equipment Law 2012; Medical Equipment Regulations (Registration) 2013 (KT 5773/1311); Dangerous Substances Regulations (Registration of Pesticides) 1994, amended 1998 and 2003 |
| pureglobal.com | /markets/israel and /services/pricing |
| P9-C's raw MoH AMAR pull (30,212 records) | Recomputed active registrations, active holders and per-holder counts. I re-analysed the agent's data file; I did not re-pull from the API. |
| data.gov.il `domestic_pesticides` | 291 rows via the CKAN datastore API |
| data.texas.gov a743-wj72 (DIR FY2026 VSR) | SoQL aggregates |
| sourcewell.co/contract-list | xlsx, updated 13 Oct 2026 |
| barlaw.co.il | Summa Technologies licence item |
| herzoglaw.co.il | 18 May 2026 bill note |
| State Comptroller May 2023 pesticides report | Agricultural only, so not relevant to P4 |
| Three municipal tender PDFs | None was a wage-inspection tender |

**Blocked or unreadable (none bypassed):**
- **gov.il:** 403 (Cloudflare).
- **californiaboatercard.com:** 403. I used Wayback copies instead.
- **goldfarb.com:** 403.
- **isa.gov.il:** returns 200, but it is a JavaScript single-page app with no licensee data in the HTML. I did not probe its APIs.
- **learn.recademics.com:** JavaScript app; I did not probe its APIs.
- **NASBLA course-approval page:** redirects to a members' community portal and the content is not in the HTML. The two PDFs it links to were readable.
- **Zap breast-pump category:** stuck in a redirect loop. The Zap "מסכת לד" (LED mask) search was readable.
- **bat-yam.muni.il tender PDF:** 404.
- **State Comptroller PDF:** readable, but it covers agricultural pesticides only.

**Scratch:** `scratchpad/p6plus/P9-audit/{data,scripts}`. Scripts are `cbc.py` (California list parser), `grepctx.py` and `pdf.py`. For PDF text and xlsx I used pypdf and pandas from P9-E's scratch venv, always run with `-I`.

**Scoring convention:** frozen rubric. Criterion scores are 0–5 in rubric order:

| Group | Criteria | Step values |
|---|---|---|
| CF | Spending · Speed · Capital · Margin · Labour | ×5 · ×4 · ×4 · ×4 · ×3 |
| Scal | Depth · Recurring · Acquisition · Leverage · Defensibility · Fit | ×3 · ×4 · ×4 · ×4 · ×3 · ×2 |
| Dist | Clarity · Discoverability · Proven · First · Beyond | ×4 · ×4 · ×6 · ×3 · ×3 |

Balanced = 0.4 CF + 0.4 Scal + 0.2 Dist. Adjusted = Balanced − penalty.

**Calibration note: Agent F's guidance that Defensibility should be at most 2 for moats obtainable in under ~9 months.**
- **I apply it,** but as a conclusion from evidence, not as a blanket rule. My own measurements support it independently in three places:
  1. California's approved boater-course list grew 11 → 19 providers in 2022–26, with keyword-style names such as "A Quick Boater Course", "A+ Approved Boating Course" and "Take My Boat Test".
  2. NASBLA explicitly lets a provider license another provider's approved course content (T&C Administrative §7), which shortens a follower's path.
  3. AMAR shows about 58–94 new holders per numbering band.
- **Exceptions where I score above 2:**
  - **P5** (term-gated co-op award with a fixed re-solicitation window): F's own exception applies. Score 3.
  - **P4:** reg. 11(4) lets the committee refuse a product when a less-harmful registered product exists for the same purpose. That is a quasi-cap protecting the first registrant. Score 3.
  - **P10:** the moat takes 5–7 years, so the cap does not apply. Score 4.
- **Effect:** on ideas whose discovery agents implied 3+, applying the cap moves Adjusted by about −0.6 to −1.2 each. No ranking changes.

---

## Summary table

| ID | Verdict | Suggested penalty | One-line reason |
|---|---|---|---|
| P1 Boater-safety course | **Partly supported; two core claims refuted** | 12 | NASBLA fees verified ($4,500/$5,500 + $550 per state; full re-review every 3 years). But: **(a)** California's list grew **11 (2022) → 15 (2023) → 19 (2026)**, including doorway-style names, so the "holder counts stay small" claim fails in the deadline state. **(b)** California already has a **free NASBLA-approved Spanish course from DBW** plus America's Boating Club in Spanish, and New York lists 2 Spanish options. The Spanish gap is real only in Texas (Boat-Ed alone). **(c)** NASBLA lets providers license third-party approved content, so a follower can be faster. California cards: 37.7k (2022), 53.7k (2023), 82.2k (2024). No 2026 data. |
| P2 Independent IRH via platforms | **Weak; channel claim refuted** | 13 | **Pure Global does serve Israel**: a /markets/israel page offers "local partner … acting as your Israeli Representative" for a flat annual fee. Israel is not in its 18-market price table, which is what P9-C saw. The white-label slot is filled. ISO 9001 is **not** a legal requirement on the holder as such: Reg. 20 puts it on whoever **stores and transports** devices, together with a business licence. Reg. 21 requires the applicant to appoint a contact person **from among its employees**. The law has criminal liability (§15) and officer liability (§16). Registry figures reproduce: 13,404 active, 1,160 holders, Emergo 134/84, L.Sh. 93/61. |
| P3 Niche Class II device, DTC | **Weak** | 12 | Statutory decision deadline is 120 days (Reg. 7). The 45 business-day fast track is [Secondary]. The ISO 9001 burden falls on storage/transport, so it can go to a certified 3PL, but inventory still exceeds the budget. Zap "מסכת לד" returns **17 results** (9 beautician equipment, 2 facial care), so the visible DTC category is thin. No sales data. |
| P4 Household-pesticide registration | **Weak, but moat partly confirmed** | 12 | Regs (1994/2003): application needs efficacy-trial results **and literature**, foreign registration documents, a toxicology summary and a quality test at a lab the commissioner approves. Every decision needs the inter-ministerial committee's consent. There is **no statutory decision deadline**. Validity is 3 or 6 years. Transfer needs the holder's consent. Refusal is allowed if a less-harmful registered alternative exists. Local trials are **not explicitly mandated**. Time and cost: [Unknown]. Dataset: 291 rows, messy; at least 6 holders whose earliest active registration falls in the 610–682 band. |
| P5 Co-op-first public-sector SaaS | **Supported as data; weak as a newcomer path** | 13 | DIR FY2026 reproduces exactly: $3,842.9M across 582 vendors, data through 2026-08. Sourcewell reproduces: 1,060 contracts, 932 suppliers, 142 solicitations, median 6 awards, Public Safety Software 39. The cohort uses **currently active** contracts, so vendors that left are excluded (survivor bias). The founder has no product and no references. |
| P6 DIR reseller | **Supported (figures); weak (fit)** | 13 | Ondaro $4.66M (7 customers) and SATRDE $1.03M (7 customers) reproduce. Vertosoft is now $16.95M across 129 customers, up from $15.6M/117 when Agent E pulled it. Margin is [Unknown]. Both newcomers rode one large brand. |
| P7 Nimbus tier 5 | **Not re-opened** (gov sources blocked) | 14 | No spending or winner data exists. Pass/fail and re-opening, so no moat. |
| P8 Open-finance bank feeds | **Weak** | 13 | **At least 7 licensees by Dec 2023** ("Summa is the seventh company in Israel to receive this license", barlaw.co.il, 5 Dec 2023). A 2026 bill note says reliefs exist for **foreign** information-service providers. Capital and insurance amounts: [Unknown]. The ISA site is a JS app, so the licensee list was unreadable. |
| P9 Adequacy-positioned back office | **Not re-opened** (Agent F's EC check accepted) | 13 | The decisive assumption (a buyer premium for avoiding SCCs) is untested, and Agent F himself thinks it false. |
| P10 Marketplace liquidity roll-up | **Not re-opened** | 13 | Fails both capital and the time window by the agent's own account. |
| P11 Payroll-audit firm | **Weak; price still unknown** | 13 | Two searches found no priced wage-inspection tender. Three municipal PDFs opened were unrelated. 2,029 certified auditors against about 2,065 service-contractor licences (P9-C) suggests oversupply. |

---

## P1. Approved online boater-safety course (D1/D2)

### Evidence

**NASBLA fees** [Verified: higherlogicdownload…/Fee_Structure.pdf, 2026-10-13]

| Review | Member | Non-member |
|---|---|---|
| Classroom | $2,450 | $3,500 |
| Timed internet | $3,150 | $4,500 |
| Interactive internet | $3,850 | $5,500 |
| Additional state | $385 | $550 |

- The course fee includes one launch state. A custom question bank adds $300.
- "Payment of fees does not guarantee course approval."
- **Agent D's figures reproduce.**

**NASBLA Terms and Conditions** [Verified: Terms_and_Conditions.pdf, 2026-10-13]
- Admin §6: "ALL NASBLA Approved courses must have a complete review every three years."
- Admin §5: approval is "at the sole discretion of NASBLA".
- Def. 20: "State" includes "another regulating jurisdiction" outside the US.
- Def. 5: translations need a signed "Certificate of Accuracy".
- Admin §21: providers report student and certificate counts to each state by 1 December.
- **New, and adverse to the moat:** Admin §7 says "A course provider may incorporate course materials from a third-party vendor (i.e., publisher) instead of developing proprietary materials". The third party's permission is required, and its materials must themselves be NASBLA-approved.
  - So a follower can **license** an approved course rather than write one. That shortens the content step, which is the founder-heavy 3–9 months Agent D assumed.
  - It may also cut the founder's own cost, but it removes content quality as a moat.
- No turnaround time is stated anywhere: [Unknown].

**Texas** [Verified: tpwd.texas.gov internet_courses page, 2026-10-13]
- Six English providers, each plus a $10 state fee:

  | Provider | Price |
  |---|---|
  | Recademics | $29.99 ($19.99 military) |
  | Boat-Ed | $54.95 |
  | BOATsmart! | $39.95 |
  | BoatUS | $1.00 |
  | BOATERexam | $49.95 |
  | iLearnToBoat | $74.95 |

- **One Spanish offering: Boat-Ed Texas Spanish at $54.95.** Agent D's Texas claims reproduce.

**New York** [Verified: parks.ny.gov boating-education, 2026-10-13]
- **Eight online providers, not five:**
  - America's Boating Club ("Spanish online course available");
  - Boat-ED;
  - BOATERexam;
  - BOATsmart;
  - BoatTests101 ("Disponible en español");
  - Boat-Ed+;
  - New York Quick Boater Course;
  - Recademics.
- So New York already has **two Spanish options**. Agent D's count of 5 is outdated or incomplete.

**California**
- **The state's own free course exists in English and Spanish** [Verified: dbw.parks.ca.gov/?page_id=30826]:
  - "The California Course for Safe Boating course and exam are free … The only required fee is the one-time $10 fee for the California Boater Card".
  - The 2024 report says "DBW home-study course has also been translated to Spanish, making DBW the first to produce a Spanish language boating safety course in California that is approved by … NASBLA".
  - America's Boating Course is also offered in English or Spanish [Verified: page 28734].
- **The Spanish wedge is refuted for California**, the largest card market.

**California provider-list history** [Verified: Wayback snapshots of californiaboatercard.com/courses/, parsed by `cbc.py`, 2026-10-13]

| Snapshot | Providers |
|---|---|
| 2018-07 | 10 |
| 2020-08 | 11 |
| 2021-07 | 11 |
| 2022-08 | 11 |
| 2023-07 | 15 |
| 2024-07 | 15 |
| 2025-01 | 15 |
| 2026-06 | 19 |
| 2026-08 | 19 |

- **2023 entrants:**
  - "A+ Approved Boating Course"
  - "Safe2Boat"
  - "Super Quick Course" (gone by 2024, replaced by "A Quick Boater Course")
  - "Drive A Boat USA"
- **2026 entrants:**
  - Recademics
  - Boat-Ed+
  - AnchorPoint Boater Safety
  - The Qualified Captain
  - Take My Boat Test
- **Exit:** iLearnToBoat left in 2026 (Kalkomey's second brand).
- **Reading:**
  - In the deadline state the list nearly doubled within 4 years.
  - Several entrants use alphabetical or keyword names ("A+ …", "A Quick …"). That is the doorway-brand pattern Agent D attributed only to cheap test-based approvals.
  - The "content-reviewed approvals stay at 5–6 for a decade" finding holds for Texas, a non-deadline state, but **not** where demand spiked.
  - A follower can obtain the moat about as fast as the founder.
- The DBW 2024 report said 16 courses, against 15 on the list in Jan 2025. That is consistent within one listing difference.

**Demand, including after the deadline** [Verified: DBW "2024 California Boater Card Program Report", April 2025, p. 13–14]

| Year | Cards issued |
|---|---|
| 2018 | 18,090 |
| 2019 | 21,154 |
| 2020 | 46,071 |
| 2021 | 39,053 |
| 2022 | 37,693 |
| 2023 | 53,730 |
| 2024 | 82,211 |

- Cumulative issuance was about 300k at 1 Jan 2025.
- Aug 2024–Aug 2025: 144,608 [Secondary: DBW 2025 commission summary via search, P9-AUDIT #1; Agent D marked it Verified].
- **No 2025 calendar-year or 2026 figure is public** [Unknown]. The phase-in ended on 1 Jan 2025.
- In pre-final-phase years, 2021–22 ran at roughly 38–39k a year. That is a reasonable [Hypothesis] floor for post-deadline steady state, and it is shared by 19 providers plus a free state course.
- DBW: "Google search advertisement was the primary digital marketing tool … optimal return on investment". That is the state's outreach, not provider CAC.
- New York 2026 volumes: not found [Unknown].

**Newcomer outcome (Recademics)**
- On the Texas, New York and California lists [Verified]. Its homepage links pages for all 50 states, which are SEO pages and not proof of approval.
- The only public count is the free refresher course: "136 Students" [Verified: recademics.com].
- Paid volume: [Unknown]. Its learning-platform app is JavaScript-only.

**Free anchors**
- BoatUS: $1 in Texas; "Free Boater Safety Course" on boatus.org [Verified].
- California DBW: free in English and Spanish [Verified].

### Verdict and scores
- **Supported:** fees, the Texas list and prices, mandatory demand, and a newcomer getting listed.
- **Refuted:** "holder counts stay small" (California), "Spanish gap" (California and New York), and "follower needs as long" (third-party licensing allowed).
- Budget: the first state costs $4.5–5.5k before ads, 2.3–2.8× the $2k budget.
- CAC: [Unknown].

| Group | Scores | Total |
|---|---|---|
| CF | 4,1,2,4,4 | 60 |
| Scal | 3,1,3,4,2,4 | 55 |
| Dist | 5,4,1,2,3 | 57 |

- Proven channel is 1 because a state list is a directory listing, and a directory is not credited without newcomer outcomes.
- Balanced 57.4; penalty 12 → **45.4**.

---

## P2. Independent Israel Registration Holder (C1, B3 merged)

### Evidence

**Statute** [Verified: he.wikisource.org "חוק ציוד רפואי", transcription, 2026-10-13]
- §3(b): an application "תוגש … בידי תושב ישראל או תאגיד הרשום בישראל". That is, it must be filed by an Israeli resident or an Israeli-registered corporation.
- §11: the holder must carry out monitoring and inspection and report special events.
- §15: offences carry up to 1 year in prison, 3 years where public health is harmed, and doubled or quintupled fines for corporations.
- §16: officers are presumed to be in breach.
- **Liability is real and personal to officers.**

**Regulations 2013** [Verified: he.wikisource "תקנות ציוד רפואי (רישום ציוד רפואי בפנקס וחידושו)", KT 5773/1311; amendments after the transcription, including the 2023 declaration route, not checked]
- Reg. 7(a): a decision within **120 days**.
- Reg. 19: the manufacturer must hold an ISO 13485 certificate.
- **Reg. 20: devices "יובל ויאוחסן בידי מי שמחזיק אישור … תואמים את דרישות תקן ISO 9001, וכן רישיון עסק לאחסון והובלה". That is, devices must be transported and stored by someone with ISO 9001 certification and a business licence for storage and transport.**
  - So ISO 9001 attaches to **whoever stores and transports**, not to the registration holder as such.
  - An IRH that never handles goods can, on this text, avoid ISO 9001 [Hypothesis; MoH practice may differ, and gov.il was blocked].
  - This **resolves the "sources conflict" note**: both secondary sources are partly right.
- Reg. 21: the applicant appoints a contact person "מתוך עובדיו", i.e. from among its own employees.
- Reg. 22: for life-supporting devices, implants, imaging and lasers, that person needs a life-sciences or medical degree or an engineering certificate.
- Reg. 23: labels must carry the holder's name and phone in Hebrew, Arabic and English.

**Registry recomputation** (P9-C's 30,212-record pull, re-analysed, expiry ≥ 2026-10-13)

| Measure | Value |
|---|---|
| Active registrations | **13,404** |
| Active holders | **1,160** |
| Emergo Israel | 134 registrations / 84 manufacturers |
| L.Sh. | 93 / 61 |
| Arazy | 11 / 6 |
| BIOREG | 2 |
| Regulog Plus | 3 |
| Median active registrations per holder | 2 |
| Holders with exactly 1 | 465 |

- Agent C's figures reproduce.

**Global platforms** [Verified: pureglobal.com/markets/israel, 2026-10-13]
- The page says: "Our local partner's expertise in Israel's medical device market offers you: … Acting as your Israeli Representative, managing the registration process and ensuring ongoing compliance with AMAR's regulations", with "AI-powered dossier compilation and local representation, all for a flat annual fee".
- Israel is among the 32 markets in Pure Global's menu, but **not** in the priced 18-market table, where prices start at $1,000–3,000 a year per listing [Verified: /services/pricing].
- **So Agent C's "Pure Global does not list Israel" is wrong.** Pure Global already has an Israeli partner, and the white-label slot at the largest tech-enabled platform is taken.
- Asphalion, Freyr and Qualtech Israel pages: not found within the search budget [Unknown]. Freyr listing Israel was already noted by C.

**Newcomer outcomes:** recent service holders have 0–3 registrations (reproduced above).

### Verdict and scores
- **Main channel claim refuted.** The ISO 9001 budget concern is reduced, but service labour and liability remain.
- The moat (an Israeli entity) blocks foreigners only. Israeli competitors face no barrier, and holder inflow continues.

| Group | Scores | Total |
|---|---|---|
| CF | 3,2,3,3,2 | 53 |
| Scal | 2,4,2,2,2,2 | 48 |
| Dist | 4,2,1,1,2 | 39 |

- Balanced 48.2; penalty 13 → **35.2**.

---

## P3. Niche Class II device with exclusivity, DTC (B1)

### Evidence
- **Timeline:**
  - The statutory decision deadline is 120 days (Reg. 7) [Verified, as above].
  - The 45 business-day fast track is [Secondary: Emergo] and was not re-opened (gov.il 403).
  - The 14-day route with two reference authorisations is [Secondary: meddeviceguide].
- **ISO requirement:** Reg. 20 applies ISO 9001 to storage and transport. A DTC holder that uses a certified, licensed 3PL may not need its own certificate [Hypothesis]. The inventory capital of about $3–6k [Hypothesis, B] still exceeds the budget.
- **Category competition (one example)** [Verified: zap.co.il search "מסכת לד", 2026-10-13]:
  - 17 results in total: 9 in beautician and salon equipment, 3 lighting, 2 facial care, 2 costumes, 1 welding.
  - So the consumer LED-mask category on Israel's main price-comparison site is thin. That means either low demand or sales through non-Zap channels (Instagram, AliExpress). Unit sales: [Unknown].
  - Agent B's breast-pump figure (98 results) was not re-checked; the Zap category redirect looped.
- **Exclusivity reliability:** 19.7% of active manufacturers already have more than one Israeli holder [B's analysis; not recomputed]. That is consistent with my registry check that holders are numerous and small.
- **Personal-import leakage:** [Unknown].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 2,2,1,3,3 | 43 |
| Scal | 2,1,3,3,2,2 | 44 |
| Dist | 3,2,1,2,3 | 41 |

- Balanced 43.0; penalty 12 → **31.0**.

---

## P4. Israeli household-pesticide registration (B2)

### Evidence

**Regulations** [Verified: he.wikisource "תקנות החומרים המסוכנים (רישום תכשירים להדברת מזיקים לאדם)", KT 5754/1285 plus amendments 1998 and 2003]
- Reg. 2: no sale, import or use unless the product is registered **in the importer's name**.
- Reg. 3(a), annexes required:
  1. "תוצאות ניסויים בתכשיר וספרות על דרכי השימוש בו" (trial results **and** literature) as proof of efficacy;
  2. foreign registration and labels;
  3. a toxicology summary plus SDS; a full toxicology dossier on request;
  4. shelf life;
  5. a quality-test certificate "שנעשתה במעבדה" from a lab the commissioner approves;
  6. a label in Hebrew and Arabic.
- Reg. 3(b): 12 copies of each annex.
- **There is no explicit requirement that trials be local.** Foreign trial data and literature appear admissible. That partly answers B's decisive question, but the committee can demand more [Verified text; practice Unknown].
- Reg. 9: every decision needs the consent of a **6-member inter-ministerial committee** (3 from Environment, 3 from Health). **No decision deadline exists anywhere in the regulations.**
- Reg. 10(b): validity is 3 or 6 years.
- Reg. 11(4): **refusal is allowed if "קיים תכשיר רשום המיועד לאותן המטרות המזיק פחות"**, i.e. a less-harmful registered product exists for the same purpose. This favours the first, safest registrant in a category and works as a quasi-cap.
- Reg. 2b: transfer requires the holder's written consent and, for imports, the manufacturer's consent.
- A second importer of the **same** product is not barred by the text [Hypothesis]. Exclusivity therefore rests on the manufacturer contract.
- Fees: none in the regulations [consistent with B's "free" claim].

**Registry** [Verified: data.gov.il `domestic_pesticides` datastore, 291 rows, modified 2026-10-13]
- Fields are partly shifted (purpose text appears in the holder column), so holder counts depend on parsing. 56 raw "holders", including junk; the genuine number lies between Agent B's ~25 and about 45.
- At least 6 genuine holders' earliest active registration falls in the 610–682 band, so **newcomers do enter**, slowly.
- Authorised user: "מדבירים" (exterminators) on 43 rows and "הקהל הרחב" (general public) on 37, with most rows blank.

**Time, cost and local-lab fees:** [Unknown].

### Verdict and scores
- The moat is **confirmed as committee-gated and slow, with no deadline**.
- The "local efficacy trials needed" fear is **not supported by the text**.
- Time and cost remain unknown, so it is very likely outside 9 months [Hypothesis].

| Group | Scores | Total |
|---|---|---|
| CF | 2,0,1,3,3 | 35 |
| Scal | 1,3,2,3,3,1 | 46 |
| Dist | 4,2,1,2,2 | 42 |

- Defensibility is 3 because of the Reg. 11(4) quasi-cap.
- Balanced 40.8; penalty 12 → **28.8**.

---

## P5. Co-op-contract-first public-sector SaaS (E1)

### Evidence
- **DIR FY2026** [Verified: data.texas.gov a743-wj72 SoQL, 2026-10-13]: sum $3,842,853,667, 582 distinct vendors, latest month 202608. **Reproduces exactly.**
- **Sourcewell** [Verified: sourcewell.co/contract-list xlsx, "Last updated Oct. 13, 2026"]: 1,060 contracts, 932 suppliers, 142 solicitations, median 6 awards per solicitation; Public Safety Software 39; "Software Solutions … Public Sector and Education Administration" 13. **Reproduces.**
- **Method check on the cohort** (P9-E `dir.py`, read):
  - Newcomers are defined from the **currently active** contracts dataset, so a vendor whose 2023–24 contract ended or was terminated is excluded. That makes "29% $0 / 47% ≥$100k" an **upper bound** [method observation].
  - Selection effect: awardees already had products.
- **Newcomer path for this founder:**
  - No product and no references.
  - Sourcewell scores "Marketplace Success" and "Ability to Sell and Deliver" [E, Verified].
  - Speed to first sale is 2–4 years.

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 5,0,2,4,2 | 55 |
| Scal | 4,5,2,3,3,3 | 67 |
| Dist | 4,3,2,1,3 | 52 |

- Defensibility 3 applies F's term-contract exception.
- Balanced 59.2; penalty 13 → **46.2**.
- It is the highest on the list only because spending and recurring revenue are real. It is not executable inside the Phase 9 window.

---

## P6. DIR contract-vehicle reseller (E2)

### Evidence [Verified: DIR FY2026 SoQL, 2026-10-13]

| Vendor | FY2026 sales | Customers |
|---|---|---|
| Ondaro LLC | $4,663,828 | 7 |
| SATRDE LLC | $1,029,029 | 7 |
| Vertosoft | $16,953,894 | 129 (vs E's $15.6M/117: the data has been updated since) |
| Veoci | $702,914 | 4 |
| Saltus | $30,687 | 3 |

- All reproduce.
- Reseller margin, the authorisation terms that allow adding brands mid-term, and designated-reseller bans are all [Unknown] or [Secondary].
- Both newcomers rode one major brand (ServiceNow, Zendesk) plus existing partner status [E].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 4,1,2,1,2 | 42 |
| Scal | 3,3,2,2,2,1 | 45 |
| Dist | 3,2,2,1,2 | 41 |

- Balanced 43.0; penalty 13 → **30.0**.

---

## P7. Nimbus tier-5 listing (E3)

### Evidence and scores
- Not re-opened. mr.gov.il tender PDFs were read by E; gov.il is blocked.
- There is no winner list, no spending data, and admission is pass/fail. Defensibility is 1.

| Group | Scores | Total |
|---|---|---|
| CF | 1,1,3,4,3 | 46 |
| Scal | 2,4,1,3,1,4 | 49 |
| Dist | 3,1,0,1,1 | 22 |

- Balanced 42.4; penalty 14 → **28.4**.

---

## P8. Open-finance bank feeds for accountants (F9-3)

### Evidence
- **Holder count:** "Summa is the seventh company in Israel to receive this license" [Verified: barlaw.co.il/insights_and_news/advising-summa-technologies-on-obtaining-financial-services-license, dated 5 Dec 2023]. So there were **at least 7 licensees by end-2023**. The current count is [Unknown]; the ISA site is a JS app.
- **Foreign entry:** a May 2026 bill note says its approach "resembles" the existing financial-information-services regime, under which "certain regulatory reliefs may be granted to foreign providers" [Verified: herzoglaw.co.il/en/?p=77252, 18 May 2026]. The licence is therefore not a foreigner-proof moat either.
- **Capital and insurance:** the requirements exist (Barnea 2024, per F) but the amounts are [Unknown].
- **Reading:**
  - The "plausibly scarce" claim is weakened: at least 7 holders within about 2 years of the law, plus a foreign-relief route.
  - The alternative (using a licensee's API) carries no moat.

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 2,1,1,4,4 | 46 |
| Scal | 2,5,2,4,2,4 | 64 |
| Dist | 4,2,1,2,2 | 42 |

- Balanced 52.4; penalty 13 → **39.4**.

---

## P9. Adequacy-positioned back office for EU/UK accountants (F9-2)

- Not re-opened. Agent F verified the EC IP/24/161 adequacy reconfirmation.
- The decisive assumption (buyers pay for avoiding SCC/TIA paperwork) has no evidence. Israeli wages erode the margin.

| Group | Scores | Total |
|---|---|---|
| CF | 3,2,3,2,1 | 46 |
| Scal | 3,4,2,1,1,2 | 44 |
| Dist | 3,2,1,1,2 | 35 |

- Balanced 43.0; penalty 13 → **30.0**.

---

## P10. Local-marketplace liquidity roll-up (O1)

- Not re-opened.
- Agent A's own evidence: sub-scale targets have 0–30 ratings, and the price of worthwhile targets is unknown. Capital is far beyond the budget. The moat takes 5–7 years, so F's cap does not apply.

| Group | Scores | Total |
|---|---|---|
| CF | 3,0,0,3,1 | 30 |
| Scal | 3,3,2,3,4,2 | 57 |
| Dist | 2,2,1,1,3 | 34 |

- Balanced 41.6; penalty 13 → **28.6**.

---

## P11. Software-assisted payroll-audit firm (C2)

### Evidence
- **Price signal:** none found.
  - Two Hebrew searches (P9-AUDIT #5–6) surfaced no priced wage-inspection tender.
  - I opened three candidate PDFs with pypdf:
    - Arad 16/2023 is an RMI accounting review;
    - Nes Ziona 1/21 is payroll accounting services (חשבות שכר), not a wage inspection;
    - Be'er Yaakov's tender-committee minutes are unrelated.
  - **The decisive assumption (price per audited worker exceeds auditor cost) remains [Unknown].**
- **Supply:** 2,029 certified wage inspectors with falling inflow [P9-C, data.gov.il; not recomputed], against about 2,065 service-contractor licences. That points to price pressure [Hypothesis].
- **Labour:** the founder cannot sign audits himself. This is a pure service business.

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 3,2,3,1,1 | 42 |
| Scal | 2,4,2,2,1,2 | 45 |
| Dist | 4,3,1,2,2 | 46 |

- Balanced 44.0; penalty 13 → **31.0**.

---

## Shortlist ranking after audit

| Rank | ID | Adjusted |
|---|---|---|
| 1 | P5 Co-op-first SaaS | 46.2 |
| 2 | P1 Boater-safety course | 45.4 |
| 3 | P8 Open-finance bank feeds | 39.4 |
| 4 | P2 IRH | 35.2 |
| 5= | P3 Niche device | 31.0 |
| 5= | P11 Payroll audit | 31.0 |
| 7= | P6 DIR reseller | 30.0 |
| 7= | P9 Adequacy back office | 30.0 |
| 9 | P4 Pesticide registration | 28.8 |
| 10 | P10 Marketplace roll-up | 28.6 |
| 11 | P7 Nimbus | 28.4 |

- **No Phase 9 idea comes near the top cluster (49.6–55.4).**
- My audit independently confirms Agent F's falsification:
  - where the founder can obtain the moat in months, so can followers (California boater list, AMAR inflow, at least 7 open-finance licensees);
  - where the moat holds (P4 committee, P5 term award, P10 liquidity), it is out of reach on time or capital.

---

## Leader second opinions

**H6 college-baseball API, 52.2: agree, hold.**
- The SIDEARM noncommercial terms are the same risk type Phase 6 priced at penalty 13.
- CFBD and Highlightly operating openly is weak comfort, not proof of safety.
- I would raise the penalty to 14 only on evidence of enforcement.

**K8 Framer kit, 52.0: I prefer 51.4 (First customers −1) over 50.4 (Speed −1). Hold is not defensible.**
- **Why cut at all:** every bound points the same way:
  - at most about 9–13% of listed creators were paid in a month;
  - the median 2026 creator has 43 followers;
  - 1 of about 290 sampled items is featured;
  - supply is growing 2–3×.
  - K8's CF of 84 is the top cluster's highest and assumed fast first sales.
- **Why First customers rather than Speed:**
  1. The $784k to 649 accounts is labelled an **affiliate/creator** payout (Secondary, via createwith citing LinkedIn), so it does not cleanly measure template sales within 60 days.
  2. Follower counts and featuring rates describe **how hard it is to get the first buyers**, not how soon a listing can go live.
- The difference between 50.4 and 51.4 is inside the noise band. Do not stack both cuts.
- **Dissent recorded:** if the reconciler takes the decisive assumption's "within 60 days" literally, Speed −1 (50.4) is equally defensible.

**H1 Meshtastic kits, 51.2: agree, hold, with a calibration flag.**
- Archived Tindie (about 90% of 2024–26 listings with 0 reviews) is a weak negative on a channel H1 never planned to use.
- Flag: H1's penalty of 7 is the lowest of any leader and sits below the historical 9–14 band, while its Distribution score of 71 rests on no measured newcomer conversion at $300+.
- The rule (raise the penalty only on direct contradiction) prevents a cut now. The next phase that can read Amazon should apply the leader auditor's trigger: Proven −1, giving 50.0.

**M1 Sage 50 API, 49.6: agree, hold.**
- The archived "Medium Segment" agreement (§3.1.1, §3.3.2, termination for convenience on 90 days' notice) leans adverse. But it is not Sage 50 text, and it is silent on vendor-facing hosted APIs.
- The 48.6 downside (penalty 13) is not yet triggered. I would apply it if any Sage 50 US/CA agreement text shows the same §3.3.2 wording without a SaaS addendum.
- The low entry cost ($350, then $250 a year) is a genuine positive and is not scored.

---

## Decisive assumptions (and status after audit)

| ID | Decisive assumption | Status |
|---|---|---|
| P1 | A newly approved provider in one state acquires paid completions at CAC ≤ ~$12, against 19 California providers, a free state course in English and Spanish, and BoatUS at $1, after the deadline spike ends | Unverified. The Spanish wedge is refuted in CA and NY and survives only in TX. Holder growth is refuted in CA. |
| P2 | One or more platforms or EU ARs will white-label a new Israeli IRH at $1.5–3k per client per year | Weakened: Pure Global already uses a local Israeli partner |
| P3 | 60+ DTC units a month for one niche device at CAC < ₪200 | Unverified. Zap shows a thin LED-mask category (17 results). |
| P4 | Registration in ≤9 months at <$2k dossier and lab cost | Unverified. No deadline exists, committee consent is required, and foreign efficacy data appear admissible. |
| P5 | A product with 1–3 pilots can score into an award band in a category re-soliciting within ~12 months | Unverified. The cohort is an upper bound (active contracts only). |
| P6 | Reseller margin ≥5% and a mid-term brand add is allowed | Unknown |
| P8 | Licence under ~$10k and under ~10 non-bank holders | Weakened: ≥7 holders by Dec 2023, plus a foreign-relief route |
| P11 | Tender price per audited worker exceeds certified-auditor cost | Unknown; no price found in 2 searches and 3 PDFs |
