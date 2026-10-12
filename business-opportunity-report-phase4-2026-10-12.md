# Phase 4: Continued Opportunity Discovery

**Date:** 2026-10-12
**Companion reports:**
- `business-opportunity-report-2026-10-12.md` (Phase 1)
- `…-phase2-…` (Phase 2)
- `…-phase3-…` (Phase 3)

---

## Bottom line

**Phase 4 did not find an opportunity stronger than the current leaders.** One idea reaches the top tier: **niche Apify Actors**, small pay-per-use data-extraction tools sold on the Apify marketplace (J7). It scores **55.4**, which places it **third on the leaderboard across all phases**. That is between the hobbyist data API from Phase 3 (H6, 57.2) and the Meshtastic family kits (H1, 54.6), and within scoring noise of both. Every other Phase 4 candidate scores 51 or lower.

The audit improved the evidence in places, but it removed more opportunities than it confirmed:
- **J10, Israeli restaurant direct ordering:** Tabit, Israel's main restaurant POS company (funded with $35M), already sells branded ordering at roughly a tenth of Wolt's commission. Wix offers commission-free ordering.
- **J8, futures prop-firm copier:** the planned differentiator, per-firm rule enforcement, already ships in the incumbent Tradecopia.
- **J6, add-on modules for Perfex CRM:** new modules released in 2026 have 1–16 lifetime sales each.
- **J1, Hebrew/Russian memoir books:** Remento and Storyworth confirmed they don't support Hebrew. But MyHeritage, an Israeli company, runs MyStories, which has almost the same feature set. Whether MyStories supports Hebrew is unknown.

**The evidence base is weaker than in Phase 3.** The session-wide search quota ran out early in discovery:
- Each discovery agent got only 6–9 searches.
- The auditor got 2 and the red team about 10.
- Everything else came from fetching specific pages directly.

Wherever a competitor or market question couldn't be settled, the score carries a penalty, and section 9 lists those questions.

---

## 1. Research methodology

The structure, scoring and evidence standards are the same as Phase 3. Nothing was changed.

**Discovery.** Six independent agents (A–F) each covered the same universe as in Phase 3, steered toward areas Phase 3 hadn't covered. Each worked from the same brief, with these additions:
- An exclusion list of all ideas from Phases 1–3 (about 120).
- An explicit ban on browser and signed-in account access.
- A cap of 14 WebSearch calls per agent.

**Search budget.** The shared session quota (200) was already nearly used up, so actual usage was much lower than the cap:

| Agent | Searches that returned results |
|---|---|
| A | 6 |
| B | 8 |
| C | 8 |
| D | 7 |
| E | 7 |
| F | 6 |

After that, every agent worked by fetching specific URLs. Reddit, Etsy, eBay, Kickstarter, Amazon, Fiverr, BuiltByBit, aescripts, Wolt and parts of gov.il refused fetches.

**Screening and review.** I merged the results (about 55 distinct ideas), screened them, and shortlisted 13. An independent Evidence Auditor (2 searches plus 56 page fetches) and an independent Red-Team Investor (about 10 searches plus page fetches) then reviewed the shortlist.

**Scoring.** The formula is unchanged from Phase 3:
- Balanced = 0.4 × Cash-flow + 0.4 × Scalability + 0.2 × Distribution
- Adjusted = Balanced − evidence penalty (0–15)

The criteria and weights are the same as Phase 3.

**No contact, purchases, building, or browser use** took place in Phase 4.

---

## 2. New research universe (about 55 distinct ideas)

