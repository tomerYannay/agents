# Phase 10 Red-Team Investor report (P10-REDTEAM), 2026-10-13

**Scope.** Why each of Q1–Q12 would fail *for this founder*. The founder is Israel-based, technical, part-time, has about $2k and wants to own a business, not sell hours. I also challenge the five leaders at criterion level: H7, H6, H1, the monday app and J7. I worked independently of the evidence auditor and did not read its output. I did read the leader auditor's `audit-leaders.md` and re-cut its public Apify sample.

**Searches and sources.**
- WebSearch: **8 of 8 used**, all logged as `P10-REDTEAM`. Topics:
  1. WhatsApp Business API ban on general-purpose AI assistants
  2. California employment-agency law and reverse recruiting
  3. 2025–26 nurse-practitioner full-practice-authority changes
  4. Self-serve AI translation for government meetings, and alternatives to Wordly
  5. 2026 US tariffs on Chinese lighting and furniture
  6. Instagram Messaging API rules for automated DMs
  7. Done Global telehealth prosecution
  8. AI agents replacing back-office work in insurance agencies
- Primary pages fetched with curl or WebFetch, using a generic User-Agent:
  - Cal. Civ. Code §§1812.501, 1812.502 and 1812.507 (california.public.law);
  - CMF Group's NP full-practice-authority roundup (29 Jun 2026);
  - SF Public Press on Bay Area AI translation (Jun 2024);
  - LightNOW / ALA tariff alert (5 Aug 2026);
  - the R.E. Cost Seg PartnerStack page.
- Local data, with no re-crawl:
  - TrustMRR `.md` files in `P8-D/data/md` for ai-dm-setter, glossa-live and leadx;
  - the leader auditor's Apify sample (`P10-auditL/data/apify`), re-cut by my script `scripts/apify_self.py`.
- **Blocked or failed:**
  - The R.E. Cost Seg affiliate agreement is a Google Drive file. The direct download returned "Can't download file", and the viewer needs JavaScript or a sign-in. **I could not read whether it bans PPC. Not bypassed.**
  - I did not open Meta's primary Instagram policy pages. The Instagram findings come from vendor blogs.
  - The Supreme Court IEEPA ruling date (20 Feb 2026) comes from one secondary source.
- Scratch: `scratchpad/p6plus/P10-redteam/{scripts,data}`. Scores are reproducible with `scripts/score.py` (output in `data/scores.txt`). No browser, contact, sign-ups or purchases.

**Conventions.**
- Frozen rubric. Step values are CF 5/4/4/4/3, Scal 3/4/4/4/3/2, Dist 4/4/6/3/3.
- "Steps" are the 0–5 criterion scores in rubric order:
  - CF: spending, speed, capital, margins, independence.
  - Scal: depth, recurring, scalable acquisition, operating leverage, defensibility, founder fit.
  - Dist: clarity, discoverability, proven channel, first customers, growth beyond outreach.
- **Phase 9 calibration applies:** defensibility is capped at 2 for any moat obtainable in under about 9 months. It binds on nothing here, because every Q-idea already scores Def ≤2 on its own evidence.
- **Corrected premise applies:**
  - I use about 10–12% as the prior that a $300+ launch reaches $3k MRR, not 51% (Agent D 1b, Agent F Test B).
  - I do not credit paid ads as a high-ticket channel on the strength of TrustMRR's paid-channel lift. 22 of 26 paid-channel winners are consumer apps under $100.
- **Copying model:** Agent E's 3× CPC at fixed conversion is the stress case (Google "Actual CPC" mechanics: followers raise the incumbent's clearing price).

---

## 0. Headline

1. **Nothing in Phase 10 reaches the leader cluster.**
   - The best ideas are **Q1, small-body AI meeting translation, at 44.8** and **Q11, UK charge signals, at 44.2**. Both are software, and neither is sold mainly through paid ads.
   - Every service idea lands at 21–38: Q3, Q4, Q5, Q6, Q9 and Q10.
   - The physical-goods ideas, Q7 and Q8, land at 27–28.
2. **The Phase 10 recipe fails its own copying test for every one-off ticket.** I applied Agent E's 3× CPC rule to the agents' own unit-economics tables (`data/scores.txt`):

   | Idea | CAC today → at 3× CPC | Profit per sale |
   |---|---|---|
   | Q4 reverse recruiting | $670 → $2,010 | +$980 → **−$360** |
   | Q5 expat tax | $600 → $1,800 | +$650 → **−$550** |
   | Q6 pet relocation | $470 → $1,410 | +$730 → **−$210** |
   | Q7 equipment order | $375 → $1,125 | +$5 → **−$745** |

   Recurring ideas survive only on **retention that nobody has measured**:

   | Idea | Payback at 3× CPC |
   |---|---|
   | Q3 | 5.0 months |
   | Q9 | 3.2 months |
   | Q10 | 4.3 months |
   | Q2 | 4.2 months |

   Every input is the discovery agent's own [Hypothesis]. The direction ("paid acquisition whose unit economics survive copying") holds only where price per account is recurring *and* retention is long. That leads back to Agent F's Lane 1, a B2B vertical tool, not a productised service.
