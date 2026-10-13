# Phase 8 — Discovery Agent C (Traditional, offline and service businesses)
Method: reverse-engineer young, profitable, NON-content businesses from Empire Flippers (EF) and Flippa listings. Date: 2026-10-13. WebSearch used: 5 of 6 (P8-C).

## 0. Data and caveats (read first)
- **EF public API**, full pull of `api.empireflippers.com/api/v1/listings/list` (29 pages, 2,878 listings: 2,679 Sold, 175 For Sale, 24 Pending Sold; listings from 2014 to Oct 2026) [Verified: API, 2026-10-13]. Age at listing = `first_listed_at` − `first_made_money_at`. Fields used: monetizations, niches, monthly net profit/revenue, `hours_worked_per_week`, `customer_type`, summary text.
- **What "verified" means.** EF says it vets the P&L and traffic before listing. That is broker due diligence, not an audit, and the P&L is still the seller's. I label these figures **[Verified-EF: listing #, API 2026-10-13]**, meaning "EF-vetted and seller-reported". Three listing pages were opened (#86244, #87450, #94286). Their totals match the API (for example #86244: $103,416 net profit on $535,281 revenue, a 19% margin, i.e. 12-month totals) [Verified: empireflippers.com/listing/86244/, 87450/, 94286/, 2026-10-13].
- **Data-quality issues.**
  - `first_made_money_at` is sometimes reset when a site was bought and relisted. Example: #83542 says "launched 2018" but shows 2025.
  - Owner-hours fields sometimes contradict the summary. Example: #87450 has 4 h/week in the text and 20 h in the field.
- **Flippa.** The `api.flippa.com/v3` listings API needs authorisation (HTTP 401), so I did not use it. The public search page `flippa.com/search?filter[property_type][]=service` is server-rendered and shows 370 open "Service" listings. From 8 pages I parsed the 112 cards that show both monthly profit and age [Verified: flippa.com search pages, 2026-10-13]. These figures are seller-presented. Flippa's "Data Verified" badge means connected data sources, not a vetted P&L, so I label them [Anecdote/vendor claim].
- **Survivorship bias is severe.**
  - EF only lists businesses with roughly 12+ months of profit, and in practice a profit floor. For 2023+ listings, the 5th percentile is $1,761/month and the 10th percentile is $2,104/month.
  - So "share of young EF listings with ≥$2k/month" measures EF's intake filter, not newcomer success.
  - Neither marketplace shows the denominator: businesses that never reached a sale. The informative numbers are therefore (a) the composition of young winners (which models appear at all), and (b) what the winners have in common.

## 1. Base rates

### EF, all years (2,878 listings)
| Group | Listings | Young (≤3 y at listing) | Young with ≥$2k/mo | Median young profit |
|---|---|---|---|---|
| Non-content (any Service/Agency/Lead Gen/SaaS/Subscription/Info/Digital/App/Other) | 405 | 156 | 112 (72%) | $3,753 |
| E-commerce/FBA | 1,020 | 510 | 422 (83%) | $4,995 |
| Content (ads/affiliate/KDP/YouTube) | 1,453 | 999 | 446 (45%) | $1,719 |

The "Non-content" row includes mixed sites, for example display-ad sites with a minor "Other" stream.

"Pure" non-content means at least one non-content monetisation and no display, affiliate, Amazon Associates, KDP or YouTube revenue. There are 202 such listings, 85 of them young, and 61 of those young (72%) show ≥$2k/month.

| Model (pure set) | Listings | Young | Young ≥$2k | Young ≥$5k | Median owner h/wk (young) |
|---|---|---|---|---|---|
| Service | 50 | 24 | 18 | 11 | 7.5 |
| Agency | 17 | 3 | 3 | 2 | 5 |
| Lead Gen | 12 | 5 | 2 | 1 | 1 |
| SaaS | 57 | 19 | 11 | 7 | 4 |
| Subscription | 47 | 21 | 18 | 12 | 5 |
| Info Product | 17 | 8 | 7 | 4 | 5 |
| Digital Product | 32 | 9 | 8 | 5 | 5 |
| Application | 17 | 7 | 5 | 4 | 2 |

