# Phase 5: Continued Opportunity Discovery

**Date:** 2026-10-12
**Companion reports:** Phases 1–4 (`business-opportunity-report-*.md`)

---

## Bottom line

**Phase 5 did not find a new leader.**

Two new candidates reached the top tier:
- **Hebrew tender and receivership-sale intelligence (K13): 53.6.**
- **A Framer "vertical kit" of functional plugins plus pre-wired templates (K8): 53.2.**

Both sit within scoring noise of the existing #3–#6 positions.

**The most important result is a correction to two earlier leaders.** For the first time, the auditor measured what *new* sellers actually get on the marketplaces those leaders depend on:
- **Apify Actors (J7):** among 390 Actors less than a month old, the median had 1 monthly user. None of the Actors under 3 months old had 100 or more monthly users. Corrected from **55.4 to 50.8**.
- **Blender add-ons (H7):** a typical new Superhive add-on sells fewer than 10 copies in its first 2–3 months. Featured winners do reach 100–2,000+ sales within a year. Corrected from **59.4 to 56.6**.

After these corrections, the **college-baseball data API (H6, 57.2)** leads the cumulative board. Its own distribution evidence has not been re-checked against new entrants, so it should be checked next (see section 9).

The cross-cutting lesson from the six storefronts sampled (Superhive, Apify, Gumroad, JetBrains, Wix, WooCommerce) plus the App Store:
- AI-assisted building has flooded every open marketplace with new listings.
- In every one of them, the typical new listing got close to zero traction.
- Total money flowing through a platform says little about what a newcomer will earn.
- Ideas that can reach buyers directly score relatively better under the existing rubric. Examples: Israeli outreach, Yad2 sellers, Hebrew search.

---

## 1. Research methodology

**Unchanged from Phases 3–4:**
- Six independent discovery agents.
- Shortlist of 13.
- An independent Evidence Auditor and an independent Red-Team Investor.
- Rescoring with the unchanged formula: Balanced = 0.4 × Cash-flow + 0.4 × Scalability + 0.2 × Distribution, minus an evidence penalty of 0–15. The criteria and weights are also unchanged.

**Search budget:**
- I tested search before starting, and it was working again.
- Each agent was capped at 12 searches, with a shared log to avoid repeating queries.
- The refill was only partial. The quota ran out after about 41 discovery searches:

  | Agent | Searches |
  |---|---|
  | A | 6 |
  | B | 9 |
  | C | 7 |
  | D | 4 |
  | E | 3 |
  | F | 11 |

- The quota then refilled partly during the review stage. The auditor ran 16 searches and the red team 2.
- Agents worked around the limit with public data APIs:
  - App Store data: the iTunes Search API, about 100 queries.
  - Gumroad search data.
  - The JetBrains Marketplace API.
  - The Apify Store API: the auditor sampled about 700 Actors.
  - Superhive product pages: about 108 sampled with rate limiting.
- These gave **better new-entrant evidence than any earlier phase.** Community and marketplace sales evidence stayed weak, because Reddit, Etsy, eBay, Fiverr, Kickstarter, Trustpilot (partly), Walmart, Clio and Zendesk blocked automated fetching.

**Other conditions:**
- No browser or signed-in account was used.
- No one was contacted, nothing was bought or built.

---

## 2. New research universe (about 45 distinct ideas)

