# Phase 10: High-Ticket Offers with Paid Acquisition

**Date:** 2026-10-13
**Branch:** `local-research-phase6-10`
**Working files:** `research-notes/phase10/`
- Six discovery reports
- Final leader re-check (`audit-leaders.md`)
- Shortlist (`shortlist.md`)
- Evidence audit (`audit-shortlist.md`)
- Red-team report (`redteam.md`)

Scoring script: `scratchpad/p6plus/P10-score/score.py`. It reproduces every total in §6.

This is the final phase. The cross-phase synthesis is in `business-opportunity-final-report-phases1-10-2026-10-13.md`.

---

## Bottom line

**No Phase 10 idea enters the top cluster.** The best is Q1, self-serve AI live translation for small US public bodies, at **47.0**, which ranks about #22. The 12 shortlisted ideas score 24–47.

**Phase 10's most important output is a correction to the premise it was built on.** Phase 8 reported that winners without an audience over-index on high price per account (5.1× lift) and on paid channels (3–6×). Phase 10 re-analysed the same TrustMRR sample with two independent agents (D and F). Both concluded:

| Phase 8 claim | Corrected finding |
|---|---|
| A price of $300+/month gives a 5.1× lift; 51% reach $3k | That counted only profiles that already had revenue. Counting stated prices, including launches with zero revenue: **10–11.5% of $300+ launches reach $3k MRR, against 6.5% at $100–299 and 3.2% under $100.** The lift is about 3×, and about 90% still miss. Much of it is arithmetic: about 10 customers clear $3k. Measured by customer count, the $300+ group does *worse*: 30.8% reach 10 subscriptions. 41% of the group are services or agencies. |
| Paid ads give a 3–6× lift | **Mostly a low-ticket consumer-app effect.** 22 of 26 winners on paid channels are consumer apps priced under $100. Business Google Ads users: 9.1% reach $3k (n=44, baseline 4.7%), and 50 of 97 young Google Ads users have $0. At high price per account, LinkedIn, cold email, calls and partners do as well as or better than Google or Meta ads. |
| What survives | For solo founders without an audience, a residual price lift remains (about 3.6–5.4× on the revenue-only frame, n=33). Pricing high does not raise the share that sell nothing. |

**Paid acquisition is fragile under copying.**
- Google's auction makes each follower raise your cost per click. Agent E recommends planning at 3× the current cost per click.
- At that level, profit per sale turns negative for every one-off high-ticket service tested: reverse recruiting −$360, expat tax −$550, pet relocation −$210, equipment dealer −$745.
- Empire Flippers businesses built on paid traffic run at a median **28–42% margin**, against 82–95% for others.
- Dealers whose prices are fixed by manufacturers and who rely on paid ads run at **5–10%**.
- About half of small search advertisers churn within a year (Borrell 2009, dated).

**Final leader re-check: all five leaders hold.**
- **H7 55.4:** new Superhive sample of 221 add-ons; median 2 sales in the first 3 months; 1% reach 100.
- **H6 52.2.**
- **H1 51.2:** dissent at 49.2 (see §6).
- **monday.com app 50.8.**
- **J7 50.8:** a 1,500-Actor sample shows 2026 newcomers at a median of 1 user; dissent at 49.2.

The red team recommends presenting the top cluster as a **tie**, and this report agrees. No idea is 5 or more points clear of the next.

---

## 1. Methodology (unchanged)

- **Rubric:** frozen, scored at criterion level.

  | Score | Criteria (step weight) |
  |---|---|
  | CF | Spending ×5 · Speed ×4 · Capital ×4 · Margin ×4 · Labour ×3 |
  | Scal | Depth ×3 · Recurring ×4 · Acquisition ×4 · Leverage ×4 · Defensibility ×3 · Fit ×2 |
  | Dist | Clarity ×4 · Discoverability ×4 · Proven ×6 · First customers ×3 · Beyond founder ×3 |

  Balanced = 0.4 CF + 0.4 Scal + 0.2 Dist. Adjusted = Balanced − penalty.
- **Agents:** six discovery agents, a final leader auditor, a 12-item shortlist, and an independent evidence auditor and red team working in parallel.
- **Scoring:** new ideas take the mean of the two reviewers' scores. Leader corrections are made only as named criterion steps, and a penalty rises only on direct contradiction.
- **Searches:** 54 WebSearches, all logged.

  | Agent | Searches |
  |---|---|
  | A, B, C, D, F | 6 each |
  | E | 5 |
  | Leader auditor | 4 |
  | Shortlist auditor | 7 |
  | Red team | 8 |

