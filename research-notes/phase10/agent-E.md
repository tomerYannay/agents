# Phase 10 — Discovery Agent E (Distribution), label P10-E

Date: 2026-10-13. WebSearch used: **5 of 6** (logged in `research-notes/search-log.txt`). Scratch: `scratchpad/p6plus/P10-E/` (scripts in `scripts/`, data in `data/`).

Remit: measure paid and partner channels for high-ticket offers ($300+/month or $1,500+ one-off). Then propose 3–5 opportunities where the channel evidence is strongest, each with a cheapest test and kill threshold (described only, not run).

## Headline findings
1. **On TrustMRR, paid channels lift B2C apps much more than B2B.** I re-cut the local P8-D sample (7,883 profiles; no re-crawl).
   - **B2B:** Google Ads 9.1% reach ≥$3k MRR (n=44) and Meta Ads 12.0% (n=25), against a 4.7% B2B base. That is about 2–2.5×.
   - **B2C:** Meta Ads 23.9% (n=46), against a 4.0% base. The headline "Meta 20.7%" is mostly consumer apps with $3–$60 ARPA.
   - **Most declarers fail:** 50 of 97 young Google Ads declarers have $0 MRR.
   - **Partner channels in B2B:** affiliates 17.4% (n=46) and partnerships 10.8% (n=37).
   - **Once ARPA is ≥$100, the channel hardly matters.** Paid 33%, partner 33%, outbound 37% and SEO 30% all reach ≥$3k (n=9–27). This group is conditional on having revenue, so it is survivor-biased. Price per account seems to drive more of the lift than the channel.
2. **Google Ads Transparency Center is public without login. The Meta Ad Library was not reachable with permitted tools.**
   - The Google Transparency Center's own JSON endpoints answered without login. They gave advertiser name matches with ad counts, plus each ad's first-shown and last-shown dates.
   - After a modest number of requests, Google returned its "unusual traffic" CAPTCHA redirect (`google.com/sorry`). I stopped and did not bypass it. It was still blocked after 20+ minutes of polling at 3-minute intervals.
   - So the planned density and longevity table for 10 niches is **not delivered**. Only probe data exists (below).
   - Meta Ad Library: curl returned 403 and WebFetch got "socket hang up". Not measured.
3. **Published CPC benchmarks exist only at industry level.** No free primary source gives keyword-level CPCs for high-ticket B2B niches. Vendor and agency figures put B2B SaaS cost per SQL at $400–800 for SMB and $800–1,500 for mid-market.
4. **Partner bounties for high-ticket B2B are plentiful and open to newcomers.** On the PartnerStack marketplace:
   - 417 programmes are listed and 59 pay $500 or more per referral. Examples: Deel $1,500, Rippling $1,600, Papaya Global $2,000 per closed deal, and Datarails $500 per qualified lead plus $5,000 per closed deal.
   - **The terms block the paid-arbitrage route.** Datarails bans all PPC on Google and Meta. HubSpot bans ads that compete with its own and requires ads to point to the affiliate's own site.
   - No source publishes what newcomer affiliates actually earn.
5. **What happens to CAC when competitors enter.** Google's own documentation says you pay what is needed to beat the Ad Rank of the advertiser below you. With no rival below, you pay only the reserve price. So followers raise your CPC directly. Published cross-vertical spreads suggest crowded high-intent terms cost about 2.5–6× more than uncrowded category terms.

---

## 1. Published CPC and conversion benchmarks (by vertical)