3. **New verified or secondary contradictions of shortlist claims:**
   - **Q3: the specialty wedge is shrinking.**
     - New Jersey's S2996 (signed 30 Mar 2026) removes the joint protocol for APNs with more than 5,000 hours in **primary care and behavioral health**. That is the psych-NP wedge Q3 proposes.
     - Oklahoma's HB2298 (in force Nov 2025) allows independent Schedule III–V prescribing.
     - California's AB 890 "104" NPs reach independence in 2026.
     - About 30 states plus DC now grant some form of full practice authority, up from 22 in 2020 [Verified: cmfgroup.com, 29 Jun 2026].
     - The AANP list of 23 jurisdictions that Q3 relies on is already partly out of date.
   - **Q3: the high-price tier sits in the enforcement zone.** The $1.5–3k controlled-substance collaboration tier is where Done Global's founder and clinical president were convicted (late 2025, N.D. Cal.). The allegations included corporate practice of medicine and paying prescribers per prescription [Secondary: Ropes & Gray, Jan 2026].
   - **Q4: California is not just "pending verification"; it is covered by statute.**
     - Under Civ. Code §1812.501(a), anyone paid "directly or indirectly by a jobseeker" who "attempts to procure employment" is an employment agency.
     - Under §1812.501(b), anyone charging for "career management… or the development of résumés" on a non-hourly basis is an "employment counseling service". The employer-paid exemption in §1812.502(a) excludes counseling services.
     - Under §1812.507, no agency may take a jobseeker fee without a bona fide job order [Verified: california.public.law].
     - So **both** NY and CA, the two largest pools of laid-off tech and H-1B workers, are out of Q4's segment. Other states are [Unknown].
   - **Q1: the price wedge is already held by Glossa.**
     - Glossa sells $299 for 100 hours to anyone. Its realised ARPU is about **$145** ($14,206 MRR ÷ 98 subscriptions) [Verified: local TrustMRR].
     - At Wordly's own rates, a small town already spends about $600–900 a month. Gilroy pays about $300 per 2-hour meeting [Secondary: SF Public Press].
     - So the "10× wedge" is per hour, not per buyer budget. San Francisco declined AI translation over accuracy and cultural competency.
   - **Q2: automated follow-up is restricted.**
     - Instagram's API allows free-form messages only within 24 hours of the user's last message, and only to users who wrote first. The 7-day HUMAN_AGENT tag is barred for bot messages [Secondary: vendor blogs].
     - WhatsApp has barred general-purpose AI assistants since 15 Jan 2026. Business-specific bots for sales and booking remain allowed [Secondary: multiple].
     - The setter's "follows up" feature must therefore be human, or happen inside the 24-hour window.
4. **Survivorship in the comparables is visible in their own timelines:**
   - **LeadX (Q11):** founded Jun 2023. Revenue was $597 in Feb 2026 and $36.3k in Aug 2026, then $27.1k in Sep, with 15 subscriptions. That is about 2.5 years near zero, then lumpy revenue that looks like annual prepayment.
   - **ai-dm-setter (Q2):** declares **10** channels, of which Meta Ads is one, so attribution is unknowable. It is a team of 2–5.
   - **Glossa (Q1):** labelled B2C and Cyprus-based.
   - **EF Q7/Q8 cohorts:** sellers at exit. 8 of 14 had a loss month. #88863 is n=1 and for sale at $1.98M.
5. **Leader calls:**
   - **H7: hold 55.4.** Its #1 position is **not meaningful**. The gap to H6 is 3.2, under the 5-point noise threshold.
   - **H6: hold 52.2** (dissent 51.2).
   - **monday: hold 50.8.**
   - **H1: penalty 7 → 9, giving 49.2.**
   - **J7: speed −1, giving 49.2** (my position; the leader auditor rejected it).
   - **The final report should present a tied top cluster of about 49–56, with no sole winner.**

---

## 1. Cross-cutting attacks