- **Main data:**
  - the local TrustMRR sample (7,883 profiles; not re-crawled)
  - the Empire Flippers public API (2,878 listings, with monthly P&L)
  - Superhive product JSON (221 new add-ons)
  - Apify Actor API (1,500 Actors)
  - the SEC adviser file (Sep 2026)
  - PartnerStack's marketplace
  - Google Ads Transparency Center JSON endpoints, by advertiser name only
  - state statutes; the AANP practice map
  - LocaliQ/WordStream 2026 benchmarks (vendor)
- **Blocked or not measurable** (none bypassed):
  - Google Ads Transparency Center can't be searched by keyword, and returned a CAPTCHA after limited use.
  - Meta Ad Library returned 403 or a bot challenge.
  - No published keyword-level CPCs exist.
  - California statutes (403).
  - The Texas statutes site (JavaScript).
  - The R.E. Cost Seg affiliate terms (Google Drive refused the download).
  - Wing pricing (JavaScript).
  - Amazon and Meshtastic dealer sites (bot checks).
  - monday marketplace data (JavaScript shell).
- **Boundaries:** no contact, purchases, sign-ups, browser use, deployments or ads. All tests below are **described, not run**.

---

## 2. Direction and why

Phases 5–9 showed three things:
- newcomer success runs at about 4–6% per attempt;
- copies arrive within about 6 months;
- moats a founder can buy with $2k do not hold.

Phase 10 therefore targeted the traits Phase 8 had measured in winners without an audience: a high price per account, sold through paid or partner channels, with delivery that can be delegated. Each idea also had to show how its unit economics hold up when competitors copy it.

---

## 3. Discovery summary

**A, consumer high-ticket services**
- Six ideas, none with a moat. Under the "3 followers" shock, contribution falls to between one fifth and one half of base.
- Advertiser counts by name: Taxes for Expats 100–200, Airpet 200–300, Octopus Legacy 1,000–2,000.
- Kills:
  - Licensing: SSDI/VA, green-card petitions.
  - Upfront-fee bans: credit repair, student loans.
  - Price too low: credential evaluation, divorce documents.

**B, high-ticket physical goods**
- 14 young US dealer or dropship stores on Empire Flippers:
  - median $4.5k/month profit at a 10.5% margin
  - median 9 owner hours/week
  - 8 of 14 had a loss month in the last year
- Stores relying on paid traffic: 5–10% margins. Organic-led stores: 13–29%.
- Dealer terms are restrictive: discretionary approval, minimum-price rules that cover Google Ads, and termination "for any reason".
- Shopify can hold 120-day payment reserves.

**C, productised services**
- Of 2,878 Empire Flippers listings, **none** is a bookkeeping, compliance, billing or payroll business.
- About 79% of young B2B service listings are marketing agencies.
- Only 8 service listings name paid search.
- Bench (bookkeeping) collapsed in December 2024 and now gives catch-up work away free.

**D, high price per account on TrustMRR**
- Produced the premise correction above.
- Only 6 profiles meet the strict target; only one, ai-dm-setter, is a clear software comparable.
- About 70% of named winners sell revenue tools to people who sell (coaches, agencies, sales teams).
- Patterns: local-language copies of US-proven categories; pricing below an enterprise incumbent; small teams.

**E, channel measurement**
- CPC benchmarks (vendor):

  | Category | Cost per click | Cost per lead |
  |---|---|---|
  | Legal | $9.87 | $131.63 |
  | Business services | $5.87 | $93.69 |
  | B2B SaaS | $8.86 (+29% year on year) | — |

- PartnerStack lists 59 programmes paying $500+ per referral. Several ban PPC, so ad arbitrage into them is blocked.
- Google's auction rules confirm that followers raise each other's costs.

**F, contrarian**
- Produced the selection analysis above.
- Recommends a **B2B vertical tool at $300+/month, delivered the same way for every account, sold by founder outbound plus one partner channel**, with paid search only as support.
- Alternative lane: consumer subscription apps acquired through Meta or TikTok.
- Neither lane is likely to beat about 10–18% per attempt.

---

## 4. Shortlist (12)

