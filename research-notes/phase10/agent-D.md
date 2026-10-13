# Phase 10 — Discovery Agent D (Software): high-ticket, audience-free TrustMRR winners

Date: 2026-10-13. Label: P10-D. WebSearch used: **6 of 6** (P10-D lines in search-log.txt). WebFetch: 6 (1 TrustMRR page, glossa.live, spf.io ×2, wordly.ai city-council page, mv-voice.com, Google Ads Transparency (JS-only; unusable)).

**Data.** No re-crawl. I used the existing Phase 8 random sample of 7,883 TrustMRR profiles (`scratchpad/p6plus/P8-D/data/md`, about 69% of the site, fetched 2026-10-13). I took the Phase 8 `parsed.json` and enriched it with the monthly revenue timeline and the declared channel list. Scripts are in `scratchpad/p6plus/P10-D/scripts` (`enrich.py`, `base.py`, `price.py`, `listw.py`, `trend.py`, `ppw.py`, `kw.py`), and outputs are in `P10-D/out`. Filters follow Phase 8:
- glitch filter applied;
- "young" means a self-entered founding date in 2023–2026 (n = 6,134);
- "audience-free" means the founder shows under 2,000 X followers.

All TrustMRR figures are [Verified: trustmrr.com/startup/<slug>.md, fetched 2026-10-13]. Every reading of cause or replicability is [Hypothesis].

---

## 0. Bottom line

1. **The assignment's exact target group barely exists.** It asks for audience-free winners founded 2023–26, with $300+ per subscription per month, $3k+ MRR and a declared paid or partner channel. **Only 6 profiles in the sample qualify**, and 2 of those are an agency and a stealth fintech. At $100–300 per subscription, **none** of the 26 audience-free winners declares a paid or partner channel. Most high-ticket winners (34 of 54) declare no channel at all.
2. **The headline "$300+ = 5× lift" mostly comes from the denominator.**
   - Measured per subscription (which requires MRR > 0), 58% of audience-free young $300+ profiles reach $3k MRR (28 of 48).
   - Measured by **stated price**, which includes pre-revenue profiles, the rate is **10.3% (22 of 214)** when the top plan is $300+. It is **11.5% (7 of 61)** when the *cheapest* plan is $300+.
   - The comparable figures are 6.5% for a $100–299 top plan and 3.2% for under $100.
   - So high price is a real lift of roughly **3×**, not 5×. About 9 in 10 high-ticket launches still miss $3k.
3. **Paid and partner channels help low-ticket products, not high-ticket ones.**
   - Under $100: profiles declaring paid or partner channels hit $3k+ at 12.0% (14 of 117), against 1.2% for organic-only. That is consumer apps on Meta/TikTok, plus a few B2B tools with affiliates.
   - At a $300+ top plan: paid/partner 15% (3 of 20) against organic-only 14% (8 of 57). There is **no meaningful difference**.
   - At high ticket, the channels that co-occur with winning are **outbound and demo-led**: LinkedIn 5 of 21, cold email 4 of 19, cold calling 2 of 8. Google Ads (1 of 9) and Meta Ads (1 of 4) do worse or no better.
   - The Phase 10 premise of "high ticket **sold through paid ads**" is therefore **not supported** by this dataset. "High ticket sold through demos, outbound and partners" is.
4. **What high-ticket audience-free winners are.**
   - About 37% of the identifiable $300+ winners are **services or agencies in disguise**: Windmill ($3,999/month personal-brand agency), Defined Chase, Karmable, Barron Tech, Dynalis, RankAI's "expert-led" tier.
   - Most of the rest sell **revenue to sellers**: AI SDR and lead data (Sbl, LeadX, Upscale, Pipelime), DM-to-call setters, funnels, backlinks.
   - Only a handful are **vertical tools**: AppBird (app/game studios), Glossa (churches), Aila (loan officers), Audn (AI pentesting).
   - Selling is often demo-gated ("plans shared on a 30-min demo").
