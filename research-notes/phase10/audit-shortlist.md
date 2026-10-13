# Phase 10 Evidence Audit of shortlist Q1–Q12 (P10-AUDIT), 2026-10-13

**Auditor:** independent Evidence Auditor (P10-AUDIT). I worked independently of the red team and did not read its output.

**WebSearch:** 7 of 8 used, each logged as `P10-AUDIT` in `research-notes/search-log.txt`:
1. Mountain View / Wordly $43,750 for 300 hours (Q1)
2. Teams Premium and Zoom translated-captions pricing (Q1 substitutes)
3. German-language AI DM setters for coaches (Q2)
4. State laws on fee-charging job-search services (Q4)
5. Psychiatric NP collaborating-physician fees, Texas and Florida (Q3)
6. Reverse-recruiting refunds and complaints (Q4)
7. Small public bodies buying AI or live translation, with board-approved costs (Q1)

**Primary sources re-opened.** I used WebFetch, or curl/Python with a generic `research-bot` User-Agent. No personal identifiers were sent.

| Source | What was checked |
|---|---|
| trustmrr.com/startup/{ai-dm-setter, glossa-live, leadx, setsmart}.md (live, 2026-10-13) | MRR, subscriptions, monthly series, channels, price, country |
| mv-voice.com 2026-09-09 article; city of Mountain View govdelivery bulletin (2026-08-26) | Contract, hours, total cost, procurement route |
| wordly.ai/pricing; glossa.live | Self-serve versus quote; hour packages |
| eCFR API: 2 CFR 200.1 and 200.320; 48 CFR 2.101 (versions as of 2026-10-01) | Micro-purchase and simplified-acquisition thresholds |
| Meta Terms for WhatsApp Business Platform (last modified 2026-09-23); Messenger Platform policy overview | §4.7 AI Providers; 24-hour window; bot disclosure |
| setsmart.io | Price, languages, customer claim |
| AANP 2026 State Practice Environment PDF (05/2026) | State categories |
| Florida Statutes §464.0123; Texas Occupations Code §157.0512 (texas.public.law) | APRN autonomy scope; prescriptive-authority agreement rules |
| collaboratingdocs.com/pricing; zivianhealth.com/collaboration; singleaimhealth.com/collaborating-physician-pay/texas | Prices, specialties, physician pay |
| nysenate.gov GBS §171 | Employment-agency definition |
| fortune.com 2026-03-25 (Reverse Recruiting Agency) | Prices, clients, refund |
| irs.gov PTIN page; Streamlined procedures pages (overview and foreign-resident) | PTIN fee; eligibility; years required; penalties |
| greenbacktaxservices.com/pricing | Per-form prices |
| api.empireflippers.com listings 88863, 95128, 81079, 67576 | P&L, TACoS, COGS, monthly profit, days listed |
| ipata.org/active-members | Fees, references, USDA, IATA |
| SEC ia09012026.csv (P10-C's file, re-analysed, not re-pulled) | 2024–26 SEC effective dates; ≤10 employees |
| Companies House streaming API reference; Companies House personal-information charter; ltds.uk | Charges stream; reuse; reseller pitch |
| api.apify.com/v2/store?search=companies house | Count of existing Companies House actors |
| market.partnerstack.com/page/recostseg | Commission and PPC terms |

**Blocked or unreadable (none bypassed):**
- **statutes.capitol.texas.gov:** JavaScript app. I used texas.public.law for Occupations Code §157.0512. The Local Government Code §252.021 municipal bid threshold could not be read from either site.
- **leginfo.legislature.ca.gov and law.justia.com:** 403 on California Civil Code §1812.501. California's rules on job-search services remain [Unknown].
- **civiciq.com:** 403 on the Mainland Regional/Boostlingo record, so it stays Secondary.
- **R.E. Cost Seg programme terms (Google Drive):** download refused ("can't download file"). PPC rules are [Unknown].
- **Microsoft Teams Premium page:** timed out. **Zoom translated-captions pages:** 404, so Zoom pricing is Secondary.
- **spf.io/pricing:** 404.
- **wingassistant.com/pricing:** JavaScript shell.
- **Companies House developer home page:** states no reuse terms.

**Scratch:** `scratchpad/p6plus/P10-audit/data` (downloads), with inline Python run with `-I`. The AANP PDF is owner-encrypted, so I read it with the Read tool rather than pypdf.

**Scoring convention:** the same frozen rubric as Phase 9. Criterion scores are 0–5 in rubric order:

| Group | Criteria | Step values |
|---|---|---|
| CF | Spending · Speed · Capital · Margin · Labour | ×5 · ×4 · ×4 · ×4 · ×3 |
| Scal | Depth · Recurring · Acquisition · Leverage · Defensibility · Fit | ×3 · ×4 · ×4 · ×4 · ×3 · ×2 |
| Dist | Clarity · Discoverability · Proven · First · Beyond | ×4 · ×4 · ×6 · ×3 · ×3 |

Balanced = 0.4 CF + 0.4 Scal + 0.2 Dist. Adjusted = Balanced − penalty.

**Calibration applied throughout:**
- **Corrected premise.** I credit high price per account at about a 3× lift, not 5×, and assume about 90% of $300+ launches still miss $3k MRR.
- **Paid ads.** These count as Proven-channel evidence only for low-ticket consumer apps. For B2B or high-ticket offers, a declared Meta or Google Ads channel on one survivor scores at most Proven 2.
- **Defensibility.** Capped at 2 for any moat obtainable in under about 9 months (Phase 9). Where an incumbent or a free substitute already sits in the wedge, I score 0–1.
- **Copying test.** "Three followers bid on the same keywords" is assessed per idea. Where the price is MAP-bound or the offer is undifferentiated, I treat contribution as converging toward break-even, as the EF paid-led cohort shows (5–10% margins).

---

## Summary table

| ID | Verdict | Penalty | Adjusted | One-line reason |
|---|---|---|---|---|
| Q1 Small-public-body AI translation | **Partly supported; two claims refuted** | 12 | **49.2** | Mountain View's $43,750 for 300 hours reproduces, and the city confirms it is a pilot. **But:** (a) Wordly is **not quote-only**: it sells online, "starts at about $1,500 for a 10-hour package". (b) Glossa's real ARPU is **≈$146** ($14,505 MRR across 99 subscriptions), so the newcomer template sells mostly *below* $300. (c) Teams Premium (~$10/user) and Zoom offer translated captions as cheap substitutes [Secondary]. Small-body spending exists at low ticket: a NJ high school board approved Boostlingo at $295/month [Secondary]. It still went through board approval. |
| Q2 German AI DM setter | **Template verified; wedge weak; policy constraints found** | 12 | **47.4** | ai-dm-setter reproduces: $20,746 MRR, 29 subscriptions, $5.2k (Nov 2025) → $23.3k (Sep 2026), with an April dip. It declares 10 channels, Meta Ads among them. The English field anchors far below €400 (SetSmart $99; others $97–297). LLMs make "German" a configuration setting, not a moat. **Meta policy:** automated sends are limited to the 24-hour window; the human-agent tag is manual-only; **bot disclosure is required "when required by applicable law", with Germany singled out**. That undercuts "in the coach's own voice". WhatsApp §4.7 allows a business-specific bot through a Solution Provider. |
| Q3 Collaborating physician (specialty) | **Demand verified; specialty wedge partly refuted** | 12 | **44.6** | AANP 05/2026 map reproduces: 11 restricted and 12 reduced states, plus PR/VI/AS reduced. **Zivian already lists aesthetics/med spas** with no matching fee and a 7-day match. Texas caps a physician at **7 APRN/PA FTEs**, so the bench grows linearly. **Florida autonomy covers primary care only**, so psychiatric and aesthetic NPs still need a physician, which supports the psych wedge. Psychiatric collaboration median $590/month [Secondary]; telepsych firms such as Legion build their own benches. |
| Q4 Reverse recruiting | **Weak; legal exposure larger than stated** | 13 | **39.2** | NY §171(2)(c)(3) covers anyone who, for a fee, "provides information or service of any kind purporting to promote, lead to or result in employment", which squarely covers reverse recruiting. A Texas AG opinion (1991, dated) read the old act as barring an applicant fee before offer acceptance. California is unreadable (403). RRA (Fortune) **refunds the first month's fee**. Refund-rate data: none; complaints anecdotal. Heavy VA labour per client means staffing drift. |
| Q5 Complex expat tax | **Spending verified; no price wedge** | 12 | **40.4** | Greenback per-form prices reproduce: Streamlined $1,750; 8621 $185/275; 5471 $280/665; 8865 $445; 3520 $440; 8854 $420. A complex case at Greenback (e.g. Streamlined plus 6× 8621) is **≈$2.9–3.4k**, which *is* the proposed $1.9–3.5k band. Legal: PTIN $18.75 lets the founder's firm prepare returns; representation needs an EA/CPA/attorney. Streamlined Foreign: 3 years of returns, 6 years of FBARs, a 330-day non-residency test, no penalties [Verified IRS]. |
| Q6 Pet relocation | **Weak** | 13 | **27.4** | IPATA verified: $1,000 application + $1,275/year, 2 member references, USDA licence (US), IATA LAR. One-off tickets, prepaid airfare float, highest liability. Unchanged from discovery. |
| Q7 B2B equipment dealer | **Figures verified; economics confirmed thin** | 12 | **34.8** | #81079: $1,174/month profit, 13% margin, TACoS 12.4%, COGS 70%, **81.7% organic**, sold for $32.9k. Its monthly profit ranges −$768 to $3,963. Paid-led #67576: 71% paid search, **5% margin**, and the seller lists "new competitors … same product from the same supplier" as a risk. The copying claim is confirmed. |
| Q8 Own-label factory-direct | **Verified but n = 1, and the template is weakening** | 13 | **31.8** | #88863 reproduces ($58,192/month average, TACoS 30%, COGS 12%, 6 hours/week plus 3 VAs). But it has been **on the market 320 days unsold** at $1.98M, and its last 3 reported months average **≈$42k** (Apr–Jun 2026: $37.8k, $54.6k, $33.6k). #95128: TACoS 46%, 20 hours/week, listed 32 days, profit $8.96k in September. Tariffs [Unknown]. |
| Q9 Insurance-agency seats | **Not materially re-opened** (Wing page JS) | 13 | **36.6** | A staffing model with no moat, and AI substitutes the task set. |
| Q10 Small-RIA compliance desk | **Trigger data reproduces; fit poor** | 13 | **34.6** | SEC file: 1,178 (2024), 1,321 (2025) and 1,372 (Jan–Sep 2026) effective dates, of which **1,205** have ≤10 employees (re-analysed P10-C file). These are survivors only. Regulated consulting is an agency-drift model. |
| Q11 UK charge signals | **Weak; moat refuted** | 13 | **43.8** | Companies House runs an official **charges stream**. Companies House acknowledges commercial reuse, with the reuser becoming a UK GDPR controller. The Apify Store returns **564** actors for "companies house" (top: 55 thirty-day users), including one covering officers, PSC and **charges**. ltds.uk's homepage does **not** pitch finance brokers (agent's snippet claim not confirmed). LeadX reproduces: $23,983 MRR, 15 subscriptions, monthly series volatile ($36.3k Aug → $27.1k Sep). UK spending: [Unknown]. |
| Q12 Cost-seg / R&D referral desk | **Unverifiable; weakest** | 14 | **25.4** | R.E. Cost Seg 15% of revenue reproduces. Duration, payout timing and PPC rules are blank on PartnerStack, and the terms file could not be downloaded. The decisive $0 check therefore **remains open**, and the firm itself bids on the same keywords. |