| Source (date) | Sample / bias | Key figures |
|---|---|---|
| LocaliQ, "Search advertising benchmarks", last updated 1 Jun 2026 [Verified: https://localiq.com/blog/search-advertising-benchmarks/, accessed 2026-10-13] | "Thousands" of LocaliQ client campaigns on Google and Microsoft Ads. Mostly SMB and local advertisers. Vendor that sells ad management. No date range given. | All-industry: CPC $5.42, CVR 8.18%, CPL $66.69. CPL fell for the first time in 5 years. **Attorneys and legal:** CPC $9.87, CVR 5.55%, CPL $131.63. **Business services:** $5.87, 4.85%, $93.69. **Career and employment:** $5.81, 3.05%, $67.36. **Dentists:** $8.00, 10.67%, $72.97. **Education:** $4.81, 13.14%, $77.48. **Finance and insurance:** $3.39, 2.64%, $74.44. **Industrial and commercial:** $5.87, 8.20%, $75.19. **Physicians:** $4.76, 12.43%, $40.04. **Real estate:** $3.22, 3.70%, $102.51. **Home improvement:** $8.33, 8.05%, $90.92. |
| WordStream Google Ads benchmarks | — | HTTP 403. Not read. Its 2025 LocaliQ archive copy was also not fetchable (web.archive.org blocked for WebFetch), so I could not compute a year-on-year change. |
| SaaS Hero, "2026 B2B SaaS cost per qualified lead benchmarks" (published 27 Feb 2026, modified Jul 2026) [Verified: https://www.saashero.net/google-ppc/b2b-cost-per-qualified-lead/, accessed 2026-10-13] | Agency. Aggregates third-party blogs with no sample sizes. Internally inconsistent (median CPL given as $213 and as $237). | Average B2B SaaS Google CPC **$8.86 (+29% YoY)**. Cost per SQL by ACV: <$10k ACV $400–800; $10–50k $800–1,500; >$50k $1,500–3,500. By channel: Google cost per MQL $80–280 and MQL→SQL 26–30%; Meta MQL $150–250; LinkedIn MQL $75–200. Cybersecurity cost per SQL $500–900. |
| GrowthSpree, "LinkedIn Ads benchmarks 2026 by vertical" (24 Apr 2026) [Verified: growthspreeofficial.com page, accessed 2026-10-13] | Own clients: 300+ B2B SaaS accounts, $60M spend. LinkedIn agency. | LinkedIn CPC $5–18 by vertical. CPL $75–400. Cost per SQL: HR tech $350–700; DevTools $400–800; industrial $400–900; fintech $800–2,000; cybersecurity $1,200–3,000. Lead Gen Forms convert 6–10%, landing pages 2–4%. |
| GrowthSpree, "Google Ads for cybersecurity SaaS" (14 May 2026) [Verified, accessed 2026-10-13] | Same vendor. Cites its own Q1/Apr 2026 data with no methodology. | **Compliance (SOC 2/HIPAA/PCI): non-brand CPC $15–25; comparison queries $60–150.** FedRAMP $25–40 / $120–250+. Attributes the premium to "50+ active vendors" and "bid wars". |
| Dreamdata B2B benchmarks (undated, © 2019–2026) [Verified: https://dreamdata.io/b2b-benchmarks, accessed 2026-10-13] | Attribution vendor. No sample disclosed. | Google 46% and LinkedIn 41% of B2B paid spend. No cost-per-deal figures. |

**Use for underwriting:**
- **Plain SMB B2B service keywords:** CPC ≈ $5–10 and CPL ≈ $70–130 (LocaliQ, SMB-heavy).
- **B2B SaaS and compliance:** CPC ≈ $9–25 and cost per SQL ≈ $400–1,500.
- All of these are vendor-sourced and unaudited. None is keyword-level for our candidate niches, so niche CPCs remain [Unknown] until someone opens Keyword Planner. That needs a Google Ads account, which is outside our rules.

## 2. Ad libraries: public readability and what was measured
- **Google Ads Transparency Center** [Verified: https://adstransparency.google.com, accessed 2026-10-13]:
  - **What works without login.** The page loads without login and has no robots.txt. Its own RPCs (`SearchService/SearchSuggestions`, `SearchService/SearchCreatives`) return JSON without auth.
  - **Limitation:** it searches by advertiser name or domain, not by keyword. So "advertisers per keyword" cannot be measured. The closest proxy is advertisers whose names match a term.
  - **What was measured before the block:**
    - "bookkeeping" returned **100 name-matched advertisers, the cap**. 10 were shown first, mostly small US/CA/AU firms with 1–15 ads each.
    - COR Bookkeeping (US): 13 ads. First shown 2025-03-11, last shown 2026-09-17, so a 2025 entrant still running about 18 months later.
    - BookkeepingPro (US): 6 ads, shown 2026-02-05 to 2026-06-29. A 2026 entrant that appears to have stopped after about 5 months.
    - These are anecdotes, not rates.
  - **Then I hit Google's CAPTCHA.** It redirected to `google.com/sorry`. I stopped and polled at 3-minute intervals for over 20 minutes without solving anything. It stayed blocked at report time.
  - **Not delivered:** the planned 10-niche table. It would have covered 12 US advertisers per niche: share of 2025–26 first-ad advertisers, share still active, and run length. The niches were bookkeeping, fractional CFO, compliance, R&D tax credit, cost segregation, medical billing, credentialing, immigration, trademark and lead generation.
  - The script `P10-E/scripts/gatc2.py` is resumable and stops on block. The Research Director or a later agent can rerun it at about one request every 3 seconds.
- **Meta Ad Library**:
  - The web UI returned HTTP 403 to curl and "socket hang up" to WebFetch. I could not fetch the API documentation either.
  - [Secondary/background, not verified this session] The Ad Library API needs a developer account with identity confirmation and an access token. It covers all ads only for EU-delivered ads (DSA); elsewhere it covers political and issue ads only.
  - **Not measured. Not bypassed.**

## 3. Affiliate and partner programmes paying for high-ticket B2B referrals
- **PartnerStack marketplace** [Verified: https://market.partnerstack.com/, parsed 2026-10-13]:
  - **417 programmes; 182 pay ≥30% or ≥$200; 59 pay ≥$500 per referral.**
  - **HR and payments bounties:**
    - Deel: $1,500 per paying customer.
    - Rippling: $1,600.
    - RemotePeople: $1,500.
    - Payoneer Workforce: $1,000 per qualified lead plus $1,500 per customer.
    - Papaya Global: $1,000 per opportunity plus $2,000 per closed deal.
  - **Other large bounties:**
    - Datarails: $500 per qualified lead plus $5,000 per closed deal.
    - MarketerHire: $5,000.
    - Navan: up to $1,000.
    - RUN Powered by ADP: $1,000+.
    - ShipBob: $1,000 per SMB.
  - **Vertical demo-plus-close bounties:** Boulevard $750 per demo plus $750 per customer; Weave $250 per demo plus up to $750.
  - **Percentage-of-ACV programmes:** Shade and Signal House 10–25% on about $25k ACV; Goflow 10% on $5k+.
  - **Cost segregation:** R.E. Cost Seg pays 15% of total revenue [Verified: market.partnerstack.com/page/recostseg; duration field blank].
- **Other programmes:**
  - Engineered Tax Services: 10% per qualified referral plus overrides on sub-affiliates [Secondary: search snippet; page 404].
  - Gusto R&D credit referral: $500 gift card (2022 terms) [Secondary].
  - HubSpot affiliate: 30% recurring for up to 1 year, 180-day cookie, no minimum sales, free to join, reviewed in 2–3 days [Verified: https://www.hubspot.com/partners/affiliates, accessed 2026-10-13].
- **Can newcomers join?** Yes, nominally. The pages say "apply" with no minimums.
- **Can newcomers earn using paid traffic? Mostly blocked by the terms:**
  - **Datarails** affiliate T&C §4.6 bans "any paid placements, including pay-per-click campaigns" on restricted networks, including Google and Meta. It also bans brand bidding. A qualified lead means a meeting of 15+ minutes, ICP fit is "in its sole discretion", and clawbacks run 30/60/90 days [Verified: https://www.datarails.com/datarails-aff-toc/, accessed 2026-10-13].
  - **HubSpot** policy (Aug 2024): no ads that compete with HubSpot's own advertising, including branded keywords, and ads must go to your own site [Verified: https://www.hubspot.com/partners/affiliates/program-policies].
  - **Deel**'s terms are in a PDF I could not access [Unknown].
- **Earnings distribution:** no primary source publishes the share of partners who earn [Search 2: none found]. The only figures are vendor claims, such as SaneBox's "average partner earns $2,300 in 90 days" [Anecdote/vendor claim].
- **Verdict:** bounties are large and open, but **paid-traffic arbitrage into these programmes is contractually restricted** in the verified cases, and newcomer earnings are [Unknown]. Earlier phases already excluded "generic affiliate/reseller programmes" (P6). Nothing here overturns that.

## 4. Newcomers without an audience winning on paid channels (TrustMRR local sample)
Method: `P10-E/scripts/paid.py` on `P8-D/data/parsed.json`. "Young" means founded 2024 or later, with marketing channels stated (n=1,737; ≥$3k base 4.3%). The channel field is founder-declared and lists **all** channels used. Winners usually list 5–10, so this measures association, not attribution.

| Young, channels stated | n | ≥$1k MRR | ≥$3k MRR |
|---|---|---|---|
| Any paid ads | 177 | 22.6% | 11.3% |
| Any paid, founder <2k X followers | 165 | 21.2% | 10.3% |
| Any partner (affiliate, partnerships, referral) | 140 | 18.6% | 9.3% |
| B2B Google Ads | 44 | 25% | 9.1% |
| B2B Meta Ads | 25 | 32% | 12.0% |
| B2B LinkedIn Ads | 8 | 12.5% | 0% |
| B2B Affiliate | 46 | 30% | 17.4% |
| B2B Cold email | 96 | 13.5% | 7.3% |
| B2B SEO | 471 | 10.6% | 3.6% |
| B2C Google Ads | 43 | 7% | 0% |
| B2C Meta Ads | 46 | 41% | 23.9% |

**Audience-free, high-ARPA, paid or partner declarers with verified Stripe revenue** (from local profile .md files, synced 2026-10-13):

| Profile | Founded / country / team | Channel declared | Verified figures | Monthly trend |
|---|---|---|---|---|
| **ai-dm-setter** | 2025-05, FR, 2–5 people, 0 X followers | Meta Ads, Partnerships (plus SEO, Instagram, LinkedIn) | AI setter for coaches' Instagram and WhatsApp DMs. MRR $20,735; 29 subs; **ARPA ≈ $715**; $167.7k in the last 12 months | $5.2k (Nov 25) → $23.3k (Sep 26), rising |
| **private-venture-50** | 2025-11, FR, **solo** | Google Ads (plus SEO, cold DM and email) | Dev tools. MRR $9,056; **6 subs; ARPA ≈ $1,509**; $85k in 11 months | Volatile, $3.9k–16.5k per month, flat |
| **private-enterprise-35** | 2025-11, CH, 2–5 people | Google, Meta, TikTok and LinkedIn Ads, referral | Fintech/AI. MRR $15.5k; 38 subs; ARPA ≈ $409; $187k | Volatile, $10–35k per month. Stripe key expired 2 Oct 2026. |
| **backlinker-ai** | 2023-07, US | Affiliate, Partnerships | $300/month backlink outreach. MRR $19.5k; 48 subs | Flat to declining from a $24k peak |
| **aerie** | 2025-11, US | LinkedIn Ads | GTM engineering service. MRR $1.5k; 4 subs | One $18.7k spike, otherwise about $1.4k |

**Reading:**
- n=1 survivors. Phase 8 caveat applies.
- Only about 6 young profiles combine ARPA ≥$300 with a paid or partner channel. That is too few for a rate.
- The ai-dm-setter trend is the only clean, rising, audience-free, high-ARPA paid-social case.
- Profiles do not expose Meta ad spend, so CAC is [Unknown].

## 5. CAC when competitors enter a niche
- **Mechanism** [Verified: Google Ads Help, "Actual CPC", support.google.com/google-ads/answer/6297]:
  - You pay "what's minimally required to clear the Ad Rank thresholds" and to beat the advertiser directly below you.
  - With no eligible competitor below, "you only pay the reserve price".
  - So a lone bidder in an empty niche pays about the reserve price, and each follower bidding near your value raises your CPC directly.
- **Magnitude evidence (cross-sectional, vendor):**
  - Compliance SaaS non-brand CPC $15–25 against $60–150 on comparison queries, attributed to 50+ vendors' "bid wars" (GrowthSpree 2026). That is a 3–6× premium.
  - SMB business-services CPC is $5.87 (LocaliQ).
  - SaaS Hero reports B2B SaaS CPC +29% YoY.
  - LocaliQ reports all-industry CPL fell in 2026 for the first time in 5 years. Inflation is not uniform.
- **Theory and empirics.** No direct study of advertiser entry surfaced (Search 4). Athey and Nekipelov's structural GSP work finds bidders in dense phrases still earn well above their CPC [Secondary: search summary]. Entry squeezes rents but does not erase them.
- **Rule of thumb for this project** [Hypothesis, anchored on the spreads above]:
  - When 3 followers bid on the same exact-match high-intent terms, expect CPC to move from near-reserve (about $3–8) towards the marginal bidder's value per click. That is about **2–4×** in a small niche.
  - CAC scales the same way unless conversion improves.
  - **Survivable** if LTV:CAC is ≥3 at the post-entry CPC. That means planning at 3× today's CPC, which is already common in benchmark verticals, so it is achievable.
  - Offers needing near-reserve CPCs to break even should be rejected.
  - **Defences that survive copying:**
    - higher landing conversion (a better offer or proof);
    - longer retention;
    - non-auction channels such as partners and integrations;
    - long-tail and negative-keyword discipline.
  - First-mover advantage on keywords is **not** a moat (Phase 8's 6-month copy window applies).

---

## Opportunities where channel evidence is strongest
Scoring note: none of these clears the evidence bar the Phase 8–9 priors demand. I ranked them by channel evidence only.

### E1. AI DM setter subscription for DM-selling coaches and consultants, sold through Meta Ads (non-English segment)
1. **Concept:** a done-for-you AI "appointment setter" that answers Instagram and WhatsApp DMs in the seller's voice, qualifies prospects and books calls. Setup is done by a contractor; the AI runs it after that.
2. **Customer and geography:** coaches, consultants and info-product sellers who run Meta Ads or Instagram content. The entry segment is one non-English market (e.g., Spanish/LatAm, Portuguese/BR, German) where the FR comparable does not sell.
3. **Model:** $400–700/month subscription, with a demo call to close.
4. **Spending evidence:**
   - ai-dm-setter's verified Stripe revenue: $175.9k all-time, $20.7k MRR, 29 subs, rising each month for 11 months [Verified: local TrustMRR .md, synced 2026-10-13].
   - Other DM-automation profiles in the sample are lower-ARPA (confidential-startup-72: $12.3k MRR at $84 ARPA, affiliate channel).
5. **Competitors:** ManyChat ($15–$100s per month, DIY), human setters, other AI setter tools [Unknown count]. Customers dislike human setters' cost and inconsistency (comparable's own copy) [Anecdote].
6. **Entry:** language and segment. It is not first-to-notice; a follower can do the same. **Defensibility ≤2.**
7. **Acquisition:**
   - Meta Ads to coaches (B2B Meta 12% ≥$3k, n=25), plus partnerships with coaching-programme owners who resell to their students.
   - CPL for this audience: [Unknown]. SaaS Hero puts Meta B2B MQLs at $150–250 [vendor].
   - Meta Ad Library density not measured (blocked).
8. **Operations:** Israeli operation is fine. **Platform risk is high:** Instagram Messaging API rules and the WhatsApp Business policy on AI bots [Unknown details; must be read before the test]. This sits close to excluded ledger items ("AI receptionists", P8 "Thumbtack auto-responders", "generic AI agency/chatbots"). It differs in segment (DM-selling coaches), price (about $700) and channel (Meta Ads), and should be judged on that basis.
9. **Labour:** onboarding about 2–4 hours per client by a contractor. The software scales.
10. **Unit economics** [Hypothesis]:
    - Inputs: $600 ARPA, 6-month average life, so $3.6k LTV.
    - CAC at a $200 demo cost and a 25% close rate: $800.
    - After 3 followers enter (CPC ×3): about $2.4k CAC, so LTV:CAC ≈ 1.5. Marginal.
    - Track A plausible; Track B needs retention.
11. **Kill risks:** Meta API or policy change; churn among coaches (an income-volatile segment); copycats.
- **Cheapest test** (describe only):
  - Spend $600–800 on Meta lead ads in one language, targeting coaches.
  - Send them to a demo page with a Loom demo and a waitlist priced at $490/month.
  - First read the Instagram and WhatsApp automation policies.
  - **Kill** if cost per booked demo exceeds $250, or if fewer than 2 of the first 8 demos agree to a paid pilot within 30 days.

### E2. High-ACV vertical B2B tool sold on exact-match Google Ads ("few customers, big tickets")
1. **Concept:** a pattern, not a niche. It is a channel template for Agent C or D ideas: a tool or productised service priced at $500–1,500/month, sold to one profession through high-intent Google search terms.
2. **Customer:** decided by C or D.
3. **Model:** subscription of $500–1,500/month.
4. **Evidence:**
   - private-venture-50: solo founder, 6 subs at about $1.5k ARPA, $85k in 11 months, Google Ads declared [Verified local].
   - B2B Google Ads declarers reach ≥$3k at 9.1% against a 4.7% base. But 52% of Google Ads declarers have $0.
5. **Competitors:** per niche.
6. **Entry:** per niche.
7. **Acquisition:** CPC $5–10 for SMB services and $15–25 for compliance-type terms; cost per SQL $400–1,500 (vendor benchmarks above).
8. **Capital:** a $2k budget buys about 200–400 clicks. At a 3–5% conversion rate that is about 6–20 leads. That is enough to test whether leads arrive, not whether the business is profitable.
9. **Labour:** demo-led sales means founder hours early on.
10. **Unit economics** [Hypothesis]:
    - Inputs: $1k ARPA, 12-month life, so $12k LTV.
    - CAC: $1–3k today, $3–9k after 3 followers.
    - LTV:CAC stays above about 1.3 even in the bad case, and is better at higher ACV.
    - **This is the most copy-resilient of the five** because the price absorbs CPC inflation.
11. **Kill risk:** the niche keyword volume may be too small to fill a $2k test.
- **Cheapest test:**
  - Run $1,000 on 10–20 exact and phrase keywords to a "book a demo / get pricing" page. If the policy allows, use a pre-sale page that clearly states "early access".
  - **Kill** if CPL exceeds $150 after 150 clicks, or if there is no qualified call from the first 10 leads.
  - Before spending, pull the niche's advertisers from the Transparency Center by domain once it is reachable. If more than 10 advertisers are active, assume post-entry CPC is already priced in.

### E3. Partner-paid referral desk for cost-segregation / R&D-credit studies, sold through Google Ads to property investors and SMB owners
1. **Concept:** run search ads and a qualification funnel, then refer qualified prospects to study firms that pay 10–15% of the fee.
2. **Customer:** US real-estate investors (cost seg) or SMBs (R&D credit). The firms pay.
3. **Payout:** R.E. Cost Seg 15% of revenue [Verified PartnerStack listing] and ETS 10% [Secondary]. Study fees per engagement are [Unknown — not verified this session].
4. **Evidence:** payout terms only. No referral volume or newcomer earnings are published.
5. **Competitors:** the study firms advertise directly, and CPA referral networks exist. Advertiser density not measured (blocked).
6. **Entry:** "none credible" beyond a better funnel. We would be bidding against the payer.
7. **Acquisition:** Google Ads finance and real-estate CPCs $3–5, CPL $74–103 (LocaliQ, broad categories).
8. **Operations:**
   - Low capital. Likely regulated adjacency: tax-advice claims, and the lead-gen exclusions noted in Phase 6 L6.
   - PPC permission in these programmes' terms is [Unknown]. The verified Datarails terms show it is often banned.
   - Ledger note: near the P6 lead-gen exclusions (PI/Medicare/moving leads, lead-gen sites). It differs in being a B2B partner-paid bounty, not a pay-per-call buyer.
9. **Labour:** low.
10. **Unit economics** [Hypothesis]: needs a payout of at least about 3× CAC per closed referral. Commission is paid only after the client pays, so cash flow lags 60–120 days.
11. **Kill risk:** the terms ban PPC; payouts are delayed or clawed back; the partner bids on the same keywords.
- **Cheapest test** (desk step first, $0):
  - Read the R.E. Cost Seg and ETS programme terms for PPC and brand-bidding rules.
  - **Kill immediately** if PPC is banned.
  - Otherwise run $500 Google Ads to a qualification form. **Kill** if CPL exceeds $120, or if the partner accepts fewer than 2 qualified referrals in 45 days.

### Killed or weak (channel evidence negative)
- **Paid-search arbitrage into high-bounty SaaS affiliate programmes** (Deel, Rippling, Datarails etc.). The verified terms ban PPC or brand bidding (Datarails, HubSpot), and HR/fintech category terms are where vendors bid themselves. Newcomer affiliate earnings are unpublished. Killed. It is also a ledger repeat (P6 "generic affiliate/reseller programmes").
- **LinkedIn Ads as a primary channel for a <$5k-ACV offer.** B2B LinkedIn declarers had 0 of 8 at ≥$3k, and vendor cost per SQL is $350–3,000. Weak.
- **Meta Ads for B2C high-ticket.** Meta's lift is real for $3–60 consumer apps. In the sample it does not carry over to $300+ B2C offers; no such profile was found. Agent A's ideas should not borrow the 23.9% B2C Meta rate.
- **backlinker-style $300/month SEO services via affiliates.** Flat or declining comparable, and a ledger exclusion (P8 "generic AI ads/SEO agents").

## Ranking and decisive unverified assumptions
1. **E2 (high-ACV vertical tool on exact-match Google Ads):** the most copy-resilient channel economics. Decisive unknown: the target keyword's CPC and monthly volume, which needs Keyword Planner or a live test.
2. **E1 (AI DM setter, non-English coaches, Meta Ads):** the cleanest rising audience-free comparable. Decisive unknowns: Meta's Instagram/WhatsApp AI-automation policy, and cost per booked demo.
3. **E3 (partner-paid cost-seg/R&D referrals):** decisive unknown is whether the programme terms allow PPC. That is a $0 check.

## Feed to other agents
- Use LocaliQ 2026 industry CPC and CPL as the floor and multiply CPC by 3 for the post-entry case.
- Treat Meta's TrustMRR lift as B2C-only.
- For B2B, partner and affiliate declarers (17% ≥$3k, n=46) did as well as or better than paid declarers.
- The Transparency Center is public and scriptable, but rate-limited. Use about 1 request every 3 seconds and stop on `google.com/sorry`.

WebSearch count: 5 (cap 6).