| Agent | Viable ideas (preliminary evidence) | Killed (reason) |
|---|---|---|
| **A: Consumer** | **Hebrew/Russian voice-memoir books** (Storyworth: 65k Trustpilot reviews, "1M books"; Remento: 753 reviews in the last 12 months) · **Polish/EU citizenship-by-descent front end** (Israeli applications rose from 2,506 in 2021 to 9,173 in 2024) · Youth sports highlight reels (unverified) · German "translate-and-launch" for indie authors (threatened by Kindle Translate) | Psychometric exam prep (free state course, 14+ providers) · Hyrox apps (clone-saturated) · Music teaching Patreon (talent-dependent) |
| **B: Physical** | **Memoir books** (found independently, same as A) · **Hebrew personalised children's books** (Wonderbly: 17,392 reviews in 12 months) · **Caregiver-managed "memory phone"** (RAZ $349 + $20/mo) · On-demand parts for discontinued products · Hearing-aid consumables auto-ship | AeroGarden parts (brand relaunched) · K9 nose-work kits (47 Etsy listings) · Israeli food/cosmetics export (tariff, no edge) |
| **C: Traditional** | **Grave care in Israel for families abroad** (Bezikaron ₪799–1,510/yr; Qabar Safai is the same model for Pakistan) · **Fixed-price headstone ordering** (Midrag average ₪8,503; 4,223 contractor reviews) · **Commercial rooftop solar cleaning contracts** (7–9 ₪/kW) · French/Russian care management for aging parents in Israel · Grave care in the former Soviet Union · Burial-in-Israel coordination · Arabic/Haredi wedding marketplace (Mit4Mit is Hebrew-only) | Arabic psychometric prep (free state course) · Substitute kindergarten-staff marketplace (free public apps) · CNC quoting broker (ManuFuture, Hubs) |
| **D: Software** | **Perfex/RISE/Odoo add-on modules** (Perfex core 25,970 sales; REST API module 3K) · **Apify Actors** ($1.6M/month paid to 4,500 developers; 80% revenue share) · **Futures prop-firm trade copier** (Tradecopia 363 reviews in 12 months) · **MT5 prop-rule utility** (Forex Trade Manager 686 reviews) · Hytale server plugins (6,609 projects) · DaVinci Resolve plugins · Garmin watch faces | FiveM scripts (oversupplied) · Figma/Raycast/Obsidian (closed or free-only stores) · Minecraft plugins (whole category about $1.15M/yr) · Unity tools (entrenched) |
| **E: Demand-first** | **Israeli restaurant direct ordering** (Wolt ~27% + VAT; 60%+ share) · Tami4 filter auto-ship (5+ sellers on Zap) · Thumbtack-exit acquisition for cleaners (Trustpilot 2.1) · Israeli daycare billing (brightwheel Trustpilot 1.3) | HoneyBook refugees (8+ rivals) · Fresha refugees (saturated) · Wild Apricot/Gingr/Mindbody/Rover (low volume) |
| **F: Contrarian** | **English research on TASE-only stocks** (TA-125 +28.6% in 2024, +50.6% in 2025) · **Defense-tech scouting for EU buyers** ($3B raised in H1 2026) · **EU 72-hour preparedness kits** (EU strategy, Preppi) · Hebrew deal channels (affiliate) · EU-standard parallel import into Israel (needs $10–30k) · Hebrew AI audiobooks | GLP-1 foods (CPG giants) · Non-English AI receptionists ($25–99/mo, Spanish included) · AI dubbing · Agritech data · Digital-nomad and other generic trend plays |

**Patterns that recurred across agents:**
1. **Memoir books in Hebrew/Russian.** Agents A and B reached this independently.
2. **Israeli diaspora and aging services.** Memoir books, grave care, care management. This continues the Phase 3 pattern.
3. **Marketplace-distributed digital tools** with visible sales counts (CodeCanyon, MQL5, Apify).

**Coverage gaps.** Because of the search cap, agent C produced no discovery in marine, agriculture inputs, fleets, printing, refurbished trade equipment or tourism.

---

## 3. Initial shortlist (13)

