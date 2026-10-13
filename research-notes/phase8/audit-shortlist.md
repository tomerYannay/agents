# Phase 8 Evidence Audit of shortlist N1–N14 (P8-AUDIT), 2026-10-13

**Auditor:** independent Evidence Auditor (P8-AUDIT).

**WebSearch:** 5 of 10 used, all logged as `P8-AUDIT` in `research-notes/search-log.txt`:
1. German online hygiene training and incumbents
2. CONTPAQi SDK/API
3. Fresha/Booksy native Google-review requests
4. German STR guest-messaging outsourcing
5. Unified-API third-party connector programmes

**Primary sources re-opened (WebFetch, or curl/Python with a generic `research-bot` User-Agent; no personal identifiers sent):**

| Source | What was checked |
|---|---|
| gesetze-im-internet.de | §43 IfSG, full text |
| frankfurt-main.ihk.de | Schulungsanbieter list |
| German providers | hygieneschulung.org, hygieneschulung24.de |
| alimentiaformacion.com | price, legal basis, disclaimers |
| TrustMRR `.md` profiles | Alimentia (startup-a66a92db7a72), photo-sharing, Coucou (startup-a8e78dd113c0), myfrank, hidden-business-8, soldcomps, propgpt-ai-props-analysis |
| Empire Flippers public API | #94286, #86244, #85405, #91698, #95287, #96752, including monthly P&L |
| CONTPAQi | contpaqi.com |
| AR Software | GitHub README, arsoft.net product page, GitHub repo API |
| NuGet | search API for CONTPAQi packages |
| Mexican SaaS sites | homepage census of 38 sites |
| Fresha | help centre (ratings and reviews) |
| Booksy | Booksy Biz blog (reviews) |
| Supergood | report cards for Fresha and Booksy |
| Crowd Supply | /apply page; MiciMike project page |
| WordPress.org | plugins API, 6 queries |
| iTunes Search API | 23 queries across US, IL, BR, ES, DE, PL and NL |
| Prediction markets | docs.kalshi.com, docs.polymarket.com |
| Other | sold-comps.com, chift.eu, kululu.com |

**Blocked or unreadable (none bypassed):**
- kalshi.com developer agreement: HTTP 429, so its terms were not read.
- Fresha `/for-business/integrations` and the help-centre Data Connector article: JS-rendered, and no article text was retrievable. `fresha.com/terms` returned 404.
- Shopify App Store search for "contpaqi": JS/login wall.
- Five sites returned 403 to the Mexican SaaS census: konfio.mx, tiendanube.com/mx, siigo.com/mx, kapital.mx and netsuite.com.
- Indeed/Glassdoor-type sources were not attempted.

**Scratch:** `scratchpad/p6plus/P8-audit/{data,scripts}`. The scripts are `wp.py`, `it.py`, `it2.py`, `it3.py` and `mx.py`; the raw JSON/HTML is in `data/`.

**Scoring convention:** frozen rubric. Criterion scores are 0–5 in rubric order:

| Group | Criteria | Step values |
|---|---|---|
| CF | Spending · Speed · Capital · Margin · Labour | ×5 · ×4 · ×4 · ×4 · ×3 |
| Scal | Depth · Recurring · Acquisition · Leverage · Defensibility · Fit | ×3 · ×4 · ×4 · ×4 · ×3 · ×2 |
| Dist | Clarity · Discoverability · Proven · First · Beyond | ×4 · ×4 · ×6 · ×3 · ×3 |

Calibrated against Phase 7: M1 = 3,2,4,5,3 / 2,5,2,4,1,5 / 4,3,2,2,4 → 68/63/58, Adjusted 52.0.

## Summary table

