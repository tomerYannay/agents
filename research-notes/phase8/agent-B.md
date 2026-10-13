# Phase 8 — Discovery Agent B (Physical products, manufacturing, e-commerce)
Method: reverse-engineer verified newcomer winners in physical products. Date: 2026-10-13. WebSearch used: 6 of 6 (all logged as P8-B).

## 0. Datasets, access and caveats
| Source | What I pulled | Access |
|---|---|---|
| **Crowd Supply** | All 700 browse tiles (raised, backers, % funded, project id); 295 project pages with id ≥ 8000 (goal, "funded on" date, price, update dates); 78 sitemap-only pages, which turned out to be the hidden failed or suspended campaigns. | robots.txt allows; 1 request/s. [Verified: crowdsupply.com/browse, /sitemap.xml, project pages, 2026-10-13] |
| **Kickstarter** | Direct access blocked (HTTP 403 on discover JSON and robots.txt). I used the public Webrobots monthly snapshot instead (`Kickstarter_2026-10-12…json.gz`, 81,643 unique projects). | [Verified: webrobots.io/kickstarter-datasets, 2026-10-13]. **Strong bias:** the snapshot holds 52k successful vs 17k failed projects, while Kickstarter's real success rate is about 40%. Failed campaigns are under-sampled, so I use it only for *relative* comparisons and pledge distributions of the projects captured. |
| **Indiegogo, BackerKit** | Not used. | 403, blocked. Not bypassed. |
| **Empire Flippers API** | All 2,854 sold and for-sale listings. 1,041 physical (FBA, FBM, eCommerce, DropShipping); 519 listed ≤36 months after first revenue; 140 first monetised 2022+. | [Verified: api.empireflippers.com listings API, 2026-10-13]. P&L is EF-vetted but seller-reported: "Verified-EF". |
| **Flippa** | 20 server-rendered e-commerce search pages: 1,000 of 2,568 open listings; 316 aged ≤3 years. | [Verified: flippa.com/search, 2026-10-13]. Figures are seller-presented; "Data Verified" means connected Shopify or GA data, not an audit. Six listing pages opened. |

**Survivorship.** EF and Flippa only show survivors that someone wants to sell. EF effectively requires about $2k/month profit or more (Agent C measured the 5th–10th percentile at $1.8–2.1k). Neither marketplace shows businesses that never sold. Crowd Supply is the only dataset here with a real denominator for launched projects, and it pre-filters applicants.

## 1. Base rates

### 1a. Crowd Supply, campaigns funded or ended 2024–Oct 2026
- **Launched campaigns:** 106 visible, plus about 10 hidden failures or suspensions found only in the sitemap (for example GenBook RK3588 at 16% funded, HaloMAX at 13%, Edgi-Talk at 3%, ESAP-30 at 17%). That is about 116 launched in total.
- **Funding rate:** about 91–92% reached their goal. This matches Crowd Supply's own claim that "over 90% … reach their funding goals".
- **Applicant filter:** Crowd Supply "turns away over 75% of applications". So **at most about 23% of applicants end up funded**. Projects that never got past pre-launch are also not visible. [Verified: crowdsupply.com/apply, 2026-10-13]
- **Amounts raised, visible campaigns (n=106):**
  - Median **$28.9k**, median 127 backers.
  - 27% under $10k, 31% $10–50k, 19% $50–100k, 23% ≥ $100k.
- **First project on Crowd Supply vs repeat creators:**
  - 63 first-timers: median **$26.0k**; 25 raised ≥ $50k and 13 raised ≥ $100k.
  - 43 repeat creators: median $31.5k.
  - Being new to the platform is not a handicap. But "first on Crowd Supply" does not mean "no audience" (examples: Craft Computing is a YouTuber; Machinery Enchantress has a large following).

**By product type** (keyword classification, n=106):

