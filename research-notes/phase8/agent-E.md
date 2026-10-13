# Phase 8 — Agent E (Distribution-first): how audience-free newcomers got their first customers

Date: 2026-10-13. WebSearch used: **6 of 6** (all logged as P8-E). Everything else came from WebFetch, curl or public JSON.

## 0. Datasets and access (read this first)

| Source | Access | What I used |
|---|---|---|
| **Indie Hackers** product pages and interviews | **Blocked**: HTTP 403 to curl and WebFetch on /products, /interviews and posts | Nothing verified. One search snippet only (labelled Secondary) |
| **TrustMRR marketing-channel pages** (`/channels/<38 channels>`) | Public. Each page shows how many startups tagged that channel plus the top 30 by all-time verified revenue | 38 pages; 440 unique startups. Their public `/startup/<slug>.md` profiles give founded date, founder X followers, revenue verified through the payment provider, B2B/B2C and declared channels |
| **Starter Story** episode pages (full transcripts, public) | Public. The sitemap lists 3,302 stories | The 200 newest pages; 98 dated 2024–2026. About 40 single-product stories coded, ~30 summarised via WebFetch (self-reported) |
| Apple App Store (iTunes Search API) | Public | Cross-checks: CalBuddy, Khosmos, the Hebrew newcomer cohort, the French artisan-invoicing cohort, event photo apps |
| Product Hunt launch stats | Not fetched directly | Used TrustMRR's "Product Hunt" channel tag as a proxy |

Note on TrustMRR's llms.txt: it says full marketplace pagination needs the authenticated API. I stayed on the public page-1 channel lists and the public `.md` profiles that file points to. I did not paginate, log in or use an API key. Agent D is mining TrustMRR by population; I used only the channel dimension.

**Caveats that apply to every TrustMRR number below:**
- Channels are self-declared current tags, not "first-customer" channels. Most startups tag 4–15.
- "Founded" is self-declared.
- "X followers = 0" can mean the founder never linked X. My audience-free proxy (under 1,000 followers) therefore overstates how audience-free these founders are, for example where the founder has an Instagram following instead.
- Revenue figures are payment-provider verified. Last 30 days is written "30d".

## 1. Channel base rates (TrustMRR, verified revenue, accessed 2026-10-13)

**Rigorous base rate.** A startup's last-30-day revenue can never exceed its all-time revenue. So when the 30th startup on a channel page (ranked by all-time revenue) has under $2k all-time, the page is a complete list of every startup in that channel earning ≥$2k in the last 30 days. For the other channels the count is a lower bound.

