# Phase 8 — Discovery Agent D (niche software / digital / technical)
## Dataset: TrustMRR verified-revenue profiles, mined for 2024–2026 entrants

Date: 2026-10-13. WebSearch used: **6 of 6** (P8-D lines in search-log.txt). WebFetch: about 8 primary pages. Bulk data came from TrustMRR's public `/startup/<slug>.md` pages (robots.txt allows them; the site advertises them for AI agents; limit is 60 requests per minute and we ran at about 45 per minute). The orchestrator stopped the crawl at 7,866 of about 11,500 sitemap slugs. The slugs were shuffled with a fixed seed, so **the data is a random sample of about 69% of TrustMRR**. Scripts and raw data are in the scratchpad at `p6plus/P8-D/{scripts,data}`. No browser, login, contact or personal identifiers were used; the User-Agent was a generic `research-bot`.

---

## 0. Bottom line

1. **Base rate.** Of 5,965 sampled startups whose self-entered founding date is 2024–2026:
   - 3.9% have verified MRR of $3k or more.
   - 7.4% have $1k or more, and 1.6% have $10k or more.
   - For the 2024 cohort (more time to grow), the shares are 8.0% at $3k+ and 14.5% at $1k+.
   - Listing is self-selected: founders who list are proud of their numbers or want to sell. Treat these as **upper bounds** for a random newcomer.
2. **Most winners have no audience.** 82% of young $3k+ winners have founders with fewer than 2,000 X followers. Audience still triples the odds: the hit rate is 3.5% under 2k followers and 11.2% at 10k or more.
3. **What the audience-free winners share (lift = hit rate ÷ base rate):**
   - **Price:** monthly revenue per subscription of $100–300 gives 2.9× and $300+ gives 5.1×. Under $10 gives 0.37×.
   - **Team:** 2–5 people gives 4.4×; solo gives 0.8×.
   - **Model and buyer:** sales/lead-gen tools 1.7×, B2B 1.4×, and built on top of a dominant platform (Shopify, LinkedIn, Upwork, eBay, Google, Planity) 1.4×.
   - **Location:** US-based 2.0×; India 0.06×.
   - **Declared channels:** paid or partner channels (TikTok Ads 6.3×, influencers 5.0×, Meta Ads 4.3×, affiliate 3.7×, partnerships 3.1×) beat indie-maker channels (Product Hunt 0.14×, Hacker News 0×, Reddit 0.39×, X 0.40×, SEO 0.66×). Causation probably runs both ways: winners can afford ads and affiliates.
4. **The Conductor pattern is rare in this data.**
   - Dev tools and APIs underperform (2.2% hit rate, 0.63×).
   - No young "legacy accounting/ERP integration API" reached $1k MRR. Conductor (founded 2022) is unique in the sample.
   - The nearest young analogue is **SoldComps**, an eBay sold-prices API built on HTML parsing. It went from $347 to $19,984 per month (Apr–Sep 2026) with a founder showing 0 followers. That is a "restricted official API → cheap self-serve data API" case, which already sits under ledger M2 (see section 5).
5. **Three opportunities proposed (D1–D3)** apply the over-represented traits: B2B, $50–150 per month, built on a closed platform, sold through partners or affiliates. All are hypotheses with a named decisive assumption. None is strong enough to displace M1 on evidence. D1 (review-and-rebook add-on for salons on Fresha/Booksy, modelled on a verified French Planity add-on) is the best fit.

---

## 1. Method and caveats

- **Population.**
  - TrustMRR startup sitemap: 11,550 URLs. Parsed: 7,883 profiles (3 returned 404).
  - Fields used: founding date (self-entered), current MRR, active subscriptions, last-30-day and all-time revenue, payment provider, founder X followers, B2B/B2C, markets, team size, pricing text, declared marketing channels, for-sale status and country.
- **Young:** founding date between 2024-01-01 and 2026-12-31 (n = 5,965).
  - 1,298 profiles (16%) have **no founding date**. Mostly these are RevenueCat-connected mobile apps, and they are excluded.
  - Founding dates are self-entered and sometimes wrong. Example: coldcaller.pro says "founded 2026-04" but shows verified revenue from January 2026. Some "2024-01-01" entries have six-figure lifetime revenue that suggests an older business.
