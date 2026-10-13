# Phase 10 — Agent F (Contrarian), label P10-F

Date: 2026-10-13. WebSearch used: 6 of 6. All analyses were run locally on files from earlier phases, with no re-crawling:
- the TrustMRR sample: P8-D/data/md, 7,883 profiles;
- the Empire Flippers dump: P8-B/data/ef_all.json, 2,854 listings.

Scripts and outputs are in `scratchpad/p6plus/P10-F/` (scripts/ and data/).

## Bottom line

1. **The 5.1× high-price lift is mostly a measurement artefact plus selection, not a lever.**
   - **It is arithmetic.** At $300+ a month per account, about 10 customers reach the $3k MRR threshold. Measured in customers, the $300+ group does no better, and in fact slightly worse.
   - **It is conditioned on survival.** It was computed only on businesses that already had revenue. Including zero-revenue launches, the hit rate falls from 51% to roughly 12–20%, or about 10% for solo product-only founders.
   - **It is concentrated in agencies, stealth operators and teams.** A smaller residual lift survives. Launches priced at $300+ are not more likely to end at $0 than cheap ones.
2. **The Phase 10 recipe combines two traits that come from different archetypes.**
   - High price lives with founder-led outbound: LinkedIn, cold email, DMs and calls.
   - Paid ads live with low-price consumer apps.
   - In the sample, 1 business has $100+ ARPU and declares paid channels only, and it made $0. No $300+ winner relies on paid ads alone.
3. **Paid-acquisition newcomers fail often.** About half of SMB search advertisers do not return within a year (dated sources). Paid-traffic businesses that survive to sale run at a median margin of about 28%. A single platform change (ATT) cut Meta-dependent small firms' revenue by 8–40%.
4. **Many high-ticket models are agency work in disguise.** That covers most done-for-you marketing, GEO and "AI agent" setups at $300+, and most Phase 10 A/C-style productised services. The market prices their profit at about 2.2× annual earnings, against 3.3× for SaaS.
5. **Better alternative:** keep the price point but change the channel. Pursue a B2B vertical tool at $300+ a month, sold through founder outbound plus one partner channel, and use paid ads only as retargeting or a supplement. A second-best, archetype-consistent lane is a paid-UA consumer subscription app. That lane is the founder's strongest skill fit but more fragile. Neither lane is far better than about 10–18% per attempt, and the confidence intervals are wide.

---

## Part 1 — Is the high-price lift causal or selection?

### 1.1 Reproduction
The Phase 8 definition:
- businesses founded 2024–26, with glitch-filtered data and founders with under 2k X followers;
- restricted to those with MRR > 0 and subscriptions > 0 (n = 1,898).

| ARPU band | n | hit rate (MRR ≥ $3k) | 95% CI | lift |
|---|---|---|---|---|
| <$10 | 813 | 3.7% | 3–5% | 0.37 |
| $10–30 | 645 | 8.4% | 6–11% | 0.84 |
| $30–100 | 322 | 19.6% | 16–24% | 1.95 |
| $100–300 | 79 | 29.1% | 20–40% | 2.91 |
| **$300+** | **39** | **51.3%** | **36–66%** | **5.12** |

Reproduced exactly [Verified: local TrustMRR snapshot, synced 2026-10-13].

### 1.2 Test A — measure the outcome in customers, not revenue (the mechanical check)

| ARPU band | ≥10 active subs | lift | ≥30 active subs | lift |
|---|---|---|---|---|
| <$10 | 44.2% | 0.99 | 29.0% | 1.05 |
| $10–30 | 44.8% | 1.00 | 27.3% | 0.99 |
| $30–100 | 48.4% | 1.08 | 27.6% | 1.00 |
| $100–300 | 40.5% | 0.91 | 24.1% | 0.87 |
| **$300+** | **30.8%** | **0.69** | **10.3%** | **0.37** |

High-price businesses do not acquire customers more easily; they acquire fewer.

Holding customer count fixed at 5–30 subscriptions, $300+ businesses reach $3k in 92% of cases, while those under $100 reach it in 0%. The lift is the price × count identity.