| Agent | Viable ideas (key evidence) | Killed |
|---|---|---|
| **A Consumer** | **GSPro golf-sim course studio** (GSPro $250/yr; commissions $1.2–5k; designer Patreons with 8–661 paid members) · **Quilting companion app / hobby-app studio** (YarnPal 33,879 ratings, Loopsy 16,509, Sewpal 11,939; quilt apps ≤202) · **Old-handwriting transcription for genealogists** (Transkribus €99–449/yr) · Localized kids' visual-routine app (DE/FR leaders ≤142 ratings) · Bridge bidding app (Cuebids 223) · Dry-fire app | Hunting draw-odds (GOHUNT), sheet-music arranging (~$125 per arranger lifetime), Chessable courses |
| **B Physical** | **Assistive switches + programmable interface** (AbleNet $75; Logitech kit $99.99) · **Film-camera revival kits** (USCamera ~71K sold, snippet) · **Pinball mods + LED controller** · Gym cables and upholstery outside the US · GA flight-sim panels | Laser-material blanks (xTool), boat registration decals |
| **C Traditional** | **Low-minimum packaging broker for Israel** (Packhelp: 125,300 companies) · **Boat charter co-hosting** (Click&Boat: 4,376 reviews/yr) · US boat-transport brokerage · Facility-maintenance aggregator · Small-hotel revenue management · Espresso machine refurbish-and-rent | Israel inbound tourism (1.3M visitors vs 4.6M in 2019), refurbished marine electronics, Israeli fleet services |
| **D Software** | **Trade-specific SketchUp extension** (Curic $99, 327 ratings) · **Hebrew tender and receivership intelligence** (Ifat incumbent) · Gated vertical-platform connectors · Membership for owners of a specific machine (CNC membership $127/mo, 164 ratings, creator-led) · Creative micro-plugins | JetBrains paid plugins (new ones get 10–133 downloads), professional Chrome extensions, Wix/HubSpot micro-apps, regional-marketplace Shopify connectors, pallet-manifest tools |
| **E Distribution** | **Framer vertical kit** ($6.5M+ paid to creators in 2025) · Wix workflow app (Bookings 1,719 reviews at 3.4★; about 60% of new apps have 0 reviews) · Squarespace code plugins · Fixed-scope builds via expert directories · SaaS group buying for Israeli startups · Faire wholesale agency | Cross-platform widgets (Elfsight, Common Ninja), vintage Israeli posters (42 auction lots in about 10 years) |
| **F Contrarian** | **Seller-paid EV battery certificate (Israel)** (>100k EVs; 12–25% capacity variance within a model) · **Overnight court-transcript production** · Legacy feed-in-tariff solar inverter service · Dental-tourism coordination · Orphaned-EV parts (parked) | Nearshoring sourcing agent (needs local people), Turkish-supplier replacement (market already adapted); Florida insurance, trades succession and drone inspection (need local presence) |

---

## 3. Shortlist (13)

| # | Business | Paying customer | Spending evidence | Competition | Differentiation | Acquisition | Capital | Main risk |
|---|---|---|---|---|---|---|---|---|
| K1 | Assistive switches + programmable interface | Families, SLPs/OTs, schools | AbleNet $75, Logitech $99.99 | AbleNet, Enabling Devices, Amazon, volunteer groups | Price, plus app-configured interface | Therapist communities, Amazon | Med (prototype, CPSIA) | Institutional vendor lock; free alternatives |
| K2 | Film-camera revival kits | Film shooters, flippers | Snippet: USCamera 71K sold | USCamera, LowNex | Per-model bundle + video | eBay/Etsy search | Low | ~$12 margin; US fulfillment |
| K3 | Pinball mods + LED controller | Home pinball owners | Mezel catalogue | Mezel, Pinball Life | App lighting | Pinside, owner groups | Low | Tiny volumes |
| K4 | Seller-paid EV battery-health certificate | Israeli EV sellers, car lots | Techno Test paid EV checks from ₪630 | **Techno Test already includes battery checks** | Shareable certificate for listings | Yad2 sellers, car lots | Low–Med (licence unknown) | Adverse selection (DE uptake ~2%); incumbent |
| K5 | Overnight transcript production | US court-reporting agencies | $2.50–4.55/page fees | Verbit, US scopists at $1–1.50/page | Time zone | Associations | Low | Labour-margin; certification |
| K6 | Low-minimum packaging broker | Israeli small brands | Packhelp/noissue abroad | Israeli printers; **online labels exist** | Box configurator, two-tier sourcing | Hebrew search, Facebook groups | Low | Bypass; misprint liability |
| K7 | Boat charter co-hosting | Private boat owners | Click&Boat volume | **Platform's own Boat-Manager role** | Pro management | Listing outreach | Low | Needs on-site staff; seasonal |
| K8 | Framer vertical kit | Framer designers and SMBs | $6.5M+ creator payouts in 2025 | 24 therapy templates; booking via Cal.com/Calendly | Functional plugins + wired templates | Framer Marketplace | ~$0 | New-entrant discoverability; platform dependence |
| K9 | GSPro course studio | Golf-sim owners, clubs | Commissions $1.2–5k | Hobbyist designers | Lidar pipeline | GSPro Discord/forums | Low | ~$12/hr unless automated; likeness |
| K10 | Quilting companion app | Hobby quilters | Category proven (33k-rating apps) | **2026 quilt apps at 0–23 ratings**; PIXELCELL | Deep content | Instagram ads | Med (ad tests) | Paid acquisition cost vs lifetime value; new-entrant traction |
| K11 | Old-handwriting transcription | Genealogists | Transkribus paid tiers | Volunteers, ChatGPT, 0-rating AI apps | Hebrew/Yiddish + human check | Genealogy groups | ~$0 | Free substitutes |
| K12 | Trade-specific SketchUp extension | Small fabricators | Curic $99, 327 ratings | Generic plugins; new entrants 14–22 downloads | Drawing-to-quote for one trade | Trade channel | ~$0 | No trade knowledge; seat counts |
| K13 | Hebrew tender + receivership intelligence | Israeli SMB contractors, investors | Ifat exists (pricing unknown) | Ifat Tenders, free government portals | AI matching + receiver/liquidator sales | Direct Israeli outreach, Hebrew search | ~$0 | Ifat; scraping legality; willingness to pay |