| # | Business | Buyer | Spending evidence | Competitors | Our differentiation | Channel | Capital | Main risk |
|---|---|---|---|---|---|---|---|---|
| J1 | Hebrew/Russian voice-memoir hardcover | Adult children in Israel and the diaspora (gift) | US category strong | **MyHeritage MyStories** (Israeli; Hebrew unknown); Remento and Storyworth have no Hebrew (verified) | RTL Hebrew/Russian, WhatsApp voice, printed in Israel | Meta gift ads, roots-project tie-ins | Low | MyStories adds Hebrew; Israeli acquisition cost |
| J2 | Hebrew personalised children's books | Israeli parents | Global category strong | AniSipur (local); Wonderbly/Librio have no Hebrew | Hebrew culture, local print | Meta, kindergarten bulk orders | Low | Small market, low ticket |
| J3 | Polish/EU citizenship research front end | Israelis with Polish ancestry | 9,173 applications/yr | Law firms that bundle archive search | Fixed price, transparent tracking, DIY kit | Hebrew search intent | Low | Lawyers bundle it; fee-sharing rules |
| J4 | Grave care for families abroad (+ headstones) | Diaspora children | Bezikaron priced; Qabar Safai analogue | Bezikaron (English site, not aimed at the diaspora) | USD billing, yahrzeit timing, English reports | Google, funeral homes abroad | Low | Hard to reach the diaspora |
| J5 | Commercial rooftop solar cleaning | Farms, factories | Midrag ₪/kW pricing | Installers' maintenance contracts | Independent, cheaper | Outbound | Low | No founder fit; thin margin |
| J6 | Perfex/RISE/Odoo modules | Self-hosted CRM buyers | Incumbent modules 1–3K sales | Entrenched authors | Vertical modules, porting | CodeCanyon search | ~$0 | **New modules sell 1–16** |
| J7 | Niche Apify Actors | Growth and data teams, AI agents | $1.6M/month payouts | Store incumbents per data source | Regional/vertical sources, reliability | Apify Store, MCP | ~$0 | Skewed earnings; terms of service |
| J8 | Futures prop copier + rule guard | Multi-account futures traders | Tradecopia momentum | Tradecopia (**already has rule guard**), CrossTrade, TradeSyncer | None remaining | Affiliates | Low | Liability; no differentiation |
| J9 | MT5 prop-rule utility | Prop traders | Utilities sell (686 reviews for the leader) | Guardian tools with 2–8 reviews | Per-firm presets | MQL5 in-terminal store | ~$0 | Weak sub-niche demand |
| J10 | Israeli restaurant direct ordering | Restaurants | Wolt fees resented | **Tabit Order/Wheels, Wix, Mishloha** | Marketing layer only | Field sales | Low | Incumbents own the ordering infrastructure |
| J11 | English TASE research | Foreign investors | Unknown | TipRanks/TASE translation; Leumi research | TASE-only coverage | Substack | ~$0 | Licensing; credibility |
| J12 | EU 72-hour kits | PL/Baltic/Nordic households | EU strategy | Generic Amazon/Allegro kits | Design, local plans | Amazon.de, TikTok Shop | High (inventory) | Demand spikes with news; compliance |
| J13 | Caregiver-managed memory phone | Families of people with dementia | RAZ (no review footprint) | RAZ, Jitterbug, free launchers | WhatsApp mode, price | Senior affiliates, care agencies | Medium | Support burden; low volume |

---

## 4. Five deep-dive finalists

**Selection.** The four highest-scoring candidates with a distinct business model are J7, J1, J4 and J3. J9 is the fifth. J2 and J6 score about the same as J9 but were left out:
- J2 is a weaker version of J1's stack.
- J6 is contradicted by new-entrant sales data.

### F1: Niche Apify Actors (J7), score 55.4

- **Product:** a portfolio of pay-per-event scrapers and data tools for regional or vertical sources that have weak coverage on the Apify Store, such as EU national property and job portals and B2B registries in other languages. The aim is to beat poorly maintained incumbents on reliability, for example where the top Idealista Actor has a 3.76★ rating.
- **Buyer:** growth and lead-generation teams, proptech firms, analysts, and AI agents calling Actors through MCP.
- **Demand evidence:**
  - Apify reports "$1.6M paid out last month" to 4,500 developers [Verified on the Apify page by discovery; not re-checked by the audit].
  - The developer share is 80% of revenue minus platform costs, paid out monthly with a $20 minimum through PayPal or Wise [Verified: docs.apify.com].
  - Niche Actors have real usage, for example Idealista with 2,473 users and 367 monthly active.
- **Alternatives:** existing Actors per data source, commercial data vendors, building in-house.
- **Entry strategy:** pick sources with low-rated or missing Actors, keep maintenance fast with AI-assisted repair, and price competitively.
- **Acquisition:** Store search and ranking, Apify's MCP/agent discovery, and the affiliate programme. Apify's payout figures show the channel produces purchases.
- **Economics** [Hypothesis]: about $0–50/month in costs, and 2–5 days of founder time per Actor plus maintenance.

  | Scenario | Assumption | Owner profit |
  |---|---|---|
  | Downside | 5 Actors × $20/mo | ~$100/mo |
  | Base | 20 Actors × $100/mo | ~$2k/mo |
  | Upside | One hit on a large source plus the portfolio | $5–8k/mo |