| ID | Idea |
|---|---|
| Q1 | Self-serve AI live translation for small US towns, school boards and councils ($300–600/month) |
| Q2 | AI DM appointment-setter for coaches in a non-English market (German first) |
| Q3 | Collaborating-physician matching plus compliance admin for NPs/PAs in one specialty |
| Q4 | Reverse recruiting (contractor-run job search) for US professionals |
| Q5 | Complex-case US expat tax catch-up and exit desk |
| Q6 | International pet relocation coordination |
| Q7 | B2B equipment dealer through a quote desk |
| Q8 | Own-label customisable high-ticket catalogue, shipped factory-direct |
| Q9 | Offshore service-desk seats for US independent insurance agencies |
| Q10 | Compliance operations desk for new small RIAs |
| Q11 | UK Companies House charge signals for finance brokers |
| Q12 | Referral desk for cost-segregation and R&D tax-credit firms |

---

## 5. Adversarial review: key findings

| ID | Finding |
|---|---|
| Q1 | Mountain View's $43,750 for 300 hours reproduces, but it was a pilot. **Refuted:** Wordly is not quote-only; it sells online from about $1,500 for 10 hours. Glossa's real revenue per account is about $145, below $300. Teams and Zoom bundle translated captions. A NJ school board's $295/month Boostlingo purchase still needed a board vote. At Wordly's rates, a small town spends only $600–900/month, so the saving is 1.5–2×. Meetings run 01:00–07:00 Israel time. |
| Q2 | ai-dm-setter verified: $20.7k MRR, 29 subscriptions, rising from $5.2k (Nov 2025) to $23.3k (Sep 2026). But it declares **10 channels** and is a team of 2–5. Meta's rules: automated replies are allowed only within 24 hours, the human-agent tag is barred for bots, and disclosure is expected (Germany named). WhatsApp has barred general-purpose AI assistants since 15 Jan 2026; sales and booking bots are allowed. The English-language field anchors at $97–297. Selling needs German-language demos. |
| Q3 | AANP map verified: 11 restricted states and 12 reduced-practice states. New Jersey (Mar 2026) removed protocols for experienced behavioural-health NPs, which is the proposed wedge. Zivian covers aesthetics with no match fee. Texas caps each physician at 7 FTEs. The Done Global executives' convictions sit in the high-price controlled-substance tier. Two-sided cold start. |
| Q4 | NY GBL §171(2)(c)(3) and California law both regulate job-seeker-paid search, so NY and CA, the core segment, are out. The leading comparable refunds month one. |
| Q5 | Greenback already charges about $2.9–3.4k à la carte for complex cases, so there is no price gap. |
| Q7/Q8 | Empire Flippers figures confirm: the organic-led store makes $1.2k/month and the paid-led store runs at a 5% margin. The $58k/month own-label store has been unsold for 320 days, and its last three months average about $42k. |
| Q11 | Companies House publishes an official charges data stream. The Apify Store already returns 564 Companies House actors. LeadX spent about 2.5 years near $0 before lumpy revenue. |
| Q12 | The partner terms were unreadable, so whether PPC is allowed is unknown. |
| Copying | At 3× cost per click, every one-off service has negative contribution. Recurring ideas need 3–5-month payback with unmeasured retention. |

---

## 6. Phase 10 scoring (mean of the two reviewers)