- **Glitch filter:** 84 rows were removed where MRR > 0 with all-time revenue of $0, or MRR above all-time revenue. Example: a "mobileapp" row showing $703k MRR and $0 lifetime.
- **Win definition:** current verified MRR of $3k or more.
  - MRR counts subscriptions only. One-time and credit businesses are under-counted, so last-30-day revenue of $3k+ is reported alongside.
  - Revenue processed outside the connected provider is invisible. Some sellers note revenue on Whop.
- **"Audience-free"** means the founder's X followers shown on the profile are under 2,000.
  - "0" usually means an anonymous or stealth listing, or no X handle connected. It does not prove the founder has no audience: a founder can have a YouTube or newsletter audience, or a company account.
  - TrustMRR shows no other audience measure.
- **Model classification** uses a keyword classifier for the base-rate tables (approximate). The named audience-free B2B winners (n = 72) were classified by hand.
- **Selection bias.**
  - TrustMRR is also an acquisition marketplace run by a creator with a large audience. Profiles listed for sale have a higher hit rate (5.7% vs 3.0%).
  - Stealth listings ("Stealth Company") hit 24%: owners anonymise mainly when the numbers are worth selling.
  - Founders who never connect Stripe are absent. The true base rate for all 2024–26 software launches is certainly lower.

---

## 2. Base rates (69% random sample) [Verified: trustmrr.com/startup/*.md, fetched 2026-10-13]

| Population | n | MRR > 0 | MRR ≥ $1k | MRR ≥ $3k | MRR ≥ $10k | Last-30-day revenue ≥ $3k |
|---|---|---|---|---|---|---|
| All profiles | 7,883 | 40.5% | 9.2% | 5.3% | 2.3% | 7.6% |
| Founded 2024–26 | 5,965 | 37.4% | 7.4% | **3.9%** | 1.6% | 5.9% |
| founded 2024 | 551 | 51.0% | 14.5% | **8.0%** | 3.8% | 13.2% |
| founded 2025 | 2,027 | 43.7% | 10.1% | 5.6% | 2.5% | 7.4% |
| founded 2026 | 3,385 | 31.4% | 4.5% | 2.1% | 0.7% | 3.8% |
| No founding date | 1,298 | 46.8% | 9.7% | 5.5% | 2.1% | 7.5% |

- Scaled to the full site, roughly 330 startups founded 2024–26 show $3k+ MRR, against about 8,600 young listings. The 2026 cohort is 57% of young listings, so the platform is dominated by very recent, mostly pre-revenue launches.
- Secondary cross-check [Secondary: bigideasdb.com, a paid TrustMRR analytics product, via search snippet]: of revenue-positive startups, 17.6% are at $1k–10k and 4.9% at $10k–50k. That is consistent with our figures.

**By founder X followers (young, glitch-filtered, n = 5,879):**

| Followers | n | ≥ $1k | ≥ $3k | Hit rate (≥ $3k) | Share of all winners |
|---|---|---|---|---|---|
| 0 (anonymous or none) | 1,792 | 150 | 77 | 4.3% | 34% |
| 1–1,999 | 3,494 | 208 | 110 | 3.1% | 48% |
| 2k–10k | 371 | 39 | 20 | 5.4% | 9% |
| 10k+ | 151 | 29 | 17 | **11.3%** | 7% |

Audience roughly triples the odds, but 82% of winners are audience-free because that group is 90% of entrants.

---

## 3. Traits of audience-free winners (founded 2024–26, under 2k followers, n = 5,357, 190 winners at $3k+, base rate 3.5%)