---

## 4. Five deep-dive finalists

**How they were chosen:** The four top scorers are K13, K8, K12 and K10. K12 was dropped as the same marketplace-plugin model as K8. The two fast-cash candidates the red team let survive, K4 and K6, were added.

### F1. Hebrew tender and receivership intelligence (K13): 53.6

- **Offer:** AI-matched daily alerts for Israeli public tenders (ministries, municipalities, government companies, hospitals). Each alert includes a Hebrew summary of eligibility requirements and deadlines. A second feed covers court-receiver, liquidator and enforcement-office asset sales (property, vehicles, equipment), aimed at investors and dealers.
- **Price hypothesis:** ₪150–600/month, with a ₪300 base.
- **Competition:**
  - Ifat Tenders, the "leading tender database in Israel". Its pricing is unknown.
  - Free government portals.
  - Bidspirit, for auctions.
  - Other aggregators may exist; not searched.
- **Entry strategy:** Bundle the receivership-sale feed, which Ifat may not cover (unverified). Price below Ifat and offer a free 2-week digest. Requirement-matching is the AI advantage. Sell directly to contractor associations, SMB accountants and real-estate investor groups. This avoids depending on a marketplace.
- **Economics [Hypothesis]:** Costs are about ₪1–1.5k/month for hosting, LLM and scraper maintenance.

  | Scenario | Subscribers | Revenue | Owner profit |
  |---|---|---|---|
  | Downside | 10 | ₪3k/mo | ~$400/mo |
  | Base | 60 | ₪18k/mo | ~$4.4k/mo |
  | Upside | 200 | ₪60k/mo | ~$15k/mo |

  About 45 subscribers are needed for roughly $3k/month owner profit.
- **Founder labour:** 4–6 weeks to build, then 5–10 hours/week maintaining scrapers, plus sales.
- **Limitations:**
  - **Pricing, subscriber counts and willingness to pay are all unverified.**
  - Legality of scraping court and Reshumot sources is unverified.
  - The penalty is 14, the highest this phase.

### F2. Framer vertical kit (K8): 53.2

- **Offer:**
  - Working plugins (booking/appointments, gated member content, payments) for Framer sites.
  - Niche templates pre-wired to them, built by a contract designer. Examples: therapy practice, fitness studio, consultant.
  - Templates carry Framer's referral link: 50% of the referred subscription for 12 months, templates only.
- **Evidence:**
  - Framer paid creators more than $6.5M in 2025, with December payouts about 3× the prior year [Verified, secondary].
  - Creators keep 100% of template sales [Verified via search].
  - The therapy category has 24 templates, 13 of them free [Verified].
  - **Per-template sales are not visible.** A community complaint says Framer 3.0 removed template reviews ("killed the marketplace").
- **Competition:** The template designers, plus booking tools like Cal.com and Calendly that sites embed. Framer could build booking natively.
- **Entry strategy:** Compete on function, not design. A booking-ready template saves a service business a separate tool.
- **Economics [Hypothesis]:** A designer costs $300–500 per template.

  | Scenario | Volume | Owner profit |
  |---|---|---|
  | Downside | 5 sales/mo | ~$400/mo |
  | Base | 30 template sales/mo + referrals | ~$3k/mo |
  | Upside | Top-ranked | $8–10k/mo |

  Ongoing maintenance is needed as Framer updates.
- **Limitations:** Unlike Superhive and Apify, nothing was measured about what new Framer creators earn. Given the pattern everywhere else, the typical new template probably sells little. Penalty 13.

### F3. Quilting companion app / hobby-app studio (K10): 47.4