| ID | Auditor steps (CF / Scal / Dist, pen) | Red-team steps | **CF** | **Scal** | **Dist** | Balanced | Pen | **Adjusted** | Aud / RT |
|---|---|---|---|---|---|---|---|---|---|
| Q1 AI translation, public bodies | 4,2,4,4,4 / 3,4,2,4,1,3 / 4,3,1,2,2, 12 | 3,1,4,5,2 / 3,4,2,4,1,3 / 4,3,1,1,3, 12 | 66.5 | 58.0 | 46.0 | 59.0 | 12 | **47.0** | 49.2 / 44.8 |
| Q2 German AI DM setter | 4,3,4,4,3 / 3,3,2,3,1,2 / 4,3,2,2,3, 12 | 3,2,3,4,2 / 3,3,2,4,1,1 / 4,3,2,2,3, 12 | 65.0 | 49.0 | 55.0 | 56.6 | 12 | **44.6** | 47.4 / 41.8 |
| Q11 UK charge signals | 2,3,5,4,4 / 1,4,2,4,0,4 / 4,2,1,2,2, 13 | 2,2,5,5,3 / 1,4,2,5,0,3 / 4,3,1,2,2, 13 | 68.5 | 52.0 | 44.0 | 57.0 | 13 | **44.0** | 43.8 / 44.2 |
| Q3 Collaborating physician | 4,2,2,2,3 / 3,5,2,3,2,1 / 5,4,2,2,3, 12 | 4,1,2,3,3 / 3,4,2,3,2,1 / 4,4,2,1,3, 13 | 53.0 | 55.0 | 59.5 | 55.1 | 12.5 | **42.6** | 44.6 / 40.6 |
| Q9 Insurance-agency seats | 4,3,3,2,1 / 4,4,2,2,0,1 / 4,3,1,2,2, 13 | 4,3,3,2,2 / 4,4,2,2,0,1 / 4,3,1,2,2, 13 | 56.5 | 46.0 | 46.0 | 50.2 | 13 | **37.2** | 36.6 / 37.8 |
| Q5 Expat tax desk | 5,3,3,2,2 / 3,2,2,2,1,2 / 4,4,2,2,2, 12 | 4,2,3,2,2 / 3,2,2,2,1,1 / 4,3,1,1,2, 12 | 58.5 | 39.0 | 49.5 | 48.9 | 12 | **36.9** | 40.4 / 33.4 |
| Q4 Reverse recruiting | 3,4,4,2,2 / 3,2,2,2,1,2 / 4,4,2,3,2, 13 | 3,3,4,2,2 / 3,2,2,2,0,2 / 4,3,1,3,2, 13 | 59.0 | 38.5 | 54.0 | 49.8 | 13 | **36.8** | 39.2 / 34.4 |
| Q10 RIA compliance desk | 3,2,3,3,1 / 2,4,2,2,2,0 / 5,3,1,2,2, 13 | 3,1,2,3,2 / 2,4,2,2,1,0 / 5,4,1,1,2, 13 | 47.5 | 42.5 | 50.5 | 46.1 | 13 | **33.1** | 34.6 / 31.6 |
| Q7 Equipment dealer | 4,2,2,1,3 / 3,1,2,3,1,3 / 4,3,2,2,2, 12 | 4,1,1,1,3 / 3,1,1,3,1,2 / 3,3,2,1,3, 12 | 45.0 | 39.0 | 50.0 | 43.6 | 12 | **31.6** | 34.8 / 28.4 |
| Q8 Own-label factory-direct | 4,2,1,2,3 / 4,0,2,3,1,2 / 3,3,2,2,2, 13 | 3,2,1,2,3 / 3,0,2,3,1,1 / 3,3,1,2,2, 13 | 46.5 | 36.5 | 45.0 | 42.2 | 13 | **29.2** | 31.8 / 26.6 |
| Q12 Referral desk | 2,2,4,2,4 / 2,0,1,3,0,3 / 3,3,0,2,1, 14 | 2,2,3,2,4 / 3,1,1,4,0,2 / 3,3,0,2,2, 14 | 52.0 | 32.5 | 34.5 | 40.7 | 14 | **26.7** | 25.4 / 28.0 |
| Q6 Pet relocation | 3,3,2,2,1 / 2,0,2,2,1,1 / 4,4,2,2,2, 13 | 3,2,1,2,1 / 2,0,2,2,1,0 / 4,3,1,1,2, 13 | 42.0 | 26.0 | 49.5 | 37.1 | 13 | **24.1** (kill) | 27.4 / 20.8 |

**Leader decisions**

| Leader | Decision | Reviewers |
|---|---|---|
| H7 | **Hold 55.4.** New sample: 221 paid add-ons released Jun–Oct 2026; median 2 sales under 3 months; 77% have ≥1 sale; 1% reach 100; supply about 390–490/month. Already priced in Phase 8. | All three hold. The red team says #1 is "not meaningful". |
| H6 | **Hold 52.2.** CFBD has 3,684 paid members at about $6–29k/month; Highlightly charges $7.99–44.99. Low price per member was already priced in Phase 6. | All hold. Red-team dissent 51.2. |
| H1 | **Hold 51.2** (penalty 7). | The leader auditor holds. The shortlist auditor and red team both argue for penalty 9 (**49.2**), because the Amazon channel behind Dist 71 has been unreadable for 3–4 phases and the rubric's penalty covers "weaker" evidence. The board keeps the Phase 6–9 convention that penalties rise only on direct contradiction, so 49.2 is recorded as the **majority dissent**. The cluster is presented as a tie either way. |
| monday.com app | **Hold 50.8.** Marketplace data is not public. No Israeli invoicing vendor's homepage mentions monday. | All hold. |
| J7 | **Hold 50.8.** 1,500-Actor sample: 2026 newcomers have a median of 1 user (30 days) at every age up to 9.5 months; 0–3% reach 100+. | Red-team dissent 49.2 (speed −1): a newcomer's "1 user" is likely the developer's own test. Two auditors reject this as double counting. |