| Trait | Group (n) | Hit rate | Lift |
|---|---|---|---|
| **Monthly revenue per subscription** (MRR ÷ subs; only startups with MRR > 0, base 10.0%) | <$10 (813) | 3.7% | 0.37 |
| | $10–30 (645) | 8.4% | 0.84 |
| | $30–100 (322) | 19.6% | 1.96 |
| | $100–300 (79) | 29.1% | 2.92 |
| | **$300+ (39)** | **51.3%** | **5.14** |
| **Team size (declared)** | 1 person (852) | 2.8% | 0.79 |
| | **2–5 people (162)** | **15.4%** | **4.35** |
| **Buyer** | B2C (1,898) | 3.1% | 0.88 |
| | B2B (1,173) | 4.9% | 1.37 |
| **Model (keyword classifier)** | dev tool / API (940) | **2.2%** | **0.63** |
| | AI consumer/prosumer tool (1,106) | 3.2% | 0.89 |
| | consumer mobile app (774) | 5.8% | 1.64 |
| | AI B2B tool (289) | 5.2% | 1.46 |
| | **sales / lead-gen tool (324)** | **6.2%** | **1.74** |
| | marketplace/directory (92) | 5.4% | 1.53 |
| **Built for a named dominant platform** (Shopify, LinkedIn, Upwork, eBay, Google Ads/Maps/Reviews, App Store, SketchUp, Slack …) | yes (1,225) vs no (4,132) | 5.1% vs 3.1% | 1.43 vs 0.87 |
| **Country** | US (1,057) | 7.0% | 1.97 |
| | FR (425) | 4.7% | 1.33 |
| | GB (382) | 3.1% | 0.89 |
| | IN (439) | 0.2% | 0.06 |
| **Payment provider** (proxy for founder type) | Stripe 4.2% · RevenueCat 5.9% · Superwall 15.1% · Polar 0.5% · Dodo 0.0% · Lemon Squeezy 0.9% | | |

- The revenue-per-subscription effect is partly mechanical: fewer customers are needed to reach $3k. But it also says winners charge business prices. Among startups with any revenue, half of those charging $300+ per subscription reach $3k MRR, against under 4% of those under $10.
- The near-zero rates for Polar, Dodo and Creem show that the indie-maker merchant-of-record crowd, mostly selling to other makers, rarely wins.

**Declared marketing channels** (the 1,551 audience-free young startups that list channels; base 4.2%):

| Channel | n | Hit rate | Lift | Channel | n | Hit rate | Lift |
|---|---|---|---|---|---|---|---|
| TikTok Ads | 19 | 26.3% | 6.3 | SEO | 908 | 2.8% | 0.66 |
| Influencers | 48 | 20.8% | 5.0 | Blog | 446 | 2.9% | 0.70 |
| Meta Ads | 73 | 17.8% | 4.3 | App store optimisation | 220 | 2.7% | 0.65 |
| Affiliate | 72 | 15.3% | 3.7 | X / Twitter | 595 | 1.7% | 0.40 |
| Partnerships | 46 | 13.0% | 3.1 | Reddit | 365 | 1.6% | 0.39 |
| Email marketing | 101 | 9.9% | 2.4 | Product Hunt | 165 | **0.6%** | 0.14 |
| Cold calling | 31 | 9.7% | 2.3 | Hacker News | 51 | **0%** | 0 |
| YouTube / Facebook | ~200 each | ~7.7% | ~1.8 | Cold email | 141 | 5.0% | 1.2 |

[Verified data; causal reading is Hypothesis.] Channel fields are founder-declared, and winners can afford paid and affiliate channels after they win. Still, the "launch on PH/HN/X/Reddit + SEO" playbook that dominates indie-maker advice is the *worst*-performing set here. This is consistent with Phase 5's newcomer findings and with Conductor's 4 Product Hunt upvotes. (This hands Agent E a TrustMRR-side measurement.)

**Hand classification of the 72 named, audience-free, B2B/"Both" winners at $3k+ MRR:**

| Model | Count | Examples (MRR, revenue per subscription per month, followers) |
|---|---|---|
| Marketing/growth tools for SMBs and agencies (ads, local SEO, AI visibility, funnels, reviews, AI creative) | ~28 | Adspirer $54.7k ($73, 182); NotFair $12.2k ($116, 142); Local SEO Bot $11.6k ($139, 14); MyFrank $9.9k ($56, 0); Coucou (Planity reviews) $5.9k ($118, 299); Funneled/Plutocracy $18.0k ($858, 131) |
| Sales / lead-gen / outbound | ~15 | traxy.ai $51.0k ($217); LeadShark $19.6k; Lancer (Upwork) $18.4k ($159, 87); Yadulink $8.3k; Maverick $6.5k ($242, 0); coldcaller.pro $3.1k MRR but ~$18.6k revenue/month (credits) |
| Data / scraping / API infrastructure | ~8 | LLM Gateway $78.8k; SoldComps $21.6k ($39, 0); AutoContent API $17.0k; PostPeer $4.6k; Social Fetch $3.1k |
| Builders / dev / no-code | ~8 | Sleek $20.9k; AppAlchemy $5.6k; UXMagic $6.3k |
| Vertical tools for one profession | ~7 | JourneyFuse (travel advisors) $8.6k ($19/seat, 0); Archifruits (architects) $5.1k; VendPlacer (vending operators) $3.2k MRR / ~$11k revenue/month; DownConvert (SketchUp) $3.8k |
| Services-enabled / white-label | ~4 | Windmill $121k ($1,516); White Glove Content $72k; ChatDash $19.9k |
| **Integration API to a legacy/closed system** | **0** | (Conductor, 2022, is the only one in the whole sample) |