- **Offer:** A subscription quilting app at $5.99/month or $39.99/year: block library, cutting and yardage math, project tracker, photo-to-palette.
- **Evidence:**
  - The craft-companion category monetizes: YarnPal 33,879 ratings, Loopsy 16,509, Sewpal 11,939.
  - **But recent entrants are fading.** PIXELCELL's newer apps have 605–1,542 ratings. 2026 quilt apps (TideStitch, Quilt Duck, QuiltFit and others) have 0–23 [Verified, iTunes API].
- **Economics [Hypothesis]:** Revenue is about $34 net per annual subscription after Apple's cut.
  - **Downside:** about 30 subscribers from a $2k ad test, which is a loss.
  - **Base:** a cost per install of $1.50 and 8% trial-to-paid conversion gives about 100 subscribers per $1.5k of ad spend.
  - **Track A** needs about 1,100+ net annual subscribers.

  The business depends on how cheaply paid ads can acquire users.
- **Labour:** Scales beyond the founder once content exists. Running AI features costs money per use.

### F4. Seller-paid EV battery-health certificate, Israel (K4): 40.2

- **Offer:** A ₪250–450 battery state-of-health (SoH) test, ordered by the seller. It produces a verified link and QR code to paste into Yad2 or a dealer listing. Dealer packs are available.
- **Evidence:**
  - More than 100k EVs in Israel.
  - A 12–25% capacity spread within the same model, worth "tens of thousands of shekels" [Verified, Bizportal Aug 2026].
  - **Techno Test already sells EV pre-purchase checks that include battery capacity and cell checks**, from ₪630 [Verified].
  - In Germany only about 2% of used-EV listings carried a battery certificate, even though AVILOO is available [Verified, heise].
  - OEMs (Polestar) issue free certificates.
- **The real advantage left:** a shareable, seller-side certificate. Measurement equipment like the AVILOO B2B box licence is available to anyone.
- **Economics [Hypothesis]:** Contribution is ₪150–200 per test.

  | Scenario | Tests/mo | Contribution |
  |---|---|---|
  | Downside | 10 | ₪1.75k |
  | Base | 60 | ₪10.5k (~$2.8k) |
  | Upside | 150 incl. dealer subscriptions | ₪26k (~$7k), needs technicians |

  AVILOO licence cost is unknown.
- **Risks:**
  - **Adverse selection:** only sellers with good batteries will pay.
  - Liability for wrong readings.
  - Techno Test adding a shareable certificate.
- **Labour:** Labour-dependent unless a garage-partner network or self-test devices replace mobile testing.

### F5. Low-minimum packaging broker for Israeli brands (K6): 43.0

- **Offer:** Hebrew self-serve quoting with a box dieline and mockup generator. Short runs (25–300) go to Israeli digital printers. Runs of 500 or more go to vetted importers. Human proof within one business day.
- **Evidence:**
  - Packhelp claims 125,300 companies.
  - Israel's online label ordering is already served (Kvutzat Haatakot) [Partial].
  - No Israeli low-minimum printed-box configurator was found, which is weak evidence.
  - Label price anchor: ₪200–350 per 1,000.
  - **No Israeli demand data.**
- **Economics [Hypothesis]:** Average order ₪2,500 at 30% margin gives about ₪750 gross per order.

  | Scenario | Orders/mo | Gross |
  |---|---|---|
  | Downside | 3 | ₪2.25k |
  | Base | 15 | ₪11k (~$3k) |
  | Upside | 40, with an ops assistant | ₪30k (~$8k) |

  Ad spend is unknown.
- **Risks:** Printers undercutting the broker, misprint and reprint liability, holiday and import delays.
- **Labour:** Ops-heavy. Quoting is automatable.

---

## 5. Adversarial review

| Candidate | Survived | Contradicted / weakened | Effect |
|---|---|---|---|
| **H7 (leader)** | The channel still produces winners: curated picks reached 11/12 with ≥10 sales; True Sky 1,900+ sales in 11 months | Median new add-on sells <10 copies in its first 2–3 months; supply of new add-ons up about 2.5× (~385/month) | **Corrected −2.8** |
| **J7 (leader)** | $1.6M/month payout confirmed | New Actors: median 1 monthly user; 0% of under-3-month Actors reach ≥100 monthly users; ~600+ new Actors/day | **Corrected −4.6** |
| K13 | No contradiction found | Pricing, demand, other competitors all unverified | Hold. Red team rates it best balanced. |
| K8 | Payout terms and totals | Per-template sales invisible; marketplace-quality complaint; plugins earn no referral | Hold (red team: downgrade) |
| K12 | Paid extensions sell (Curic 327 ratings) | New entrants get 14–22 downloads; no trade knowledge | Hold (red team: downgrade) |
| K10 | Category proven | Recent entrants' traction collapsing | **Down** |
| K4 | Paid EV inspections exist | **Techno Test already checks batteries**; German certificate uptake ~2%; adverse selection | **Down** |
| K6 | Gap for printed boxes possible | Online labels already exist in Israel | Hold (Track A) |
| K1 | Incumbent prices confirmed | No volume evidence for cheap switches | Hold |
| K5 | Paid market exists | Scopists cost $1–1.50/page; Verbit; labour-bound | Down |
| K7 | Third-party managers recognised in platform terms | Platform has its own Boat-Manager role; needs on-site staff | Near-kill |
| K9 | GSPro price confirmed | ~$12/hr economics unless automated | Down |
| K3 | Active catalogue | Tiny volumes | **Kill** |