| ID | Verdict | Suggested penalty | One-line reason |
|---|---|---|---|
| N1 German food-hygiene certificate | **Killed** as specified (B2C Alimentia clone); residual B2B variant **Weak** | 13 | §43(1) IfSG reserves the initial briefing to the Gesundheitsamt or a doctor it commissions. The job-seeker certificate Alimentia sells in Spain has no private German equivalent. The employer-side LMHV/Folgebelehrung market already has online sellers at €29. |
| N2 Certification study kits | **Partly supported** | 12 | #94286 figures reproduce, but it is a **co-broker deal** (materials prepared by an outside broker, not EF), and profit **fell from ~$51k/mo (H2 2025) to ~$11.7k/mo (Apr–Jun 2026)**. It is distinct from the excluded apps by format and channel only. |
| N3 CONTPAQi API | **Weak** | 13 | No official CONTPAQi API or public SDK licence was found. AR Software is a **cloud web service + local sync agent** at $720/yr per RFC, so the "hosted gap" is narrower than claimed. One large vendor (Bind ERP) built its own CONTPAQi connector. Paid demand is unmeasured. |
| N4 German STR guest desk | **Partly supported** | 12 | #86244 reproduces ($8.6k/mo profit, 19% margin; monthly profit ranged −$345 to $18.8k). No German per-unit desk surfaced, but English-language 24/7 desks exist (Valcove $9.95/h, Tailwind, Guesty GCS). German newcomer CAC is unknown. |
| N5 Local-language Meta-ads store | **Weak** | 13 | The comparables are real but volatile. The Czech #91698 averaged **−$4.1k/mo profit over Feb–May 2026**, and its owner works **30 h/week**, not "home-fulfilling solo, low hours". The $2k budget allows about two tests. |
| N6 Crowd Supply developer tool | **Supported** (channel stats), **weak** fit | 11 | "Turns away over 75%", ">90% funded", 12% fee and a 50–100% matching order are all verified on /apply. Hardware lead time (MiciMike ships Jan 2027) and founder fit are the problem. |
| N7 Collectible-scanner micro-studio | **Partly supported** | 12 | Early-cohort indie wins are real (Acorn 15.5k ratings). But studios now enter new booms within months: Next Vision's ToyWorth (Jun 2026) is already #2 in LEGO value, and 112 card-scanner entrants arrived in 2026. |
| N8 Prediction-market companion | **Weak** | 13 | PropGPT is verified ($82k MRR). But companion newcomers are mostly <50 ratings: 224 apps released 2025+ across 3 searches, and only Prediction Radar (525), SharpPicks (116) and Ratio (105) among true companions exceed 100. Kalshi's agreement was blocked (429). |
| N9 Event photo-sharing, new language | **Partly supported** | 13 | The DE comparable reproduces ($549k all-time) but is **strongly seasonal**: $6.5–9.3k/mo Nov–Feb against $28–52k Apr–Aug. It is listed for sale at $1.5M. The target market is unchosen. Global free-to-start web incumbents exist (Kululu, POV, WedShoots). |
| N10 Hebrew AI-app copy | **Weak** | 13 | The calorie category is already taken by 3 Hebrew-native apps plus a localised entrant: Calcounti 3,372, Calz 2,826, CalBuddy 2,520 and Cvidya 875 ratings. No unserved category is named. |
| N11 Salon review add-on (Fresha/Booksy) | **Killed** (Fresha leg); Booksy residual **Weak** | 14 | **Fresha natively ships "Google Rating Boost"**, which sends clients to Google after the Fresha review. Booksy auto-requests reviews 30 min and 24 h after each appointment, but on its own platform. Its API is alpha and partner-gated. MyFrank is not a booking add-on. |
| N12 WooCommerce GMC monitor | **Partly supported** | 13 | The Shopify analogue reproduces ($14,745 MRR, 244 subs; flat ~$8k Jan–Jul, then a jump; for sale at 0.9×). **The "no WooCommerce monitor" claim is refuted**: three 2026 WP.org newcomers exist with 0–10 active installs. |
| N13 Connector supplier to aggregators | **Unsupported** | 14 | There is no evidence any unified-API vendor licenses or revenue-shares third-party connectors. Chift sells its own "Local agents". |
| N14 Padel/beach-tennis organiser apps | **Weak** | 13 | In the BR "padel americano" search, **0 of 162** apps released 2025+ have ≥100 ratings. Rank-to-revenue is unknown. |

---

## N1. German online food-hygiene certificate (E1)

### Evidence

**§43 IfSG** [Verified: gesetze-im-internet.de/ifsg/__43.html, 2026-10-13]
- Abs. 1: a person may start food work only with a certificate "des Gesundheitsamtes oder eines vom Gesundheitsamt beauftragten Arztes". It must show that they were "vom Gesundheitsamt oder von einem durch das Gesundheitsamt beauftragten Arzt belehrt".
- **So a private online provider cannot deliver the Erstbelehrung.** Only a doctor individually commissioned by a Gesundheitsamt can, and that commission is local, so it is not something the founder can obtain [Hypothesis on obtainability].
- Abs. 4: the **employer** delivers the follow-up briefing after the person starts work and every 2 years. The employer may use third parties, per IHK.