- **Scalability:** grows without the founder's hours, but maintenance grows with the size of the portfolio. Track A is realistic. Track B needs a hit.
- **Risks:**
  - Earnings are concentrated among a few developers. The average is about $355 per developer per month, so most Actors earn little.
  - Terms-of-service and GDPR exposure. Avoid personal and login-gated data.
  - Anti-bot measures.
  - Apify changing its fees.
- **Labour:** scales beyond founder hours.

### F2: Hebrew/Russian voice-memoir books (J1), score 51.0

- **Product:**
  - A weekly question by WhatsApp or phone; the elder answers by voice.
  - AI transcribes and edits the answers into first-person Hebrew or Russian chapters.
  - An RTL hardcover printed in Israel, with a QR code per chapter for the original audio.
  - Price ₪450–650; extra copies ₪150–250.
- **Buyer:** Israelis aged 30–60 buying for parents or grandparents. Russian-speaking families; later, diaspora Hebrew and Yiddish speakers.
- **Demand evidence:**
  - Storyworth: 65,172 Trustpilot reviews, 3,926 in the last 12 months.
  - Remento: "1,800+ reviews", 4.9.
  - **Remento supports English and Spanish only and does not ship to Israel.** Storyworth supports English and Spanish, with printing for "most but not all languages" [Verified, audit].
  - No Israeli demand data.
- **Alternatives:**
  - **MyHeritage MyStories:** Israeli-owned. It sends weekly questions, accepts audio answers, and produces a hardcover with QR codes. Hebrew support is unverified.
  - Ghostwritten memoirs, which cost far more.
  - AniSipur-style local print shops.
- **Entry strategy:** Hebrew and Russian RTL output, WhatsApp-first voice input for elders who don't use email, local printing, and question sets about Israeli life (aliyah, army, kibbutz, emigration from the USSR).
- **Acquisition:**
  - Meta gift ads before Rosh Hashana, Pesach and milestone birthdays.
  - Russian-language Israeli communities.
  - Retirement homes.
  - The 7th-grade school roots project.
  - The channel is proven in the US only.
- **Economics** [Hypothesis]: contribution of about ₪350 per book before acquisition cost; target acquisition cost ₪100–150.

  | Scenario | Volume | Result |
  |---|---|---|
  | Downside | 5 books/mo | ~₪1k/mo |
  | Base | 30/mo | ~₪6–7k/mo (~$1.8k) |
  | Upside | 120/mo in holiday peaks | ~₪25k/mo seasonally |

- **Scalability:** mostly software. Proofreading Hebrew output is a per-unit cost. Track A, with B only through expansion to Russian and diaspora languages.
- **Risks:**
  - MyStories supports or adds Hebrew.
  - Seasonal demand.
  - Elders drop out partway.
  - Speech-to-text quality for elderly Hebrew and Russian speakers.
- **Labour:** mostly scalable.

### F3: Grave care in Israel for diaspora families (J4), score 47.4

- **Product:**
  - An annual subscription of $300–450 for four visits.
  - Visits are timed to the yahrzeit on the Hebrew calendar, with an English or French photo and video report.
  - Optional kaddish arranged through partners, re-lettering, and headstone orders (average ₪8.5k) as upsells.
  - Local crews do the fieldwork.
- **Buyer:** US, UK, French and Canadian Jews, and Israeli emigrants, with parents buried in Israel.
- **Demand evidence:**
  - Bezikaron charges ₪799–1,510 a year, has 166 Google reviews, a site in Hebrew, Russian and English, and no diaspora targeting [Verified, audit].
  - Qabar Safai sells the same model to families abroad with graves in Pakistan.
  - About 1,590 people who died abroad were buried in Israel in 2016.
- **Entry strategy:** USD billing, scheduling around the yahrzeit, English reports. Alternatively, become Bezikaron's overseas sales channel.
- **Acquisition:** Google ("grave cleaning Israel"), referrals from Jewish funeral homes abroad (commissions already exist in this chain), and synagogue newsletters. Search volume is unknown.
- **Economics** [Hypothesis]: about $180–240 gross per subscriber per year.

  | Scenario | Subscribers | Gross |
  |---|---|---|
  | Downside | 30 | ~$500/mo |
  | Base | 200 | ~$3.5k/mo |
  | Upside | 500 | ~$9k/mo |