### Leader score corrections

- **H7:**
  - Proven channel 4→3 and Scalable acquisition 3→2, based on measured new-entrant outcomes.
  - Distribution 73→67. Scalability 62→58.
  - Balanced 71.4→68.6. Penalty 12 kept. **Adjusted 59.4→56.6.**
- **J7:**
  - Proven channel 3→1, First customers 3→2, Scalable acquisition 3→2.
  - Distribution 63→48. Scalability 62→58.
  - Balanced 67.4→62.8. Penalty 12 kept. **Adjusted 55.4→50.8.**
- **Why these corrections are evidence-based:** both earlier scores credited platform-wide payout totals as channel evidence. Phase 5 measured the outcomes for new listings on those same platforms. Both reviewers recommended these corrections independently (auditor: H7 −3 to −4, J7 −4 to −6; red team: H7 about 55–57, J7 about 49–51).
- **Not changed, but should be re-checked the same way:**
  - **H6:** Its channel evidence is one successful incumbent (CFBD).
  - **monday.com app (52.0):** It relies on a marketplace.

  I have no new-entrant evidence for either, so their scores stay as they are.

---

## 6. Phase 5 rankings (unchanged formula)

| # | Opportunity | Cash flow | Scalability | Distribution | Balanced | Penalty | **Adjusted** | Confidence |
|---|---|---|---|---|---|---|---|---|
| K13 | Hebrew tender + receivership intelligence | 74 | 66 | 58 | 67.6 | −14 | **53.6** | Low |
| K8 | Framer vertical kit | 84 | 56 | 51 | 66.2 | −13 | **53.2** | Low–Medium |
| K12 | Trade SketchUp extension | 75 | 52 | 44 | 59.6 | −12 | **47.6** | Medium (contradicting new-entrant data) |
| K10 | Quilting / hobby app studio | 63 | 60 | 51 | 59.4 | −12 | **47.4** | Medium (contradicting) |
| K1 | Assistive switches + interface | 60 | 51 | 55 | 55.4 | −11 | **44.4** | Low–Medium |
| K6 | Israeli packaging broker | 61 | 47 | 54 | 54.0 | −11 | **43.0** | Low |
| K2 | Film-camera revival kits | 56 | 41 | 61 | 51.0 | −10 | **41.0** | Low (snippet-only) |
| K4 | EV battery certificate | 57 | 39 | 59 | 50.2 | −10 | **40.2** | Medium (incumbent confirmed) |
| K9 | GSPro course studio | 50 | 44 | 61 | 49.8 | −10 | **39.8** | Low–Medium |
| K11 | Handwriting transcription | 60 | 38 | 51 | 49.4 | −11 | **38.4** | Low |
| K5 | Overnight transcripts | 50 | 44 | 52 | 48.0 | −10 | **38.0** | Medium |
| K7 | Boat co-hosting | 54 | 40 | 48 | 47.2 | −10 | **37.2** | Low |
| K3 | Pinball mods | 52 | 32 | 55 | 44.6 | −10 | **34.6** | Low |

**Rankings by objective:**
- **Fast cash** (realistic time to $2–5k/month):
  1. K6, with prepaid orders at ~₪750 gross each.
  2. K4, with high-ticket local tests, held back by the incumbent and adverse selection.
  3. K13, which builds slowly as subscriptions accumulate.
  4. K8, whose cash-flow score is high because capital is near zero and margin is 100%, but which depends on ranking well.
- **Scalable:** K13 (66), then K10 (60), then K8 (56).
- **Balanced:** K13 (53.6), then K8 (53.2), then K12 (47.6).