- About 20 of the 72 (28%) are complements to one dominant platform.
- Probable channels:
  - LinkedIn and Instagram tools: the platform itself, plus affiliates and creators.
  - Ad tools: Meta/Google ads and agency partners.
  - JourneyFuse: host-agency channel, Facebook group and "vs Travefy/TravelJoy/Tern" comparison pages [Verified: journeyfuse.com, 2026-10-13]. It claims 4,100+ advisors, yet verified MRR is $8.6k from 432 subscriptions, so the claims outrun the revenue.
  - Shopify Google Merchant Center scanner: declares affiliate, influencers and partnerships.

**Negative evidence (patterns that look attractive but fail on base rates):**

- **"Hosted version of the hype tool"** (OpenClaw hosting and skills): ~73 young entrants in an earlier 4.6k-row cut, none at $3k MRR (AuraClaw reached $4.8k in a month of one-time revenue).
- **Directory / launch-boilerplate tools sold to indie makers:** many entrants, few winners.
- **Accounting and legacy integrations:** among 2024–26 entrants (QuickBooks Online dunning, invoice parsing, brewery ERP), none reached $1k MRR.

---

## 4. Patterns over-represented among AUDIENCE-FREE winners (synthesis)

1. **Sell to a business that earns money from the outcome, at $50–$900 per month.** Lead-gen, reviews, ads and funnels are tools the buyer reads in revenue terms.
2. **Ride one dominant platform's installed base and its missing feature.** Examples: Upwork with no auto-proposal feature, Planity with no Google-review flow, eBay's restricted sold data, Shopify stores failing Google Merchant Center policy, LinkedIn lead magnets. The platform defines the customer list, the vocabulary customers search with, and the communities where they gather.
3. **Small team (2–5), not solo.** Solo profiles do worse than average.
4. **Distribution through partners, affiliates, creators or paid social, not launch sites.**
5. **US-based or a large non-English home market (France) with local-language focus.** France is over-represented: MyFrank, Coucou, coldcaller.pro, Yadulink, AI DM Setter, Dynalis.
6. **Developer-facing APIs are the *worst* model class on average.** The exceptions (Conductor, SoldComps, AutoContent API) remove a specific, painful restriction that developers already search for by name.

---

## 5. Note for the ledger (not a new opportunity)

- **M2 (licensed niche data API) evidence update.**
  - SoldComps: [Verified: trustmrr.com/startup/soldcomps.md and sold-comps.com, 2026-10-13]
    - $21,591 MRR, 545 subscriptions, plans at $0/$9/$29/$79.
    - Monthly revenue: $347 (Apr 2026), $968, $1,070, $4,337, $12,791, **$19,984 (Sep 2026)**.
    - Founder shows 0 followers, domain rating 10.
    - Data comes from parsing eBay's HTML in real time. The product is also listed on **Apify and RapidAPI**.
  - This is the strongest newcomer counter-example to Phase 5's "median new Apify Actor = 1 monthly user". It shows the outlier tail exists when the dataset is one that a large reseller population needs and the official API restricts.
  - It does not make M2 better for a newcomer: ToS and scraping risk is real, and the slot is taken.
- **M1 (Sage 50 API).** TrustMRR offers no second young instance of the Conductor pattern; dev tools and APIs underperform overall (lift 0.63). This neither kills nor supports M1. It means M1 rests on Conductor alone.

---

## 6. Opportunities

### D1. Review-and-rebook autopilot for salons on Fresha and Booksy (UK/US/AU)