| Type | n | Median raised | ≥ $50k |
|---|---|---|---|
| Retro-console / handheld mods (FlippyDrive, PicoIDE, DeckSight, GB-Link, Game Bub) | 9 | **$165.8k** | 7 |
| E-paper / distraction-free devices (PocketMage, Zerowriter Ink, Modos, Diptyx, Open Book Touch) | 6 | **$172.4k** | 6 |
| SDR / RF | 25 | $52.9k | 13 |
| Developer and bench tools (USB, KVM, JTAG, power, serial) | 20 | $21.2k | 6 |
| Home Assistant / local-first | 7 | $25.3k | 2 |
| Generic MCU / FPGA dev boards | 13 | $7.5k | 2 |

### 1b. Kickstarter, launched 2024+ and ended (biased snapshot, n=30,193)
| Category | n | Median pledged | ≥ $50k |
|---|---|---|---|
| Tech / Hardware | 226 | $35.5k | 44% |
| Tech / Gadgets | 911 | $24.3k | 33% |
| Design / Product Design | 1,726 | $17.1k | 29% |
| Games / Gaming Hardware (first-time creators) | 122 | $2.7k | 16%; success rate 49% even in the biased sample |
| Fashion / Apparel | — | $0.8k | — |
| Food / Drinks | — | $3.6k | — |
| Crafts / Printing | — | $0.2k | — |