---

## Q1. Self-serve AI live translation for small US public bodies (D-G2)

### Evidence
**Mountain View** [Verified: mv-voice.com 2026-09-09; city bulletin 2026-08-26]
- "That includes a $43,750 contract with Wordly that covers 300 hours of live software translation access."
- The total pilot cost is $58,367. The remaining ~$14.6k went on Council Chambers equipment.
- The city calls it a pilot "to assess the benefits of AI translation". It runs at City Council, the Environmental Planning Commission and the Rental Housing Committee.
- The procurement route (council vote, city-manager authority or RFP) is **not stated** in either source. The staff report was not found.
- Accuracy: a resident said "98% good", with awkward English→Chinese phrasing.
- Mountain View has about 80k residents, the upper end of Q1's "under ~100k" target.

**Wordly** [Verified: wordly.ai/pricing, 2026-10-13]
- Annual packages: Starter 10 h, Pro 25 h, Pro+ 50 h, Corporate 100 h, Corporate+ 250 h, Enterprise 500+ h.
- "Pricing starts at about $1,500 for a 10-hour package."
- **Buy Online through the Wordly Store**, plus a quote path. Education and non-profit discounts of 10%.
- **The shortlist's "Wordly is quote-only" is refuted.** Wordly is self-serve at the top of the funnel, though priced at about $150/hour.