| Channel (startups tagging it) | Startups with ≥$2k in last 30d | Share | Of which founded 2023+ and founder <1k X followers | Exact? |
|---|---|---|---|---|
| Hacker News (85) | 4 | **4.7%** | 3 (none ≥$50k all-time) | exact |
| Threads (146) | 10 | 6.8% | 5 | exact |
| Pinterest (69) | 7 | 10.1% | 4 | exact |
| Cold calling (53) | 9 | 17.0% | 8 | exact |
| Forums (34) | 6 | 17.6% | 4 | exact |
| Discord (97) | 18 | 18.6% | 12 | exact |
| LinkedIn Ads (28) | 6 | 21.4% | 4 | exact |
| Press/PR (28) | 7 | 25.0% | 5 | exact |
| TikTok Ads (56) | 19 | **33.9%** | 9 | exact |
| YouTube Ads (18) | 8 | 44% | 5 | exact |
| Product Hunt (285) | ≥14 | ~**4.9%** (#30 has only ~$6k all-time) | 9 | ≈exact |
| Reddit (637) | ≥20 | ≥3.1% | 15 | lower bound |
| TikTok organic (555) | ≥28 | ≥5.0% | 18 | lower bound |
| SEO (1,768) | ≥25 | ≥1.4% (#30 has $250k all-time, so far deeper) | 11 | lower bound |
| Google Ads (185) | ≥28 | ≥15% | 11 | lower bound |
| Meta Ads (166) | ≥28 | ≥17% | 13 | lower bound |
| Influencers (92) | ≥24 | ≥26% | 16 | lower bound |
| Affiliate (143) | ≥25 | ≥17.5% | 15 | lower bound |
| Partnerships (93) | ≥22 | ≥24% | 15 | lower bound |
| Cold email (260) | ≥23 | ≥8.8% | 16 | lower bound |
| Word of mouth (259) | ≥26 | ≥10% | 11 | lower bound |

**Depth of the strongest earners.** The 30th-best startup by all-time revenue in each channel:

| Channel | 30th-best all-time revenue |
|---|---|
| SEO | $250k |
| Content marketing | $161k |
| Blog | $110k |
| TikTok | $109k |
| Google Ads | $105k |
| Cold email | $20k |
| Reddit | $21k |
| Product Hunt | about $6k |
| Hacker News | $0 (its 10th-best is only about $1.9k) |

**Audience-free newcomer winners in the 440-startup sample.** 157 startups were founded 2023 or later and earned ≥$2k in the last 30 days. 116 of them had founders with under 1,000 X followers; 50 had 0. Their median 30-day revenue was **$9.0k**, the same as the audience-owning winners ($8.9k). B2B/B2C mix: B2B 42, B2C 37, both 18, unspecified 19.

29 of the 116 tag only one or two channels, so their channel can be credited. Their channel families:

| Channel family | Startups | Share |
|---|---|---|
| Organic short-form social (TikTok 6) | 10 | **34%** |
| Search: SEO 3, ASO 3, Google Ads 1, blog/content 2 | 8 | **28%** |
| Creators/affiliates | 5 | 17% |
| Outbound + LinkedIn | 5 | 17% |
| Word of mouth | 3 | 10% |
| Communities (Reddit, forums, Slack) | 3 | 10% |
| Paid social | 3 | 10% |

B2B single-channel winners cluster in SEO, LinkedIn, word of mouth and cold email. B2C winners cluster in TikTok, ASO and influencers.

**What the base rates say:**
1. **Launch sites and communities are weak as revenue channels for anyone.** Hacker News, Product Hunt and Threads convert about 5–7% of the startups that tag them into $2k/month earners, and their winners are small.
2. **Paid ads, creators, affiliates and partnerships have the highest hit rates (17–44%).** This is partly reverse causality: profitable products adopt paid channels. Paid as a FIRST channel is only evidenced by the self-reported cases in §2.
3. **SEO is crowded but has the deepest earners.** Among single-channel audience-free winners, search ties with TikTok as a credited channel.

## 2. Table: 38 verified or self-reported newcomer winners (launched 2023–2026, ≥$2k/month)

V = TrustMRR verified (`trustmrr.com/startup/<slug>.md`, accessed 2026-10-13). S = self-reported on Starter Story (episode date given; Anecdote). AF = founder had no meaningful audience.

| # | Product (slug) | Launch | Revenue | Founder audience | First / main channel | Price | B2B/C | Non-software |
|---|---|---|---|---|---|---|---|---|
| 1 | Alimentia Formación (startup-a66a92db7a72), ES | 2026-04 | V $37.5k/30d; $167.6k all-time in 6 months | AF (1 X follower) | SEO (city/region pages) + Google Ads | €12 per certificate, course free | B2C + B2B team links | Training/certification service |
| 2 | Event photo-sharing (photo-sharing), DE | 2024-04 | V $30.2k/30d; $549k all-time | AF (0) | Google Ads + SEO (+IG) | per event | B2C | — |
| 3 | Khosmos, FR | 2023-03 | V $24.1k/30d; MRR $21.8k; $365k all-time; 125 FR App Store ratings | AF (0) | SEO + ASO | €23.99/mo | B2B (artisans) | — |
| 4 | Stealth SMB voice agents (unnamed-company-21), US | 2024-01 | V $83.8k/30d; $776k all-time | AF (0) | **SEO only** | — | B2B | — |
| 5 | QR Code AI (qr-code-ai), FR | 2023-06 | V $17.8k/30d; $321k all-time | AF (297) | **SEO only** | freemium | B2B | — |
| 6 | Boothie, TR | 2026-06 | V $43.6k/30d; $140k in <4 months | AF (31) | **TikTok carousels from ~12 persona accounts (US/DE/TR); "no money, no paid ads"** | sub/IAP | B2C | — |
| 7 | Nutria (AI calories) | 2025-07 | V $82.6k/30d; $558k all-time | AF (0) | TikTok only | IAP | B2C | — |
| 8 | Depuff AI | 2025-06 | V $39.2k/30d; $919k all-time | AF (0) | TikTok only | IAP | B2C | — |
| 9 | anonymous-startup-95, ES | 2025-11 | V $40.7k/30d; $109k all-time | AF (0) | TikTok, "only organic growth" | IAP | B2C | — |
| 10 | TrackAI, PL | 2025-06 | V $21.4k/30d; $278k all-time | AF (89) | **Meta Ads only** | weekly/annual | B2C | — |
| 11 | Brawler (AI boxing) | 2026-05 | V $60.5k/30d; $142k all-time | AF (0) | Meta Ads + influencers | $9.99/mo | B2C | — |
| 12 | Photo AI Studio, CA | 2023-12 | V $3.7k/30d; $204k all-time | AF (223) | **Google Ads only** | credits | B2C | — |
| 13 | AppBird, US | 2026-03 | V $17.9k/30d; $141k all-time | AF (0) | **LinkedIn only** | $199–399/mo | B2B | — |
| 14 | coldcaller.pro, FR | 2026-04 | V $13.6k/30d; MRR $3.1k; $84.7k all-time | AF (49) | **Word of mouth only**, "100% community driven" | €19–99/mo | B2B | Data product |
| 15 | Deeplead, DE | 2026-02 | V $7.7k/30d; $56k all-time | AF (6) | Word of mouth + cold email | $37–297/mo | B2B | — |
| 16 | FiveML (LinkedIn automation), CY | 2025-04 | V $4.8k/30d; $103k all-time | AF (67) | LinkedIn + cold email | $149.99/user | B2B | — |
| 17 | UpLinked, NL | 2024-07 | V MRR $2.7k; $200k all-time | AF (0) | LinkedIn | $59/mo | B2B | — |
| 18 | Refined Listings, US | 2024-09 (SaaS) | V $30.9k/30d; $265k all-time (ex-agency) | AF (0) | Cold email + Google Ads + referral | credit packs $128–750 | B2B (realtors) | Agency origin |
| 19 | GMC compliance scanner (hidden-business-8), AE | 2025-03 | V $15.6k/30d; $123k all-time | AF (0) | Affiliates, partnerships, influencers | — | B2B (Shopify) | — |
| 20 | Social-comment moderator (confidential-startup-7), IT | 2025-01 | V $12.4k/30d; $177k all-time | AF (0) | Blog + affiliate | $29–249/mo | B2B | — |
| 21 | Rank Prompt, US | 2025-05 | V $48.7k/30d; $287k all-time | AF (37) | Blog, content, newsletter | tiers | B2B | — |
| 22 | Werewolf Undercover, FR | 2025-09 | V $7.8k/30d | AF (375) | **ASO only** | $3.99/wk | B2C | — |
| 23 | Swish AI, US | 2025-08 | V $5.0k/30d | AF (364) | **Influencers only** | $25/mo | B2C | — |
| 24 | Knoott (wedding gift registry), MX | 2025-03 | V $8.2k/30d | AF (75) | Blog, content, IG, Pinterest | 1% + fee | B2C | Marketplace |
| 25 | Altitude Cleaning Crew, US | 2025-05 | V $16.4k/30d; $277k all-time | AF (833) | Google Ads, Meta, SEO | per clean | B2C | **Local service** |
| 26 | FF Group (truck dispatch back-office), US | 2023-10 | V $43k/30d; $916k all-time | AF (42) | Cold calling, cold email, many more | % of loads | B2B | **Service** |
| 27 | Fast Corp (Bulgarian company formation), BG | 2025-07 | V $8.6k/30d; $56k all-time | AF (0) | Meta/Google Ads + partnerships | packages | B2B/C | **Service** |
| 28 | Go Tall (gotall) | 2025-07 | V $886k in 12 months, now $30.8k/30d. S "first sale after two days", ~$100k/mo peak | AF (0) | TikTok comment replies, then UGC, then paid | $35/yr, $5/wk | B2C | — |
| 29 | AppAlchemy | 2025-02 | S "$17k MRR" at 4 months with ~70 X followers (Jul 2025). V now $5.5k/30d, $244k all-time, listed at $27.5k | AF at launch | **Reddit only**; declined after the founder stopped posting | sub | B2C/prosumer | — |
| 30 | CalBuddy (Israel, Hebrew) | 2025-05 | S $1k first month, then $20k/mo at month 4 (paid ads), then "over 81K" (Aug 2026). **2,520 IL App Store ratings [Verified iTunes API]** | — | **Paid ads first**, then 50/50 rev-share with 2 influencers | sub | B2C | — |
| 31 | NaturalWrite | 2025 | S $100k in 90 days (41k/32k/27k) | AF | **One TikTok account**; "from the first video we got the first sale"; paid influencers gave "almost no conversions" | — | B2C | — |
| 32 | SaveWise | 2024 | S $25k/mo after 15 months | AF | PH/HN/IH traffic "none … stuck"; 300–400 influencer emails, 1 reply; **Facebook groups + Reddit** worked | lifetime | B2C | — |
| 33 | Setter AI | 2024-02 | S $10k MRR | AF | **One-keyword landing page ranking on Google + calendar link**; $500 paid before code | $50–5,000/mo | B2B | — |
| 34 | AngelMatch / InvestorHunt | ~2023 | S $29k MRR; InvestorHunt $2.8k "just SEO" | AF | Product Hunt (~$4k first month), then programmatic SEO (~half of revenue) | $59+/mo | B2B | Database |
| 35 | Harpagea (idle RPG) | ~2025 | S ~$13k/mo | "I had no audience" | First sale in days; one Reddit post took it from $1k to $10k/mo; $0 ads | $4.99–9.99 IAP | B2C | Game |
| 36 | Chart Detector AI | ~2025 | S $56k/mo | AF | **TikTok paid ads**, ~$18k/mo spend | $12.99/wk | B2C | — |
| 37 | Manifestation app | 2025-08 | S ~$30k/mo | AF | **~25 TikTok accounts** posting daily | $40/yr | B2C | — |
| 38 | Trades booking widget (AU) | ~2025 | S A$50–85k/mo | Had 70 agency clients | **Door-to-door with iPads**, then Google booking integration | — | B2B | — |

Also from Phase 7: **Conductor** (QuickBooks Desktop API). V $42k MRR, 4 Product Hunt upvotes; channel was developer search plus comparison pages.

**Time to traction (verified start dates vs all-time revenue):**

| Product | Time | All-time revenue |
|---|---|---|
| Boothie | under 4 months | $140k |
| Alimentia | 6 months | $168k |
| coldcaller.pro | 6 months | $85k |
| AppBird | 7 months | $141k |
| Deeplead | 8 months | $56k |
| Go Tall | 12 months | $886k |

Self-reported "first sale within days" appears for Go Tall, Harpagea and NaturalWrite.

**Durability warning.** Several winners decay fast:
- AppAlchemy fell from a claimed $17k MRR to $5.5k verified after the founder stopped posting on Reddit.
- Go Tall fell from about $100k/month to $30.8k/30d.
- Boothie, Go Tall, AppAlchemy and 1Lookup are all listed for sale.

Organic social and community channels are founder-labour channels. Revenue stops when posting stops.

## 3. Patterns worth copying (and ones not to)

1. **For audience-free B2C, the proven playbook is US-proven app category + persona-account TikTok (or paid TikTok/Meta) + weekly/annual subscription.** It is heavily supplied: Starter Story's 2025–26 episodes are mostly this playbook. On TrustMRR, TikTok-tagged startups reach $2k/30d at only ≥5%.
2. **For audience-free B2B and services, buyer-intent search works without an audience.** The examples are SEO-only and Google-Ads-only winners, Setter AI's one-keyword page and the Alimentia certificate funnel. Brief lesson 5 asked for "evidence that the channel produces purchases for comparable offers"; search has it in several categories.
3. **Local-language copies of proven US categories work when the founder is local:**
   - CalBuddy and Calcounti in Hebrew
   - Khosmos and coldcaller.pro in French
   - Alimentia in Spanish
   - Deeplead in German
4. **Winning niches flood within about 18 months.** A French App Store search for "devis facture artisan" returns **≥15 artisan quoting/invoicing apps released 2025–26 with 0–15 ratings each** (Artisyo 8, Rappidos 15, Donizo 7, Fabro 6, Billies 0, Batikko 0 …). Khosmos (2023) has 125. Copying a 2023 winner in 2026 means joining the flood. This matches lesson 1.

## 4. Opportunities (not in the ledger)

### E1. Pay-to-download food-hygiene certificate for German food workers and employers (Alimentia model, moved to Germany)

1. **Concept.** A free online course for the German food-hygiene training (Lebensmittelhygiene-Schulung under LMHV / EU 852/2004) plus the 2-yearly infection-protection follow-up briefing (IfSG §43 Folgebelehrung). The user pays only to download a QR-verifiable certificate. An employer dashboard tracks each employee's 2-year renewal.
2. **Paying customer.** German restaurant, café, bakery and food-retail employers (B2B team links) and individual job seekers (B2C). Austria is an optional second market.
3. **Model and price.** About €12–15 per certificate (B2C). €8–10 per employee in packs (B2B), recurring every 2 years for the Folgebelehrung.
4. **Spending evidence.**
   - The Spanish model is verified: Alimentia Formación earned $37,456 in the last 30 days and $167,590 since 2026-04-09 [Verified: trustmrr.com/startup/startup-a66a92db7a72.md, 2026-10-13]. Price €12; claims "+15.000 alumnos certificados"; offers company links and per-city pages [Verified: alimentiaformacion.com, 2026-10-13]. Revenue ÷ €12 implies roughly 2,500–3,000 certificates a month [derived].
   - The German obligation is real and open to third parties: the hygiene training "kann durch den Arbeitgeber selbst oder durch Dritte durchgeführt werden". The Folgebelehrung is due "alle zwei Jahre" and "kann vom Arbeitgeber oder einem Dritten durchgeführt werden" [Verified: frankfurt-main.ihk.de Pflichtschulungen, 2026-10-13]. Only the initial briefing (Erstbelehrung) must come from the Gesundheitsamt (~€30).
   - Austrian WKO employee course costs €55, or €120 for non-members [Secondary: P8-E search].
5. **Competitors.** IHK in-person sessions (IHK Bonn: March/October 2026) and providers listed by the IHK. No cheap pay-per-certificate German online player surfaced in one search [Unknown; absence not proven]. Spain's market has many sellers at €10–30 [Secondary: goveasy].
6. **Entry strategy.**
   - Price far below in-person IHK courses (€55–120 equivalents).
   - Instant QR certificate plus Wallet pass.
   - **Employer renewal tracking** for the 2-year cycle, which Alimentia does not need in Spain because Spain has no fixed renewal cycle.
   - Programmatic Bundesland/city pages.
7. **Acquisition.** Google Ads on "Hygieneschulung online", "Folgebelehrung online" and similar, plus programmatic SEO. Newcomer evidence: Alimentia went from zero to $37k/30d in about 6 months with the founder at 1 X follower. In the base-rate table Google Ads is ≥15% and among the best paid channels. German CPCs [Unknown].
8. **Capital, ops, legal.**
   - Under $2k to build and test.
   - Needs a German-qualified signatory: Alimentia uses a biologist and a licensed physician. A paid reviewer for content would fit the budget [Hypothesis].
   - Digital delivery; Israel-operable.
   - EU VAT via the non-Union OSS scheme.
   - Risks: food inspectors (Lebensmittelüberwachung) could reject a 10-minute course, so make it substantive; and liability for certificate claims.
9. **Labour.** Low. Fully automated after setup.
10. **Unit economics [Hypothesis].**
    - €12 gross, about €10 net of VAT, about €9.5 after fees.
    - If Google Ads cost per certificate is €3–5, contribution is about €5–6 each.
    - Track A (about $3k/month profit) needs ~550 certificates a month, roughly 20% of Alimentia's estimated volume.
    - Track B needs multiple countries and certificates: Italy via a regionally accredited partner (Italy is regional, often requires an accredited ente, ~€35, 3–5-year validity [Secondary: P8-E search]), Austria, an allergen add-on.
11. **Risks / kill.** German cost per sale too high; inspectors or employers distrusting cheap online certificates; incumbents already dominating search ads. **Decisive assumption: German Google Ads cost per paid certificate ≤ €5 at ≥500 sales a month.**

### E2. A Hebrew-first copy of a proven US AI consumer-app category, launched with paid social and creator revenue-share

1. **Concept.** Pick a category with proven US demand and no Hebrew-native entrant. Build a Hebrew-first app with an Israeli curriculum or food/cultural fit. Launch with small paid Meta/TikTok budgets, then 50/50 revenue-share deals with 1–3 Israeli creators.
2. **Paying customer.** Israeli consumers via App Store / Google Play subscriptions.
3. **Price.** About ₪30–40/month or ₪150–250/year (CalBuddy-type pricing [Hypothesis]).
4. **Spending evidence.**
   - CalBuddy: **2,520 IL ratings since 2025-05-29** [Verified: iTunes Search API, 2026-10-13]. Founder reports $1k in the first month, ~$20k/month by month 4 from paid ads, and over $81k/month after creator revenue-share [Anecdote: Starter Story, Aug 2026].
   - Calcounti (Hebrew, 2025-03): 3,372 IL ratings.
   - Mathins (Hebrew AI maths tutor following the Israeli curriculum, 2026-04): 410 ratings in about 5.5 months.
   - Mea Kal (Hebrew study app, 2025-10): 450 ratings [all Verified: iTunes API, 2026-10-13].
   - **Base rate in my probes: 4 of about 16 Hebrew-native 2025–26 newcomers passed 400 ratings.** The rest had 0–100 (Push AI trainer 7, STOP-SMOKE 2, ConvoAI English 2, LookMentor 32, Tanakh apps 22–100). The sample is biased toward visible apps.
5. **Competitors.** Global apps with Hebrew UI (Cal AI 3,879 IL ratings; Photomath 23,827) and Israeli incumbents (Loora for English, 2,910). Weakly served categories in my probes: AI personal trainer (no Hebrew app above 7 ratings), skin analysis, quit-smoking. Demand there is unverified.
6. **Entry strategy.** Native Hebrew and Israeli-specific content (curriculum, kosher/Israeli foods, IDF fitness tests). Israeli CPMs are "significantly lower than in the US" [Anecdote: CalBuddy founder]. Israeli founder access to local creators.
7. **Acquisition.** Paid Meta/TikTok first, then creator revenue-share. Newcomer evidence: 4 verified Israeli successes in 18 months plus many failures. TikTok Ads has a 34% hit rate on TrustMRR, though that partly reflects survivors.
8. **Capital, ops.** Test budget $1–2k in ads, which is tight. Apple and Google platform rules apply. Fully Israel-operable.
9. **Labour.** Moderate: ad creatives and creator management. Delegable to creators.
10. **Unit economics [Hypothesis].** LTV ₪80–150 against Israeli CPA ₪30–60 → profitable only above ~2× LTV/CPA. A 50% revenue share halves margin on creator-sourced users. Track A plausible; Track B shown by CalBuddy (self-reported).
11. **Risks.** Category choice (must be proven but empty); quick copycats (the Hebrew calorie category already has 2+ winners and new entrants); small market ceiling. Overlaps Agent A's App Store dataset. This is an Israel-domestic play; lesson 3 is overridden only because it rests on measured newcomer outcomes. **Decisive assumption: one specific category has Israeli paid-ad CPA ≤ 50% of 12-month LTV. Test with $500–1,000.**

### E3. QR guest photo-sharing for events in an under-served language market, sold through Google Ads and venue/vendor partners

1. **Concept.** A web app (no install): guests scan a QR code, upload photos and videos, and the host gets a live album, slideshow and download. Paid per event.
2. **Customer.** Couples and event hosts; secondary resale through venues, planners and photographers. Candidate markets: Israel (Hebrew, large weddings) or Poland, Netherlands or Portugal [Hypothesis]. All unverified.
3. **Price.** €49–149 per event [Hypothesis; German-winner pricing not public].
4. **Spending evidence.** A German stealth photo-sharing-for-events business: $30,197 in the last 30 days, **$549,218 since 2024-04**, founder 0 X followers, channels Google Ads + SEO + IG [Verified: trustmrr.com/startup/photo-sharing.md, 2026-10-13].
5. **Competitors.** WedShoots (free; 28k ES and 75k FR ratings), Wedbox DE 1,081, POV, EventPics (2025, 31–148 ratings), plus many 2025–26 apps with 0–6 ratings [Verified: iTunes API]. Israel: no Hebrew App Store entrant, but web-only players are [Unknown]. Eventer has a presence.
6. **Entry.** Language plus local add-ons, for example printed QR table cards and live-screen slideshows for large Israeli weddings [Hypothesis]. Do not enter English, Spanish or French markets.
7. **Acquisition.** Google Ads on wedding-photo intent terms plus vendor referral fees. Evidence: one verified newcomer (DE). Google Ads hit rate ≥15%.
8. **Capital, ops.** Low; storage costs per event. Israel-operable.
9. **Labour.** Low.
10. **Economics [Hypothesis].** €79 average, minus ad cost per sale €20–35 and storage €2 → ~€40 margin. Track A needs ~75 events a month. Seasonal.
11. **Risks.** The free WedShoots / Bodas.net bundle anchors price at zero in many markets; hosts may just use WhatsApp or Google Photos. **Decisive assumption: Google Ads cost per paid event ≤ €30 in the chosen market.**

### E4 (low, conditional). Owner-level SMB phone-lead data for Spanish and Italian prospectors (coldcaller.pro model)

- **Evidence.** coldcaller.pro (FR): $13.6k/30d, $84.7k all-time since 2026-04, word of mouth only, €19–99/month, ~9% visitor-to-paid, 600 users, solo founder [Verified: trustmrr.com/startup/coldcallerpro.md, 2026-10-13]. Deeplead (DE): $7.7k/30d through word of mouth plus cold email [Verified].
- **Channel logic.** Users are outbound salespeople who share tools in their communities.
- **Hard blockers [Unknown, likely serious].** Sole traders' mobile numbers are personal data under GDPR. Italy's Registro delle Opposizioni and Spain's restrictions on unsolicited calls. Data-sourcing licences or scraping terms of service.
- **Decisive assumption: a licensed data source plus a lawful-basis opinion for B2B calling in ES/IT.** Without it, kill.

## 5. Killed

| Idea | Why killed |
|---|---|
| Product Hunt / Hacker News / Indie Hackers launch as the first channel | Exact rates: HN 4.7%, PH ~5%; HN's best earner has under $25k all-time. SaveWise: "none of those people stuck" |
| Reddit or TikTok founder-led organic as the core channel for a part-time founder | Verified decay at AppAlchemy ($17k claimed, now $5.5k after posting stopped) |
| Persona-account short-form content engine sold to app developers | Supply already exists (Fastlane self-reports $69k MRR; boothie sells its account generators); TikTok account-policy risk |
| Copying Khosmos (French artisan quoting/invoicing) | Flood of ≥15 apps from 2025–26 with 0–15 ratings |
| Truck-dispatch back office (FF Group) | Similar to the excluded Phase 3 "offshore dispatchers" |
| EU company formation (Fast Corp) | Needs licensed local accountants |
| Local cleaning (Altitude) | Not operable from Israel |
| Programmatic-SEO B2B databases (AngelMatch model) | Too close to the excluded lead-list and award-digest ideas; no new segment identified |

## 6. Ranking, diligence, decisive assumptions

**Ranking:**
1. **E1, the German online food-hygiene certificate.** The strongest verified audience-free comparable (6 months to $37k/30d); low labour; an employer obligation with a 2-year renewal.
2. **E2, Hebrew-first AI consumer app.** Four verified Israeli newcomer successes since 2025; founder-fit; but a choose-the-category risk and copycat risk.
3. **E3, event photo-sharing.** One verified DE comparable; crowded nearby markets.
4. **E4.** Conditional on legal clearance.

**Top two for deep diligence:**

- **E1.** Decisive: *German Google Ads cost per paid certificate ≤ €5 at ≥500 sales/month, and German employers and inspectors accept a private online LMHV/IfSG-follow-up certificate.* Next checks:
  - Google Keyword Planner volumes and CPCs, viewed without logging in [Unknown how].
  - The full IHK provider list (Frankfurt/Bonn pages).
  - Gesundheitsamt guidance on whether online follow-up briefings are acceptable.
  - The competitor set for "Folgebelehrung online".
  - Italy as a second market via an accredited partner.
- **E2.** Decisive: *a specific weakly served category where Israeli paid-ad CPA ≤ 50% of 12-month LTV.* Next checks: a census of IL App Store ratings across about 30 US-top AI-app categories to find Hebrew gaps (coordinate with Agent A); estimates of Israeli Meta CPMs.

## 7. Method limits

- Indie Hackers was inaccessible, so no Stripe-verified IH badges were used.
- TrustMRR channel tags are current and multi-tag, not first-customer channels.
- The "audience-free" proxy relies on X followers only.
- Starter Story transcripts are self-reported, and the show over-represents consumer iOS apps.
- No Product Hunt API data was used.
- German, Italian and Israeli ad costs are all [Unknown].

**WebSearch count: 6** (Spain food-handler certificate; Italy HACCP online; Portugal HACCP, which was inconclusive; Indie Hackers first-100 roundup, snippet only; Colombia food-handler certificate; German hygiene training).

Raw data: scratchpad `p6plus/P8-E/data/` (channels.json, startups.json, af.txt, ss.json).