**Gesundheitsämter are digitising the Erstbelehrung themselves.** Dresden has a fully online Belehrung, and Berlin reported digitisation in April 2026 [Secondary: search snippets, P8-AUDIT #1]. This removes the B2C job-seeker demand that drives Alimentia in Spain.

**German incumbents already sell the residual employer products online:**
- **hygieneschulung.org**: €29 net for the LMHV/EG 852/2004 Hygieneschulung and €29 for the §43 Folgebelehrung; "Zertifikat sofort"; "Die Kosten werden häufig vom Arbeitgeber übernommen" [Verified, 2026-10-13].
- **hygieneschulung24.de**: e-learning for whole teams [Verified].
- **IHK Frankfurt provider list** [Verified: frankfurt-main.ihk.de Schulungsanbieter, 2026-10-13]. It names 20+ providers, many online: BAV Akademie, Berliner Hygiene Fachschule, Dr. Berns, FSI, Hygieneschulung.org, **Metro online**, oncampus, SGS and TÜV Süd.
- A ZFU-listed online Folgeschulung at €29 [Secondary: snippet].
- **Price wedge:** Alimentia's €12 sits below the €29 incumbents, but the German buyer is the employer, and employers may deliver the briefing themselves at no cost.

**Alimentia** [Verified: trustmrr.com/startup/startup-a66a92db7a72.md, synced 2026-10-13]
- Stripe-verified: $37,108 last 30 days; $167,849 all-time; founded 2026-04-09; X followers 1; channels SEO, Google Ads and Instagram; one-off payments (MRR $0).
- **Agent's figures reproduce** (minor drift: $167.6k became $167.8k).
- Monthly revenue: Apr $3.8k, May $15.4k, Jun $26.7k, Jul $34.5k, Aug $33.2k, Sep $39.6k. It has **plateaued around $33–40k since July**.

**Spanish legal basis** [Verified: alimentiaformacion.com, 2026-10-13]
- The site sells at €12 including VAT and cites RD 109/2010 and Reg. (CE) 852/2004.
- It also says "No somos un organismo público…", "No existe un carnet 'oficial' del Ministerio de Sanidad" and that AESAN "no homologa ni expide" the certificate.
- So the Spanish market rests on employer and job-seeker custom, not a state-issued card. Germany has the opposite structure for the initial certificate.
- RD 109/2010 itself was not opened [Secondary, as stated by the site].

**Still unknown:** German CPCs and search volumes [Unknown]. Whether Gesundheitsämter accept €12 online LMHV certificates [Unknown; the €29 incumbents operate, which suggests online is accepted for LMHV and the Folgebelehrung].

### Verdict and scores
- The core claim ("Alimentia model transfers to Germany") is **refuted** for the B2C certificate.
- The residual (a cheaper online LMHV + Folgebelehrung for employers, with renewal tracking) is a me-too entry into an incumbent field.
- Suggested scores for the residual:

| Group | Scores | Total |
|---|---|---|
| CF | 2,3,5,4,4 | 70 |
| Scal | 3,2,2,4,1,3 | 50 |
| Dist | 4,3,1,2,3 | 49 |

- Balanced 57.8; penalty 13 → **44.8**.
- **Recommend dropping from finalists.** Austria and Italy variants need separate legal checks.

---

## N2. Certification study kits via paid social (C2)

### Evidence

**EF #94286 public API** [Verified: api.empireflippers.com listings?listing_number=94286, 2026-10-13]
- Revenue $2,098,197 and profit $433,278 over 12 months; first revenue 2024-05-01; asking $950k; For Sale; 10 h/week; B2C; 3 Shopify sites; summary text as the agent quoted.
- **New facts the agent missed:**
  1. **"This is a co-broker deal … all materials have been prepared by the broker."** The P&L was prepared by an outside broker, so the agent's "EF-vetted" label overstates it. Relabel as [Anecdote/broker-presented, listed on EF].
  2. **The trend is down sharply.** Monthly profit:

     | Period | Revenue/mo | Profit/mo | Margin |
     |---|---|---|---|
     | H2 2025 | $210k | $50.9k | 24% |
     | H1 2026 | $140k | $21.3k | 15% |
     | Apr–Jun 2026 | $105k | **$11.7k** | **11%** |

     The worst months were Apr 2026 at $6.6k and May 2026 at $5.6k.
  3. Expenses run at 76–94% of revenue, consistent with heavy Meta spend. Newcomer CAC remains [Unknown].
- The "$36.1k/mo" headline is the 12-month average, not the current run-rate.

**Distinct from the excluded "licensure exam-prep apps" (Phase 2)?**
- Partly. The format (print + PDF bundle) and channel (Meta ads) differ.
- The demand pool is the same: credential candidates. A red-team reviewer could reasonably call this a repackage.
- The niche of #94286 is undisclosed (teaser PDF and data room are gated behind unlock; not accessed).

**PTCB** volume (49,253 exams, 2025) is cited by the agent [Verified by agent; not re-opened].

### Verdict and scores
- Spending is real at scale, but the single comparable is broker-presented and deteriorating, which suggests rising CAC in its niche.

| Group | Scores | Total |
|---|---|---|
| CF | 4,3,3,3,4 | 68 |
| Scal | 3,1,3,4,1,2 | 48 |
| Dist | 4,3,2,2,4 | 58 |

- Balanced 58.0; penalty 12 → **46.0**.
- **Decisive:** a newcomer can buy a customer for under 40% of AOV in a credential with weak incumbents. Testable for ~$1k.

---

## N3. CONTPAQi self-serve API (F1; F3/F5 variants)

### Evidence

**CONTPAQi itself**
- The homepage links only to `/distribuidores` and ConectaT, a community for accountants.
- No developer, SDK or API section was found [Verified: contpaqi.com, 2026-10-13].
- A search found no official REST API or public SDK licence. Licences are sold annually through certified partners [Secondary: Guía deSoftware via snippet, P8-AUDIT #2].
- **The SDK terms for hosted third-party use remain [Unknown].**

**AR Software** [Verified: GitHub README; arsoft.net/contpaqi-comercial-api; GitHub API, 2026-10-13]
- The README: "Haz interfaz con … CONTPAQi Comercial Premium a través de un servicio web en la nube", with a downloadable "sincronizador". Licence "$720 dlls por RFC" per year; free for development; an additional licence gets 20% off. It has Swagger/OpenAPI docs, and the page is in English.
- **Correction to F:** this is already a cloud API plus local agent, Conductor-shaped. The remaining wedges are price (below about $60/mo), multi-product coverage (Contabilidad, Nóminas) and polish. "Only hosted multi-tenant option" is not a credible wedge.
- Repo: 15 stars; code last pushed Jun 2024. NuGet SDK releases continue (v6.3, Aug 2026). Sales volume is [Unknown].

**NuGet:** 131 packages match "contpaqi". The top download counts belong to T-Systems Mexico's ContpaqiNube/Node packages, 160k downloads on the largest [Verified: NuGet search API]. That is legacy CONTPAQi cloud work, not a current API offer.

**Demand census** (homepages only; 33 reachable of 38) [Verified, 2026-10-13]
- **Bind ERP** markets "Único integrado con CONTPAQi Contabilidad" via its own "CONECTA BIND".
- **Alegra** offers migration from CONTPAQi/Aspel.
- cfdi.com.mx is CONTPAQi's own e-invoicing.
- The other 30 sites (fintechs, payroll, POS, Belvo, Facturapi) do not mention CONTPAQi on their homepage.
- Reading: there is some vendor need, but the largest vendor built it in-house. Fintechs show no visible demand [weak signal; homepages only].

**Conductor pattern rests on n=1 in TrustMRR, and the QBD niche drew 3 clones** [from agents D and F; not re-verified here].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 2,2,4,5,3 | 63 |
| Scal | 2,5,2,4,1,4 | 61 |
| Dist | 3,3,1,2,3 | 45 |

- Balanced 58.6; penalty 13 → **45.6**.
- The variants (TallyPrime with a crowded indie field; Sage Pastel with Sage gating) score no better.

---

## N4. German human-plus-AI STR guest desk (C1)

### Evidence

**EF #86244** [Verified: EF API, 2026-10-13]
- Sold; $44,607/mo revenue, $8,618/mo profit, 19% margin; first revenue 2023-11; 5 h/week; not a co-broker deal.
- **Monthly profit is volatile:** −$345 in Nov 2024, $3.0–5.8k in Dec 2024–Mar 2025, $9.4–18.8k in Apr–Sep 2025.
- Reproduces the agent.

**Competitors** [Secondary: snippets, P8-AUDIT #4]
- Guesty Guest Communication Services (price unpublished; agent verified that it exists).
- Tailwind (Extenteam), with agents in a unified inbox.
- Valcove Hospitality at $9.95/hour for 24/7 coverage, claiming 750+ properties.
- German full-management agencies at 10–30% of rental income.
- **No German-language per-unit desk surfaced.** Absence is not proof.

**Unknown:** German manager counts, willingness to pay, CAC, and PMS API terms (Smoobu).

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 4,3,4,2,2 | 62 |
| Scal | 3,5,2,3,1,2 | 56 |
| Dist | 4,2,2,2,2 | 48 |

- Balanced 56.8; penalty 12 → **44.8**.
- It is a labour business (Track C) with thin margins. The language wedge is plausible but untested.

---

## N5. Local-language Meta-ads store in a small EU market (B8-3/B8-4/C4)

### Evidence (EF API, all non-co-broker) [Verified, 2026-10-13]

| Listing | Facts | Monthly profit |
|---|---|---|
| **#85405** (SE/DE/NO) | Sold; first revenue 2023-02; 6 h/week; margin 14% | Rose from $16k (Sep 2024) to $97k (May 2025); comparable is real |
| **#91698** (CZ/SK/HU) | For Sale; first revenue 2025-04; **30 h/week**; margin 37% | $29–62k in Jun 2025–Jan 2026, then **Feb $350, Mar −$21.1k, Apr $7.2k, May −$2.8k** |
| **#95287** (FR/CH/BE) | Profit swings | −$3.8k to $15k |
| **#96752** (DE/GB/FR) | — | −$1k to $38.8k |

- #91698 is a hero-product burnout: the "$25.5k/mo" is a 12-month average.
- **Reading:** survivor P&Ls show high variance and fast product decay. They are not stable newcomer outcomes. The founder's $2k covers about 2 product tests. VAT/OSS, GPSR and COD add fixed load [agent; not re-verified].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 4,3,2,2,3 | 57 |
| Scal | 4,1,3,3,1,1 | 45 |
| Dist | 3,3,2,2,3 | 51 |

- Balanced 51.0; penalty 13 → **38.0**.

---

## N6. Firmware-first tool on Crowd Supply with a manufacturer partner (B8-1)

### Evidence

**/apply** [Verified: crowdsupply.com/apply, 2026-10-13]
- "we turn away over 75% of applications"
- "over 90% of projects launched … reach their funding goals"
- "typically 12%" fee; matching order "typically between 50% and 100%"
- "over 122,000 newsletter subscribers"
- All of Agent B's channel claims reproduce.

**MiciMike** [Verified: project page, 2026-10-13]
- $132,699 raised on an $8,000 goal from 637 backers at $99.
- Elecrow builds it under Project Aviary.
- **Not yet delivered:** pre-orders ship 2027-01-08, after a "Delivery Delay" update on 2026-10-09.
- Agent B's cohort file was spot-checked: the MiciMike line matches.
- Medians (first-timers $26k; developer tools $21.2k) were not recomputed [Secondary: agent B data].

**Unknown:** partner payment terms before payout, post-campaign sales, and the founder's hardware capability.

### Verdict and scores
- The channel is the best-measured newcomer channel in Phase 8. The model is slow, one-off and outside the founder's core skills.

| Group | Scores | Total |
|---|---|---|
| CF | 3,1,3,3,2 | 49 |
| Scal | 2,1,2,2,2,2 | 36 |
| Dist | 4,3,3,2,3 | 61 |

- Balanced 46.2; penalty 11 → **35.2**.

---

## N7. Trend-timed collectible value-scanner micro-studio (A1)

### Evidence (iTunes Search API, US, 2026-10-13) [Verified]

| Search | Entrants | Result |
|---|---|---|
| "card scanner value" | 48 in 2025 (10 reached ≥1k); 112 in 2026 (5 reached ≥1k, 16 ≥100) | Leaders: StarSnap 28.0k (Next Vision), Acorn 15.5k (indie), FoilSnap 14.4k (Next Vision), Cardly 11.3k (Scate) |
| "lego minifigure value" | 26 in 2026 | Brickify 5.9k; **ToyWorth (Next Vision, released 2026-06-29) already 984** |
| "pop mart scanner" | — | No 2025–26 app ≥1k; best is a Funko scanner with 246 |
| "labubu" | — | No dedicated scanner hit |
| "coin identifier" | 81 in 2026 | 0 at ≥1k |
| "sneaker price checker" | — | No winner |

- **Reading:** some indie early-entry wins exist, but the boom-to-studio window now looks like **weeks to a few months**, not 6–12.
- Revenue per app is [Unknown].
- The ThriftAI revenue estimate remains [Anecdote].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 3,3,4,4,2 | 65 |
| Scal | 3,4,2,3,0,4 | 53 |
| Dist | 3,3,2,2,2 | 48 |

- Balanced 56.8; penalty 12 → **44.8**.
- It is a hit-seeking portfolio with a real Track B tail.

---

## N8. Prediction-market research/alert companion (A2)

### Evidence

**PropGPT** [Verified: TrustMRR .md, Superwall-verified]
- $82,021 MRR; 2,101 subscriptions; $9.99/week; 2,629 US ratings; founder with 194 X followers.
- Monthly revenue peaked at $107.7k in May 2026 and was $86–88k in Jul–Sep.

**iTunes, 3 US searches; 224 unique apps released 2025+** [Verified, 2026-10-13]
- **Platforms dominate:** DraftKings Predictions 15.5k, FanDuel Predicts 6.7k, OG 1.7k, Fanatics Markets 1.2k.
- **True companions:** Prediction Radar 525, Ratio 105 (both Quad Innovations), SharpPicks 116.
- The rest are under 50: "Polymarket Prediction Alert AI" 24, "Share: Polymarket Predictions" 44, FlipX 37.

**APIs**
- Kalshi docs: "By continuing to use or access Kalshi's API, you are agreeing to be bound to our Developer Agreement". The **agreement itself was blocked (HTTP 429)**.
- Polymarket has public market-data SDKs [Verified: docs.polymarket.com].
- Commercial-redistribution terms are [Unknown].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 3,3,5,4,2 | 69 |
| Scal | 3,4,2,3,0,4 | 53 |
| Dist | 3,3,1,2,2 | 42 |

- Balanced 57.2; penalty 13 → **44.2**.

---

## N9. QR guest photo-sharing in an under-served language market (E3)

### Evidence

**German comparable** [Verified: trustmrr.com/startup/photo-sharing.md]
- $29,333 last 30 days; $549,349 all-time; founded 2024-04; 0 followers; Google Ads + SEO + Instagram; 45% margin.
- **Listed for sale at $1.5M (4.2×).**
- **Seasonality:** Nov 2025–Feb 2026 at $6.5–9.3k/mo; Apr–Aug 2026 at $28–52k/mo.

**Competitor checks** (iTunes; app-only, so the web players are under-counted) [Verified, 2026-10-13]

| Market | Finding |
|---|---|
| IL | Hebrew searches show only tiny 2025–26 entrants (EZ Invite 7, RollieBox 3, Momentz 3, Sunframe 1) |
| PL | 2026 entrants with 1–4 ratings |
| NL | Wedbox 682 |
| DE | celebrate 15.6k, Wedbox 1.1k, weddies 413, EventPics 148 |

- **Kululu** (kululu.com) sells QR event photo sharing globally, web-based, "Start free" [Verified].
- An open Israeli market is therefore plausible, but web competitors are [Unknown] and free anchors exist.
- Market choice, CAC and per-event price are [Unknown].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 4,3,5,3,4 | 76 |
| Scal | 2,0,3,4,1,4 | 45 |
| Dist | 4,3,2,2,3 | 55 |

- Balanced 59.4; penalty 13 → **46.4**.

---

## N10. Hebrew-localised copy of a proven AI consumer category (E2)

### Evidence

**iTunes IL "ספירת קלוריות"** [Verified, 2026-10-13]

| App | Released | IL ratings |
|---|---|---|
| Calcounti | 2025-03 | 3,372 |
| Calz (Wachanga) | 2025-05 | 2,826 |
| CalBuddy | 2025-05 | 2,520 |
| Cvidya | — | 875 |

- 126 apps released 2025+, of which 9 have ≥100 ratings and 3 have ≥1k.
- The example category is closed.
- No alternative category with verified demand is named.
- CalBuddy's revenue remains [Anecdote: Starter Story].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 3,3,3,3,2 | 57 |
| Scal | 1,4,2,3,0,4 | 47 |
| Dist | 2,3,2,2,2 | 44 |

- Balanced 50.4; penalty 13 → **37.4**.

---

## N11. Review-and-rebook add-on for Fresha/Booksy salons (D1/D3)

### Evidence

**Fresha native feature** [Verified: fresha.com help centre "Ratings and reviews overview", 2026-10-13]
- "After every completed appointment, clients are automatically invited to share star ratings…"
- "With **Google Rating Boost**, clients are encouraged to continue to Google after leaving a review on Fresha and share the same review there."
- Fresha's own training module: "Turn positive Fresha feedback into more Google reviews… Connect your profile, choose which clients are invited."
- Fresha also imports Google reviews ("Bring your Fresha and Google reviews together").
- **This removes the core gap D1 assumed for Fresha** ("platform with no Google-review flow").

**Booksy native feature** [Verified: biz.booksy.com blog]
- Automated review requests 30 minutes after the appointment, plus a 24-hour follow-up, to **Booksy's own** reviews.
- No Google flow is mentioned, so the gap is still open on Booksy.
- **Booksy API:** "Public API … at alpha.docs.booksy.net … alpha status and partner-gated" [Vendor claim: Supergood report card, 2026-10-12].

**Fresha API:** no merchant API or webhooks; read-only BI Data Connector [Vendor claim: Supergood]. Fresha's own Data Connector page was JS-rendered and unreadable, so this is not independently verified.

**Coucou** [Verified: TrustMRR startup-a8e78dd113c0]
- $5,913 MRR, 50 subscriptions, €67/€97; founded 2025-02; 299 X followers.
- Took ~19 months to reach $5.9k; monthly revenue $1.6k (Nov 2025) to $5.8k (Sep 2026).
- **Reproduces.**

**MyFrank** [Verified: TrustMRR myfrank]
- $9,873 MRR, 175 subscriptions, 0 followers; **listed for sale since 2026-01-13**.
- **Not a booking-platform add-on.** It does QR per-employee reviews for multi-site hospitality and retail.
- Revenue fell from $8.2k (Dec 2025) to $1.4k (Feb 2026), then rose to $10.3k (Sep 2026).
- It is a weak analogue for N11.

### Verdict and scores
- Killed for Fresha. A Booksy-only residual has a partner-gated API and Booksy could ship the same "boost".
- Scores for the residual:

| Group | Scores | Total |
|---|---|---|
| CF | 3,2,4,4,3 | 64 |
| Scal | 2,5,2,4,0,4 | 58 |
| Dist | 4,2,1,2,2 | 42 |

- Balanced 57.2; penalty 14 → **43.2**.
- D3 (Fresha integration API) inherits the same ToS risk and is not separately rescued.

---

## N12. Continuous Google Merchant Center monitor for WooCommerce and agencies (D2)

### Evidence

**Shopify analogue** [Verified: trustmrr.com/startup/hidden-business-8.md, Lemon Squeezy-verified]
- $14,745 MRR; 244 subscriptions (~$60 each); founded 2025-03; 0 followers; channels affiliate, influencers and partnerships.
- Monthly revenue: $5.4k (Nov 2025) → ~$7.7–9.0k flat (Jan–Jul 2026) → $11.4k (Aug) → $14.5k (Sep).
- **For sale since 2026-02-15 at $175k (0.9× revenue)**, with 10 offers. A low multiple can signal buyer doubt about durability [Hypothesis].

**WordPress.org plugins API** [Verified: api.wordpress.org, 2026-10-13]
- **Refutes "no WooCommerce monitor found".** 2026 newcomers targeting exactly this:

  | Plugin | Added | Active installs |
  |---|---|---|
  | `suspension-shield-for-woocommerce` ("Audit your WooCommerce store for the price, stock and policy issues behind Google Merchant Center suspensions") | 2026-07-20 | 10 |
  | `feedproof-for-woocommerce` ("Catch the WooCommerce product data issues behind Google Merchant Center disapprovals") | 2026-06-19 | 0 |
  | `pw-feed-store-readiness-audit` ("Free Merchant Center readiness and policy-risk audit tools") | 2026-08-06 | 0 |
  | `clean-image-for-google-merchant-wc` | 2025-12 | 30 |

- **Incumbent context:** Google for WooCommerce (`google-listings-and-ads`) has 800k installs and surfaces Merchant Center issues inside WordPress. Feed plugins have 10k–90k installs.
- **Newcomer outcome in the WP.org channel: ~0–10 installs in 2–4 months**, consistent with Phase 5's WooCommerce finding.

**Agency demand and recurring willingness to pay among WooCommerce merchants** are [Unknown].

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 3,3,5,5,4 | 79 |
| Scal | 2,3,2,4,0,5 | 52 |
| Dist | 4,3,1,2,2 | 46 |

- Balanced 61.6; penalty 13 → **48.6**.
- It is the highest of the shortlist because the build is cheap, margins are software-level and founder fit is high. The channel is the weak point: it needs the analogue's affiliate/partner route, not WP.org.

---

## N13. Connector supplier to unified-API aggregators (F2)

### Evidence
- A search found no partner-built connector programme, connector marketplace or revenue share at Apideck, Codat, Merge or unified.to. Apideck says it maintains its connectors in-house [Secondary: snippets, P8-AUDIT #5].
- Chift's own navigation lists "Local agents" as a Chift product, so it builds on-prem agents itself [Verified: chift.eu, 2026-10-13].
- Buyers are ~10 named firms; the outcome is binary.

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 1,1,4,4,3 | 50 |
| Scal | 1,4,1,4,1,4 | 50 |
| Dist | 4,2,0,1,1 | 30 |

- Balanced 46.0; penalty 14 → **32.0**.
- It is only an exit option for N3 or M1 (sell the connector), not a standalone business.

---

## N14. Amateur padel/beach-tennis/darts organiser apps outside the US (A3)

### Evidence (iTunes, 2026-10-13) [Verified]
- **BR "padel americano":** 162 apps released 2025+, and **none has ≥100 ratings**. Playtomic has 221 BR ratings.
- **ES "padel":** 84 apps released 2025+; 1 at ≥100, the Red Bull game with 682. Small tools have 21–59.
- **DE "darts scorer":** 100 apps released 2025+; 2 at ≥100. Incumbents (Dart Zähler 24.9k, DartCounter 8.3k) dominate.
- The agent's grossing-chart presence is not contradicted, but rank-to-dollars is [Unknown] and probably tiny.

### Verdict and scores

| Group | Scores | Total |
|---|---|---|
| CF | 2,3,5,4,4 | 70 |
| Scal | 1,2,1,4,0,4 | 39 |
| Dist | 3,3,1,2,1 | 39 |

- Balanced 51.4; penalty 13 → **38.4**.

---

## Shortlist ranking after audit

| Rank | ID | Adjusted |
|---|---|---|
| 1 | N12 GMC monitor | 48.6 |
| 2 | N9 event photo-sharing | 46.4 |
| 3 | N2 certification study kits | 46.0 |
| 4 | N3 CONTPAQi API | 45.6 |
| 5= | N7 collectible-scanner studio | 44.8 |
| 5= | N4 STR guest desk | 44.8 |
| 5= | N1 residual B2B hygiene training | 44.8 |
| 8 | N8 prediction-market companion | 44.2 |
| 9 | N11 Booksy residual | 43.2 |
| 10 | N14 padel organiser apps | 38.4 |
| 11 | N5 local-language store | 38.0 |
| 12 | N10 Hebrew AI-app copy | 37.4 |
| 13 | N6 Crowd Supply tool | 35.2 |
| 14 | N13 connector supplier | 32.0 |

No Phase 8 idea reaches the top cluster (52–55).

---

## Leader second opinions

**H7 Blender add-ons, 55.4 (from 56.6).** Agree.
- The method (embedded JSON `order_items_count`) is stronger than Phase 5's badges.
- The proven-channel cut 3→2 is proportionate.
- Two cautions:
  1. The age buckets are small (n=23–84), so the medians move a lot with a few products.
  2. Survivorship flatters older cohorts, so the "no 2026-vs-2025 decline" finding is weak evidence.
- Do not also cut acquisition (already cut in Phase 5). H7 remains nominal #1 only inside the noise band.

**M1 Sage 50 API: hold at 52.0, or downgrade to 50.8.** I lean to **50.8** (Depth 2→1).
- M1's buyers are vertical SaaS, and for them the ratio is 0.12 (0 of 97 in four verticals), closer to the kill line (0.08) than the keep line (0.2).
- The overall 0.19 is lifted by AP platforms that build in-house.
- Phase 8 adds context that does not directly contradict the decisive assumption but lowers the prior:
  - Conductor is the only legacy-integration API in ~7.9k TrustMRR profiles (Agent D).
  - The QBD niche drew three priced clones within ~6 months (Agent F).
  - In Mexico, the largest vendor built its own CONTPAQi connector (this audit).
- Keep penalty 12 until the Sage 50 agreement is read. A red-team case for Defensibility 1→0 (clone speed) would give 49.6; I would not stack it, because Sage's gating cuts both ways.

**H2 rescore (revived smart-home hardware, currently 38.6).** Support only a modest rescore, about +2 to +3, to roughly **41**.
- MiciMike's $132.7k raise is verified, but:
  - it is **undelivered** (ships Jan 2027 after an Oct 2026 delay notice);
  - its motive is **privacy/local control on a device that still works**, not a dead cloud;
  - it is one case.
- That justifies Proven channel +1 (+1.2 Adjusted) and arguably Spending +1 (+2.0).
- The Bose SoundTouch and Wemo shutdowns are [Secondary] and were not re-verified here. No SoundTouch board exists to prove demand.
- Hardware lead time, a copy already in pre-launch (LocalDot) and founder fit keep H2 well below the top cluster.

**SoldComps evidence for M2** [Verified: trustmrr.com/startup/soldcomps.md; sold-comps.com, 2026-10-13]
- **Figures reproduce:**
  - $21,591 MRR; 545 subscriptions (~$40 each); last 30 days $22,075 (+48%).
  - Monthly $347 (Apr) → $968 → $1,070 → $4,337 → $12,791 → $19,984 (Sep 2026).
  - 0 followers; domain rating 10; not listed for sale; plans $0/$9/$29/$79.
- **Data method:** "Every request fetches data in real time directly from eBay" and "We monitor every site and ship parser updates", i.e. HTML parsing. "Not affiliated with the marketplaces it supports". Also sold via Apify and RapidAPI.
- **Reading:**
  - It is a genuine audience-free outlier and a counter-example to the Apify newcomer median.
  - It is n=1 and about 6 months into revenue. The ToS and blocking risk is real.
  - M2 still names no dataset.
- **Recommendation:** hold M2 at 44.4. At most, Proven channel 1→2 (+1.2 → 45.6), with penalty held at 13.

## Decisive unverified assumptions (finalist candidates)

| ID | Assumption |
|---|---|
| N12 | WooCommerce merchants or agencies pay a recurring fee (not a free or $99 one-off) at a rate comparable to the Shopify analogue, reached through agency/affiliate partners rather than WP.org |
| N9 | Google Ads cost per paid event ≤ €30 in a chosen market whose web competitors are measured; off-season revenue covers fixed costs |
| N2 | Newcomer CAC under 40% of AOV in one credential. Note the comparable's own margin fell to 11% |
| N3 | ≥30 vendors pay ~$40/RFC/month despite AR Software at $60 and in-house builds; CONTPAQi terms permit a hosted service |
| N7 | The founder can enter a boom before Next Vision-type studios, a window now measured in weeks to months |