**Glossa** [Verified: trustmrr.com/startup/glossa-live.md; glossa.live, 2026-10-13]

| Metric | Value |
|---|---|
| Country | **CY** |
| Founded | 2025-06 |
| X followers | 105 |
| Current MRR | $14,505 |
| Active subscriptions | **99** (ARPU ≈ **$146**) |
| Last 30 days revenue | $33,143 |
| Monthly revenue | $7.0k (Nov 2025) → $31.8k (Sep 2026) |

- Prices: PAYG $5/hour; Standard $99 for 25 h; Advanced $299 for 100 h; Premium $499 for 250 h.
- "Used by hundreds of churches". No government use is mentioned.
- **The template is real, and it is a <$300 ARPU business.** It does not show that $300–600 sells.

**Substitutes** [Secondary: search 2]
- Teams Premium includes live translated captions at about $10/user/month (also in M365 E5).
- Zoom's translated captions launched as a $5/user/month add-on; its 2026 packaging is unclear.
- Both serve remote viewers, not in-room attendees on their phones. But many small bodies run hybrid meetings on Zoom or Teams already.

**Small-body spending** [Secondary: search 7; CivicIQ 403]
- Mainland Regional HS board (NJ) approved Boostlingo translation services at **$295/month ($3,540/year)** on 2026-06-15. Whether it is live or AI is unclear.
- That price lies inside Q1's band. **It still required a board approval** (likely on the consent agenda).

**Thresholds** [Verified: eCFR 48 CFR 2.101 and 2 CFR 200.1/200.320, as of 2026-10-01]
- The FAR micro-purchase threshold is **$15,000** and the simplified acquisition threshold is $350,000.
- For local bodies spending *federal awards*, 2 CFR 200 lets them use informal (micro-purchase) methods up to the FAR level unless they set a lower one.
- Local-fund thresholds are set by state law and local policy. Texas LGC §252.021 was unreadable.
- **Reading [Hypothesis]:** $3.6–7.2k/year is under typical informal-purchase limits. The NJ example shows boards still put even small recurring contracts on an agenda, so "by card within 60 days" is plausible only where staff hold delegated authority.

### Verdict and scores
- **Supported:** public-body spending on AI translation, and low-ticket small-body purchases.
- **Refuted:** "Wordly and spf.io are quote-only" (Wordly has an online store), and "Glossa proves $300+" (ARPU $146).
- **Unverified:** the 60-day card/PO decisive assumption.
- **Copying:** with 3 followers, intent keywords such as "city council meeting translation" are low-volume. Wordly and Glossa can go down-market at once, and Microsoft/Zoom bundle captions. Contribution margin survives because compute is cheap; win rate does not.