---

## 7. Finalists: deep dives

**Selection:** top five by score: Q1, Q2, Q11, Q3 and Q9. Q9 is a staffing business and is covered briefly. All scenario figures are **[Hypothesis]**.

### F1. Self-serve AI live translation for small US public bodies (Q1): 47.0

- **Offer:** card-payable live translated captions for council and school-board meetings, at $300–600/month by hours.
- **Evidence:**
  - Mountain View paid Wordly $43,750 for 300 hours as a pilot.
  - Gilroy pays about $300 per 2-hour meeting.
  - Glossa, which sells to churches, grew from $4.1k to $31.8k monthly revenue (Dec 2025 to Sep 2026) at about $145 revenue per account.
- **Competition:** Wordly (self-serve from about $1,500 for 10 hours), Boostlingo ($295/month to a NJ school board), Glossa, KUDO, Interprefy, Teams and Zoom captions.
- **Risks:**
  - The price wedge already exists.
  - Purchases may need board votes.
  - Accuracy carries legal liability (Title VI, limited English proficiency).
  - Support is needed during US evening meetings, which is Israeli night.
- **Channel:** outbound to clerks and superintendents, and associations. Google search volume is low. Capital is under $2k.
- **Economics:**

  | Scenario | Paying bodies | Owner profit |
  |---|---|---|
  | Downside | — | Pilots don't convert; about $0 |
  | Base (24 months) | 15–25 at about $350 | **About $4–7k/month** after AI and inference costs (Track A) |
  | Upside | — | Hundreds of bodies via an association partner; $15k+/month |

- **Decisive assumption:** small bodies buy at $300–600/month from a non-US newcomer within about 60 days, instead of choosing Glossa, Wordly or bundled captions.
- **Desk check:** search 30 small-town or school-board agenda packets for translation line items. Kill if more than a third already name an AI vendor, or fewer than 5 of 30 show any translation spend.
- **Real-world test:** 200 targeted contacts plus $400 of ads offering 30-day pilots. Kill if fewer than 5 pilots, or fewer than 2 convert at $300+/month within 90 days.

### F2. German AI DM appointment-setter for coaches (Q2): 44.6

- **Offer:** an AI setter that qualifies and books calls from Instagram and WhatsApp inbound messages for DACH coaches, at €400–700/month.
- **Evidence:** ai-dm-setter (France), as in §5. SetSmart covers five languages but not German.
- **Risks:**
  - Meta automation rules (24-hour window; bots barred from the human-agent tag; disclosure).
  - Coaching churn is about 5–7% a month.
  - Selling needs German-language demos.
  - Followers could add German as a translation task.
  - Close to ledger exclusions (AI receptionists, auto-responders).
- **Unit economics at 3× cost per click (red team):** acquisition cost about $2,400 against about $3.6k lifetime value. LTV:CAC is about 1.5.
- **Economics:**

  | Scenario | Accounts | Owner profit |
  |---|---|---|
  | Base | 10–20 at €450, after a 30% partner share | **About $3–6k/month** |
  | Upside (several languages) | — | $15k+/month |

- **Decisive assumption:** DACH coaches pay €400+/month, and a German partner or demo seller can sell it.
- **Desk check:** read Meta's Instagram Platform policy (primary source) and look for existing German "KI-Setter" offers. Kill if AI replies posing as the account holder are forbidden, or if 3 or more German setters already exist.
- **Real-world test:** €800 of Meta lead ads with a contracted German demo seller. Kill if fewer than 8 demos, or fewer than 2 paid pilots at €390+ from 10 demos within 6 weeks.

### F3. UK Companies House charge signals for finance brokers (Q11): 44.0

- **Evidence:**
  - LeadX (US UCC liens plus a multi-source bundle) had lumpy revenue of $0.6k–36.3k a month, reaching $36.3k in Aug 2026, after about 2.5 years near zero.
  - The UK data is free through an official stream and is already resold (564 Apify actors, ltds.uk, pagecrawl.io).