| Attack | Evidence | Who it hurts most |
|---|---|---|
| **Paid-channel economics under copying** | Google charges what is needed to beat the Ad Rank below you, so each follower raises your CPC (Agent E). At 3× CPC, every one-off ticket goes negative (headline 2). B2B Google Ads declarers: 9.1% reach $3k, and 50 of 97 young declarers have $0. EF paid-traffic businesses run at a median 28–42% margin, against 82–95% for others. Paid-led dealer stores run at 5–10%. Channable: EU Shopping ROAS −43% YoY. | Q4, Q5, Q6, Q7, Q8, Q12 |
| **Agency and staffing drift** | Agent F's tests (2+ yeses = agency): **Q4** (linear VA hours; client relationship), **Q5** (EA hours per case; bespoke scope), **Q6** (8–15 h per move), **Q9** (a seat *is* labour), **Q10** (contractor CCO hours; liability) and **Q3** (coordinator plus physician bench; partial). EF agencies sell at about 2.25× profit against 3.31× for SaaS. EF has **0** bookkeeping or compliance comparables (Agent C). | Q4, Q5, Q6, Q9, Q10; Q3 partly |
| **Licensing** | **Q4:** NY GBL §171 and **Cal. Civ. §1812.501–507** (verified); UK EAA 1973. **Q5:** Circular 230 (only an EA, CPA or attorney can represent) and IRC §7216 consents; certifying "non-willful" is a penalty-relief statement the preparer stands behind. **Q3:** state collaboration rules, fair-market-value and anti-kickback rules, corporate practice of medicine (Done Global), and malpractice placement. **Q6:** USDA registration under 9 CFR 2.25 if the business takes custody; IPATA needs 2 member references. **Q10:** SEC Marketing Rule work and E&O; liability if named. **Q2:** Meta platform terms (headline 3). | Q3, Q4, Q5, Q10 |
| **Selling from Israel** | Q1 support peaks during US evening meetings, which is 02:00–06:00 in Israel. Q2 needs German demos the founder cannot give. Q3, Q9 and Q10 need US demo calls and trust in the person. At high ticket, TrustMRR winners use **LinkedIn 5/21, cold email 4/19, calls 2/8, against Google Ads 1/9** (Agent D), so the founder must sell, part-time, with 0–3 hours of overlap. | Q1, Q2, Q3, Q9, Q10, Q11 |
| **Two-sided cold start** | Q3 cannot sell to NPs without physicians, nor recruit physicians without NPs. The test needs both sides at once. Zivian solved it with $3M of seed money. | Q3 (also Q6's partner agents) |
| **Capital** | **Q7:** supplier prepay on $2k orders, Shopify 120-day reserves, a US LLC (about $500) and $1k of ads, so the first two orders float more than the budget. **Q8:** samples $300–800, ads $1k, cross-border returns and tariffs (now a 10–12.5% Section 301 layer on lighting from 24 Jul 2026, stacked on legacy China duties [Secondary: LightNOW]). **Q6:** prepaid cargo airfare of $2–4k per move. **Q3:** state legal review of $2–5k [Unknown]. | Q7, Q8, Q6, Q3 |
| **Survivorship** | EF listings are exits. TrustMRR profiles are self-listed and only about 1 in 10 high-ticket launches clears $3k. The strict "$300+, paid/partner, audience-free" set is **n=6**, and 2 of those are an agency and an opaque stealth listing. Several comparables are flat or for sale: Backlinker −12%, Defined Chase −40%, EF divorce-docs listing unsold since Apr 2025. | Q2, Q7, Q8, Q11; Q9 (EF #62527 is 5.4 years old) |
| **Corrected premise** | The price lift is about 3×, not 5×. Measured in customer counts, $300+ performs *worse* (30.8% reach 10 subscriptions). 41% of the $300+ group are services. I give **no** proven-channel credit to any idea for "paid ads plus high ticket"; at most 2 where a named, verified competitor or comparable acquires through the channel. | All |

---

## 2. Per-idea red team

### Q1. Self-serve AI live translation for small US towns, school boards and councils ($300–600/month)
**What I checked:**
- **Glossa** [Verified: local TrustMRR .md]:
  - pricing $99 / $299 / $499 a month, plus $5/hour/language pay-as-you-go;
  - 98 active subscriptions, $14,206 MRR, so ARPU is about $145;
  - Cyprus-based, labelled B2C;
  - monthly revenue went from $4.1k (Dec 2025) to $31.8k (Sep 2026).
- **Government market** [Secondary: SF Public Press, Jun 2024]:
  - Gilroy pays about $300 for a 2-hour meeting with Wordly.
  - Wordly plans cost about $100–300 an hour.
  - San Francisco abstains, saying "there's no better interpreter and translator than the human".
  - A test of Wordly rendered "budget" as "butter" and "so moved" as "emotionally touching".
- Interprefy and KUDO are also in the market. **No self-serve government entrant surfaced** (search #4). That is not proof that none exists.

**Top 3 failure modes:**
1. **The wedge is already for sale, and the buyer budget gap is small.**
   - A clerk can buy Glossa's $299 plan today.
   - A town holding 2–3 meetings a month spends about $600–900 at Wordly's rates, so a $300–600 offer is a 1.5–2× saving, not 10×.
   - Wordly can add a small-town tier whenever it chooses.
2. **The public-sector cycle and accuracy liability.**
   - Phase 9 measured DIR software newcomers at a median of $19.7k a year, with 43% selling $0.
   - Public-hearing errors carry legal and civil-rights risk under Title VI/LEP.
   - Cities such as San Francisco prefer humans.
   - The decisive assumption (card or PO purchase within 60 days, without an RFP) is unmeasured.
3. **Founder labour at the wrong hours.** Meetings run 18:00–22:00 US time, which is 01:00–07:00 in Israel. Support is needed live during the meeting.

**Paid channel:** low search volume for government terms, and no CPC data. The real channel is outbound plus associations, which needs a US seller.

**Hard blockers:** none verified. A VPAT or SOC 2 may be required [Unknown].

**Verdict:** **Weak, but best of Phase 10.**
- Steps: CF 3,1,4,5,2 = 61 · Scal 3,4,2,4,1,3 = 58 · Dist 4,3,1,1,3 = 46 → 56.8, penalty 12 → **44.8**.
- **Decisive assumption:** small bodies buy at $300–600 a month from a non-US newcomer within 60 days, rather than buying Glossa or Wordly.
- **Cheapest desk check:** in 30 small-town or school-board agenda packets (public PDFs), search for "Wordly", "Glossa", "interpretation" and "translation" line items. **Kill if** more than a third already use a named AI vendor, or if fewer than 5 of 30 show any translation spend.
- **Cheapest real-world test:** 200 targeted clerk and superintendent contacts plus $400 of Google Ads, offering a 30-day pilot on one meeting series. **Kill if** fewer than 5 pilots start, or fewer than 2 convert to ≥$300/month within 90 days.

### Q2. German AI DM appointment setter for DACH coaches (€400–700/month)
**What I checked:**
- **ai-dm-setter** [Verified: local TrustMRR .md]:
  - monthly revenue $5,175 (Nov 2025) → $23,270 (Sep 2026); $20,735 MRR; 29 subscriptions;
  - team of 2–5, France;
  - **10 declared channels** (SEO, blog, content, Instagram, LinkedIn, Meta Ads, cold DM, influencers, partnerships, word of mouth);
  - "plans shared on a 30-min demo".
- **Platform rules:**
  - WhatsApp barred general-purpose AI assistants from 15 Jan 2026; business-specific sales and booking bots are allowed (search #1).
  - Instagram allows messages only to users who wrote first, free-form only within the 24-hour window. The HUMAN_AGENT tag is barred for bots, and misuse can cost API access (search #6, vendor blogs).

**Top 3 failure modes:**
1. **Founder fit and selling.**
   - It is demo-sold, in German, to coaches. The founder neither speaks the language nor knows the culture.
   - The comparable is a 2–5 person team with 10 channels, so "Meta Ads" is not shown to be what worked.
   - Coaching churn of 5–7% a month is the segment norm.
2. **Copy plus platform risk.**
   - SetSmart already covers 5 languages, and adding German is a translation task.
   - Meta can tighten automation rules at any time. Post-ATT, Meta-dependent small firms lost 8–40% of revenue (Agent F).
   - Followers also bid for the same DACH partner slots, pushing revenue share to 30–40%.
3. **At 3× CPC** (Agent E's inputs), CAC rises from $800 to $2,400 against about $3.6k LTV at 6-month life. LTV:CAC is about 1.5, which is marginal.

**Ledger proximity:** AI receptionists, auto-responders and "generic AI agency/chatbots". It differs only in segment, language and price.

**Verdict:** **Weak.**
- Steps: CF 3,2,3,4,2 = 57 · Scal 3,3,2,4,1,1 = 50 · Dist 4,3,2,2,3 = 55 → 53.8, penalty 12 → **41.8**.
- **Decisive assumption:** DACH coaches pay €400+ a month and a German partner sells it for the founder.
- **Cheapest desk check:** read Meta's Instagram Platform policy and the Messenger/Instagram message-tag docs (primary). Then check DACH coach marketplaces (Digistore24/Copecart partner directories) for existing "KI-Setter" listings. **Kill if** the policy forbids AI-generated replies posing as the account holder, or if 3 or more German setters already exist.
- **Cheapest real-world test:** €800 of Meta lead ads to DACH coaches with a German demo booking page and a contracted German demo seller. **Kill if** fewer than 8 demos are booked, or fewer than 2 paid pilots at ≥€390 come from the first 10 demos within 6 weeks.

### Q3. Collaborating-physician matching plus compliance admin for NPs/PAs (one specialty)
**What I checked:**
- **CMF Group** [Verified, 29 Jun 2026]:
  - New Jersey's S2996 (30 Mar 2026) removes joint protocols for APNs with more than 5,000 hours in primary care and behavioral health.
  - New York's 3,600-hour exemption was due to lapse on 1 Jul 2026; a bill to make it permanent was pending.
  - Oklahoma's HB2298 (Nov 2025) allows independent Schedule III–V prescribing.
  - California's AB 890 104-level NPs reach independence in 2026.
  - About 30 states plus DC have some full practice authority.
- **Done Global** [Secondary: Ropes & Gray, Jan 2026]: executives convicted late 2025. The allegations included corporate practice of medicine and pay-per-prescription incentives.

**Top 3 failure modes:**
1. **Demand erodes by statute, and the chosen wedge erodes first.**
   - Behavioral health is exactly where New Jersey removed protocols.
   - The $1.5–3k controlled-substance tier is the area of Done-type enforcement.
   - Every full-practice-authority law shrinks the market. Each one is a year-to-year legislative bet.
2. **Two-sided cold start with liability.**
   - The founder must recruit specialty physicians at ≤$650 and sign NPs at ≥$850, at the same time, in specific states.
   - Agreement templates for each state, malpractice placement and fair-market-value review cost more than $2k [Hypothesis].
   - Physicians bear chart-review liability, and the platform bears the reputational exposure.
3. **A funded incumbent owns the paid channel.**
   - Collaborating Docs runs 100–200 Google ads (verified).
   - Zivian has no match fee and a 7-day match.
   - At 3× CPC, CAC is about $1,125 against $225/month contribution: a 5-month payback that needs ≥15-month retention [Unknown].

**Hard blockers:** none verified. Anti-kickback and corporate-practice exposure needs counsel [Unknown].

**Verdict:** **Weak.**
- Steps: CF 4,1,2,3,3 = 53 · Scal 3,4,2,3,2,1 = 53 · Dist 4,4,2,1,3 = 56 → 53.6, penalty 13 → **40.6**.
- **Decisive assumption:** specialty NPs in the remaining restricted states are under-served by Collaborating Docs and Zivian (a match-time gap) *and* the specialty survives the next 2 legislative cycles.
- **Cheapest desk check:** read the Collaborating Docs and Zivian state pages for the target specialty and the 3 largest restricted states (TX, FL, CA-103). Check the current AANP map. **Kill if** both incumbents list the specialty with a stated match time under 2 weeks.
- **Cheapest real-world test:** $800 of Google Ads in TX and FL plus a $300 physician-interest ad. **Kill if** there are fewer than 7 qualified NP leads, fewer than 2 NPs accept ≥$800/month, or fewer than 4 specialty physicians accept ≤$650/month.

### Q4. Reverse recruiting for US professionals ($1,200–1,500/month)
**What I checked:** California Civ. Code §§1812.501, 1812.502 and 1812.507 [Verified: california.public.law, 2026-10-13]. Jobseeker-paid procurement of employment counts as an employment agency. Résumé and career-management services billed other than hourly count as an employment counseling service. The employer-paid exemption does not cover counseling services. A jobseeker fee needs a bona fide job order.

**Top 3 failure modes:**
1. **Licensing removes the best segment.**
   - NY and CA are both covered, and they hold the largest concentrations of laid-off tech and H-1B workers, which is Q4's entry segment.
   - The UK is barred.
   - Other states (IL, NJ, MA and others) are [Unknown], so each new state adds a legal check.
2. **Unit economics under copying.**
   - $980 contribution per client becomes **−$360** at 3× CPC.
   - Success means churn: the client leaves when hired.
   - Refunds on "no job" outcomes and FTC outcome-claim risk.
   - Providers already sell at $349 a month.
3. **Staffing in disguise.** It needs 10–15 VA hours per client per week. It meets Agent F's agency tests 1, 2 and 5. Defensibility is 0.

**Verdict:** **Kill for this founder.**
- Steps: CF 3,3,4,2,2 = 57 · Scal 3,2,2,2,0,2 = 37 · Dist 4,3,1,3,2 = 49 → 47.4, penalty 13 → **34.4**.
- **Decisive assumption:** refunds stay under 15% and average term is 3 months or more, in states where no licence is needed.
- **Cheapest desk check:** read the private employment agency statutes of the next 5 largest states (TX, IL, NJ, MA, WA) for "fee paid by applicant". **Kill if** 3 or more require a licence or bond for jobseeker-paid services.
- **Cheapest real-world test:** $1,200 of Google Ads, excluding licensed states, selling a $150 paid search audit. **Kill if** fewer than 6 audits sell, CPL is above $120, or fewer than 2 audits convert to a paid month within 14 days.

### Q5. Complex-case US expat tax catch-up and exit desk with an EA partner
**Top 3 failure modes:**
1. **Price compression and incumbents.**
   - MyExpatTaxes sells Streamlined at $875 and Exit at $1,175, with 4k+ Trustpilot reviews. Greenback sells every complex form à la carte.
   - Taxes for Expats runs 100–200 ads.
   - At 3× CPC, contribution falls from $650 to **−$550** per case.
2. **Licensing and liability without domain knowledge.**
   - Circular 230 representation needs an EA, CPA or attorney, plus §7216 consents.
   - Streamlined's non-willful certification and PFIC errors carry real penalties.
   - The founder is a pass-through to an EA, so the margin is a markup on EA hours.
3. **Seasonal, one-off and trust-led.** Buyers choose review-rich firms, a newcomer starts with 0 reviews, and the renunciation catalyst is already covered by incumbent articles.

**Verdict:** **Kill for this founder.**
- Steps: CF 4,2,3,2,2 = 54 · Scal 3,2,2,2,1,1 = 38 · Dist 4,3,1,1,2 = 43 → 45.4, penalty 12 → **33.4**.
- **Decisive assumption:** the median scoped quote is ≥$1,500 at CPL ≤$150.
- **Cheapest desk check:** price the 3 most common complex profiles (Canada PFIC, UK pension plus ISA, Australian super) on the published price lists of Greenback, MyExpatTaxes and Bright!Tax. **Kill if** incumbents' totals are under $1,500 for 2 of 3.
- **Cheapest real-world test:** $1,000 of geo-targeted search in a peak season with a $150 paid scoping call. **Kill if** CPL exceeds $150, fewer than 4 scoping calls sell, or the median quote is below $1,500.

### Q6. International pet relocation coordination through partner agents
**Top 3 failure modes:**
1. **Capital and liability.** Prepaid cargo airfare per move exceeds the budget. A single animal death ends a review-dependent brand. Airline embargoes are seasonal.
2. **Pure operations labour.** 8–15 coordination hours per move across time zones.
3. **No margin evidence.** Gross margin after pass-through is [Unknown]. At 3× CPC, contribution is **−$210** per move.

**Verdict:** **Kill.**
- Steps: CF 3,2,1,2,1 = 38 · Scal 2,0,2,2,1,0 = 25 · Dist 4,3,1,1,2 = 43 → 33.8, penalty 13 → **20.8**.
- **Decisive assumption:** gross margin is ≥$1,200 per move with subcontracted IPATA partners.
- **Cheapest desk check:** compare the published partner/agent tariffs of 2 lane agents (where public) with consumer quotes. **Kill if** the spread is under $1,200.
- **Cheapest real-world test:** $800 of lane keywords with a $250 refundable deposit. **Kill if** there are fewer than 15 quote requests or 0 deposits.

### Q7. B2B equipment dealer quote desk (US)
**Top 3 failure modes:**
1. **Paid search converges to break-even under MAP.** Contribution is about $380 per $2k order, and at 3× CPC the order loses about $745. Paid-led survivors run at 5–10% net (#67576, #57358, #69490).
2. **Capital and float.** Supplier prepay plus Shopify reserves on $2k tickets, plus an LLC and a staging store, exceed $2k before the second order.
3. **Gatekeeping and time.** Dealer approval is at the brand's "sole and absolute discretion". The survivor median is 19.5 months to listing, and 8 of 14 had a loss month. Organic SEO is the profit engine, which the Phase 8 copy window erodes.

**Verdict:** **Kill for this founder.**
- Steps: CF 4,1,1,1,3 = 41 · Scal 3,1,1,3,1,2 = 36 · Dist 3,3,2,1,3 = 48 → 40.4, penalty 12 → **28.4**.
- **Decisive assumption:** ≥4 dealer approvals for a foreign-owned new store, and ≥40% non-paid order share within 12 months.
- **Cheapest desk check:** count brands with published online-dealer and dropship terms in one niche. **Kill if** fewer than 10 of 30.
- **Cheapest real-world test:** apply to 15 brands. **Kill if** fewer than 4 approve within 6 weeks.

### Q8. Own-label factory-direct customisable high-ticket catalogue
**Top 3 failure modes:**
1. **n=1 Track B evidence.** #88863 ($58k/month) is a seller's exit at its peak, for sale at $1.98M. #95128 runs at TACoS 46% and 20 owner hours a week.
2. **Copying is trivial and price is unprotected.** Followers can buy the same factory SKU. Agent E found no $300+ B2C paid-channel winner in TrustMRR. Shopping ROAS fell 43% in the EU.
3. **Tariff volatility and capital.**
   - IEEPA duties were struck down and replaced first by Section 122, then by a 10–12.5% Section 301 action on lighting from 24 Jul 2026, on top of legacy China duties [Secondary: LightNOW].
   - Section 232 imposes 25% on upholstered wood furniture.
   - Cross-border returns.
   - $2k buys one test.

**Verdict:** **Kill for this founder.**
- Steps: CF 3,2,1,2,3 = 44 · Scal 3,0,2,3,1,1 = 34 · Dist 3,3,1,2,2 = 42 → 39.6, penalty 13 → **26.6**.
- **Decisive assumption:** landed cost ≤45% of price, and a newcomer reaches TACoS ≤45%.
- **Cheapest desk check:** HTS duty stack for the product code (USITC HTS plus USTR 301 lists). **Kill if** landed cost exceeds 45% of target price.
- **Cheapest real-world test:** $1,000 of Google plus Meta retargeting. **Kill if** fewer than 3 orders, or TACoS exceeds 45%.

### Q9. Offshore service-desk seats for US independent insurance agencies
**What I checked (search #8):** agency management systems at $99 a month include COI generation and renewal tracking (NowCerts, InsurAMS). Arahi AI lists $299 a month per agent and claims a 90% time cut on renewals [vendor claims].

**Top 3 failure modes:**
1. **It is staffing.** The margin is a labour markup (about $650 on $1,600). Every Agent F agency test applies.
2. **AI and software eat the task set.** $99–299 a month of software covers COI and renewal tasks against a $1,200–3,500 seat. Price compresses from below.
3. **Dense, copyable field.** Wing (500+ agencies), Stealth Agents, MyOutDesk. CPL about $84 now; at 3× CPC, CAC is about $2,100 against $650 a month, a 3.2-month payback. EF #62527 is 5.4 years old, not newcomer evidence.

**Verdict:** **Weak (Track A at most, as a staffing firm).**
- Steps: CF 4,3,3,2,2 = 58 · Scal 4,4,2,2,0,1 = 46 · Dist 4,3,1,2,2 = 46 → 50.8, penalty 13 → **37.8**.
- **Decisive assumption:** seats last ≥6 months despite AI substitution.
- **Cheapest desk check:** read Wing's and Stealth Agents' insurance pages and 20 recent public reviews. **Kill if** they offer a sub-$1,200 insurance seat with system-specific training.
- **Cheapest real-world test:** $700 of ads for a 2-week paid trial seat. **Kill if** CPL exceeds $150, or 10 calls produce fewer than 2 seats.

### Q10. Compliance operations desk for newly registered small RIAs
**Top 3 failure modes:**
1. **Founder fit is 0.** It is securities-compliance work, and the founder has no domain. Trust goes to brand-name OCCO firms after enforcement actions.
2. **High drift and liability.** Ex-CCO contractor hours, E&O insurance, and blame for missed filings.
3. **Small, captured market.** About 1,200 small SEC registrants a year (verified). Custodians and launch consultants bundle introductions to compliance firms [Hypothesis].

**Verdict:** **Kill for this founder.**
- Steps: CF 3,1,2,3,2 = 45 · Scal 2,4,2,2,1,0 = 41 · Dist 5,4,1,1,2 = 51 → 44.6, penalty 13 → **31.6**.
- **Decisive assumption:** new small RIAs pay $600–1,200 a month to a non-brand provider.
- **Cheapest desk check:** Form ADV Schedule D / Item 1 data for 2026 registrants (the IAPD bulk file) on named compliance consultants. **Kill if** more than 60% already name one.
- **Cheapest real-world test:** $600 of ads offering a $900/month programme. **Kill if** CPL exceeds $200, or fewer than 2 of 8 calls accept.

### Q11. UK Companies House charge signals for commercial and asset-finance brokers
**What I checked:** LeadX's timeline [Verified: local TrustMRR]:

| Month | Revenue |
|---|---|
| Oct 2025 | $4.0k |
| Dec 2025 | $1.6k |
| Feb 2026 | $0.6k |
| Mar 2026 | $4.1k |
| Jun 2026 | $14.5k |
| Jul 2026 | $10.0k |
| Aug 2026 | $36.3k |
| Sep 2026 | $27.1k |

- 15 subscriptions; founded Jun 2023.
- LeadX bundles company, contact, lien, web and review data. It is not a UCC-only feed.

**Top 3 failure modes:**
1. **The data is free and already resold.** An Apify actor, pagecrawl.io and ltds.uk already pitch brokers. Followers can undercut to £50. Defensibility is 0.
2. **Small market.** About 1–2k UK brokers [Unknown]. Track B is unreachable.
3. **The comparable is survivor-shaped.** It spent about 2.5 years near zero, then lumpy (likely annual) payments, with a multi-source data product the founder would have to rebuild for the UK.

**Verdict:** **Weak.** The score rests on a cheap start (CF), not on evidence; same caveat as H7.
- Steps: CF 2,2,5,5,3 = 67 · Scal 1,4,2,5,0,3 = 53 · Dist 4,3,1,2,2 = 46 → 57.2, penalty 13 → **44.2**.
- **Decisive assumption:** UK brokers pay £250+ a month for signals derivable from free data.
- **Cheapest desk check:** price pages of ltds.uk, Endole and Red Flag Alert for charge alerts. **Kill if** any sells broker charge alerts under £100 a month.
- **Cheapest real-world test:** a 2-week prototype feed and 60 LinkedIn messages to brokers. **Kill if** fewer than 3 commit to £250+ a month.

### Q12. Referral desk for cost-segregation and R&D-credit firms, fed by Google Ads
**What I checked:**
- The R.E. Cost Seg PartnerStack page shows "15% of total revenue".
- Its terms link to a Google Drive PDF ("Affiliate Partner Agreement V.2 – 15%"). The download was **refused ("Can't download file")**, and the viewer needs JavaScript or a sign-in. **Blocked; not bypassed.**

**Top 3 failure modes:**
1. **Bidding against the payer.** The study firms buy the same keywords. Verified analogues (Datarails, HubSpot) ban PPC or brand bidding.
2. **No volume or earnings evidence.** Commission lags 60–120 days, and study fees are [Unknown].
3. **Ledger proximity.** Lead-gen exclusions from P6 (L6) and generic affiliate programmes.

**Verdict:** **Kill** unless the terms permit PPC.
- Steps: CF 2,2,3,2,4 = 50 · Scal 3,1,1,4,0,2 = 37 · Dist 3,3,0,2,2 = 36 → 42.0, penalty 14 → **28.0**.
- **Decisive assumption:** the programme terms allow non-brand PPC, and CPL ×3 is still under 1/3 of the commission.
- **Cheapest desk check:** obtain the agreement PDF through the PartnerStack join flow. This is a sign-up, so the founder must do it. **Kill if** PPC is banned.
- **Cheapest real-world test:** $500 of ads to a qualification form. **Kill if** CPL exceeds $120, or fewer than 2 referrals are accepted in 45 days.

---

## 3. Leader challenges (final phase)

Every step below is checked against the corrections logs to avoid double counting:
- H7: P5 proven channel and scalable acquisition; P8 proven channel.
- J7: P5 proven channel, first customers and scalable acquisition.
- H6: P6 proven channel, scalable acquisition, defensibility and penalty 13.
- H1: P6 proven channel, defensibility and penalty 7.
- monday: P6 proven channel.

### H7 Blender add-ons: **hold 55.4.** The #1 position is **not meaningful**
- **Measured channel against the assumptions:**
  - 77% of 0–3-month paid add-ons get ≥1 sale, which supports speed to first sale.
  - The median is 2 sales, with 1% reaching 100 in 3 months. This is priced by P5 and P8 (proven channel 2, scalable acquisition 2).
  - No H7 criterion is still scored on a contradicted assumption.
- **Corrected premise:** H7's $14 median price falls in TrustMRR's <$30 band (lift 0.37–0.84). That is a subscription dataset, and H7 is a one-off marketplace, so I do not convert it into a step.
- **Is the #1 meaningful?** No.
  - The gap to H6 is 3.2, under the 5-point noise rule.
  - H7 has been the nominal leader since Phase 5 mainly because CF 80 rewards a cheap start.
  - Per product it is a 1–5% lottery, the same as every other measured base rate.
  - **The final report should present a tie.**

### H6 College-baseball API: **hold 52.2** (dissent 51.2)
- Low ARPU ($1.6–7.9 per CFBD member) is the Phase 3 modelling assumption ($5–10), priced in P6. It is not a new contradiction.
- The Phase 9 dissent stands: noncommercial terms on every primary source, which would mean penalty 14 and 51.2. No enforcement trigger has occurred.

### H1 Meshtastic kits: **penalty 7 is not defensible → 9, giving 49.2**
- The methodology defines the penalty as "higher penalty = weaker **or** more contradicted evidence". Contradiction is not the only trigger.
- Among the leaders, H1 has the **least** measured evidence and the **lowest** penalty:
  - no conversion at $300+ measured anywhere in 4 phases;
  - Amazon blocked in Phases 6, 9 and 10;
  - Tindie about 90% 0 reviews;
  - branded $150+ nodes 0–39 ratings.
- By contrast, H7 (penalty 12) and J7 (penalty 12) have n=221 and n=1,500 measured newcomer samples.
- Raising to 9 brings it to the bottom of the historical 9–14 band. It is a calibration fix, not a new evidence count. The P6 step 6→7 priced the 0–39 ratings; this step prices "unmeasurable for 4 phases".
- Phase 10's B2C finding (no $300+ B2C paid-channel winners; Agent E) concerns Meta and TrustMRR, not Amazon or YouTube. I do **not** use it as a contradiction.
- If the reconciliation rule requires a contradiction for leader penalties, record this as a dissent.
- CF 61, Scal 49, Dist 71 → Balanced 58.2 → **49.2**.

### monday.com Israeli invoicing app: **hold 50.8**
- No new contradiction:
  - incumbents still do not integrate with monday;
  - the NIS 5,000 allocation threshold is a snippet-level positive;
  - newcomer outcomes are unmeasurable.
- The Phase 6 red-team dissent (first customers −1, giving 50.2) is not re-pressed, because there is no new evidence.

### J7 Apify Actors: **speed to first sale −1 → 49.2** (the leader auditor rejected this)
- The auditor rejected speed −1 because "85–95% of newcomers get ≥1 user within 3 months".
- **My re-cut of the auditor's own sample** (`scripts/apify_self.py`, n=1,387 Actors created in 2026) shows that "≥1 user" is likely the developer:

  | Age | Median lifetime users | ≥2 users in last 30 days | ≥5 lifetime users |
  |---|---|---|---|
  | 0–1 month | 2 | 15% | 5% |
  | 1–3 months | 2 | 27% | 16% |
  | 3–6 months | 3 | 38% | 44% |
  | 6–9.5 months | 11 | 39% | 61% |

  - Freshly created Actors show `totalRuns 1, totalUsers 1` on their creation day (for example, the thequietstack Actors in `store.json`), which is consistent with the developer's or the platform's own test run [Hypothesis].
  - Users are not payers, and pay-per-event revenue per user is unpublished.
- So J7's speed step, the original assumption of fast first *paid* use through Store search, is contradicted by its own channel's newest data. The ground the auditor relied on does not measure sales.
- **Not double counting:** P5 cut first customers (Dist), proven channel and scalable acquisition. Speed (CF) was never cut.
- Confidence: medium-low, because whether user #1 is the developer is inferred.
- CF 75→71 → Balanced 62.4 → **49.2**.

### Recommended leader board
H7 55.4 · H6 52.2 · monday 50.8 · (K13 50.6 · K8 50.4 · UK MTD 50.2: not re-checked) · **H1 49.2** · **J7 49.2**.
- **Present this as a tied cluster of about 49–56.** No idea separates by 5 or more points.
- **Best Phase 10 entry:** Q1 at 44.8, about 4 points under the bottom of the cluster.

---

## 4. Recommended ranking (Phase 10)

| Idea | CF | Scal | Dist | Pen | Adj | Verdict |
|---|---|---|---|---|---|---|
| Q1 AI meeting translation, small public bodies | 61 | 58 | 46 | 12 | **44.8** | Weak, best of phase |
| Q11 UK charge signals | 67 | 53 | 46 | 13 | **44.2** | Weak |
| Q2 German AI DM setter | 57 | 50 | 55 | 12 | **41.8** | Weak |
| Q3 Collaborating-physician service | 53 | 53 | 56 | 13 | **40.6** | Weak |
| Q9 Insurance-agency seats | 58 | 46 | 46 | 13 | **37.8** | Weak (staffing) |
| Q4 Reverse recruiting | 57 | 37 | 49 | 13 | **34.4** | Kill (for this founder) |
| Q5 Expat tax complex desk | 54 | 38 | 43 | 12 | **33.4** | Kill (for this founder) |
| Q10 RIA compliance desk | 45 | 41 | 51 | 13 | **31.6** | Kill (for this founder) |
| Q7 B2B equipment dealer | 41 | 36 | 48 | 12 | **28.4** | Kill (for this founder) |
| Q12 Cost-seg referral desk | 50 | 37 | 36 | 14 | **28.0** | Kill unless terms allow PPC |
| Q8 Own-label factory-direct | 44 | 34 | 42 | 13 | **26.6** | Kill (for this founder) |
| Q6 Pet relocation | 38 | 25 | 43 | 13 | **20.8** | Kill |

**Tracks:**
- **Track A:** Q1 or Q11, but only through outbound or partner selling, not paid search. Q9 can reach Track A only as a staffing business, which the brief disfavours.
- **Track B:** none of the Phase 10 ideas has a credible route for this founder. Q3's Track B needs a funded two-sided build.

**Cheapest information (all free desk checks):**
- Q1: agenda packets, to count existing AI-vendor use.
- Q3: incumbents' specialty match times plus the current AANP map.
- Q4: 5 more state employment-agency statutes.
- Q12: the programme agreement (needs the founder's own sign-up).

**Verified or secondary contradictions of shortlist claims:**
- Q3: New Jersey removed protocols in behavioral health (Mar 2026), and about 30 states now have some full practice authority.
- Q4: California regulates jobseeker-paid procurement and résumé/career services (verified statute).
- Q1: Glossa already sells the price wedge ($299/100 h; realised ARPU about $145).
- Q2: Instagram bars bot use of the HUMAN_AGENT tag outside the 24-hour window [vendor blogs]. WhatsApp has banned general-purpose AI assistants since 15 Jan 2026.

**Sources (accessed 2026-10-13 unless dated):**
- [Cal. Civ. Code §1812.501](https://california.public.law/codes/civil_code_section_1812.501) · [§1812.502](https://california.public.law/codes/civil_code_section_1812.502) · [§1812.507](https://california.public.law/codes/civil_code_section_1812.507)
- [CMF Group, NP FPA 2026 roundup (29 Jun 2026)](https://www.cmfgroup.com/blog/nurse-practitioners/np-full-practice-authority-2026-legislation-roundup/)
- [Brach Eichler on NJ S2996](https://www.bracheichler.com/insights/health-law-alert-governor-sherrill-signs-law-granting-independent-practice-authority-for-certain-advanced-practice-nurses/) (search only)
- [Ropes & Gray on the Done Global prosecution (Jan 2026)](https://www.ropesgray.com/en/insights/alerts/2026/01/dojs-done-global-telehealth-prosecution-signals-expanded-criminal-risk) (search only)
- [SF Public Press on AI translation (Jun 2024)](https://www.sfpublicpress.org/as-bay-area-cities-adopt-real-time-ai-translation-for-public-meetings-sf-abstains/)
- [GovTech: cities and live automated translation](https://govtech.com/civic/cities-bring-live-automated-translation-to-public-meetings) (search only)
- [LightNOW / ALA Section 301 alert (5 Aug 2026)](https://www.lightnowblog.com/2026/08/ala-tariff-alert-new-section-301-tariffs-now-in-effect/)
- [respond.io: WhatsApp general-purpose chatbot ban](https://respond.io/blog/whatsapp-general-purpose-chatbots-ban) (search only)
- [Spur: Instagram DM automation rules](https://www.spurnow.com/en/blogs/instagram-dm-automation-rules) (search only, vendor)
- [Arahi AI for insurance agents](https://arahi.ai/blog/ai-for-insurance-agents-boost-efficiency-automated-operations-2025) (search only, vendor)
- [R.E. Cost Seg on PartnerStack](https://market.partnerstack.com/page/recostseg) (terms PDF blocked)
- Local: TrustMRR `.md` for ai-dm-setter, glossa-live and leadx (P8-D); the leader auditor's Apify `store.json` and `detail.json` (P10-auditL), re-cut by `P10-redteam/scripts/apify_self.py`.