- First-time creators (no earlier project in the snapshot) look the same as repeat creators in Product Design and Gadgets.
- **Capital behind those numbers.** Crowdfunding agencies report roughly $2–5 cost per lead and **about $29–32 per $1 reservation**, with depositors converting at 20–40% [Anecdote/vendor: LaunchBoom case studies; Kickstarter Creator blog, via WebSearch P8-B #3]. That works out to about $75–150 of ad spend per backer. A median $17k Product Design launch (about 130 backers) therefore implies **$10–20k of pre-launch ads**, 5–10× the founder's budget.
- Crowd Supply replaces that spend with curation, a 122k-subscriber newsletter and a matching order of 50–100% of backer pledges [Verified: crowdsupply.com/apply].

### 1c. Empire Flippers, physical e-commerce first monetised 2022+ (n=140)
- **Status:** 91 sold, 49 for sale. Median net profit **$6.9k/month**.
- **Channel:** 70 Amazon-FBA-only, 22 Shopify-only, 17 FBA + Shopify, 23 dropshipping.
- **Denominator:** unknowable (EF intake filter).
- **Non-English EU sellers** (DE, FR, SE, CZ, IT, ES): 14 businesses, median profit **$9.4k** vs $5.7k for the 86 US businesses. Small n, but they are over-represented among the large outcomes (SE #85405 $52.6k; CZ #91698 $25.5k).
- **High-ticket / AOV ≥ $500 non-Amazon stores:** 17 across all years; 5 first monetised 2023+, with profit **$1.2–5.9k/month** (#81079, #87595, #74833, #79333, #79158).
- **Amazon Seller survey context:** Jungle Scout's 2022–23 reports say 76–89% of *active* sellers are profitable. Those are self-reported survivors, so this is not a newcomer base rate. A secondary blog cites about $3,800 as typical launch spend [Secondary, unverified].

### 1d. Flippa, open e-commerce listings aged ≤3 years (n=316 of the first 1,000)
- 211 are "Data Verified". Median claimed profit $3.8k/month; 203 claim ≥ $2k and 77 claim ≥ $10k.
- Heavy presence of:
  - research peptides (regulatory risk)
  - Meta-ads DTC brands
  - high-ticket no-inventory stores
  - personalised made-to-order goods

### 1e. What the base rates say
1. **Crowdfunding.** For an audience-free founder with $2k, Kickstarter's numbers are bought with ad money. Crowd Supply is the one channel where newcomers' median outcome (about $26k raised) does not require ad spend. Its own curation, newsletter and matching order do the work. The catch is a 75%+ rejection rate and a hardware delivery burden.
2. **E-commerce.** Young winners almost all have **one of three acquisition engines**:
   - paid Meta ads around one hero problem-solving product
   - Google Search/Shopping plus SEO for high-AOV purchase intent
   - Amazon search, which needs inventory capital

   None had a founder audience as the main engine. Organic TikTok or Instagram brands do appear, but their audiences were built inside the business.

## 2. Winner profiles (EF-vetted unless marked)

| Listing | Started | Product / price | Channel | Profit/mo | Capital / ops | Founder audience |
|---|---|---|---|---|---|---|
| EF #85405 | Feb 2023 | Orthopaedic back brace → 5 ergonomic SKUs, Sweden + DE/NO | Meta ads in local markets, later SEO; TACoS 46% | $52.6k on $367k | China agent stores and ships; freelancers | None stated |
| EF #91698 | 2025 | Grounding mats, Eastern Europe | 40 localised FB pages, 10 ad accounts, cash on delivery | $25.5k | Owner self-fulfils from home | None |
| EF #95287 | 2023 | Head shavers + blade subscription, French-speaking markets | Facebook ads | $5.1k | China supplier dropships; 10–20 h/wk | None |
| EF #84829 | 2024 | Attachments for a dominant vacuum brand, Amazon FR/IT/DE | Amazon + German YouTuber on commission | $5.1k | FBA inventory; 2 h/wk | None |
| EF #74833 | Mar 2023 | High-ticket elderly-care products, AOV $1,353 | Google Ads (TACoS 11%) + 38% organic | $3.6k | 31 US dropship suppliers; 8 h/wk for two partners | None |
| EF #79158 | Jan 2023 | Survival/security high-ticket, authorised dealer for 27 US suppliers | 66% organic search + Google Ads | $4.0k | No inventory; 1 VA | None |
| EF #87595 | Sep 2023 | Niche electronic equipment, AOV ~$3,000 | Organic SEO | $1.7k | Factory dropships; 1 h/wk | None |
| Flippa 14144546 | mid-2024 | Solar/off-grid, AOV $3,000, 150+ US suppliers | Shopify + paid ads | $25.6k claimed (8% margin) | 3PL/dropship, 2 VAs | None stated [Anecdote] |
| Flippa 13373980 | ~2024 | Electric cigar humidors, AOV ~$2,800 | Paid + SEO | $7.7k (about $95k/yr) | 100% dropship, 10 h/wk | None [Anecdote] |
| Flippa 13223639 | ~2025 | 3D-printed pottery/clay tools | Meta ads about $3k/mo | $200k TTM revenue; profit fields inconsistent | STL files are the production asset | None stated [Anecdote] |
| Crowd Supply MiciMike | funded Jun 2026 | $99 drop-in Home Assistant mainboard for 1st-gen Google Home Mini | Crowd Supply + press (Hackster, CNX, HA Podcast) | $133k raised on an $8k goal, 643 backers | Elecrow builds and programs; Crowd Supply/Mouser fulfil | Individual HA user; no audience cited [Verified page] |
| Crowd Supply DeckSight | Feb 2025 | $199 OLED drop-in for LCD Steam Deck | Crowd Supply + Steam Deck HQ press | $166k, 1,063 backers | Small design firm | Not stated |

**Patterns an audience-free solo founder with ~$2k could replicate:**
- **P1: "Drop-in for an installed base."**
  - Examples: Steam Deck, Google Home Mini, Casio F-91W, Bambu X1 (X1Plus Expander, $99.5k), Dyson attachments (#84829).
  - The installed base supplies the audience: press and forums cover the device, so they also cover the fix.
- **P2: Curated presale with a manufacturing partner.**
  - Crowd Supply takes 12%, matches 50–100% of pledges with its own order, and handles VAT, warehousing and fulfilment.
  - Elecrow's Project Aviary and Soldered's Inkubator give free or refundable PCBA prototypes and engineering help [Verified pages, 2026-10-13].
  - So production is funded by the campaign, not the founder.
- **P3: Local-language paid social in small, cheaper ad markets.**
  - Measured CPMs: Sweden about $13.5 and Germany about €14.8, vs US about $23.4 [Vendor data: superads.ai benchmark pages, 2026-10-13].
  - PL/CZ/RO estimates are $2.5–5.5 [Secondary: Adligator estimates].
- **P4: Intent capture for high-AOV goods without inventory.**
  - Google Search/Shopping plus SEO with an authorised-dealer dropship.
  - Profit is modest ($1.2–7.7k/month) but needs no audience and little capital.
- **P5: Made-to-order production with no inventory.**
  - Examples: POD, print farms, personalised goods. Paid by Meta ads.

## 3. Opportunities
Not in the ledger unless flagged. B8-2 is an explicit **re-check of H2** with new evidence, not a new idea.

### B8-1. Firmware-first developer/field tool on Crowd Supply, built through Elecrow's or Soldered's partner programme
1. **Concept.** A small, software-differentiated hardware tool for engineers and technicians, launched as a Crowd Supply presale.
   - Hardware is co-designed and manufactured by the partner (Elecrow or Soldered).
   - The founder owns the firmware, desktop/mobile app and documentation.
   - First candidate [Hypothesis]: a pocket RS-485/Modbus/CAN fieldbus sniffer with a polished cross-platform decoder app.
   - Adjacent proven cases: WiCAN Pro OBD/HA $236k; HydraLink automotive Ethernet $13.7k; ManT1S single-pair Ethernet $23k; TermDriver 2 $31k; USB Insight Hub $20.5k; PocketPD $82k; Openterface Mini-KVM $552k.
2. **Customer.** Embedded, automation and automotive engineers and hobbyists worldwide, mostly US and EU.
3. **Model.** One-off hardware at $60–200. Crowd Supply takes about 12%. After the campaign the product stays in Crowd Supply and Mouser's store, and other channels are allowed (non-exclusive).
4. **Spending evidence.** Developer/bench tools: n=20 since 2024, median $21.2k, 6 raised ≥ $50k. First-time creators overall: median $26k. About 92% of launched campaigns are funded [Verified: Crowd Supply pages, 2026-10-13].
5. **Competitors.** Saleae, Total Phase, cheap AliExpress USB-RS485 dongles and PEAK-System CAN adapters. Users of the cheap tools dislike their poor software [Hypothesis].
6. **Entry strategy.** Win on software: protocol auto-detection, a good UI, and scripting/exports. Price between AliExpress dongles and pro tools.
7. **Acquisition.**
   - Crowd Supply curation and newsletter (122k), plus the trade press that routinely covers Crowd Supply launches (Hackster, CNX Software).
   - Newcomer outcome: first-timers' median is $26k, but the 75% rejection rate applies.
   - After the campaign: Mouser listing and SEO on protocol-debugging queries.
8. **Capital, operations and operability.**
   - Prototype PCBA is free or refunded under Aviary; enclosure and certification costs are [Unknown].
   - Production is paid from campaign proceeds plus the Crowd Supply matching order. **Whether the partner extends terms before payout is [Unknown]**, because the Aviary and Inkubator pages are silent on who pays.
   - Feasible from Israel: partners are in Shenzhen and Croatia, and fulfilment is from Crowd Supply's US warehouse.
   - CE/FCC obligations for test equipment are [Unknown].
9. **Labour.** Heavy up front (spec, firmware, app, documentation). After that the founder ships units in one box, and the firmware and app scale. Support load is moderate.
10. **Unit economics** [Hypothesis]:
    - A $30k campaign plus a $15–30k Crowd Supply order, at about 45% gross margin after the 12% fee and BOM, is about $20–27k gross profit one-off. Ongoing store sales are [Unknown].
    - Track A needs about 2–3 products in the catalogue. Track B only for a top-quartile hit (≥ $100k, 23% of launched campaigns).
11. **Risks.**
    - Rejected by Crowd Supply.
    - Hardware engineering beyond the founder's skills, even with partner help.
    - Delivery delays (common in the update logs).
    - Long lead time (6–12 months to the first dollar).
    - Small niche.

### B8-2. (Re-check of ledger H2, "Crowd Supply revival boards") De-clouded drop-in mainboards for consumer devices whose vendor cloud died
- **What is new since Phase 3.**
  - Verified newcomer proof: the MiciMike Google Home Mini board raised **$133k against an $8k goal from 643 backers**. Its creator is a single Home Assistant user with no audience cited; Elecrow handles manufacturing and Crowd Supply/Mouser handle fulfilment [Verified: crowdsupply.com/micimike-rev-devices/…, 2026-10-13].
  - The category is being copied: "LocalDot", an Echo Dot gen-3 replacement mainboard, is already in pre-launch.
  - Fresh orphaned installed bases [Secondary: The Register 2025-10-13 (opened), and search snippets on Wemo]:
    - **Bose SoundTouch** cloud ended 18 Feb 2026: streaming and multi-room stopped, and Bose did not open-source it. No replacement board was found on Crowd Supply.
    - **Belkin Wemo** cloud ended 31 Jan 2026.
- **Effect on scoring.** It removes H2's main evidence gap: a verified audience-free outcome now exists. It adds a speed risk: copies arrive within months.
- **Decisive assumption.** A drop-in board for a specific SoundTouch model can be engineered within partner-programme prototype budgets, and the SoundTouch installed base is large enough. Units sold are [Unknown].
- **Recommendation.** Rescore H2 rather than treat this as new.

### B8-3. Local-language, hero-product DTC store for one small non-English EU market (Nordics or CEE), Meta-ads driven
1. **Concept.** Pick one problem-solving product with clear before/after, of the kind in EF's winners (pain relief, ergonomics, grounding, grooming). Launch a native-language Shopify store and localised Meta ad creative in a market that English-first dropshippers skip: Sweden, Czechia, Poland, Romania or Hungary. Fulfil through a China agent or an EU 3PL, with cash on delivery where customary.
2. **Customer.** Consumers in one EU country.
3. **Model.** One-off orders with an AOV of about €40–90, plus consumable or subscription add-ons (#95287: blade subscription with 305 subscribers).
4. **Spending evidence** [Verified-EF, API 2026-10-13]:
   - **#85405:** SE, Feb 2023, $52.6k profit on $367k/month.
   - **#91698:** CZ/CEE, 2025, $25.5k profit on $69.6k/month.
   - **#95287:** FR, $5.1k.
   - **#96752:** DE, $15.2k.
   - **Flippa 12303269:** Poland lamps, Google Ads, €9.1k/month [Anecdote].
   - The 14 non-English EU young winners have a median of $9.4k vs $5.7k for US ones.
5. **Competitors.** Local marketplaces (Allegro, CDON, Alza, eMAG) and Temu/AliExpress. Buyers dislike slow shipping and foreign-language support [Hypothesis].
6. **Entry strategy.**
   - Native-language creative and support (AI-drafted, native-reviewed).
   - Cheaper reach: Sweden CPM about 36% below the global average; US about $23 [Vendor benchmark, 2026-10-13].
   - Local payment methods such as COD, Swish or BLIK.
7. **Acquisition.**
   - Meta ads, with Google Ads as a second channel.
   - Newcomer evidence: #91698 went from nothing in 2025 to $25k/month profit with a home-fulfilling solo owner.
   - The newcomer *failure* rate is [Unknown]; EF shows only survivors. CAC for a newcomer is [Unknown].
8. **Capital and operations.**
   - $2k covers a store, samples and about $1–1.5k of ad tests: thin, about 2 product tests.
   - Inventory can wait until the first sales via agent dropship.
   - Israel-based operation needs:
     - EU VAT handling: IOSS for consignments ≤ €150 shipped from outside the EU; local VAT registration if using an EU 3PL.
     - Product-safety rules (GPSR requires an EU responsible person).
     - COD logistics partners.
   - Health claims are restricted (EU medical-device rules for "orthopaedic" claims).
9. **Labour.** Creative production is the bottleneck (#85405 runs 5 video editors). AI video and image tools plus freelancers can carry it, and the owner's hours stay roughly flat as revenue grows.
10. **Unit economics** [Verified-EF margins: 14% (#85405), 37% (#91698), 22% (#95287)]. Track A at about €25–35k/month revenue at 15–20% net. Track B is demonstrated by #85405 and #91698.
11. **Risks.**
    - Meta CPM inflation: Germany's median CPM about doubled Jul 2025 → Jul 2026 [Vendor benchmark].
    - Ad-account bans.
    - Winning-product copycats.
    - COD refusal rates.
    - Product-safety compliance.
    - A $2k budget allows very few tests.

### B8-4. High-ticket authorised-dealer storefront for one US consumer niche (intent-led, no inventory)
*(Consumer sibling of Agent C's C4. C4 targets B2B equipment outside the US; this targets US homeowners and hobbyists.)*
1. **Concept.**
   - A specialist Shopify store for one $800–4,000 product class, with deep comparison and spec content.
   - Candidate classes [Hypothesis]: cold plunges, home saunas, cigar humidors, off-grid solar generators, mobility aids.
   - The store applies to US brands and distributors for authorised-dealer dropship accounts.
   - Acquisition is Google Shopping/Search plus SEO; phone and chat sales run through a VA.
2. **Customer.** US consumers, with occasional small businesses.
3. **Model.** One-off orders at 10–30% net margin.
4. **Spending evidence:**
   - [Verified-EF, API]: #74833 (AOV $1,353, $3.6k/mo, TACoS 11%, 0.25% conversion); #79158 ($4.0k, 27 dealer suppliers, 66% organic); #79333 ($5.9k); #87595 ($1.7k).
   - [Anecdote, Flippa pages opened]: humidors, AOV ~$2,800, $7.7k/mo, 10 h/wk; solar/off-grid, AOV $3k, $25.6k/mo at an 8% margin.
5. **Competitors.** Brand DTC sites, Amazon, and big-box stores (Home Depot, Wayfair). Buyers dislike the lack of expert advice on expensive purchases [Hypothesis].
6. **Entry strategy.** Win on niche expertise and a phone sales desk, plus a US-supplier network that ships quickly. Credible but not unique: the model is heavily promoted by course sellers, so saturation is likely [Secondary: ecommerceparadise and similar affiliate blogs].
7. **Acquisition.**
   - Google Shopping/Search intent, which suits a newcomer without an audience. #74833 reached TACoS of 11%.
   - Newcomer CAC and the share of stores that never get traction are [Unknown].
8. **Capital, operations and operability.**
   - No inventory. A US LLC, EIN and resale certificate are expected by dealers [Secondary: practitioner blogs]; about $300–800.
   - Ad testing about $1–1.5k.
   - Payment-processor reserves on high-ticket new stores [Hypothesis].
   - Israel is fine for operations; US-hours phone support needs a VA.
   - Brand dealer approval is "moderate–hard" with no rejection-rate data [Secondary, WebSearch P8-B #4].
9. **Labour.** Order handling and sales calls go to a VA (#74833: 8 h/wk combined). Content can be AI-assisted.
10. **Unit economics.** Track A ($2–7k/month) is the typical verified outcome; Track B is rare (one anecdotal $25.6k at an 8% margin).
11. **Risks.**
    - Dealer approvals refused to an unknown foreign-owned store.
    - Rising Google CPCs.
    - Chargebacks and freight damage on large items.
    - MAP limits on margin.
    - Course-driven saturation.
    - Slow SEO.

### B8-5. Made-to-order niche hobby or utility tools via on-demand 3D-print-farm fulfilment (zero inventory)
1. **Concept.**
   - Design a tight catalogue of functional parts for one craft or hobby that buys repeatedly: clay cutters and texture rollers (as Flippa 13223639), and analogous niches [Hypothesis: cake or fondant tools, leathercraft jigs, model-railway scenery tools].
   - Sell through your own Shopify store with Meta ads, plus Etsy.
   - US print farms print and ship per order through an API: Slant 3D Teleport/API/Portals, with no minimums, "no costs until an item is sold", and parts shipped from US farms [Verified: slant3d.com, 2026-10-13].
2. **Customer.** US and EU hobbyists.
3. **Model.** One-off orders at $15–60, with bundles and repeat purchases of new designs.
4. **Spending evidence:**
   - Flippa 13223639: about $200k TTM revenue, about $10k/month in sales, with Meta spend of about $3k/month. Data Verified via GA and WooCommerce, but its profit fields are internally inconsistent [Anecdote, page opened 2026-10-13].
   - EF #74865: personalised lights, $2.9k/month, 77% organic.
   - Flippa custom business stamps: $19.5k/month, made-to-order, $128 AOV, 4 years old [Anecdote].
5. **Competitors.** Etsy 3D-print sellers (supply is surely large; Etsy is blocked, so it was not measured) and Amazon generics. Buyers complain about print quality [Hypothesis; one Slant Shopify-app reviewer left for quality reasons, Verified: apps.shopify.com/slant, 1 review, 2026-10-13].
6. **Entry strategy.** Fast iteration of designs tested on ads, which suits the founder's CAD-plus-software skills and AI-generated creative. The defensibility is weak.
7. **Acquisition.**
   - Meta ads (as in 13223639) and Etsy search.
   - Etsy newcomer outcomes are unmeasured (blocked).
   - Slant's own Shopify app has 1 review since Aug 2024 [Verified], which suggests small adoption through Shopify; others may use the API or Teleport.
8. **Capital and operations.**
   - Under $2k: CAD time, prototypes and an ad test.
   - Per-part price is not public (quote only) [Unknown], so margins are unverified.
   - Fully operable from Israel.
9. **Labour.** Design work and ad testing; fulfilment needs no labour.
10. **Unit economics** [Hypothesis]: Track A if per-part cost is ≤ 35% of price and ad CAC is ≤ 30%. Track B unlikely.
11. **Risks.**
    - Print-farm cost and quality.
    - Easy copying (STL theft).
    - Etsy saturation.
    - Overlap with ledger exclusions:
      - P3 "Patreon STL studios and own-design services for print farms". That was selling designs to farms; this is a DTC brand.
      - P4 "3D-printed parts for discontinued products". That was a different demand driver.

## 4. Killed or not proposed
- **Ad-built Kickstarter hardware launches.** About $75–150 of pre-launch ads per backer [vendor benchmarks] means $10–20k for a median Product Design outcome. That is 5–10× the budget.
- **Amazon FBA private label (US).**
  - Young EF winners carry inventory and often 5–184 SKUs.
  - Survey "profitability" figures are survivor data only.
  - Capital is above $2k. Excluded by capital, not by demand.
- **EU-marketplace compatible accessories for a dominant brand (#84829).** Too close to the ledger's P3 "fast-follower Amazon accessories", and it needs FBA inventory.
- **Retro-console mod boards.** Highest Crowd Supply medians ($166k), but these are likely the content of H2. Platform-holder IP and anti-circumvention risk, and they depend on an existing scene reputation.
- **E-paper distraction-free devices.** High medians ($172k), but crowded in 2026: PocketMage, Zerowriter, AUTEUR coming soon, Diptyx, Open Book, Modos. Heavy hardware.
- **Research peptides, compounded GLP-1 telehealth, "emulation handheld" stores.** All appear among Flippa and EF young winners. Regulatory or IP exposure.
- **Pinterest-ads dropshipping (#92870, $20k/month).** One case; no newcomer evidence; the trend is fragile.
- **POD apparel and personalised gift brands.** Ledger exclusions (generic POD, creator merch, profession-themed paper goods). The young winners mostly have built-in audiences (ocean-themed POD clothing, 11k-subscriber card brand).

## 5. Ranking, deep-diligence picks, decisive assumptions
| Rank | Opportunity | Why | Decisive unverified assumption |
|---|---|---|---|
| 1 | **B8-3 Local-language hero-product DTC (one small EU market)** | Strongest verified young P&Ls in my datasets (EF #85405, #91698), audience-free, cheaper CPMs, labour delegable, Track B shown | A newcomer can reach first-order CAC below about 35% of AOV in SE or CZ/PL with native creative, inside a $1–1.5k test. Also: compliant EU VAT/GPSR/COD set-up from Israel at low fixed cost |
| 2 | **B8-1 Firmware-first developer tool on Crowd Supply via Elecrow/Soldered** | The only channel measured here where newcomers reach a median of about $26k with **no ad spend**; production funded by presale plus matching order; plays to software strength | Crowd Supply accepts the project, and the partner programme carries prototype and production cost until campaign payout. The Aviary/Inkubator pages do not say who pays |
| 3 | **B8-2 (H2 re-check) De-clouded drop-in boards** | Verified audience-free $133k outcome (MiciMike); fresh orphaned installed bases (Bose SoundTouch, Wemo) | A specific orphaned device has a large enough installed base and a board-swap path the founder and partner can engineer before a copycat. Copy speed is already visible (LocalDot) |
| 4 | B8-4 High-ticket authorised-dealer storefront (US) | Repeatable Track A, no inventory, intent-led | Dealer approvals for a new, foreign-owned store, and newcomer Google Shopping CAC |
| 5 | B8-5 Made-to-order print-farm tools | Zero inventory; one anecdotal winner | Per-part print-farm cost leaves ≥ 40% contribution after ad CAC |

**Top for deep diligence:** B8-3, B8-1, and B8-2 (as an H2 rescore).

**Cross-cutting finding for the Director.** In physical products, the audience-free winners did not rely on a marketplace's organic traffic. They either:
- **bought intent or attention** in under-served markets (Meta ads in local languages, Google for high AOV), or
- **borrowed a curated platform's audience plus a manufacturer's balance sheet** (Crowd Supply with Elecrow or Soldered).

Crowd Supply is the only measured channel where a newcomer's *median* outcome is meaningful (about $26k raised; about 92% of launched campaigns funded). The gate is the 75%+ rejection rate at application, not post-launch failure.

**WebSearch count: 6 of 6** (all logged as P8-B):
1. Jungle Scout seller report
2. Meta CPM by country
3. Kickstarter pre-launch benchmarks
4. High-ticket dealer approval
5. Slant 3D pricing
6. Cloud-shutdown devices

Primary pages and APIs fetched, none capped:
- Empire Flippers API (32 pages)
- Crowd Supply: about 400 pages (browse, project pages, sitemap-only failures, /apply, Aviary, Inkubator)
- Webrobots Kickstarter snapshot
- Flippa: 20 search pages and 5 listing pages
- superads CPM pages
- slant3d.com, apps.shopify.com/slant, The Register

Blocked and not bypassed: Kickstarter, Indiegogo, BackerKit (403). Flippa listing data behind NDA was not accessed.

Scripts and data: `/private/tmp/claude-501/-Users-tomeryannay-Projects-agents/33458dff-96bb-4d90-98b6-5161ecb65c2e/scratchpad/p6plus/P8-B/{scripts,data}`