1. **Concept.** An add-on that turns each completed appointment on a booking platform with no Google-review flow into a timed Google-review request (SMS/WhatsApp/email). It adds per-stylist attribution and a lapsed-client rebooking nudge. This is a straight transfer of the verified French Coucou model (Planity salons) to English-speaking markets and different platforms.
2. **Customer.** Independent hair, beauty, barber and nail salons and small clinics with 1–10 chairs that use Fresha or Booksy. Geography: UK, US, AU, IE.
3. **Model.** Monthly SaaS, **$49–99 per location**. This sits in the 20–29% hit-rate band. Coucou charges €67/€97 [Verified: TrustMRR pricing text].
4. **Spending evidence:**
   - Coucou: **$5,909 MRR, 50 subscriptions (about $118 each), 299 followers**. Monthly revenue grew from $1,617 (Nov 2025) to $5,836 (Sep 2026) [Verified: trustmrr.com/startup/startup-a8e78dd113c0.md].
   - MyFrank (Google reviews by employee, France): **$9,857 MRR, 175 subscriptions, 0 followers**. Monthly revenue grew from $1,437 (Feb 2026) to $10,299 (Sep 2026). It claims "300+ entreprises" [Verified: TrustMRR; myfrank.io, 2026-10-13].
   - Reviewflowz charges **$70–80 per location per month** for a Vagaro-checkout review flow. Vagaro charges $10 per month for API access [Verified: reviewflowz.com/for/vagaro, 2026-10-13].
5. **Competitors.**
   - Podium and Birdeye: expensive, generic.
   - Reviewflowz: Vagaro and Booker only on that page.
   - Fresha's own marketplace reviews keep reviews on Fresha. A comparison says Vagaro's reviews stay on Vagaro [Secondary: search snippet].
   - No Fresha- or Booksy-specific Google-review add-on surfaced in one search. That is not proof of absence.
   - Customers dislike generic review tools for price and setup friction [Hypothesis].