5. **Four gaps proposed (G1–G4); two candidates were killed by searches.** The best evidence-to-fit gap is **G2: self-serve AI live translation for small US public bodies.**
   - Spending is verified: Mountain View paid $43,750 for 300 hours from Wordly in September 2026.
   - There is a price wedge: Glossa sells churches 100 hours for $299.
   - There is a newcomer template: Glossa grew from about $0 to $14.2k MRR in about 15 months with 105 followers.
   - **G1, a German-first AI Instagram/WhatsApp DM setter for coaches**, has the closest dataset template (ai-dm-setter, France, $20.7k MRR, $715 per subscription, Meta Ads, influencers and partnerships). Its follower risk is high.
   - Advertiser competition **could not be checked**. Google Ads Transparency returns only an empty JavaScript shell to a fetch, Meta Ad Library needs JavaScript or a login, and no published CPCs were found for these keywords.

---

## 1. Base rates (young 2023–26, audience-free < 2k followers)

### 1a. By revenue per subscription (MRR ÷ active subscriptions; only profiles with MRR > 0)
| Band | n | ≥$1k | **≥$3k** | ≥$10k |
|---|---|---|---|---|
| $300+ | 48 | 36 | **28 (58%)** | 17 |
| $100–300 | 86 | 46 | **26 (30%)** | 14 |
| < $100 | 1,886 | 328 | **168 (8.9%)** | 64 |

Within $300+, by declared channel:
| Declared channel | n | Reached $3k+ |
|---|---|---|
| None stated | 32 | 18 |
| Organic only | 8 | 4 |
| Paid ads only | 3 | 1 |
| Paid ads + partner | 3 | 3 |
| Partner only | 2 | 2 |

Paid or partner in any form: **6 of 8**. These numbers are too small to be meaningful.

Within $100–300: no channel stated 20 of 66, organic only 6 of 14, **paid or partner 0 of 6**.

**Caveats.**
- The table is conditioned on having revenue, and part of the effect is mechanical: at $300+ per subscription, only 10 customers are needed for $3k.
- "Subscription" is not "account". CaptureFlow's $465 per subscription is multi-seat billing on $49–99 seat plans.
- Several $300+ rows have only 2–8 subscriptions (Karmable, Barron Tech, Saleda, Tribe Social). These are retainers, not product adoption.

### 1b. By stated price (parsed from the pricing text, so pre-revenue profiles are included; n = 2,484 audience-free young profiles with a parseable price)
| Price tier | n | MRR > 0 | ≥$3k | Paid/partner declared | Organic only | None stated |
|---|---|---|---|---|---|---|
| Top tier ≥ $300 | 214 | 120 | **22 (10.3%)** | 3/20 (15%) | 8/57 (14%) | 11/137 (8%) |
| Cheapest tier ≥ $300 | 61 | 39 | **7 (11.5%)** | 2/5 | 1/13 | 4/43 |
| Top tier $100–299 | 336 | 168 | 22 (6.5%) | 1/24 (4%) | 7/89 (8%) | 14/223 (6%) |
| Top tier < $100 | 1,934 | 939 | 62 (3.2%) | **14/117 (12%)** | **8/641 (1.2%)** | 40/1,176 (3.4%) |

Per-channel results at a $300+ top tier (wins/n): LinkedIn 5/21 · cold email 4/19 · SEO 6/52 · cold calling 2/8 · Google Ads 1/9 · Meta Ads 1/4 · affiliate 1/6 · Facebook (organic) 0/11.

**Reading [Hypothesis].**
- Prices are parsed from free text and the parser is approximate. Annual prices were divided by 12; per-hour, per-credit and per-lead prices were skipped.
- This remains an **upper bound**, because listing on TrustMRR is self-selected.
- **The realistic prior for a newcomer who launches at $300+ is about 10% to reach $3k MRR, not 50%.**
- The paid-ads lift measured in Phase 8 is a **low-ticket consumer-app effect**: GoTall, Brawler, a makeup app and a pet-video app, all on Meta or TikTok Ads.