| Group | Scores | Total |
|---|---|---|
| CF | 4,2,4,4,4 | 72 |
| Scal | 3,4,2,4,1,3 | 58 |
| Dist | 4,3,1,2,2 | 46 |

- Defensibility is 1: incumbents and bundled substitutes sit in the wedge.
- Fit is 3: US evening meetings fall at 02:00–06:00 Israel time, which is a support burden.
- Proven channel is 1: there are no government newcomer outcomes, and Phase 9's Texas DIR first-time median was $19.7k with 43% at $0.
- Balanced 61.2; penalty 12 → **49.2**.

---

## Q2. German-first AI DM setter for DACH coaches (D-G1/E1)

### Evidence
**ai-dm-setter** [Verified: trustmrr.com/startup/ai-dm-setter.md, synced 2026-10-13]

| Metric | Value |
|---|---|
| Country | FR |
| Founded | 2025-05-19 |
| X followers | 0 |
| Team | 2–5 |
| Bootstrapped | Yes |
| Current MRR | $20,746 |
| Active subscriptions | 29 (ARPU ≈ $715) |
| Last 30 days revenue | $26,877 |
| Profit margin (30 days) | 90% |
| Traffic (30 days) | 835 visitors |

- Monthly revenue:

  | Month | Revenue |
  |---|---|
  | 2025-11 | $5,175 |
  | 2025-12 | $7,100 |
  | 2026-01 | $11,897 |
  | 2026-02 | $12,185 |
  | 2026-03 | $15,306 |
  | **2026-04** | **$12,026** |
  | 2026-05 | $14,502 |
  | 2026-06 | $15,760 |
  | 2026-07 | $16,757 |
  | 2026-08 | $19,774 |
  | 2026-09 | $23,270 |

  The shortlist's "rising monthly" is **almost** right: there was one dip in April.
- Channels: SEO, Blog, Content, Instagram, LinkedIn, **Meta Ads**, Cold DM, Influencers, Partnerships, Word of mouth. That is 10 declared channels, so Meta Ads cannot be attributed.
- "Plans shared on a 30-min demo". "Certified Meta Business Partner".
- This is n = 1, a team (not solo), demo-led selling.

**Competitors**
- SetSmart TrustMRR: $0 MRR, 0 subscriptions (likely billed outside Stripe) [Verified].
- setsmart.io: Pro **$99/month** for 1,000 messages; "English, French, Spanish … and more"; "over 500 entrepreneurs" [Verified page; vendor claim].
- Search 3: Appointwise from $297, Instaset $149, InstantDM $29 [Secondary]. No German-first product surfaced. The US engine is weak for German, so absence is unproven.

**Meta policy** [Verified: Messenger Platform policy overview; Meta Terms for WhatsApp Business Platform, last modified 2026-09-23]
- "Businesses have up to 24 hours to respond to a user." The Human Agent tag "allows businesses to **manually** respond … within a 7-day period". So automated follow-ups beyond 24 hours are not allowed.
- "When required by applicable law, automated chat experiences must disclose that a person is interacting with an automated service". The policy names **California and German** users as warranting attention. The policy applies to the Instagram Messaging API, though the 24-hour examples are Messenger-only.
- WhatsApp §4.7 bars AI Providers whose AI is the "primary (rather than incidental or ancillary) functionality". It also states "you may retain an AI Provider as your Solution Provider".
- **Reading:** a coach-specific setter is likely permissible. But Meta decides what counts as "primary", and Platform data may not train models.

### Verdict and scores
- **Supported:** the template's revenue and trend.
- **Weakened:** the price anchor (the English field sits at $97–297), and the German moat (language is a model setting; SetSmart says "and more").
- **New risk:** the German disclosure expectation and the 24-hour/manual-follow-up rules. These cap the "always follows up, in your voice" pitch.
- **Copying:** an English or French incumbent adds German in days. With 3 followers on DACH coach audiences, partner revenue shares rise. ARPU is the variable that fails, not CAC.

| Group | Scores | Total |
|---|---|---|
| CF | 4,3,4,4,3 | 73 |
| Scal | 3,3,2,3,1,2 | 48 |
| Dist | 4,3,2,2,3 | 55 |

- Recurring is 3: coaching churn is ~5–7%/month [Secondary, P6].
- Fit is 2: German demos need a hired seller, and the business depends on Meta.
- Balanced 59.4; penalty 12 → **47.4**.

---

## Q3. Collaborating-physician matching plus compliance admin (C1)

### Evidence
**AANP 2026 map** [Verified: storage.aanp.org State-Practice-Environment.pdf, dated 05/2026]

| Category | Jurisdictions |
|---|---|
| Restricted | CA, TX, OK, MO, MI, TN, NC, SC, GA, FL, VA (11) |
| Reduced | WI, IL, IN, OH, KY, WV, PA, NJ, AR, LA, MS, AL (12), plus PR, VI, AS |

The "23 jurisdictions" figure reproduces for states.

**Texas** [Verified: Occ. Code §157.0512 via texas.public.law]
- Agreements must include chart review and **monthly** meetings (format chosen by the parties).
- **A physician may hold agreements with at most 7 APRN/PA FTEs**, with exemptions for underserved and facility-based practice.
- No Texas Medical Board registration is required by this section. The agreement must be produced to the board within 3 business days on request.