**Labour dependence:**
- Scales beyond founder hours: K13, K8, K10, K12.
- Mixed: K1, K2, K6.
- Labour-dependent: K4, K5, K7, K9, K11.

---

## 7. Cumulative leaderboard (all phases, Phase 3 rubric; corrected scores marked *)

| Rank | Opportunity | Phase | Adjusted |
|---|---|---|---|
| 1 | Hobbyist college-baseball data API (H6) | 3 | **57.2** (re-check pending) |
| 2 | Blender/VRChat add-ons (H7) | 3 | **56.6*** (was 59.4) |
| 3 | Meshtastic family kits (H1) | 3 | **54.6** |
| 4 | **Hebrew tender + receivership intelligence (K13)** | **5** | **53.6** |
| 5 | **Framer vertical kit (K8)** | **5** | **53.2** |
| 6 | UK MTD prep for accountants | 2 | 52.6 |
| 7 | monday.com Israeli invoicing app | 1 | 52.0 (marketplace re-check pending) |
| 8 | Hebrew/Russian memoir books (J1) | 4 | 51.0 |
| 9 | Apify Actors (J7) | 4 | **50.8*** (was 55.4) |
| 10 | Ketubot (H10) | 3 | 50.6 |
| … | Israeli allocation verification 49.8 · Spanish Holy Land box 49.4 · Non-US alerts 49.4 · J2 48.2 · H4 48.2 · J9 48.0 · H9 47.8 · K12 47.6 · K10 47.4 · … | | |

**Cross-phase verdict:**
- Ranks #1–#6 now span only 4.6 points, which is inside the roughly 5-point noise band.
- No single opportunity stands out on evidence.
- Phase 5 added two second-tier candidates (K13, K8).
- Its larger contribution is showing that marketplace-dependent leaders were overrated, and correcting them.

---

## 8. Three most promising new discoveries

1. **Best for fast cash: Low-minimum packaging broker for Israeli brands (K6).**
   - Prepaid orders mean no inventory, and about 15 orders/month reach Track A.
   - *Most important assumption to validate:* Israeli small brands will prepay for low-minimum printed boxes ordered through a Hebrew online channel at a broker margin of 25% or more, and Israeli printers don't already offer this self-serve.
2. **Best for scalable profit: Hebrew tender and receivership intelligence (K13).**
   - Recurring subscriptions, low labour, a Hebrew data moat, and direct (non-marketplace) distribution.
   - *Most important assumption to validate:* Israeli SMB contractors and asset investors will pay ₪300 or more per month for AI-matched tender and receivership alerts instead of Ifat or the free government portals.
3. **Best risk-adjusted: Hebrew tender and receivership intelligence (K13).**
   - It has the highest adjusted score, about $0 capital, and an Israel-specific moat, and it avoids the marketplace problem measured in this phase.
   - *Runner-up:* the Framer kit (K8). Its assumption to validate is that a new creator's functional template reaches 20 or more sales or referrals within 60 days.

---

## 9. Research limitations

- **Search quota:**
  - The quota refills only partially and unpredictably. About 41 discovery searches were available before it ran out; the auditor later got 16.
  - My planned reserve for review did not materialise as designed.
  - Discovery agents were therefore uneven: D had 4 searches and E had 3.
- **Sites that blocked fetching:** Reddit, Etsy, eBay, Fiverr, Kickstarter, Walmart, Clio, Zendesk, Faire, BuiltByBit, aescripts, parts of Trustpilot, Israel Hayom, and FMCSA. Superhive rate-limited the auditor, which worked around it slowly.
- **Unverified decisive items:**
  - Ifat's pricing and subscriber base.
  - Scraping legality for court and Reshumot sources.
  - Framer per-template sales and how new creators fare there.
  - AVILOO's Israel licence terms and price.
  - Israeli demand for packaging.
  - eBay volumes for film-camera kits (snippet-only).
  - Amazon volumes for cheap assistive switches.
  - Platform rules on boat co-hosting fees.
  - Subcontract rates for transcripts (benchmarked only).
- **Leaders not yet re-checked for new-entrant traction:**
  - H6: whether new hobbyist sports-data APIs gain paying members, or whether CFBD is a one-off.
  - The monday.com app.
  - H1: Amazon newcomers. NomadNode's 200+/month is one data point.
- **Rubric caveats:**
  - The rubric still favours low-capital digital products.
  - Penalties stayed within the earlier 9–14 range.
  - Gaps under about 5 points are noise.