---

## 2. The winners

### 2a. Strict set: $300+ per subscription, $3k+ MRR, audience-free, founded 2023–26, paid or partner channel declared (n = 6)

Trend compares Q3 2026 with Q2 2026 verified revenue.

| Slug | Niche / buyer | Price signal | MRR (subs) | Paid/partner channels | Trend Q2→Q3 | Note |
|---|---|---|---|---|---|---|
| ai-dm-setter (stealth, FR, 2025-05, team 2–5) | AI setter answering Instagram/WhatsApp DMs in the founder's voice and booking calls (Calendly, iClosed, GoHighLevel). Buyers: coaches, consultants, infopreneurs, agencies | Fixed monthly, plans shared on a 30-minute demo; about $715 per subscription | $20,735 (29) | Meta Ads, Influencers, Partnerships (plus cold DM, Instagram, LinkedIn) | $42.3k → $59.8k (+41%) | "Certified Meta Business Partner", EU hosting |
| backlinker-ai (US, 2023-07) | AI reporter/editorial outreach for backlinks. Buyers: agencies and SEO teams | $300/month | $19,450 (48) | Affiliate, Influencers, Partnerships | $69.7k → $61.4k (−12%) | Listed at $350k (1.7×). Seller is leaving for a job |
| private-enterprise-35 (stealth, CH, 2025-11, team 2–5) | Fintech / AI / mobile (no description) | about $409 per subscription | $15,546 (38) | Google, Meta, LinkedIn and TikTok Ads, Referral | $64.7k → $47.2k (−27%) | Opaque |
| private-venture-50 (stealth, FR, 2025-11, solo) | B2B dev tools (no description) | about $1,509 per subscription | $9,056 (6) | Google Ads (plus SEO, cold DM, cold email) | $24.4k → $32.6k (+33%) | 6 customers: retainer-like |
| defined-chase (LT, 2023-10, team 6–10) | Paid-ads **agency** for advertisers spending $100k–10M a month | about $570 per subscription, mostly one-off | $6,272 (11) | Google Ads, Partnerships | $305k → $184k (−40%) | Service, not software |
| captureflow (PL, 2026-01, solo) | AI content repurposing for founders and agencies | $49–99 per seat; about $465 per subscription through seats | $4,182 (9) | Affiliate, Partnerships, Referral | $7.4k → $12.3k (+66%) | Seat-driven ARPU |

Only **ai-dm-setter** is both clearly software and replicable. Backlinker is flat to down and for sale.

### 2b. Wider $300+ audience-free winners (any or no declared channel), n = 28
Trend: 16 up, 5 flat, 7 down. 15 of the 54 $100+ winners are stealth listings, and 8 are listed for sale. US 27 and France 8 dominate; founding years are 2025 (24), 2023 (11), 2024 (10) and 2026 (9).

| Slug | Niche / buyer | Price | MRR | Trend | Type |
|---|---|---|---|---|---|
| windmill-growth-llc | Personal-brand marketing for B2B founders | $3,999/mo | $121k | +10% | Agency |
| upscale-system-llc | CRM + lead-gen software, B2B | ~$312 | $96k | +19% | Software |
| rankai | Autonomous SEO/AI search; agencies, e-commerce | ~$365, expert-led | $56.5k | −54% | Hybrid |
| sbl | AI SDR on LinkedIn/WhatsApp (India) | $99/$189/$997 | $30.1k | +271% | Software |
| tribe-social | Custom community apps for creators | ~$3.5k, 8 subs | $28.3k | +10% | White-label |
| appbird | App/game market intelligence for studios, publishers, investors | $199/$399 | $24.9k | +188% | Software (LinkedIn) |
| leadx | GTM data incl. **UCC filings** for business lending / equipment finance | ~$1,599 | $24.0k | +151% | Data |
| plutocracy (Funneled) | Shopify funnel split-testing for performance marketers (AU) | $349/$699 | $18.0k | +29% | Software |
| dynalis-studio | Shopify brands: experts + data/AI tools (FR) | ~$1,092 | $13.1k | +65% | Hybrid |
| karmable-inc / barron-tech-llc | AI-search marketing / Microsoft GTM services | 2 subs each | $16.5k / $15.2k | −28% / +58% | Service |
| analytics-mates | AI on GA data; from $999 per property | | $4.6k MRR, $26.6k r30 | −12% | Hybrid |
| pipelime / dena-ai | AI outbound agents / AI phone system | ~$374 / ~$436 | $4.1k / $3.5k | −52% / stopped | Software, decaying |
| saleda-ai, wesam-inc | Legal workflow AI; AI-agent marketplace | 2–3 subs | $4.0k / $7.3k | up | Thin |
| 8 stealth rows | No description | $318–$1,509 | $5.4k–25k | mixed | Unknown |