The one genuinely encouraging reading: among businesses with revenue, the distribution of customer counts is roughly flat from <$10 to $100. Up to about $100, charging more did not visibly cost customers.

### 1.3 Test B — include the failures (survivorship check)
ARPU only exists for businesses with revenue, so the Phase 8 denominator excluded every zero-revenue launch. To include them, I used the declared entry price: the lowest non-zero $ figure in the profile's pricing text, for all audience-free 2024–26 launches.

| Entry price | All (n=2,206) hit rate ≥$3k | Solo, named, no cofounder | Solo, product-only (no service keywords) | Share with MRR = $0 (all) |
|---|---|---|---|---|
| <$10 | 1.9% | 1.7% | 1.6% | 51% |
| $10–30 | 4.1% | 3.0% | 1.9% | 58% |
| $30–100 | 5.0% | 4.7% | 4.1% | 57% |
| $100–300 | 6.8% | 4.8% | 8.1% (n=37) | 62% |
| **$300+** | **20.0% (7/35, CI 10–36%)** | **15.2% (5/33, CI 7–31%)** | **10.5% (2/19, CI 3–31%)** | **51%** |

Price parsing is noisy. Three of the seven $300+ "winners" have actual ARPU under $100 (adspirer, nsketchai, econic), so their parsed prices are annual or enterprise tiers. Correcting for them, the result is about 4 of 32 (12.5%):
- **Windmill:** an agency at $3,999 a month.
- **Analytics Mates:** an analytics consultancy with a platform.
- **Audn.ai:** a 2–5 person team.
- **Plutocracy/Funneled:** the only plain self-serve product.

**Interpretation.** The realistic unconditional hit rate for a founder who launches at $300+ is about 10–15%, not 51%.

The zero-revenue share is the same across price bands, at 51–62%. This is the one finding that looks causal and helpful: pricing high did not raise the chance of selling nothing. n is small and the CIs overlap [Verified: local data; Hypothesis for the causal reading].

### 1.4 Test C — the founder-like subset (the check the brief asked for)
Solo founders: team not over one person, no cofounders, under 2k followers, businesses with revenue only.

| Subset | n at $300+ | hit rate | lift |
|---|---|---|---|
| All solo, <2k followers | 33 | 48.5% | 5.43 |
| Explicitly "1 person" | 4 | 50% | 6.3 (meaningless n) |
| Solo, 0 followers | 16 | 37.5% | 3.58 |
| Solo, named founder, not stealth | 14 | 50% | 7.6 |
| Excluding stealth and service-keyword businesses | 14 | 28.6% | 4.37 |

The lift does not disappear for solo, low-audience founders. Within the revenue-conditioned frame, it is not an audience or team artefact. It does shrink once services and stealth businesses are removed (51% → 29%). It also shrinks to about 10–15% once failures are counted (Test B).

### 1.5 Composition of the 39 businesses at $300+ ARPU (selection evidence)

**Profile against the <$10 band:**

| Trait | $300+ group | <$10 band |
|---|---|---|
| Service/agency wording in profile | 41% | 15% |
| Stealth listings | 26% | 7% |
| Listed for sale | 8% | 25% |
| 3 or fewer customers (concentration) | 49% | 33–39% in the other bands |

Stealth listings carry a 6.8× lift across the whole sample. They are disproportionately established operators who hide their identity.

**Hand classification of the 20 winners** (MRR ≥ $3k; total about $361k MRR):

| Type | Count | Businesses | Share of MRR |
|---|---|---|---|
| Explicit agency | 3 | Windmill (personal branding, $3,999/mo, $121k MRR); Karmable (self-described "GTM and growth agency", 2 clients at $8,250); Dynalis Studio ("support of our experts") | about 42% |
| Service-heavy hybrid | 4 | Tribe Social (8 accounts at $3.5k, custom community apps); Analytics Mates ($698k all-time but $4.6k MRR, declining consultancy book); Wesam (marketplace in beta, 3 payers); Saleda (2 accounts at $2k) | — |
| Self-serve or sales-led product | 6 | AppBird, AI DM Setter, Plutocracy/Funneled, CaptureFlow, PipeLime, Dena | about 21% |
| Stealth, unknown | 7 | — | — |