**Florida** [Verified: §464.0123]
- Autonomous practice requires 3,000 supervised hours and is limited to "**primary care practice, including family medicine, general pediatrics, and general internal medicine**". Surgery other than subcutaneous procedures is barred.
- So **psychiatric and aesthetic NPs in Florida remain supervision-bound**, which supports the specialty wedge.

**Competitors** [Verified pages, 2026-10-13]
- Collaborating Docs: no prices published; physician malpractice included; custom quote.
- **Zivian: "No onboarding or matching fees", 7-day match, and aesthetics/med spas explicitly supported.** Psychiatry is not listed, but a PMHNP testimonial appears.
- The aesthetic half of the wedge is therefore already served.

**Pricing** [Verified: singleaimhealth.com Texas page, updated 2026-06-02]
- The Texas **average is $694/month** (not the $859 in a search snippet).
- Eight Texas psychiatry examples range $450–1,200.
- Search 5 [Secondary]: psychiatric collaboration median $590. Legion Health recruits its own collaborating psychiatrists at $1,000 per full-time PMHNP.

### Verdict and scores
- **Supported:** statutory demand, incumbent ad spend (P10-C), and physician pay levels.
- **Refuted in part:** the aesthetic wedge (Zivian serves it).
- **Constraint:** the Texas 7-FTE cap makes the physician bench linear with growth.
- **Capital:** state agreement templates, malpractice placement and a US LLC likely exceed $2k [Hypothesis]. This needs healthcare counsel (fair market value, anti-kickback).
- **Copying:** keyword CPC rises, but the binding constraint is physician supply. A follower faces the same cold start, so the bench is the only asset (Defensibility 2).

| Group | Scores | Total |
|---|---|---|
| CF | 4,2,2,2,3 | 53 |
| Scal | 3,5,2,3,2,1 | 57 |
| Dist | 5,4,2,2,3 | 63 |

- Balanced 56.6; penalty 12 → **44.6**.

---

## Q4. Reverse recruiting (A1)

### Evidence
**New York** [Verified: nysenate.gov GBS §171]
- §171(2)(c) includes any person who, for a fee, renders vocational guidance or counselling and "(3) **provides information or service of any kind purporting to promote, lead to or result in employment**".
- The §171(2)(e) exclusions do not cover career consultants.
- The NY exclusion in the idea is necessary, and the breadth of this definition suggests other states' acts may reach the model too.

**Other states**
- Search 4 [Secondary, dated]: Texas AG opinion DM-0036 (1991) read the then-act as barring an applicant fee before an offer is accepted. Historical licence-and-bond regimes existed in Ohio (1969) and Minnesota (1983). Current status: [Unknown].
- California Civil Code §1812.501: **blocked (403)**.
- Florida: not checked.

**Reverse Recruiting Agency** [Verified: fortune.com 2026-03-25]
- $1,500/month plus 10% of first-year salary.
- 45 clients helped plus 25 active; ~863 applications per client; 12.7 weeks to an offer (company analysis).
- **"The first month's fee is refunded"**, so the effective upfront revenue per client is lower than the agent assumed.

**Refunds**
- Search 6: anecdotes only (a BBB complaint about a $3k job-or-refund programme; Trustpilot refund refusals at Hirey). No refund-rate data.
- **Copying:** there are zero barriers; Jobhire runs 53 ads (P10-A). The agent's own +3-follower case cuts contribution to ≈$390 per client before refunds. Delivery of 10–15 VA hours per client per week is staffing.

| Group | Scores | Total |
|---|---|---|
| CF | 3,4,4,2,2 | 61 |
| Scal | 3,2,2,2,1,2 | 40 |
| Dist | 4,4,2,3,2 | 59 |

- Balanced 52.2; penalty 13 → **39.2**.
- The penalty is above the default because the legal exposure is directly evidenced in NY, and plausibly in Texas from the dated opinion.

---

## Q5. Complex-case expat tax catch-up and exit desk (A2)

### Evidence
**Greenback** [Verified: pricing page, 2026-10-13]

| Item | Price |
|---|---|
| Base return | $565 |
| Streamlined package | $1,750 (listed $2,445) |
| FBAR | $125 per 5 accounts |
| 8621 | $185 / $275 |
| 5471 | $280 / $665 |
| 8865 | $445 |
| 3520 | $440 |
| 8854 | $420 |
| Consultations | $250 per 30 minutes |

- A complex Streamlined case (3 years × 2 PFICs) costs ≈ $1,750 + 6 × $185 = **$2,860**, rising to ~$3.4k with distributions.
- **Q5's $1,900–3,500 complex price is the same as the incumbent's à-la-carte price.** There is no price wedge.

**IRS** [Verified: irs.gov Streamlined pages]
- Non-wilful certification.
- Foreign track: no US abode and 330 days outside the US in one of the last 3 years.
- **3 years of returns and 6 years of FBARs.**
- Compliant filers are not subject to failure-to-file, failure-to-pay, accuracy, information-return or FBAR penalties.
- No end date is stated.

**PTIN and representation** [Verified: irs.gov PTIN page]
- Anyone preparing returns for pay needs a PTIN ($18.75; EAs too).
- Representation rights come through credentials or the AFSP, not the PTIN.
- Whether a non-US person without an SSN can obtain a PTIN: the page is silent [Unknown this session].