### 2c. Comparison band: $100–300 per subscription (n = 26; none declares a paid or partner channel)
Trend: 15 up, 5 flat, 5 down, 1 new. Notable rows:

| Slug | Niche / buyer | MRR | Trend |
|---|---|---|---|
| white-glove-content | Faceless video production for creators (service) | $72.3k | +163% |
| traxy-ai | Social-listening lead lists for B2B sales | $51.0k | +304% |
| audn-ai | Automated AI pentesting, $999/mo, team 2–5 (GB) | $23.7k | ×14 |
| chatdash-llc | White-label AI dashboards for agencies | $19.9k | −14% |
| lancer-app | Upwork proposal automation | $18.4k | +36% |
| amicited / mentionable | AI-search visibility | $16.7k / $3.8k | up |
| aila | Mortgage loan-officer AI, $50 per user | $14.9k | +119% |
| **glossa-live** | **Real-time AI translation for churches, $99–499/mo** | **$14.2k** (r30 $33.5k) | **+38%** |
| notfair / local-seo-bot | Google Ads AI / Google Maps SEO for SMBs | $12.2k / $11.6k | up |
| coucou (startup-a8e78dd113c0) | Planity salon Google reviews (FR) | $5.9k | +74% |
| fiveml, the-engine, syncgtm, prymatica, arcton, maverick | LinkedIn automation, GTM data, outbound agencies | $3.5k–7.7k | mostly flat or down |

### 2d. Paid-channel winners outside the band (useful only as channel evidence)
- Refined Listings sells virtual staging to real-estate agents through Google Ads and referrals. It sells credit packs at $128–750, moved from a productised-service agency to SaaS in October 2025, and shows **r30 $30.9k**. It is listed at $495k.
- FF Group runs a US truck-dispatch back office with Meta Ads and referrals at a 5–8% commission (r30 $43k, 26–50 staff). It is a service and close to ledger exclusions.
- Attivita24 is an Italian SMB-for-sale marketplace using Google and Meta Ads with €34–149 listings (r30 $13k, solo, asking $800k).

All three are service, one-off or low-ticket models.

---

## 3. Replicable patterns (synthesis) [Hypothesis on causality]