- **Scalability:** brokered crews; route density improves margin.
- **Risks:**
  - Reaching the diaspora cheaply.
  - Trust in remote proof of visits.
  - Cemetery access rules.
  - Bezikaron adding diaspora marketing.
- **Labour:** mixed. Revenue can outgrow founder hours with crews.

### F4: Polish/EU citizenship-by-descent research front end (J3), score 45.8

- **Product:**
  - A free eligibility screener.
  - A paid "ancestor file" at ₪1,500–4,000: archive retrieval from Polish, Lithuanian and Israeli sources, plus translation and Hebrew status tracking.
  - Then a DIY filing kit, or a hand-off to a lawyer.
- **Buyer:** Israelis with grandparents born in Poland (later Germany, Austria and Lithuania).
- **Demand evidence:**
  - Israeli applications grew from 2,506 to 9,173 a year between 2021 and 2024 (Notes from Poland, 2025-02-12; confirmed by the red team, not re-fetched by the audit).
  - Law firms advertise this service.
- **Alternatives:** law firms that bundle archive research (Decker Pex Levi, Horesh) [Verified, red team], and Polish genealogy firms (from 2,500 PLN).
- **Entry strategy:** fixed price, transparency, and serving people who file themselves or are stuck on documents. Charge applicants directly, because fee-sharing between lawyers and non-lawyers may be restricted [Unverified].
- **Acquisition:** Hebrew search intent ("דרכון פולני"), and Israeli Facebook groups about European passports.
- **Economics** [Hypothesis]: about ₪1,300–1,700 gross per case after the researcher (₪800–1,200).

  | Scenario | Cases | Gross |
  |---|---|---|
  | Downside | 1/mo | ~₪1.5k |
  | Base | 5/mo | ~₪7.5k (~$2k) |
  | Upside | 15/mo (researcher capacity) | ~₪22k |

- **Scalability:** labour-dependent on contract researchers. Track A/C.
- **Risks:**
  - Unauthorised-practice-of-law boundaries.
  - Demand tied to the security climate.
  - Lawyers' bundled offers.
  - Backlogs at the Polish authorities.
- **Labour:** labour-dependent on contractors.

### F5: MT5 prop-firm rule utility on the MQL5 Market (J9), score 48.0

- **Product:** a $49–99 utility that enforces daily loss and trailing drawdown limits, news lockouts and consistency rules, with per-firm presets. It is sold in the MQL5 store inside the MetaTrader terminal (20% fee). Later ported to cTrader and Match-Trader.
- **Demand evidence:**
  - General trade managers sell well: 686, 216 and 149 reviews [Verified].
  - **But dedicated "guardian" tools have only 2–8 reviews each** [Verified, audit]. That is a weak signal for this sub-niche.
  - Platform risk: MetaQuotes suspended prop-firm licences in 2024, which was partly reversed later.
- **Economics** [Hypothesis]: about $63 net per sale.

  | Scenario | Sales | Net |
  |---|---|---|
  | Downside | 3/mo | ~$190 |
  | Base | 20/mo | ~$1.3k |
  | Upside | 60/mo | ~$3.8k |

- **Scalability:** a single tool caps out around Track A.
- **Labour:** scales beyond founder hours.

---

## 5. Adversarial review