6. **Entry strategy.** Be the add-on built specifically for Fresha/Booksy: one click, priced per salon, per-stylist leaderboards (MyFrank's hook) and rebooking.
7. **Acquisition.**
   - Salon-owner Facebook groups and salon-educator/influencer affiliates. Influencers and affiliates are the top-lift channels in section 3.
   - "Fresha Google reviews" intent searches.
   - Partnerships with salon business coaches.
   - Newcomer outcome evidence: Coucou and MyFrank, both audience-free, reached $5.9k and $9.9k MRR within about 12–18 months [Verified]. Their channels are not disclosed. CAC [Unknown].
8. **Capital and operations.**
   - Under $2k: SMS costs are passed through or prepaid.
   - **Technical blocker:** Fresha has **no merchant API, no webhooks, only a read-only BI "Data Connector"** [Vendor claim: supergood.ai API report card, 2026-10-13]. Triggers would come from that connector, from parsing confirmation emails, or from calendar sync. Booksy's API status is [Unknown].
   - SMS consent rules apply (UK PECR, US TCPA/A2P registration).
   - Can be run from Israel.
9. **Labour.** Mostly software. Onboarding can be self-serve once triggers work. Support for salons is light.
10. **Economics [Hypothesis].** $69 per month × 100 salons = $6.9k MRR, about $5.5k owner profit after SMS and tools. This needs about 100 salons, comparable to MyFrank's 175. Track A fits; Track B only with multi-platform expansion.
11. **Risks.**
    - No reliable trigger without an API, and Fresha may ship native Google-review prompts.
    - Google policy forbids incentivised or "review-gated" requests, so per-stylist reward mechanics must avoid incentives.
    - Crowded generic review-tool market.
    - **Decisive assumption:** a durable, ToS-compliant way exists to detect completed Fresha/Booksy appointments (Data Connector or email parse) for salons that don't use Vagaro. Test: read Fresha's Data Connector documentation and the Booksy partner terms.

### D2. Continuous Google Merchant Center policy monitor for WooCommerce and Google-Shopping agencies

1. **Concept.**
   - A crawler plus feed checker that continuously scans stores for the causes of Merchant Center "misrepresentation" and policy suspensions: missing identity or returns pages, price and feed mismatches, shipping inconsistencies, checkout and schema problems.
   - It alerts before Google does and produces a fix list and appeal checklist.
   - It transfers a verified Shopify-focused winner to WooCommerce and to agencies with many client stores.
2. **Customer.** WooCommerce merchants running Google Shopping or Performance Max (US/UK/EU), and PPC/Shopping agencies managing 10–100 stores.
3. **Model.** $29–49 per store per month; agency plan $199–499 per month.
4. **Spending evidence:**
   - Anonymous "scan your Shopify shop for Google Merchant Center compliance issues": **$14,721 MRR, 244 subscriptions (about $60 each), 0 followers**. Monthly revenue went from $5,430 (Nov 2025) to $14,504 (Sep 2026). Declared channels are affiliate, influencers and partnerships. Listed for sale at $175k [Verified: trustmrr.com/startup/hidden-business-8.md].
   - GMCSuspension.com sells a **$99 one-time audit** and claims 2,400 audits [Vendor claim, press release snippet].
5. **Competitors.**
   - AdNabu free 22-check scanner.
   - ShieldKit Shopify app (free, 0 reviews).
   - GMCSuspension $99.
   - Feed managers (Feedonomics, WebAppick).
   - The hidden Shopify leader.
   - No WooCommerce-specific monitor surfaced [search P8-D #2].
   - The free checkers are one-off scans with no monitoring [Secondary].
6. **Entry strategy.** WooCommerce-first, continuous monitoring with change alerts, and a multi-store agency dashboard. The free tools are one-shot, and the leader appears Shopify-only.
7. **Acquisition.**
   - WooCommerce and Google-Ads agency partnerships and affiliates (the leader's declared channels).
   - Intent searches for "merchant center suspended misrepresentation WooCommerce" from panicked merchants.
   - Phase 5 showed WooCommerce marketplace newcomers get 0 reviews, so **do not rely on the WooCommerce directory**.
   - Newcomer evidence: only the Shopify leader. CAC [Unknown].
8. **Capital and operations.** Under $2k. A crawler plus feed parsing, no inventory. Fine from Israel. Google's policy pages are public. No platform permission is needed beyond the store owner's consent.
9. **Labour.** Software. Appeal help could become service creep, so keep it as a checklist.
10. **Economics [Hypothesis].** 150 stores × $39 plus 5 agencies × $299 ≈ $7.3k MRR, about $6k owner profit. Track A; Track B is unlikely since the niche is narrow.
11. **Risks.**
    - Most suspensions have causes a crawler can't see (business verification, product claims).
    - Free tools anchor the price at $0.
    - Google could improve its own diagnostics.
    - **Decisive assumption:** WooCommerce merchants pay a *recurring* fee for monitoring, rather than a one-off $0–99 scan, at a rate near the Shopify leader's (244 subscriptions). Unverified; the leader may be selling mainly to dropshippers via influencers.

### D3. Self-serve integration API for closed SMB booking platforms (Fresha first)

1. **Concept.** A documented REST/webhook API, priced per connected business, that gives third-party developers access to appointment and client events on a booking platform with no public API. It is the "missing API" pattern applied to a *cloud* platform. It is materially different from M1 (Sage 50 desktop): different system, buyers and mechanism, using the merchant's own authorised session or Data Connector rather than a desktop SDK.
2. **Customer.** Developers of salon and spa add-ons (marketing, reviews, payroll/commission, BI, AI receptionists), plus multi-location salon groups. Geography: UK, AU, US, EU.
3. **Model.** $29–49 per connected location per month, Conductor-style.
4. **Spending evidence:**
   - **Indirect only.** Conductor: $42k MRR at $49 per company file [Verified, Phase 7].
   - Supergood sells unofficial API layers and gives Fresha an "F": no API, no webhooks, no developer program [Vendor claim, 2026-10-13]. A funded vendor targeting this gap is a weak demand signal.
   - Reviewflowz builds only on platforms that have APIs (Vagaro). This suggests add-on developers avoid closed platforms, a latent need.
   - No paying customer for Fresha data access is verified [Unknown].
5. **Competitors.**
   - Supergood: generic unofficial APIs, enterprise-oriented, pricing not shown.
   - Fresha's own Data Connector (read-only, BI).
   - No dedicated Fresha API startup surfaced.
6. **Entry strategy.** A narrow, documented, transparently priced API for one platform, discoverable by developers searching "Fresha API". Conductor's playbook: intent search and docs SEO, not launch sites.
7. **Acquisition.** Developer search and docs; comparison pages; pairing with D1 as the first internal customer. Evidence that this channel works for newcomers: Conductor and SoldComps (RapidAPI/Apify listings) only. CAC [Unknown].
8. **Capital and operations.**
   - Under $2k.
   - **Platform/ToS risk is the main issue.** Using merchant credentials to automate a SaaS dashboard may breach Fresha's terms, and access can be cut without notice.
   - Fine from Israel.
9. **Labour.** Maintenance against UI and endpoint changes is continuous.
10. **Economics [Hypothesis].** Developer customers × locations. 200 locations × $39 ≈ $7.8k MRR. Track A–B only if extended to Booksy, Planity and Treatwell.
11. **Risks.**
    - Fresha blocks the access or launches its own API.
    - Too few developers build for salons.
    - Legal exposure.
    - **Decisive assumption:** Fresha's terms permit merchant-authorised third-party access (or its Data Connector exposes enough near-real-time events) **and** at least about 10 developer teams want it. Check Fresha's terms and the Data Connector documentation before anything else.

**Ranked lower and not developed (pattern fits, evidence or entry weak):**

- **Upwork-style proposal automation for another lead marketplace.**
  - Lancer: $18.4k MRR, $159 per subscription, 87 followers. Monthly revenue $7.9k (Nov 2025) to $26.7k (Sep 2026); listed at $700k [Verified].
  - The Thumbtack analogue is already served by Thumbtack Front Desk, SwiftReplAI ($29–197), SignpostAI and Hatch (Partner API) [search P8-D #3]. No credible entry. Killed.
- **Country-specific owner-level SMB lead data** (coldcaller.pro model: ~$18.6k revenue per month by Sep 2026, 1 person, word of mouth).
  - Strong newcomer signal, but GDPR/ePrivacy risk on owners' mobile numbers.
  - It needs local-language selling, and it is close to the ledger exclusion "new-licensee lead lists". Not pursued.
- **File-version downgrade converters** (DownConvert for SketchUp: $3,754 MRR verified, though the seller's own text says "$475 MRR"; 22k users; asking price $17.9k).
  - ArchiCAD offers free official converters. A true Revit downgrade is not possible (only a lossy IFC route) [search P8-D #6]. Killed.
- **Vending / side-hustle operator tools** (VendPlacer: ~$11k revenue per month within 4 months, 0 followers).
  - Its site shows ~22,876 "locations" at ~115 per city, which looks seeded. Possible refund and reputation risk. Pattern noted, not pursued.
- **Hosted OpenClaw and hype-tool wrappers:** many entrants, near-zero $3k winners. Killed.
- **Generic AI-ads/SEO agents** (Adspirer, NotFair, Local SEO Bot): real winners, but crowded and undifferentiated for this founder. Not pursued.

---

## 7. Ranking, decisive assumptions, search count

| Rank | Idea | Why | Decisive unverified assumption |
|---|---|---|---|
| 1 | **D1 Fresha/Booksy review-and-rebook add-on** | Two verified audience-free French analogues ($5.9k, $9.9k MRR); B2B, ~$70 per month, platform-complement, partner channel | A durable, ToS-compliant trigger for completed appointments without a public API |
| 2 | **D2 WooCommerce/agency Merchant Center monitor** | Verified Shopify analogue at $14.7k MRR with affiliate/partner channel; no WooCommerce monitor found | Merchants pay recurring fees for monitoring, not a free or one-off scan |
| 3 | D3 Fresha (closed booking platform) integration API | Conductor pattern on a large cloud SMB platform; vendor-reported "no API" | Fresha ToS and Data Connector allow it, and enough developers want it |

- **Top for deep diligence:** D1 (with D3 as its technical sub-question) and D2.
- **Recommended cheapest next checks (desk only):**
  1. Fresha Data Connector documentation, plus Fresha and Booksy terms on third-party access.
  2. Count Fresha/Booksy-specific review add-ons in each platform's app or integration directory.
  3. Look for any WooCommerce Merchant Center monitor in WordPress.org plugin search, including active-install counts for newcomer outcomes.

**Key takeaway for the Research Director:** the TrustMRR population says the audience-free route that works is **B2B, $50–900 per month, built on a dominant platform's gap, sold through partners, affiliates, creators or paid social, often by 2–5 people**. It is not "launch on Product Hunt" or "build a developer API". Conductor-type integration APIs are rare even among winners, so M1 should be judged on its own evidence, not as a proven class.

WebSearch count: **6/6** (P8-D). Main sources: trustmrr.com/startup/*.md (7,883 profiles; key slugs: soldcomps, startup-a8e78dd113c0, myfrank, hidden-business-8, lancer-app, coldcallerpro, journeyfuse, vendplacer, digital-natives-services-fz-llc, plutocracy, conductor), sold-comps.com, journeyfuse.com, myfrank.io, vendplacer.com, reviewflowz.com/for/vagaro, supergood.ai/api-report-card/fresha. All fetched 2026-10-13.