1. **Sell revenue to people who sell.** About 70% of the named software winners at $100+ sell pipeline, meaning booked calls, leads, rankings or funnels, to coaches, agencies, B2B sales teams or Shopify brands. The buyer reads price against revenue, which is why $300–1,000 is tolerated.
2. **Demo-gated, fixed monthly pricing in place of self-serve tiers** (ai-dm-setter, Sbl Elite at $997, Maverick at $250–2,300). High ticket co-occurs with **LinkedIn, cold outreach and partner channels**, not with Product Hunt or SEO alone.
3. **A local-language version of a US-proven category.** France is over-represented again (8 of 54: ai-dm-setter, Dynalis, Coucou, The Engine, Mentionable, plus 3 stealth). The French winners replicate US categories in French with French-language selling.
4. **Productised service as a bridge to software.** Refined Listings, RankAI, Dynalis and White Glove Content charge a service-level price with software doing most of the delivery. Caveat: Phase 10 F's "agency in disguise" warning applies to at least 7 of 28 $300+ winners.
5. **Price-wedge entry against an enterprise incumbent in a vertical.** AppBird sells at $199–399 against Sensor Tower-class tools. Glossa charges $2–5 per hour against interpreters and Wordly. Audn charges $999 a month against human pentests. The newcomer is cheaper and self-serve for the long tail the incumbent's sales team ignores.
6. **Small teams.** Of the 16 $100+ winners stating team size, 11 are 2–5 people and 4 are solo.
7. **Decay is common.** 12 of the 54 are down more than 15% quarter on quarter, and 8 are listed for sale. Consistent with Phase 8, the comparables are n = 1 survivors.

---

## 4. Gaps

Advertiser competition: **not checkable with public tools here.**
- Google Ads Transparency Center returned only an interface shell to WebFetch (domain=wordly.ai, 2026-10-13).
- Meta Ad Library requires JavaScript or a login.
- No published CPC was found for any of these keywords, so every CPC below is marked [Unknown]. Agent E's benchmarks should be substituted.

### G1. German-first AI DM setter for DACH coaches, consultants and course sellers
1. **Concept.** An AI that answers Instagram and WhatsApp DMs in the coach's own voice, in German. It qualifies the prospect, handles objections, follows up and books the sales call. It is a straight geography transfer of ai-dm-setter.
2. **Customer.** Coaches, consultants and infoproduct sellers in DE/AT/CH who sell €2–10k programmes through DMs and Meta lead ads.
3. **Model.** Demo-sold fixed monthly fee of €390–790. The template is about $715 per subscription.
4. **Spending evidence.**
   - ai-dm-setter: $20,735 MRR, 29 subscriptions, 0 followers, team 2–5. Monthly revenue went from $15.3k (Mar 2026) to $23.3k (Sep 2026) [Verified].
   - Human DM setters cost $2–4k a month, against $50–149 for AI setters [Secondary: creatorflow.so via search snippet].