- **Defensibility:** 0. The market is about 1–2k UK brokers [Unknown].
- **Economics:** Track A at best, about $1–3k/month at 5–12 brokers paying £250.
- **Decisive assumption:** brokers pay £250+/month for signals they could derive from free data.
- **Kill test:** if any vendor sells broker charge alerts under £100/month (desk check), or if fewer than 3 of 60 brokers contacted commit at £250+.

### F4. Collaborating-physician matching for NPs/PAs (Q3): 42.6

- **Evidence:**
  - Required in 23 jurisdictions.
  - NPs pay about $500–1,200/month; physicians earn $450–750.
  - Incumbents are Collaborating Docs (100–200 Google ads) and Zivian (funded; no match fee).
- **Risks:**
  - Full-practice-authority laws are shrinking the market, and the behavioural-health wedge goes first.
  - Two-sided cold start.
  - Legal exposure: anti-kickback rules, corporate practice of medicine, and the Done Global precedent.
- **Economics:** about $225 contribution per NP per month. At 3× cost per click, payback takes about 5 months and needs 15+ months of retention.
- **Decisive assumption:** a specialty is under-served by both incumbents and survives the next two legislative cycles.

### F5. Offshore service-desk seats for insurance agencies (Q9): 37.2

- Empire Flippers listing #62527: $78k/month revenue at a 25% margin, with 60 Philippine contractors and 4 owner hours/week.
- Crowded (Wing, Stealth Agents, MyOutDesk). It is a staffing business, at risk from AI substitution. No moat.

---

## 8. Cumulative leaderboard (final; * = corrected in Phases 5–10)

Phase 10 changed no leader score, so the board is unchanged from Phase 9 except for the new entries.
- Q1 (47.0) is the best Phase 10 idea, ranking about #22.
- The top cluster (#1–#10, 49.6–55.4) is presented as a **tie**, since no idea is 5 or more points clear of the next.

| Rank | Opportunity | Phase | Adjusted |
|---|---|---|---|
| 1 | Blender/VRChat add-ons (H7) | 3 | 55.4* |
| 2 | College-baseball data API (H6) | 3 | 52.2* |
| 3 | Meshtastic family kits (H1) | 3 | 51.2* (majority dissent 49.2) |
| 4= | monday.com Israeli invoicing app | 1 | 50.8* |
| 4= | Apify Actors (J7) | 4 | 50.8* (dissent 49.2) |
| 6 | Hebrew tender + receivership intelligence (K13) | 5 | 50.6* |
| 7 | Framer vertical kit (K8) | 5 | 50.4* |
| 8 | UK MTD prep for accountants | 2 | 50.2* |
| 9 | Israeli allocation verification | 1 | 49.8 |
| 10 | Sage 50 US/CA integration API (M1) | 7 | 49.6* |

The full top 20 and the ledger are in `research-notes/`.

---

## 9. Three most promising Phase 10 discoveries

1. **Most useful finding:** the corrected premise. A high price lifts the odds about 3×, not 5×. High-ticket newcomers win through outbound and partners, not paid ads. Paid ads help mainly low-ticket consumer apps, and paid-traffic businesses run at much lower margins.
2. **Best Phase 10 idea:** Q1, AI live translation for small public bodies. It is software-native, under $2k to start, and has verified spending and a growing adjacent comparable (Glossa). Its decisive assumption can be tested with a desk check of meeting agendas.
3. **Best template** (not scored): Agent F's lane, a B2B vertical tool at $300+/month, delivered the same way for every account, sold by founder outbound plus one partner channel. It is the only recipe consistent with all of Phases 8–10's measurements. Its decisive unknown is whether this founder, part-time from Israel, can sustain outbound and convert at least 1%.

---

## 10. Research limitations

**Ad-library measurement was not possible:**
- Google's transparency tool can't be searched by keyword and hit a CAPTCHA.
- Meta's ad library was blocked.
- Keyword-level CPCs are unpublished.
- The "3 followers" cost shock is therefore a labelled hypothesis, anchored only in Google's auction rules and vendor data showing crowded terms cost about 3–6× more.

**Survivor data:**
- TrustMRR is self-selected.
- Empire Flippers comparables are n=1 listings, several of them declining or unsold.
- Price-band results for $300+ rest on 35–214 profiles.

**Unread sources:** California statutes, Texas purchasing law, Meta's own policy pages (vendor summaries were used), the R.E. Cost Seg terms, Amazon, and the monday marketplace.

**Scoring:** H1's penalty convention is contested by two of three reviewers. The rubric still rewards cheap, fast starts (CF), which flatters Q11 and the H7, J7 and K8 family.