**Copying:** keyword CPCs are shared with Taxes for Expats (100–200 ads) and Greenback. Contribution of $650 falls to $125 in the agent's own model. Seasonality is strong.

| Group | Scores | Total |
|---|---|---|
| CF | 5,3,3,2,2 | 63 |
| Scal | 3,2,2,2,1,2 | 40 |
| Dist | 4,4,2,2,2 | 56 |

- Balanced 52.4; penalty 12 → **40.4**.

---

## Q6. International pet relocation (A3)
- IPATA [Verified 2026-10-13]: $1,000 non-refundable application, $1,275 annual dues (2026), two member references, US members must be USDA-licensed (intermediate handler, Class B dealer or transporter), and one IATA LAR-certified staff member. The agent's figures reproduce.
- Not otherwise re-opened.
- The business is one-off and float-heavy. It has the highest liability, coordinator labour per move, and no moat. Copying raises CAC on a ~$1.5k gross margin per move.

| Group | Scores | Total |
|---|---|---|
| CF | 3,3,2,2,1 | 46 |
| Scal | 2,0,2,2,1,1 | 27 |
| Dist | 4,4,2,2,2 | 56 |

- Balanced 40.4; penalty 13 → **27.4**.

---

## Q7. B2B equipment dealer quote desk (B10-1)

### Evidence [Verified: api.empireflippers.com, 2026-10-13]

**#81079**
- Status Sold at $32,872.
- First revenue **2024-01** per the API (the agent said 2023; metrics start Dec 2023).
- $1,174/month profit, 13% margin, TACoS 12.42%, COGS 69.9%.
- "Organic search accounts for 81.67% of traffic"; 1 hour/week.
- Monthly profit from Dec 2023 to Nov 2024 ranged −$768 to $3,963.

**#67576**
- Status Sold. 5% margin; "paid search (71%)"; 4 employees; 10 hours/week.
- Risk listed by the seller: "**New competitors entering the space selling the same product from the same supplier** could impact earnings".

**Reading:** the agent's core claim reproduces. The profitable case is organic-led and tiny; the paid-led case is 5%. Under 3 followers at MAP, paid orders converge to break-even.

| Group | Scores | Total |
|---|---|---|
| CF | 4,2,2,1,3 | 49 |
| Scal | 3,1,2,3,1,3 | 42 |
| Dist | 4,3,2,2,2 | 52 |

- Balanced 46.8; penalty 12 → **34.8**.

---

## Q8. Own-label factory-direct customisable catalogue (B10-2)

### Evidence [Verified: EF API]

**#88863**
- For Sale at $1,978,520.
- **First listed 2025-11-26; 320 days on the marketplace.**
- TACoS 30%, COGS 12%, margin 18%; 6 hours/week plus 3 Philippine VAs (50 hours/week).
- Monthly profit, Jul 2025–Jun 2026: 52.6k, 57.8k, 112.7k, 67.5k, 88.6k, **16.3k**, 51.7k, 57.0k, 67.9k, 37.8k, 54.6k, **33.6k**. No data after June 2026.
- Seller-listed risk: "An increase in Paid Traffic pricing could make the ads unprofitable."

**#95128**
- For Sale at $305,232, listed 2026-09-11.
- TACoS 46%, COGS 37%, 20 hours/week.
- Profit $0.5k (Oct 2025) → $16.5k peak (Apr 2026) → $8.96k (Sep 2026).

**Reading:** the Track B template is n = 1. It is unsold after ~10.5 months and its recent months are below its average. Tariffs are still [Unknown]. Followers can buy the same factory SKUs, so price competition is open, unlike under MAP.

| Group | Scores | Total |
|---|---|---|
| CF | 4,2,1,2,3 | 49 |
| Scal | 4,0,2,3,1,2 | 39 |
| Dist | 3,3,2,2,2 | 48 |

- Balanced 44.8; penalty 13 → **31.8**.

---

## Q9. Offshore service-desk seats for insurance agencies (C2)
- Not materially re-opened. Wing's pricing page is a JavaScript shell. P10-C's EF #62527 evidence was already EF-verified.
- Agency and staffing drift is inherent: margin is a labour markup, and the only owner leverage is contractor management. AI receptionists target the same tasks.
- **Copying:** there is no supply-side asset, so CAC rises roughly 1.5–2× [Hypothesis, P10-C], with seat prices under pressure.

| Group | Scores | Total |
|---|---|---|
| CF | 4,3,3,2,1 | 55 |
| Scal | 4,4,2,2,0,1 | 46 |
| Dist | 4,3,1,2,2 | 46 |

- Balanced 49.6; penalty 13 → **36.6**.

---