| # | Strongest objection | Type | Verdicts (red team / audit) | Effect |
|---|---|---|---|---|
| J1 | MyHeritage MyStories offers the same product from an Israeli company | Testable (could become fatal) | Downgrade / gap confirmed for Remento and Storyworth | Hold. A one-day check on MyStories' Hebrew support decides it. |
| J2 | Small market, low ticket; AniSipur exists | Fatal-leaning | Downgrade / no Hebrew at Wonderbly | Down |
| J3 | Lawyers bundle archive search; fee-sharing rules | Testable | **Survive (best fast cash)** / not re-checked | Hold |
| J4 | Reaching the diaspora; Bezikaron has an English site | Testable / execution | Survive (low) / pricing confirmed, Bezikaron not aimed at diaspora | Hold |
| J5 | No founder fit; thin margin | Fatal for this founder | Kill | **Killed** |
| J6 | New 2026 modules have 1–16 lifetime sales | Contradicts the entry assumption | Survive / **contradicted** | **Down** |
| J7 | Earnings skewed; maintenance; terms of service | Testable / execution | Survive / 80% share confirmed | **Up (top of Phase 4)** |
| J8 | Incumbent already ships per-firm rule enforcement | Differentiator contradicted | Downgrade / **contradicted** | **Down** |
| J9 | Guardian sub-niche has 2–8 reviews per tool | Testable | Survive (side test) / confirmed crowded and low traction | Hold (low) |
| J10 | Tabit, Wix and Mishloha already own the ordering infrastructure | Fatal for a solo founder | **Kill** / **confirmed** | **Killed** |
| J11 | Licensing; TipRanks/TASE translation; credibility | Testable | Survive (low) / unverified | Hold (low) |
| J12 | Inventory and EU compliance exceed budget; demand spikes with news | Fatal within budget | Downgrade | Down |
| J13 | Support burden; no volume evidence | Execution / testable | Downgrade / RAZ price corrected | Down |

---

## 6. Updated rankings (Phase 3 formula, unchanged)

| # | Opportunity | Cash flow | Scalability | Distribution | Balanced | Penalty | **Adjusted** | Confidence |
|---|---|---|---|---|---|---|---|---|
| J7 | Niche Apify Actors | 75 | 62 | 63 | 67.4 | −12 | **55.4** | Medium |
| J1 | Hebrew/Russian memoir books | 68 | 55 | 64 | 62.0 | −11 | **51.0** | Low–Medium |
| J2 | Hebrew personalised kids' books | 67 | 49 | 64 | 59.2 | −11 | **48.2** | Low |
| J9 | MT5 prop-rule utility | 75 | 48 | 54 | 60.0 | −12 | **48.0** | Low |
| J4 | Diaspora grave care | 64 | 56 | 47 | 57.4 | −10 | **47.4** | Medium–Low |
| J6 | Perfex/RISE/Odoo modules | 76 | 47 | 51 | 59.4 | −12 | **47.4** | Medium (contradicting) |
| J8 | Futures prop copier | 65 | 57 | 61 | 61.0 | −14 | **47.0** | Low |
| J11 | English TASE research | 64 | 57 | 51 | 58.6 | −12 | **46.6** | Low |
| J3 | Polish citizenship front end | 66 | 37 | 68 | 54.8 | −9 | **45.8** | Medium |
| J10 | Israeli restaurant direct ordering | 59 | 47 | 57 | 53.8 | −12 | **41.8** | Medium (contradicting) |
| J12 | EU 72-hour kits | 48 | 44 | 61 | 49.0 | −10 | **39.0** | Low |
| J13 | Memory phone | 48 | 52 | 44 | 48.8 | −12 | **36.8** | Low |
| J5 | Rooftop solar cleaning | 48 | 43 | 38 | 44.0 | −10 | **34.0** | Low |

**Penalty notes:**
- Penalties stay within the Phase 3 range of 9–14.
- J8 gets 14, the same as the Phase 2 monday.com app, because its stated differentiator was contradicted.
- J6's and J10's contradictions are reflected in their criterion scores (proven channel, defensibility), so they are not also given a larger penalty.

**Rankings by objective:**
1. **Fast cash flow** (realistic time to $2–5k/month): J3 Polish citizenship (high ticket per case) → J1 memoir books (holiday peaks) → J7 Apify (compounds over 6–12 months).
2. **Scalable business:** J7 (62) → J8 and J11 (57; J8 has no differentiator, J11 has a licensing question) → J4 (56).

   **No Phase 4 candidate has credible evidence for Track B ($10–30k/month).** J7 gets there only through a breakout hit.
3. **Balanced (evidence-adjusted):** J7 55.4 → J1 51.0 → J2 48.2 / J9 48.0.

**Labour dependence:**
- Scales beyond founder hours: J7, J9, J6, J1, J2.
- Mixed: J4.
- Labour-dependent: J3, J10, J5, J13.

---

## 7. Cumulative leaderboard (all phases, Phase 3 rubric)