5. **Competitors.**
   - SetSmart: $99–990 a month; languages EN/FR/ES/IT/PT, **no German listed** [Secondary: AlternativeTo via snippet]. Its TrustMRR page shows $0 (Whop-billed, so not visible) [Verified: trustmrr.com/startup/setsmart.md].
   - Setter AI (TrySetter); GenDM; ManyChat for rule-based flows.
   - **No German-first setter surfaced** (search P10-D #1; the US engine is weak for German, so absence is not proven).
6. **Entry strategy.** German-native tone and objection libraries, DSGVO/EU hosting, and integrations with tools DACH coaches use (Calendly, iClosed, GoHighLevel, Copecart/Digistore24 checkout). The French template's moats (EU hosting, Meta partner status, demo selling) are all reproducible by a follower.
7. **Acquisition.**
   - Meta Ads to coaches.
   - Revenue-share partnerships with DACH "Coaching-Business" mentors and programmes whose students all need setters. This is the influencer/partnership channel the template declares.
   - Newcomer evidence: only the French template [Verified]. CAC [Unknown]. CPC for "KI Setter" or "Appointment Setter" German keywords [Unknown].
8. **Operations.**
   - Under $2k to build a prototype on Meta's official Instagram Messaging and WhatsApp Business APIs. App review is required, and Meta messaging rules restrict automated sends outside the 24-hour window.
   - It needs a German-speaking demo seller (contractor or partner), so the founder is not fluent enough to sell it alone.
   - Operable from Israel.
9. **Labour.** Onboarding involves voice cloning from past DMs and is semi-manual at first. Demos are labour until a partner sells.
10. **Unit economics under copying [Hypothesis].**
    - €590 × 30 accounts ≈ €17.7k MRR. LLM and API costs are about 5%, leaving roughly €12–14k owner profit after a seller's commission.
    - Coaching churn is about 5–7% a month [Secondary vendor benchmark, P6 search log], so customer life is about 15 months and gross LTV about €8–9k.
    - With 3 followers bidding on the same Meta audiences and partner slots, partners would demand 30–40% revenue share. CAC could double and still pay back within 3 months. **The economics survive copying; win probability falls.**
    - Track A, with a route to B.
11. **Risks.**
    - English and French tools add German, and SetSmart lists 5 languages already.
    - Meta revokes messaging permissions or changes policy.
    - The coaching market is cyclical and reputation-sensitive.
    - Partner dependence.
    - **Decisive assumption:** DACH coaches pay €400+ a month for a German-language AI setter, and a German partner channel exists.
12. **Cheapest test (describe only).**
    - Spend €800 on Meta Ads to DACH coaches, driving to a German landing page with demo booking.
    - Offer a concierge pilot: an AI draft plus human approval.
    - **Kill if** there are fewer than 8 demo bookings from €800, or no paid pilot at €390+ a month from the first 10 demos within 6 weeks.

### G2. Self-serve AI live translation for small US public bodies (towns, school boards, special districts)
1. **Concept.** Glossa-style real-time speech translation, with captions on attendees' phones and the livestream, adapted for public meetings. It adds Title VI/LEP-plan reporting, a public transcript archive in each language, and integration with meeting-video systems (YouTube, Zoom, Granicus/Swagit) [Hypothesis on integrations].
2. **Customer.** US municipalities under about 100k population, school boards and special districts that cannot afford Wordly-sized contracts. Clerks and superintendents are the buyers.
3. **Model.** $300–600 a month (about $3.6–7.2k a year, under many local purchase-card and micro-purchase thresholds [Hypothesis; thresholds vary by state]). Hours are bundled.
4. **Spending evidence.**
   - Mountain View: **$43,750 Wordly contract for 300 hours** (about $146 per hour), $58,367 in total including equipment. Pilot launched August–September 2026 [Verified: mv-voice.com, 2026-09-09].
   - San Jose: about $82k for a year of Wordly, against a $400k interpreter budget [Secondary: localnewsmatters.org via snippet].
   - Wordly's base government package is 120 hours a year, and it claims "hundreds of local governments" [Verified: wordly.ai/city-council-translation, 2026-10-13].
   - Districts must provide language access under Title VI/EEOA, and Minnesota requires district language-access plans [Secondary: vendor blogs and a news snippet].
   - **Newcomer template:** Glossa (founded 2025-06, 105 followers) sells $99 for 25 hours, **$299 for 100 hours** and $499 for 250 hours. It reached $14.2k MRR and r30 $33.5k, up 38% quarter on quarter, and says "hundreds of churches". It does **not** target government [Verified: glossa.live; TrustMRR].
5. **Competitors.**
   - Wordly: dominant, quote-based, about $146 per hour in the Mountain View contract.
   - spf.io: lists Government and Education, quote-only [Verified: spf.io, 2026-10-13].
   - Boostlingo and interpreter agencies (schools).
   - KUDO and Interprefy.
   - Disliked: price and quote friction [Hypothesis]. Accuracy limits in less common languages are reported [Secondary: Austin MN news snippet].
6. **Entry strategy.** A roughly 10× price wedge with published prices and a card-payable monthly plan. Ship the compliance artefacts clerks need (LEP usage logs, multilingual minutes), with a human-interpreter fallback through a partner for sensitive items. Glossa or Wordly could follow down-market quickly, so the edge is focus and packaging, not technology.
7. **Acquisition.**
   - Google Ads on "city council meeting translation" and "school board meeting interpretation". Wordly runs a dedicated city-council landing page, which suggests intent traffic exists [Inference]. CPC [Unknown].
   - Partnerships with meeting-video and agenda vendors, and state municipal-league and school-board-association vendor programmes.
   - Outbound to clerks, whose public LEP plans and agendas are a free list source.
   - Newcomer evidence for government: **none**. Phase 9 measured public-sector newcomers at a median of $19.7k a year, with 43% at $0 on Texas DIR, so expect slow cycles.
8. **Operations.**
   - Under $2k for speech-to-text, MT and TTS APIs. Gross margin is high at about $0.3–1 per hour of compute [Hypothesis].
   - Some buyers need a VPAT or accessibility statement, and possibly SOC 2 (Wordly has it).
   - Selling to US local government from Israel is feasible (a US LLC helps) but adds friction.
9. **Labour.** Software-delivered. Onboarding means connecting the AV audio feed. Support load is meeting-night timed, US evenings, which is Israeli night.
10. **Unit economics under copying [Hypothesis].**
    - 40 bodies × $450 = $18k MRR, about $15k owner profit.
    - Churn is low once adopted, but procurement takes 2–6 months.
    - With 3 followers, the Google CPC for a niche government keyword rises, yet total intent volume is small. The real constraint becomes association and partner slots, and Glossa or Wordly cutting price. Margins survive; growth slows.
    - Track A, with B only if school districts (about 13k in the US) convert.
11. **Risks.**
    - Wordly launches a small-government self-serve tier.
    - Accuracy liability at public hearings.
    - Procurement slowness.
    - The approach is US-evening-heavy.
    - **Decisive assumption:** small public bodies buy at $300–600 a month on a card or purchase order within 60 days, without an RFP.
12. **Cheapest test.**
    - Build a list of 200 municipalities and school boards with published LEP plans or recent interpreter line items in agendas.
    - Send outbound email plus $400 of Google Ads on the two phrases above.
    - Offer a 30-day free pilot on one meeting series.
    - **Kill if** there are fewer than 5 pilots from 200 contacts plus ads, or fewer than 2 paid conversions at $300+ a month within 90 days of the pilots ending.

### G3. UK registered-charge signals for commercial and asset-finance brokers (the LeadX/UCC pattern, transferred)
This is materially different from the P6 exclusions ("new-licensee lead lists") and P8 ("country-specific owner lead data"): the data is company-level and comes from public charge registrations, there are no personal mobile numbers, and the buyers are lenders and brokers.

1. **Concept.**
   - A daily feed of new and satisfied charges from Companies House: debentures, chattel mortgages, invoice-finance charges.
   - It is enriched with the lender name, accounts headroom and director tenure, and scored for refinancing propensity.
   - Signals: "lender X just satisfied; refinance window"; "new debenture from a high-cost lender".
2. **Customer.** UK commercial-finance, asset-finance and invoice-finance brokers, and small lenders.
3. **Model.** £250–750 a month per seat or region.
4. **Spending evidence.**
   - LeadX (US, founded 2023, 312 followers): GTM data including **UCC filings** for business lending and equipment finance. $24.0k MRR from 15 subscriptions (about $1,599 each). Revenue went from $29.2k in Q2 to $73.3k in Q3 2026 [Verified].
   - UK spending on this exact product: [Unknown].
5. **Competitors.**
   - The data is free from Companies House.
   - It is already resold or monitored by an Apify "UK company charges lookup" actor, pagecrawl.io Companies House alerts, and ltds.uk, which pitches asset and invoice-finance brokers explicitly [Secondary: search P10-D #5].
   - Credit-data incumbents (Creditsafe, Red Flag Alert, Endole) carry charges data [Secondary: general knowledge; not fetched].
6. **Entry strategy.** Vertical scoring and broker workflow, not raw data. This is weak against a follower, because anyone can ingest the same free stream.
7. **Acquisition.** LinkedIn outbound to brokers, which matches the high-ticket channel pattern. A partner or sponsor slot with the NACFB-type broker associations [Hypothesis; terms unchecked]. Newcomer evidence: LeadX only (US). CAC [Unknown].
8. **Operations.** Under $1k using the Companies House API and streaming. The data is public, so UK GDPR is low for company data, and director data needs care. Operable from Israel.
9. **Labour.** Software.
10. **Unit economics under copying [Hypothesis].** 25 × £400 ≈ £10k MRR. Because the data cost is zero, followers can undercut to £50, making price erosion likely. Track A at best.
11. **Risks.**
    - Weak defensibility.
    - The UK broker market is small (about 1–2k firms [Unknown]).
    - Incumbents add the alert.
    - **Decisive assumption:** brokers pay £250+ for charge-derived signals they could approximate free.
12. **Cheapest test.** Run a prototype feed for one region for 2 weeks, then message 60 brokers on LinkedIn with 5 free signals each. **Kill if** fewer than 3 commit to £250+ a month.

### G4. Spanish/Portuguese AI DM setter for the LatAm and Iberian infoproduct ecosystem (weaker variant of G1)
- **Same product as G1.** The channel is different: Hotmart, Kiwify and Eduzz producer ecosystems, plus launch agencies as resellers. This is a tool for producers, not an infoproduct, which distinguishes it from the P6 "Brazil infoproducts" exclusion.
- **Weakness.** SetSmart already lists ES and PT [Secondary], and LatAm willingness to pay is likely below €300 a month [Hypothesis]. It therefore probably fails the $300+ threshold.
- **Test.** As G1, with a $500 Meta test in Spain and Mexico. **Kill if** fewer than 8 demos or no pilot at $250+.
- Not recommended unless G1 works first.

### Killed during this phase
- **AppBird-pattern Roblox / UGC game intelligence.** Rotrends Pro (Super League, July 2025), RTrack (bought by Gamebeast, January 2026), RoLearn at $19–49 a month, RoWatcher, BloxMetrics and Dive already exist [Secondary: search P10-D #2].
- **Aila-pattern AI file assistant for Australian mortgage brokers.** Quickli (used by 14,000 AU brokers) launched AI Fact Find on 22 September 2026, and Waboom sells an NZ$500/month voice agent [Secondary: search P10-D #4].
- **Backlinker / AI-visibility / AI-SDR clones.** Horizontal and crowded. Templates are flat or for sale (Backlinker −12%, Pipelime −52%, ChatDash −14%).
- **Virtual staging outside the US (Refined Listings pattern).** Low ticket and crowded globally.

---

## 5. Ranking and decisive assumptions

| Rank | Gap | Why | Decisive unverified assumption |
|---|---|---|---|
| 1 | **G2 Small-public-body AI meeting translation** | Verified public spending ($43,750 for 300 hours), a ~10× price wedge, a verified audience-free newcomer template (Glossa) in an adjacent buyer segment, software-delivered | Small bodies buy at $300–600/month without an RFP within about 60 days |
| 2 | **G1 German AI DM setter** | Closest dataset template (the only replicable strict-set winner); no German-first competitor surfaced | A German partner or Meta channel yields €400+/month buyers; founder can staff German demos |
| 3 | G3 UK charge signals for finance brokers | LeadX growth; free data | Brokers pay £250+ for signals derivable from free data |
| 4 | G4 ES/PT setter | Same as G1 | Willingness to pay ≥ $250 |

**For the Research Director.**
- At high ticket, the TrustMRR data does **not** show paid ads as the winning channel.
- Use **about 10% (not about 50%) as the prior** that a $300+ launch reaches $3k MRR.
- Expect demo-led and outbound or partner selling.
- Treat about a third of "high-ticket winners" as services.

WebSearch count: **6/6**. Sources:
- trustmrr.com/startup/{ai-dm-setter, backlinker-ai, private-enterprise-35, private-venture-50, defined-chase, captureflow, glossa-live, aila, appbird, leadx, plutocracy, refined-listings, setsmart}.md (local sample plus 1 live fetch), all 2026-10-13
- mv-voice.com (2026-09-09)
- wordly.ai/city-council-translation
- glossa.live
- spf.io