## Q10. Compliance operations desk for new small RIAs (C3)
- SEC adviser file (P10-C's `ia09012026.csv`, 17,210 rows, re-analysed by me): SEC status effective in 2024: 1,178; 2025: 1,321; **2026 (Jan–Sep): 1,372, of which 1,205 have ≤10 employees (Item 5A)**. The figures reproduce exactly. These are survivors only, and the effective date includes state-to-SEC switches.
- Delivery is regulated consulting by ex-CCO contractors, with E&O insurance [Unknown cost]. The founder has no securities background, so Fit is 0.

| Group | Scores | Total |
|---|---|---|
| CF | 3,2,3,3,1 | 50 |
| Scal | 2,4,2,2,2,0 | 44 |
| Dist | 5,3,1,2,2 | 50 |

- Balanced 47.6; penalty 13 → **34.6**.

---

## Q11. UK Companies House charge signals for finance brokers (D-G3)

### Evidence
**Data access** [Verified: developer-specs streaming API reference; Companies House personal-information charter]
- The official streaming API includes a **`GET /charges` "Charges stream"**, alongside companies, filings, insolvency, officers, PSC and others.
- "Commercial organisations may sometimes use data from these registers to create their own online products"; the reuser then becomes a UK GDPR controller.
- Website content is under OGL v3.0. Register-data licence terms are not stated on the pages read.
- **No licensing barrier was found, and therefore no moat.**

**Existing resellers** [Verified: Apify Store API, 2026-10-13]
- A "companies house" search returns **564** actors. The top one, scrapesage/companies-house-scraper, has 55 thirty-day users.
- One actor is named "UK Companies House Scraper: Officers, PSC, **Charges**" (7 users).
- ltds.uk homepage [Verified]: monitoring for "directors, accountants, and compliance teams". Its watchlist tracks "charges", with free real-time alerts. **It does not pitch asset or invoice-finance brokers**, so P10-D's snippet claim was not confirmed on the homepage.

**LeadX** [Verified TrustMRR]
- $23,983 MRR, 15 subscriptions, 312 followers, US UCC data.
- Monthly revenue: $14.5k (Jun), $10.0k (Jul), $36.3k (Aug), $27.1k (Sep 2026). That is volatile, n = 1, and US-only.

**Copying:** the data costs nothing, so a follower's marginal cost is about zero. Price erosion toward £50 is the agent's own expectation.

| Group | Scores | Total |
|---|---|---|
| CF | 2,3,5,4,4 | 70 |
| Scal | 1,4,2,4,0,4 | 51 |
| Dist | 4,2,1,2,2 | 42 |

- Balanced 56.8; penalty 13 → **43.8**.
- The Cash-Flow total (70) reflects cheapness, not demand: UK spending is [Unknown].

---

## Q12. Partner-paid cost-segregation / R&D referral desk (E3)
- R.E. Cost Seg on PartnerStack [Verified]: "15% of total revenue". The fields "How long do commissions last", "When do I get paid?" and cookie length are **blank**. Referral is by link or lead form. PPC and brand bidding are not mentioned.
- The full terms are a Google Drive file that refused download. **The decisive $0 check could not be completed.**
- Study fees: [Unknown]. ETS 10%: [Secondary].
- **Copying:** we bid against the payer itself and against other affiliates. Commission arrives 60–120 days after the client pays, so cash flow is negative during a $2k test.

| Group | Scores | Total |
|---|---|---|
| CF | 2,2,4,2,4 | 54 |
| Scal | 2,0,1,3,0,3 | 28 |
| Dist | 3,3,0,2,1 | 33 |

- Balanced 39.4; penalty 14 → **25.4**.

---

## Shortlist ranking after audit

| Rank | ID | Adjusted |
|---|---|---|
| 1 | Q1 Small-public-body AI translation | 49.2 |
| 2 | Q2 German AI DM setter | 47.4 |
| 3 | Q3 Collaborating physician | 44.6 |
| 4 | Q11 UK charge signals | 43.8 |
| 5 | Q5 Complex expat tax | 40.4 |
| 6 | Q4 Reverse recruiting | 39.2 |
| 7 | Q9 Insurance seats | 36.6 |
| 8 | Q7 B2B equipment dealer | 34.8 |
| 9 | Q10 RIA compliance | 34.6 |
| 10 | Q8 Own-label factory-direct | 31.8 |
| 11 | Q6 Pet relocation | 27.4 |
| 12 | Q12 Referral desk | 25.4 |

- **No Phase 10 idea enters the top five** (50.8–55.4). Q1 at 49.2 would tie for 10th on the cumulative board, inside the noise band of ranks 6–15.
- **The corrected premise lowers the human-delivered ideas most** (Q4, Q5, Q6, Q9, Q10). Their high ticket is "agency in disguise" (Agent F), and paid-search contribution collapses toward break-even with 3 followers.
- **The two software ideas keep the best scores** because their delivery cost is near zero. Neither has a demonstrated $300+ newcomer at the target segment:
  - Q1's template sells at ARPU $146;
  - Q2's template is a 2–5-person demo-led team with 10 declared channels.

---

## Leader second opinions

The criterion breakdowns for leaders were never published (Phase 6 note), so opinions are given as named step changes.

**H7 Blender add-ons, 55.4: agree, hold.**
- The new 221-item sample (median 2 sales in 0–3 months; 1% reach 100) matches the evidence behind P5/P8 (Proven 2, Scalable acquisition 2).
- Scalable acquisition 2→1 would reuse the same base-rate and supply evidence, so I agree it is double counting.
- H7's channel is marketplace search at ~$14 per unit. It was never credited with the paid-ads lift or the $300+ price lift, so the Phase 10 correction does not touch it.

**H6 College-baseball API, 52.2: agree, hold.**
- Realised CFBD ARPU of $1.6–7.9 sits inside the $5–10 Phase 3 modelled, so Margin and Recurring are not contradicted.
- The ceiling was priced in Phase 6 (Proven −1, Scalable acquisition −1, Defensibility −1, penalty 13).
- Not credited with paid or high-price lifts.

**H1 Meshtastic kits, 51.2: I dissent; penalty 7→9 (49.2).**
- **Why, at criterion level:**
  - Dist 71 is the highest of any leader, and it rests on Amazon, YouTube and Discord conversion of a **$349–449 consumer** kit.
  - That channel has been unreadable for three phases (P6 partial, P9 and P10 blocked).
  - Phase 10 adds adjacent negative evidence: Agent E found **no $300+ B2C winner on Meta or paid channels** in TrustMRR, and the paid lift is a sub-$100 consumer-app effect. This is not a direct contradiction, because H1's plan is Amazon search plus creators, not Meta Ads, so I do **not** cut Proven.
  - The methodology defines the penalty as "weaker **or** more contradicted evidence". Weak, untestable evidence on the decisive channel is a valid ground. Penalty 7 sits below the historical 9–14 band applied to every other leader with an unmeasured channel.
  - This is the final phase, so there is no future test that could clear it.
- **If the reconciler keeps the leader auditor's "contradiction only" convention,** the reconciliation rule gives penalty 8 → **50.2**. Either way, H1 drops below monday/J7 or ties them, inside the noise band.

**monday.com Israeli invoicing app, 50.8: agree, hold.**
- The open gap (no incumbent advertises a monday integration) is weak and stays uncredited as spending evidence.
- The marketplace remains unmeasurable. Penalty 14 already prices this, as the highest leader penalty.
- Low-ticket and not credited with paid or high-price lifts.

**J7 Apify Actors, 50.8: agree, hold.**
- Proven is already 1. The 2026 data (median 1 thirty-day user; 3% reach 100 by 6–9.5 months) reproduce Phase 5.
- The rejected Speed −1 would re-price paid conversion already cut through First customers in P5, so I agree it is double counting.
- My own Apify query in Q11 (564 Companies House actors, top one with 55 users) is consistent with that crowding.

**Final-phase question: is any top-5 leader scored on an assumption its own measured channel has since contradicted?**

| Leader | Contradicted? | Basis |
|---|---|---|
| H7 | No, beyond what is priced | Superhive newcomers: P5 Proven 4→3, Scalable acquisition 3→2; P8 Proven 3→2 |
| J7 | No, beyond what is priced | Apify newcomers: P5 Proven 3→1, First 3→2, Scalable acquisition 3→2 |
| H6 | No | Measured ARPU sits inside the modelled price |
| monday | Not measurable | Channel unreadable; penalty 14 prices it |
| H1 | Not measured, so not contradicted | Its decisive channel has never been measured, so its high Distribution score is the least supported on the board, hence my penalty dissent |

- **None of the top five benefited from the Phase 8 "$300+ = 5.1×" or "paid ads = 3–6×" premises.** All five are low-ticket and marketplace- or organic-led. The Phase 10 correction therefore changes no leader score.

---

## Decisive assumptions (and status after audit)

| ID | Decisive assumption | Status |
|---|---|---|
| Q1 | Small bodies buy at $300–600/month by card or PO without an RFP within ~60 days | **Unverified; weakened.** A board approved even a $295/month contract. The template ARPU is $146. Wordly sells self-serve; Teams/Zoom bundle captions. |
| Q2 | DACH coaches pay €400+/month for a German AI setter, and a German partner channel exists | **Unverified; weakened.** The English field is at $97–297, and language is no moat. Meta's 24-hour window, manual-only human tag and bot-disclosure expectation (Germany named) constrain the product. |
| Q3 | A specialty physician bench at ≤$650/NP while NPs pay ≥$850, with specialty NPs under-served | **Partly refuted** for aesthetics (Zivian). **Supported** for psych in Florida (autonomy limited to primary care). Linear bench (Texas 7-FTE cap). |
| Q4 | Refunds/chargebacks <15% and ≥3 paid months | **Unknown.** The leading comparable refunds month 1. NY law is broad; Texas law is dated; California is blocked. |
| Q5 | Median scoped quote ≥$1,500 at CPL ≤$150 for complex cases | **Price exists but no wedge.** The incumbent's à-la-carte complex price is $2.9–3.4k. |
| Q6 | ≥$1,200 gross margin per move via subcontracted IPATA partners | Unknown |
| Q7 | ≥4 dealer approvals for a foreign-owned new store, and ≥40% non-paid orders within 12 months | Unverified. The comparables confirm paid-led stores make 5%. |
| Q8 | Landed cost after tariffs leaves ≥15% contribution at TACoS 30–45% | Unverified. The template has been unsold 320 days and its recent months are below average. |
| Q9 | Paid CAC <~$900/seat with ≥6-month retention | Unknown |
| Q10 | New small RIAs pay $600–1,200/month to a non-brand provider | Unknown. The trigger list reproduces. |
| Q11 | Brokers pay £250+ for signals derivable from free data | **Weakened.** An official charges stream exists; 564 Companies House actors are on Apify. |
| Q12 | Programme terms allow PPC, and payout ≥3× CAC | **Open.** The terms file was unreadable; PartnerStack fields are blank. |