| Rank | Opportunity | Phase | Adjusted |
|---|---|---|---|
| 1 | Blender/VRChat pipeline add-ons (H7) | 3 | **59.4** |
| 2 | Hobbyist college-baseball data API (H6) | 3 | **57.2** |
| 3 | **Niche Apify Actors (J7)** | **4** | **55.4** |
| 4 | Meshtastic family kits (H1) | 3 | **54.6** |
| 5 | UK MTD prep for accountants | 2 (rescored) | 52.6 |
| 6 | monday.com Israeli invoicing app | 1 (rescored) | 52.0 |
| 7 | **Hebrew/Russian memoir books (J1)** | **4** | 51.0 |
| 8 | Ketubot (H10) | 3 | 50.6 |
| 9 | Israeli allocation verification | 1 (rescored) | 49.8 |
| 10 | Spanish Holy Land box (H8) / non-US alerts (H5) | 3 | 49.4 |
| … | J2 48.2 · H4 48.2 · J9 48.0 · H9 47.8 · J4 47.4 · J6 47.4 · EU packaging 47.2 · J8 47.0 · … · Atlassian 44.8 | | |

**Cross-phase verdict:**
- J7 enters at #3. It is 1.8 points below H6 and 0.8 above H1, both inside the roughly 5-point noise band. It is comparable to them, not better.
- J1 lands mid-table.
- No Phase 4 idea displaces H7 or H6.

**Structural pattern across Phases 3–4.** The top four are all distributed through a marketplace or an existing channel where purchases are visible (Superhive, a Patreon-style API, Apify, Amazon). The rubric's distribution and capital criteria reward this, and Phase 3 already flagged that the rubric favours software.

---

## 8. Three most promising new discoveries

**Best quick-profit: Polish/EU citizenship research front end (J3).**
- High ticket (₪1,500–4,000) and growing demand from motivated applicants (9,173 applications a year). A handful of cases a month reaches Track A.
- *Most important assumption to validate:* Israeli applicants will pay a separate fixed-price eligibility and archive-retrieval product, rather than a lawyer's bundled package, and it can be structured legally without fee-sharing with lawyers.

**Best scalable: Niche Apify Actors (J7).** This comes with a caveat: Track B depends on a hit, and no Phase 4 idea showed credible Track B evidence.
- *Most important assumption to validate:* a newly published Actor for an underserved regional or vertical source reaches about 50 or more monthly paying users within 60 days.

**Best risk-adjusted: Niche Apify Actors (J7).** It has the highest adjusted score, needs about $0 in capital, has a confirmed 80% revenue share and an observable payout pool, fits the founder's skills, and failure costs only days.
- Runner-up: **J1, Hebrew/Russian memoir books.** It is the best new consumer idea, but conditional. *Most important assumption to validate:* MyHeritage MyStories does not produce Hebrew RTL books, and Israeli gift buyers pre-order at ₪450 or more with an acquisition cost under ₪150.

---

## 9. Research limitations

- **The search quota was exhausted** before Phase 4 discovery really started. Discovery agents got 6–9 searches each, the auditor 2, the red team about 10. As a result:
  - Phase 4's "no competitor found" statements are weaker than Phase 3's.
  - Hebrew-market competitor scans were mostly impossible: Israeli memoir and personalised-book businesses, diaspora grave-care sites, Hebrew lawyer pricing.
- **Sources that refused fetches:** Reddit, Etsy, eBay, Kickstarter, Amazon, Fiverr, BuiltByBit, aescripts, Unreal Fab, Wolt (including Wolt Drive), Mishloha, Apex, Capterra-IL, Notes from Poland (on the audit's attempt), and parts of gov.il.
- **Unverified decisive items:**
  - MyStories' Hebrew support.
  - Israeli acquisition cost for gift products.
  - Lawyer pricing and fee-sharing rules for citizenship cases.
  - How Apify earnings are distributed per developer.
  - Search volume for diaspora grave care.
  - Licensing for TASE research.
  - Prop firms' copier policies.
  - Wolt Drive pricing in Israel.
  - The count of commercial solar installations in Israel.
- **Coverage gaps:** agent C produced no discovery in marine, agriculture inputs, fleets, printing, refurbished trade equipment or tourism.
- **Scores are structured judgments.** Differences under about 5 points are noise. The rubric favours software (disclosed in Phase 3).
- **No browser or signed-in account was used in Phase 4.** No customers were contacted, nothing was bought, and nothing was built.