Among the 19 non-winners at $300+, at least 6 are consulting, build or done-for-you shops: Aerie, Pixel Money, DopeData, EditMyPodcast, JC Holdings ($3.5k audit plus $36k build) and MetaMuse.

**Founder experience and existing customers:** [Unknown]. TrustMRR does not expose founder history.

Indirect signs of prior books of business:
- Stealth-venture-10 has $389k all-time revenue but only $400 MRR.
- Analytics Mates is "founded 2024" with $698k all-time revenue.
- Windmill has $2.2M in about 29 months.

The literature supports a skill/selection channel. Gompers, Kovner, Lerner and Scharfstein (NBER w12592) find that entrepreneurs with prior successes are more likely to succeed, and they attribute much of that to skill [Verified: https://www.nber.org/papers/w12592, accessed 2026-10-13]. I found no empirical study linking a new venture's chosen price level to its survival. The pricing literature treats price as an outcome of strategy and product, which is endogeneity, not a free lever. Kaiser & Brettel (2015) surveyed 220 German tech ventures on the antecedents of pricing choice only [Secondary: springerprofessional.de abstract].

ChartMogul reports median monthly customer churn of 6.1% at ARPA under $25 against 2.2% above $500. ChartMogul links higher B2B retention to larger deals and informed buyers [Verified: https://chartmogul.com/blog/good-customer-churn-rate/, published 2022-02-23]. High price therefore also proxies for B2B buyers, who churn less.

### 1.6 Where do high price and paid channels actually co-occur?
Businesses with declared channels, audience-free, 2024–26 (n = 1,551).

**Including zero-revenue businesses:**

| Channel group | Segment | n | Hit rate ≥$3k | 95% CI |
|---|---|---|---|---|
| Paid/partner only | Consumer app | 33 | **18.2%** | 9–34% |
| Paid/partner only | B2B | 37 | 10.8% | 4–25% |
| Paid/partner + outbound | B2B | 60 | **15.0%** | 8–26% |
| Outbound/word of mouth only | B2B | 181 | 5.5% | 3–10% |
| Organic only | B2B | 282 | 1.1% | 0–3% |
| Organic only | All | 946 | 2.5% | 2–4% |

**Revenue-conditioned, by price:**
- At $100+ ARPU, only 1 business declares paid/partner channels alone, and it had 0 wins.
- Outbound/word of mouth only at $100+: 7 of 15 reached $3k.
- Paid + outbound at $100+: 4 of 11 reached $3k.

**Channels declared by the 32 businesses at $100+ ARPU:** SEO 20, LinkedIn 18, cold email 13, cold DM 13, content 12, cold calling 6, Facebook 5, partnerships 4. Google Ads and Meta Ads are rare.

**Paid-declared winners:** of 26 businesses that declare paid or partner channels and reached $3k, 22 have ARPU under $100, mostly consumer apps on Meta or TikTok via RevenueCat or Superwall. The 4 at $300+ (CaptureFlow, private-enterprise-35, AI DM Setter, private-venture-50) all also list cold DM, LinkedIn or cold email, and 3 of the 4 are stealth listings.

**Caveat: reverse causality.** Declared channels describe the business today. Winners can afford ads, and losers may delete a channel that failed.

**Conclusion:** "$300+ and paid ads" is not an observed winning archetype. The observed high-ticket archetype is "B2B, $300+, outbound (plus partners), often a small team or an existing operator". The observed paid archetype is "consumer app, under $100, Meta/TikTok, paywall tooling".

---

## Part 2 — Failure rates of paid-acquisition newcomers

No current, public cohort study of new advertisers' survival exists, as far as 6 searches could find. The best available evidence follows.

**SMB search advertiser churn (dated):**
- Borrell Associates for Clickable (2009): about 50% of SMBs do not buy online ads from the same company the following year. Some resellers' churn approaches 100% annualised [Secondary: davidmihm.com, 2009, citing Borrell/Search Engine Land; the SEL page returned 403].
- Search snippets add: up to 50% quit by 90 days and up to 90% within 6 months [Secondary: search snippet only, unverified].

**Google's own framing (LSA16, 2016):**
- "Churn" means an AdWords account inactive for 6 consecutive months.
- 52% of churn is "controllable": dissatisfaction, price, or loss to a competitor.
- 26% of customers were never asked to renew.
- 6- and 12-month contracts outperform month-to-month.

[Verified: http://www.localogy.com/2016/03/lsa16-what-google-data-says-about-small-business-advertiser-churn/, published 2016-03-08.] No base rate was disclosed.

**Platform shocks hit small paid-dependent firms hardest:**
- Aridor, Che, Hollenbeck, Kaiser and McCarthy (Management Science): after Apple's ATT, revenue growth fell 37% for the most Meta-dependent firms relative to diversified ones.
- Small firms drew about 60% of their traffic from Meta, against about 30% for large firms.
- [Verified: https://anderson-review.ucla.edu/barred-from-stalking-us-across-the-internet-returns-for-some-advertisers-plummet, 2025-09-17.]
- The abstract's "8–40% revenue decrease, borne by smaller firms" and "26% fewer new-customer orders" come from [Secondary: search snippets; INFORMS page returned 403].
- Moloco reported e-commerce cost per conversion up 155–200% in the six months after ATT [Secondary: Retail Dive via snippet].

**Acquisition costs are rising:** ProfitWell/Paddle report CAC up about 60% over 5–6 years for both B2B and B2C subscription companies [Secondary: multiple re-reports; original not reached].

**Empire Flippers: paid-traffic businesses that survived to a sale** (local data; profit is seller's discretionary earnings, survivor-biased):

| Measure | Paid-traffic businesses | Others |
|---|---|---|
| Median margin, listed 2023–26 | 28–42% | 82–95% (non-Amazon) |
| Within e-commerce/dropshipping, by listing period | 30% (2014–17) → 21% → 20% → 13% (2023–24) → 25% (2025–26) | about 36% → 23% |
| Young (≤3 years) listed 2023+, median margin | 28% (n=50) | 88% (n=77) |
| Young listed 2023+, share below 15% margin | 24% | 5% |
| Young listed 2023+, median net per month / owner hours per week | $5.9k / 8 h | — |

Paid businesses' margins sit well below non-paid ones in every period. The composition-controlled decline over time is mild and noisy, not a collapse.

Typical paid dropshipping economics: $100k a month gross turning into $6–9k net (#67576, #67137, #69750).

[Verified: local EF API dump, retrieved in Phase 8.]

**TrustMRR newcomers who declare paid channels:**
- 45% of paid-only declarers have MRR = $0, and 54% of paid + outbound declarers. Organic-only: 59%.
- Paid declarers do better than organic ones, but about half still earn nothing.

**What happens to CAC when 3 followers bid on the same keyword:**
- I found no published elasticity [Unknown].
- In auctions, a follower raises the clearing price the incumbent pays rather than merely splitting volume [Hypothesis, from second-price/quality-score auction mechanics].
- Combined with the roughly 6-month copy window from Phase 8, a paid-search-only offer has no protected unit economics.
- Retention-driven LTV (B2B churn of about 2%) is the only buffer, and it favours B2B over consumer.

**Agency client churn, for context:** "retainer agencies 18%/yr churn, 56-month client life; project agencies 42%/yr" [Anecdote/vendor claim: Focus Digital via secondary pages; original not found].

---

## Part 3 — Which high-ticket models are agency or freelance work in disguise?

**Tests.** Apply them to any Phase 10 idea. Two or more yeses mean "agency in disguise":
1. Delivery hours per account are constant or rise with the number of accounts, so contractor cost is a fixed share of revenue.
2. Gross margin after contractor cost is under about 60–65%. EF agencies have a 60% SDE margin and services 66%, against SaaS at 72% and digital products at 87%.
3. Price is "shared on a demo", "custom" or "setup plus retainer", and each client gets bespoke work.
4. Revenue sits in 3 or fewer accounts. That is true of 49% of TrustMRR's $300+ businesses.
5. Churn means losing a client relationship rather than a login, and the founder is the relationship.
6. Buyers would value the business at agency multiples. On EF, agencies sell at a median 2.25× annual profit and services at 2.50×, against 3.31× for SaaS. That is about a third less exit value per $ of profit [Verified: local EF data, n=16 agencies, 57 services, 58 SaaS].

**Disguised agency by these tests:**
- **Done-for-you marketing at $300–4,000 a month:** personal branding, GEO/"AI search visibility", "AI GTM engineering", ads management, link building. Examples: Windmill, Karmable, Aerie, Clarity Search, MetaMuse; EF #87450 and #84972. These do work, but they are agencies.
- **"AI employee" or automation builds with an audit fee and a monthly retainer:** JC Holdings, DopeData, Southsea, Pixel Money, MintMVP, Buildberg. Most have $0 MRR.
- **Custom or white-label apps at $1k+ per account:** Tribe Social has 8 accounts at about $3.5k each.
- **Analytics and data platforms sold with expert support:** Analytics Mates, whose $999 entry fee buys a consultancy book that is shrinking.
- **Phase 10 Agent A/C remits:**
  - Immigration and visa paperwork, expat tax, estate and probate admin, catch-up bookkeeping, compliance-as-a-service and outsourced operations are per-case labour. The product is a contractor's hours at a markup.
  - Several need credentialed humans: an enrolled agent or CPA for tax, a lawyer for immigration (RDG-type risk was found in Phase 6 L1).
  - "Productised with contractors" turns the founder into a staffing manager. Margins converge to about 55–65%, client relationships stay founder-held, and the business sells at about 2.2×.
  - This does not make them bad Track A cash businesses. It means they are the founder's labour or management time, which the brief says to avoid.

**Genuinely productised (not disguised) high-ticket models:**
- Software where a $300+ price reflects seats, volume or data access and delivery is the same for every account: AppBird (data intelligence, $199–399 tiers), Plutocracy/Funneled ($349–699 self-serve), Conductor-type APIs, SolarPulse ($499 per closer seat).
- Even these were sold through LinkedIn, cold outreach or demos, not paid ads.

---

## Part 4 — Better alternative direction?

**Verdict:** the evidence does not support "high-ticket + paid ads" as specified. It supports keeping one of the two traits and pairing it with the channel it actually travels with. Two archetype-consistent lanes follow. Lane 1 is the better fit for this founder's stated preferences on Track B, with one honest cost: the founder must sell.

### Lane 1 (recommended): B2B vertical tool at $300+ a month, sold through outbound plus one partner channel
- **Concept.** A self-serve-capable product with identical delivery per account and a price based on seats, volume or data. Examples: an integration or API like Conductor or Phase 7 M1, data intelligence, or a workflow tool for one trade.
- **Selling.** About 50–100 targeted outbound touches a week (LinkedIn plus email), plus one partner channel: a platform's partner directory, a consultant or reseller referral fee, or a vertical association. Paid ads are used only for retargeting and branded search.
- **Evidence.**
  - Revenue-conditioned: $100+ ARPU with outbound only, 7 of 15 reached $3k; with paid + outbound, 4 of 11.
  - Unconditional: B2B paid/partner + outbound, 15% (CI 8–26%, n=60), against 1.1% for B2B organic only.
  - B2B churn at $500+ ARPA is about 2.2% a month.
  - The 6 product winners at $300+ used LinkedIn, cold DM/email/calling, partnerships and demos.
- **What it changes from Phase 10.** The channel becomes the founder's (later a hired SDR's or an AI-assisted) outbound. It is not a keyword auction the 6-month followers can enter by outbidding. The copying risk moves to relationship and switching cost, which matters at 2% churn.
- **Labour.** Selling, not dev hours: about 5–8 hours a week of outbound and demos for 3–6 months. The work is delegable later to a commission closer or SDR, because each account's revenue ($3.6k+ a year) can fund it [Hypothesis].
- **Cheapest test.**
  - Pick one vertical from Agent D's list.
  - Send 300 personalised outbound touches over 4 weeks with a demo or prototype and a stated price of $300–500 a month. Ask for a paid pilot or a letter of intent.
  - **Kill threshold:** fewer than 3 qualified calls per 100 touches, or 0 paid pilots or deposits after 300 touches.
  - Cost: about $100–300 in data and tools. Describe only; do not run.
- **Main risk.** The founder is in Israel, works part-time and dislikes selling, and the evidence says this lane needs a seller. A 2–5 person team carries a 4.4× lift. A sales-capable cofounder or commission partner may be the real enabler.

### Lane 2 (skill fit, more fragile): paid-UA consumer subscription app
- **Concept.** A narrow consumer utility or wellness app with a paywall (Superwall/RevenueCat), whose acquisition is Meta or TikTok paid social from day one, tested as a portfolio of fast kills.
- **Evidence.**
  - Consumer apps declaring paid channels only: 18.2% reached $3k (CI 9–34%, n=33, zero-revenue businesses included).
  - Superwall carries a 4.26× lift and RevenueCat 1.68× (Phase 8).
  - SOSA 2026: about 17% of new apps reach $1k MRR within 2 years and 4.6% reach $10k (Phase 8).
- **Against it.**
  - ATT shows a single platform change can remove 8–40% of revenue from small Meta-dependent firms.
  - ProfitWell's CAC is up about 60%.
  - Followers arrive within months (over 100 padel apps, 141–151 wedding photo apps).
  - $2k funds roughly one meaningful creative-and-paywall test.
  - Ledger proximity: N10, K10 and N2 were app or paid-social variants. This is a channel-first variant, not a new niche, and should be scored as such.
- **Cheapest test.** 3 paywalled prototypes with $500 of Meta spend each, measuring install-to-trial and trial-to-paid. **Kill:** blended cost per paid subscriber above 40% of first-year net revenue per subscriber after 2 creative iterations.

### What I would not do
- Pure "$300+ productised service via Google Ads" (Phase 10 A/C style). It stacks two weaknesses: agency economics (about 60% margin, 2.2× exit, founder-held relationships) and the paid-channel copying risk.
- High-ticket "AI agent setup" offers. These have the most $0-MRR entrants in the $300+ sample.

## Decisive unverified assumptions
1. **Lane 1:** that this founder, or a hired or commissioned seller, can sustain about 300 outbound touches a month part-time and convert at least 1%. [Unknown: no data on Israel-based part-time sellers.]
2. **Lane 2:** that blended paid-social CAC for a new utility app in 2026 sits below first-year subscriber value. TrustMRR does not expose ad spend publicly; it is login-gated.
3. **Overall:** that the residual price effect is causal. The evidence for it rests on n = 35 launches at $300+ (Test B). The confidence intervals are wide, and founder experience could not be observed.

## Sources
- TrustMRR local snapshot (P8-D/data/md, synced 2026-10-13). Analyses: P10-F/scripts/analyze.py, stability.py, channels.py, chan2.py, intended.py.
- Empire Flippers local dump (P8-B/data/ef_all.json). Analyses: P10-F/scripts/ef.py, ef_agency.py.
- [Localogy LSA16, Google data on SMB churn, 2016](http://www.localogy.com/2016/03/lsa16-what-google-data-says-about-small-business-advertiser-churn/)
- [David Mihm on Borrell/Clickable SMB SEM churn, 2009](https://www.davidmihm.com/blog/smbiz/paid-search-smbs)
- [UCLA Anderson Review on Aridor et al., ATT, 2025](https://anderson-review.ucla.edu/barred-from-stalking-us-across-the-internet-returns-for-some-advertisers-plummet)
- [Management Science paper (403 when fetched)](https://pubsonline.informs.org/doi/10.1287/mnsc.2024.06600)
- [ChartMogul churn by ARPA, 2022](https://chartmogul.com/blog/good-customer-churn-rate/)
- [NBER w12592, Gompers et al.](https://www.nber.org/papers/w12592)
- [Kaiser & Brettel, pricing antecedents](https://www.springerprofessional.de/en/antecedents-to-pricing-strategy-factors-driving-the-selection-of/2290932)
- ProfitWell CAC +60% (secondary re-reports, e.g. [joinclyde.com](https://www.joinclyde.com/blog/three-ways-to-combat-rising-customer-acquisition-costs))
- Agency churn (vendor pages, e.g. [agiled.app](https://agiled.app/statistics/client-retention-statistics))

WebSearch count: 6. All six are logged in research-notes/search-log.txt.