### The base rate that matters: services barely show up among young winners
- Since 2023, 750 listings were added to EF. 268 were young, and 250 of those showed ≥$2k/month.
- Of those 268 young listings, 134 were e-commerce, 108 content, **11 service/agency/lead-gen**, 9 SaaS/app/subscription and 6 info/digital.
- Since 2025, 151 listings were young, of which **6 were service/agency/lead-gen**.

Young service businesses that reach the sale stage on EF are therefore rare, about 4% of young listings. Two possible reasons:
1. Founder-dependent services are hard to transfer.
2. EF's buyers prefer passive assets.

This dataset cannot tell those apart from "services rarely succeed".

**Owner hours.** Young winners (≥$2k/month) report median owner hours of 5/week for non-content (57% at ≤5 h), 5 for e-commerce and 3 for content. Low owner hours are a sale-readiness feature. Sellers usually reach them through **contractor teams**, not automation (details in §2).

**Lead gen has decayed.**
- Pure lead-gen sites appear in EF's young set mainly in the 2017–2022 cohorts. Examples: #58407, UK transport leads, $11.0k/month, 1 h/week; #48335, US medical emergency contacts, $10.1k/month.
- No pure lead-gen listing in the young 2023+ cohort reached ≥$2k/month. The one 2023+ young lead-gen listing (#71069, pet travel insurance, Bing-targeted) made $1.9k/month.
- This is consistent with Google-update damage that one seller notes (#78058).

### Flippa open "Service" listings (seller-presented)
- 112 parsed listings; 39 are ≤3 years old, and 20 of those claim ≥$2k/month. The median young claim is $2,080/month.
- 73 are older; 33 of those claim ≥$2k/month.
- Young claims include implausible outliers, for example "events business, 1 year, $300k/month profit" and a "prop-firm" at $33k/month. I give Flippa no evidential weight beyond showing that the same archetypes appear:
  - productised B2B content (an AE B2B SaaS long-form content firm, $7.8k/month, brokered);
  - an Australian workplace-wellbeing/EAP provider ($7.0k/month, about 15 h/week, 95% organic/referral);
  - a tenant-advocacy service (CA, $11.6k/month);
  - many sub-$1k local lead-gen and local service sites (a Minneapolis handyman lead site at $46/month profit; Sydney curtain cleaning at $585/month).

  These lower-end local listings support the view that local lead-gen sites rarely reach Track A.

## 2. Profiles of young non-content winners (EF-vetted P&L unless noted)
Each row shows profit/month, owner hours, staff and acquisition channel.

| # | Start → listed | What it is | Customer | Profit/mo (rev) | Owner h/wk | Delivery staff | Acquisition (from listing) |
|---|---|---|---|---|---|---|---|
| 87450 | Apr 2023 → Sep 2025, Sold | Google & Meta ads agency for **med spas** and outdoor e-com brands; ~$1,100/client/mo, 7–8-month engagements | SMB B2B, US | $14.2k ($31.2k) | 4 (field says 20) | 8 specialists; SOPs in Notion; GoHighLevel CRM | **Outbound prospecting + paid ads + referrals**, 4–5 new clients/mo |
| 86244 | Nov 2023 (est. Jul 2022) → Jul 2025, Sold | **Outsourced human guest-support desk for short-term-rental managers**, monthly subscription, human team 365 days plus custom platform/AI; French-language | Independent hosts, concierge agencies, property managers; mainly France | $8.6k ($44.6k; 19% margin) | ≤5 | 16–19 freelancers | **Ads + referrals**, ~10 new customers/mo, ~130 active, churn <10%/mo |
| 59835 | Sep 2020 → Mar 2022, Sold | Productised social-media marketing service behind a client dashboard (Monday.com back end, manual delivery) | 21 business clients, US | $15.5k ($32.4k) | 2 | 12 contractors with 2-step QA | Mostly direct; CAC ~$490, LTV ~$11.5k |
| 62149 | Jan 2021 → Jul 2022, Sold | SEO service for bloggers/agencies/SMBs | B2B, global | $12.4k ($26.8k) | 10 | 35 freelancers | Direct/organic/social |
| 71155 | Nov 2020 → Aug 2023, Sold | Software plus consulting for realtors | Realtors, Canada | $13.7k ($27.8k) | 20 | n/a | Direct 46%, paid 26% |
| 78971 / 85227 | Aug 2023 → Aug 2024 (relisted May 2025), Sold | **Email-blast service to 43k realtors** (listing announcements); founded by realtors | Realtors/brokerages, Canada | $7.4k → **$4.0k** (−44% trend at relist) | 15 | Owner alone | Own list; footer self-promotion; "no marketing spend" |
| 65067 | Dec 2019 → Dec 2022, Sold | Subscription "business services" for financial professionals (Kajabi) | 22 financial pros, US | $7.3k ($13.3k) | 8 | Team | Direct 78% |
| 94608 | Mar 2025 → Jul 2026, For Sale | **AI-assisted Italian editorial/thesis/translation production with human QC** | Mostly B2B: 4 reseller agencies plus direct clients; Italy/UK | $5.6k ($6.2k) | 2 | Small | Content marketplace + agency referrals, 1–2 new clients/mo |
| 92659 | May 2024 → Mar 2026, For Sale | LinkedIn-style prospecting software plus support for **financial advisors** (pivoted from SaaS to "agency") | Advisors, US | $4.8k ($8.3k) | 5 | Owner | n/a |
| 91893 | Dec 2023 → Feb 2026, Sold | Real-estate guest-post (paid link) site | 750 unique clients in 2025, 413 repeat | $3.4k | 10 | Owner | Organic search for "real estate guest post" |
| 70621 | Sep 2021 → Aug 2023, Sold | Per-job writing service for business exposure | SMBs, US | $3.6k ($5.3k) | 2 | VA | Organic search 68% |
| **94286** | **May 2024 → May 2026, For Sale** | **Study materials (PDF, ebook, printed workbooks) for specialised healthcare certification tracks** | 30,000+ buyers, AOV ~$130 | **$36.1k ($174.9k; 12-mo $433k on $2.10M)** | 10 | 1 support agent, 2 video editors | **Facebook Ads**, plus Google Ads and Klaviyo |
| 94124 | Jun 2023 → May 2026, For Sale | Accredited lifestyle-medicine CME academy for physicians, cohort launches timed to accreditation cycles | Hungarian doctors | $14.3k ($24.3k) | 10 | Contractors | n/a (credential-driven) |
| 94091 | Jul 2023 → May 2026, Pending Sold | Medical-German language app for health workers moving to Germany; 3,700 paid subscribers, +319/mo | Foreign health professionals | $9.1k ($15.6k) | 5 | Shared studio team | Meta ads plus organic; blended CAC ~$8 |
| 60428 | Aug 2020 → Apr 2022, Sold | Shopify ↔ specific payment-processor **sync app**, 640 users | Merchants | $3.2k | 2 | Developer once a year | Organic/app store |
| 87595 | Sep 2023 → Jan 2026, Sold | **High-ticket dropship of a niche electronic equipment line** (AOV ~$3,000, 29% margin); Chinese factory ships and gives tech support | B2B and B2C, US | $1.7k ($6.0k) | 1 | None | Organic SEO only |
| 91071 | Apr 2023 → Jan 2026, Pending Sold | Amazon FBA networking cables | **B2B**, US | $26.2k ($147.7k) | 6 | n/a | Amazon organic ranking |
| 86851 | Sep 2022 → Aug 2025, For Sale | Supplement brand; a third of revenue from 4 distributors | B2B and B2C | $5.2k | 10–15 | Owner | Organic + distributors |

### Patterns (what the young non-content winners share)
1. **Contractor pool behind a productised front end.** All of the high-hour-leverage services (59835, 62149, 86244, 87450, 48370) sell a fixed-scope monthly deliverable. Freelancer teams of 8–35 deliver it, with QA steps, SOPs and a dashboard or CRM. The owner sells and manages, often for ≤5 h/week. Margins run 19–55%. Profit scales with contractors, not founder hours. This is the delegation route the founder wants, but it is still a **labour business**, and margins are thin at the low end (86244 makes 19%).
2. **One fragmented B2B vertical with a recurring operational pain.** Examples: STR managers' guest messages, med spas' ad accounts, realtors' listing promotion, financial advisors' prospecting. Customers are small operators who already pay monthly for software (Guesty/Smoobu, GoHighLevel). Sales happen through **outbound plus a little paid plus referrals**, at 4–10 new clients per month. None of the service winners relied on a marketplace.
3. **Local-language wedge.** 86244 is French-first, 94608 Italian-first, 94124 Hungarian, 94091 is German for migrants. Non-English service businesses do reach the EF sale stage. The language narrows competition and the delivery uses local-language freelancers.
4. **Credential-gate learning products sold on paid social with no personal brand.** 94286, 94124 and 94091 are the three largest young non-content winners after the agencies. All sell to people who need a credential for work (certification, CME points, a language exam for licensure). They acquire through Meta/Google ads, not an audience. 94286 is the single strongest young non-content P&L in the set: $433k profit in 12 months, about 2 years after launch, on 10 owner-hours a week.
5. **Owning a B2B audience as the product.** The realtor email-blast service (78971) and the real-estate guest-post site (91893) sell visibility to a professional vertical. Both depend on a pre-built list or a ranked domain. The realtor service's profit fell 44% between its two listings.
6. **Integration utility (60428).** This corroborates the Phase 7 Conductor pattern at small scale ($3.2k/month, 2 h/week). It is already covered by M1 and the ledger's Shopify/Wix-app exclusions, so I add nothing new here.
7. **Lead gen and paid-link sites belong to an earlier era.** Strong lead-gen cases started in 2017–2020. The young 2023+ examples are small and Google-dependent.

## 3. What an audience-free, Israel-based, technical solo founder (~$2k) can replicate
- **Replicable:** patterns 1+2 (productised vertical service, contractor delivery, outbound acquisition), 3 (language wedge) and 4 (credential products via paid social). None of these needs an audience. All need either sales effort (1–3) or ad-testing budget (4).
- **Not replicable on $2k:** pattern 5 (needs an existing list or domain), and FBA/B2B inventory plays (91071 required inventory capital).
- **Where the founder's technical edge counts:** the back end that makes contractor delivery cheap. That means a PMS/CRM integration, triage, AI-drafted replies with human approval, and QA dashboards. This is how 59835 ("could be automated with investment") and 86244 ("custom platform and AI") describe their upside. The edge improves margin. It does not solve acquisition.

## 4. Opportunities

### C1. Human-plus-AI guest-messaging desk for short-term-rental managers in one non-French EU language market (German first; alternatives Dutch, Italian or Spanish)
1. **Concept.** A fixed monthly "we answer every guest message 24/7 in your PMS, in your voice" service. AI drafts the replies, a human approves each one, and the desk escalates to the manager per an SOP. It replicates EF #86244 (French) in a different language market.
2. **Customer and geography.** Independent hosts with 5–50 units, concierge/co-host agencies and small property managers in DACH (Germany, Austria, Switzerland). These are Smoobu, Guesty and Hostaway users.
3. **Model and price.** Monthly subscription per active listing. Price [Hypothesis]: about €15–30 per listing per month, or about €250–600 per client. Benchmark: 86244 earns about $343 revenue per customer per month ($44.6k ÷ ~130) [Verified-EF #86244].
4. **Spending evidence.**
   - 86244: about 130 paying customers, ~10 new per month, churn <10%/month, $535k revenue over 12 months [Verified: empireflippers.com/listing/86244/, 2026-10-13].
   - Guesty sells its own "Guest Communication Services™" ("around-the-clock guest communications … dedicated team") as an add-on on every plan, with 25% off in its top bundle [Verified: guesty.com/pricing, 2026-10-13]. A PMS selling it shows managers pay for human messaging.
5. **Competitors.**
   - Guesty's add-on, for Guesty users only, price unpublished.
   - Generic VA firms such as Stealth Agents, at $1,600/month for a dedicated VA [Secondary: search snippet, unverified].
   - Upwork and Fiverr 24/7 guest-support gigs at about $100–200 per 30 days [Secondary: search snippet].
   - Automation-only software: Smoobu, your.rentals, Host Tools at ~$10/listing, HostAI from $12 [Secondary: search snippets].
   - A German-language search surfaced only software, not a German human desk [P8-C search 5]. That absence of results does not show an absence of competitors.
   - Likely dislikes [Hypothesis]: freelancers are unreliable at night; AI-only replies cause bad reviews.
6. **Entry strategy.** A language plus PMS-integration wedge. Offer German-native replies, integrate with Smoobu (a German PMS) and Guesty, and price per listing below a dedicated VA. Use Israel's time zone (UTC+2/3) to cover European evenings and nights with an Israel-plus-Philippines shift split [Hypothesis].
7. **Acquisition.**
   - Outbound to German STR managers. They are publicly listed on Airbnb/Booking as "professional host" accounts and in co-host directories [Hypothesis].
   - Paid search on "Gästekommunikation auslagern".
   - Referrals: 86244 grew through "advertisements and referrals" [Verified-EF].
   - No newcomer channel data exists. CAC is [Unknown].
8. **Capital and operations.**
   - Under $2k to start: PMS sandbox/API access, a website, a few German-speaking freelancers on trial.
   - Fully remote, so it works from Israel. PMS API terms need checking [Unknown].
   - GDPR: the desk processes guest data and needs a data-processing agreement.
9. **Labour.** Revenue scales with freelancer shifts, not founder hours. The AI-drafting tool raises messages handled per agent hour. The founder's time goes to sales and QA.
10. **Unit economics [Hypothesis].**
    - At 40 clients × €400 = €16k revenue, contractor coverage of €8–10k and tools of €1k leave €4–6k owner profit (Track A).
    - 86244's 19% margin at $44k revenue is a sober anchor: about $8.6k/month on 130 clients.
    - Track B would need about 300+ clients or multiple languages.
11. **Risks.**
    - PMS vendors bundle AI messaging (Guesty already sells the human service).
    - Night-shift reliability.
    - A single bad guest outcome can cost a client.
    - Thin margins.
    - It is a services business, which is Track C.

### C2. Credential study kits (printed workbook plus PDF plus question bank) for one mid-sized healthcare or trade certification, sold on Meta ads without a personal brand
**Ledger note.** Phase 2 excluded "licensure exam-prep apps" and Phase 4 excluded Hebrew/Arabic psychometric prep. This proposal is materially different on all three counts:
- channel: paid social to a physical/PDF bundle, not app stores;
- product: a printed workbook with ~$130 AOV, not an app subscription;
- segment: US/UK allied-health or trade credentials.

It follows the strongest young non-content P&L in the dataset.

1. **Concept.** Pick one certification with tens of thousands of candidates a year and a 60–75% pass rate. Build an AI-assisted, SME-reviewed workbook plus PDF plus practice-exam bundle, printed on demand. Sell through Meta/Google ads and email.
2. **Customer.** Career-changers and healthcare workers sitting a credential exam, US first. Example: PTCB administered **49,253** pharmacy-technician exams in 2025, with a 69% CPhT pass rate [Verified: ptcb.org/history/credentials-by-the-numbers, 2026-10-13]. That market is crowded. Smaller tracks such as sterile processing (CRCST) or other HSPA/NHA credentials are candidates; volumes are [Unknown].
3. **Model.** One-off bundle at $60–130. Upsell question-bank access.
4. **Spending evidence.**
   - EF #94286: about $2.10M revenue and $433k profit in 12 months, 30,000+ buyers, AOV ~$130, Facebook Ads-led, first revenue May 2024 [Verified: empireflippers.com/listing/94286/, 2026-10-13; seller P&L, EF-vetted].
   - #94091 (Medical German app): 3,700 subscribers, CAC ~$8 [Verified-EF].
   - #94124 (Hungarian CME): $14.3k/month [Verified-EF].
5. **Competitors.** Mometrix, Kaplan-type publishers, Amazon study guides, certifier-sold materials and free Quizlet decks. Specific complaints are [Unknown]. #94286's niche is undisclosed and may be the very certification I would pick.
6. **Entry strategy.** Pick a credential where the top Amazon guides are thin, outdated or poorly reviewed. Update to the current exam outline within weeks of each outline change; certifiers publish content outlines. The real question is whether there is a credible gap; checking it needs a review-recency check per certification before committing.
7. **Acquisition.** Meta ads to job-title and interest audiences, plus Google search on "[cert] study guide". The evidence is that #94286 and #94091 acquire profitably via paid social. Newcomer CAC is [Unknown], and the decisive test is about $1,000 of ad spend.
8. **Capital and operations.**
   - $2k covers content production (AI plus a paid SME reviewer at about $500–1,000) and $1k of ad tests.
   - Print-on-demand fulfilment (Lulu or Amazon KDP print for the workbook) means no inventory.
   - Runs fine from Israel.
   - Certifier trademark and fair-use rules apply: no "official" claims, and no use of real exam items.
9. **Labour.** Low after creation. Revisions happen once per exam-outline cycle, and paid ads are outsourceable.
10. **Unit economics [Hypothesis].**
    - $90 AOV − $8 print/ship − $35 CAC − $5 fees ≈ $40 contribution.
    - 100 sales/month ≈ $4k owner profit (Track A).
    - #94286 shows the Track B ceiling, with ad-buying skill.
11. **Risks.**
    - CAC above contribution margin is the killer.
    - Meta policy on health-adjacent ads.
    - Exam-outline changes.
    - Incumbent price pressure.
    - It may duplicate #94286's niche.

### C3. Single-vertical paid-ads or booking agency with productised delivery (pattern 87450) — Track C, service-first
1. **Concept.** Google/Meta lead-gen management for one appointment-driven vertical. Charge a retainer of ~$1,000/month plus performance on booked consults. Deliver through a contractor team on GoHighLevel-style SOPs.
2. **Customer.** US med spas, aesthetic clinics or a similar vertical with high lifetime value per patient.
3. **Model.** $800–1,500/month retainer [Verified-EF #87450: ~$1,100/client/month, 7–8-month tenure].
4. **Spending evidence.** #87450 went from launch in April 2023 to $170k profit on $375k revenue over 12 months, adding 4–5 clients a month [Verified: empireflippers.com/listing/87450/, 2026-10-13].
5. **Competitors.** Hundreds of med-spa marketing agencies [Hypothesis; not measured]. A common complaint is lock-in contracts with poor lead quality [Hypothesis].
6. **Entry strategy.** Weak. Possible angles are a pay-per-booked-consult guarantee and better tracking/attribution tooling, which suits the founder. Otherwise **none credible beyond execution**.
7. **Acquisition.** Outbound (cold email, LinkedIn) plus referrals, as 87450 did. Newcomer outcomes are [Unknown].
8. **Capital and operations.** Low capital. Healthcare ad-policy constraints apply. Can be run from Israel, but US-hours sales calls are needed.
9. **Labour.** Delegable to contractors after about 10 clients (87450 has 8 specialists, and the owner reports 4–20 h/week). Founder sales time is the bottleneck early on.
10. **Unit economics [Hypothesis].** At 10 clients × $1,100 = $11k revenue, contractors at 45% leave about $5k owner profit (Track A). Track B is shown possible by 87450.
11. **Risks.** Ledger proximity to the "generic AI agency" exclusion; this differs because it is a single-vertical ads service, not AI. Also client churn, a commoditised offer, and the founder's lack of ad-buying track record.

### C4. Factory-direct, high-ticket B2B equipment storefront for non-US markets (pattern 87595/91071)
1. **Concept.** An SEO-led branded storefront for one class of specialised equipment with AOV above $1,500. The Chinese or Turkish factory ships directly and handles technical support. The store owns the content, specifications and quoting. Agent B covers e-commerce broadly; this is the B2B-buyer variant.
2. **Customer.** Small labs, workshops and clinics in the UK, EU or Australia. Candidate categories, all [Hypothesis]: ultrasonic cleaners, benchtop analysers, commercial kitchen modules.
3. **Model.** One-off orders at a 20–30% net margin [Verified-EF #87595: 29% margin, AOV ~$3,000].
4. **Spending evidence.**
   - #87595: $6.0k revenue and $1.7k profit per month, 1 h/week, organic SEO only.
   - #91071: B2B networking cables at $26k/month, but that is FBA with inventory [Verified-EF].
5. **Competitors.** Amazon Business, established distributors and Alibaba direct. Buyers dislike a lack of local support and returns [Hypothesis].
6. **Entry strategy.** Local-language specification content plus quote-based checkout in markets that US-centric drop-shippers ignore.
7. **Acquisition.** SEO, which is slow (months), and Google Shopping. No newcomer data exists.
8. **Capital and operations.**
   - No inventory; under $2k for the site and a sample.
   - Duties and VAT (EU IOSS does not apply above €150) and CE/UKCA conformity sit with the importer of record. This is a material compliance load [Hypothesis].
   - US tariffs on China make the US market unattractive [Unknown, current rates].
9. **Labour.** Low once ranked, as 87595 shows at 1 h/week.
10. **Unit economics.** $1.7k/month after about 2 years (87595) means Track A sits at the boundary. Track B is unlikely without paid acquisition.
11. **Risks.** Slow SEO, supplier quality, warranty liability, compliance, and low founder-fit novelty. Weakest of the four.

## 5. Killed or not proposed
- **Vertical email-blast or visibility services** (realtor blasts, pattern 78971). US incumbents already sell per-blast to agents from $25–35, about $10 per 1,000 agents, with county/radius targeting [Secondary: MondoFlyers search snippet]. The model needs an owned list, which the founder lacks; Canada's CASL and the EU's GDPR restrict building one by scraping. 85227 shows profit falling 44%.
- **Paid guest-post or link sites** (91893). This is against Google's spam policies and depends on owning a ranked domain.
- **Local lead-gen sites.** Ledger L6 and Hebrew lead-gen cover them; there are no strong 2023+ young cases on EF; Flippa young local lead sites are under $1k/month.
- **AI-assisted foreign-language editorial/translation** (94608). The ledger already covers certified translation, AI translation rights and German translate-and-launch.
- **Prospecting automation for financial advisors** (92659). LinkedIn automation breaches platform terms; it is a small, owner-run business.
- **Integration sync apps** (60428). Already covered by M1 and the Shopify/Wix-app exclusions.
- **Niche subscription data reports** (76134, 56700). Covered by M2, K13 and the digests exclusions.

## 6. Ranking, diligence targets, decisive assumptions
1. **C2 Credential study kits via paid social.** This has the strongest verified young P&L (#94286) and the most delegable model. Decisive unverified assumption: a newcomer can buy customers on Meta/Google for less than about 40% of AOV in a chosen certification where incumbent guides are weak. Check this with a review-recency audit of the top Amazon guides per candidate certification and the certification's exam volume.
2. **C1 STR guest-messaging desk, German market.** This is a near-exact replica of #86244 (130 customers, ~10 new a month, ads plus referrals), and the founder's integration skills lower delivery cost. Decisive unverified assumption: German-speaking STR managers with 5–50 units will pay about €20 per listing per month for a human-approved desk rather than Guesty's add-on or AI-only tools, and outbound can sign about 5 a month. Also check Smoobu/Guesty API terms for third-party messaging access.
3. **C3 Single-vertical ads agency.** It has a proven young P&L (#87450), but the entry wedge is weak and it is labour- and sales-heavy. Decisive unverified assumption: an audience-free newcomer can close 3–5 clinic retainers a month through outbound without a portfolio.
4. **C4 Factory-direct B2B equipment storefront.** Weakest: a small P&L, slow SEO and compliance load. Pass to Agent B's e-commerce work rather than pursue it here.

**Top 2–3 for deep diligence:** C2, C1, and optionally C3.

**Cross-cutting finding for the Director.** In EF data, young non-content winners are mainly contractor-delivered vertical services and credential-gate learning products acquired through paid social or outbound. None used a marketplace as the main channel. But young service businesses are only about 4% of EF's young listings, so the evidence base is thin (11 young service/agency/lead-gen listings since 2023). EF's intake filter means no true newcomer success rate can be computed from this data.

**WebSearch count: 5 of 6** (all logged as P8-C in search-log.txt). Primary pages fetched: EF API (29 pages), EF listings #86244, #87450 and #94286, Guesty pricing, PTCB numbers, and Flippa search pages. The Flippa API was blocked (401) and not bypassed.

Scripts/data: /private/tmp/claude-501/-Users-tomeryannay-Projects-agents/33458dff-96bb-4d90-98b6-5161ecb65c2e/scratchpad/p6plus/P8-C/{scripts,data}
