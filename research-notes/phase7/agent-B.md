# Phase 7 — Discovery Agent B (Physical products through someone else's customer relationship)

Date: 2026-10-13 · WebSearch used: **8 / 8** (logged as P7-B) · Scratch: `scratchpad/p6plus/P7-B/`

## Cross-cutting findings (these apply to every idea below)

1. **Faire, the main wholesale channel, can't be measured from outside.** faire.com returns HTTP 403 to WebFetch, including its robots.txt. Brand pages, review counts and "Top Shop" badges could not be read, so **newcomer wholesale traction on Faire remains [Unknown]**. What is public:
   - **Scale:** 100,000+ retailers and 50,000 brands outside North America; orders per brand up 123% since 2022; more than one in five new retailer–brand pairs reorder within 90 days. [Verified: 01net.it reprint of Faire release, 11 Jun 2026] In 2022: 600,000 retail accounts and 85,000 sellers. [Verified: Publishers Weekly, 7 Nov 2022]
   - **Fees:** 15% commission on reorders. On a first order from a new retailer, non-North-American brands pay 15% + a 10% new-retailer fee (25%); North-American brands pay 15% + $10. Faire Direct (retailers the brand brings itself) is 0%. Payment processing adds 1.9–3.5% + $0.30. [Secondary: Eightx, 5 Jul 2026, not checked against Faire's own terms page because it is blocked]
   - **Retailer margin:** retailers buy at about 50% of the suggested retail price, i.e. keystone. [Secondary: same source]
   - **Success stories are survivors.** The only "first-year" outcomes found are self-reports on Faire brand pages: Petty Paper "70+ stores in our first quarter"; Purrfect Little Art "~1,000 sales" in year one, including direct-to-consumer. [Search snippets only, not opened] Publishers Weekly's examples are established publishers (Red Wheel/Weiser 300+ accounts; Sourcebooks 10× in two years). None of this is newcomer evidence.
2. **Print-on-demand (POD) single-unit costs do not survive keystone wholesale.** Base costs from the public Printful catalog API (`api.printful.com/products/{id}`, fetched 13 Oct 2026), set against Lantern Press's retail prices:

   | Item | Printful base cost (before shipping) | Lantern Press retail | Wholesale at keystone | Result |
   |---|---|---|---|---|
   | 3″ kiss-cut sticker | $2.50 | $6.99 | ≈$3.50 | ≈$2.63–2.98 left after Faire's 15–25%; ≈$0.13–0.48 after POD cost, before shipping |
   | 520-piece puzzle | $24.92 | ≈$40 (1,000-piece) | ≈$20 | Below POD cost |
   | 4×6 postcard | $1.75 | — | — | Per-unit cost alone |
   | 5×7 greeting card | $2.95 | — | — | Per-unit cost alone |
   | 3″ die-cut magnet | $3.39 | — | — | Per-unit cost alone |
   | 11 oz mug | $6.75 | — | — | Per-unit cost alone |

   **Rule of thumb:** a wholesale brand needs cost of goods at or below roughly 20–25% of retail [Hypothesis derived from the figures above]. That means short-run bulk printing (inventory) or owning production, which is what Lantern Press does ("made to order", "Made in the USA"). POD works for made-to-order sales where the institution takes 5–38% (ideas B2 and B6), not for keystone wholesale.
3. **Presale models are the realistic answer to the ~$2k capital limit.** Makeship's creator terms (verified, 13 Oct 2026):
   - Each campaign sets a minimum order quantity (MOQ) of pre-sales that must be reached before manufacturing.
   - The creator receives an "agreed percentage of Net Retail Sales" within 30 days of the campaign ending.
   - School fundraisers (Square 1 Art, My Child's Art) and team stores (SquadLocker, Printful Quick Stores) also collect payment before production.
4. **Israel operability is the hidden blocker for wholesale.** Shipping case packs from Israel to US or EU gift shops adds freight, duties and slow replenishment. Any wholesale idea here assumes a print or 3PL (third-party logistics) partner in the destination market. Faire's eligibility for Israel-based brands is [Unknown] (site blocked).

---

## Opportunities

### B1. Per-location souvenir lines for independent gift shops, visitor centres and museum stores (short-run printing, many SKUs)

1. **Concept:** Place-specific designs (town, trail, lake, regional park, small museum) on stickers, magnets, postcards, tea towels and puzzles. Sold wholesale to the shop that owns the tourist foot traffic. The edge is producing hundreds of town-specific designs cheaply; fulfilment is short-run local printing.
2. **Paying customer:** Independent gift shops, outfitters, visitor centres, small museum and park stores. Start in one US region or the UK/EU.
3. **Model:** Wholesale at keystone (shop doubles the price). Opening orders via Faire, or Faire Direct at 0% for retailers the founder recruits. Reorders follow seasons.
4. **Spending evidence:**
   - Lantern Press's own Shopify `products.json` shows **at least 10,750 products** (43 full pages of 250 before a bot-verification wall stopped collection; I did not continue). They are almost all place-named stickers (399 of the first 750) and puzzles (349). [Verified: lanternpress.com/products.json, 13 Oct 2026]
   - The site states "All products are made to order and ship in 1–5 days … Made in the USA. Hand-drawn by humans." Retail examples: puzzle $39.99, stickers from $6.99, tea towel $15.99. [Verified: lanternpress.com, 13 Oct 2026]
   - Its wholesale runs through Faire. [Search snippets of Faire product pages only]
   - The incumbent shows that a large per-location catalogue sells wholesale. Its revenue is [Unknown].
5. **Competitors:**
   - Lantern Press, at very large SKU depth with its own production.
   - Countless local artists and sticker brands on Faire (count [Unknown] because Faire is blocked).
   - Customer complaints [Unknown].
   - Lantern Press explicitly markets "Hand-drawn by humans", which makes AI-generated art a **negative** positioning with this buyer [Hypothesis].
6. **Entry strategy:** Geography where Lantern Press is thin (UK/EU towns, non-US national parks), plus product types it lacks. AI should be used only for layout and variant production around commissioned or licensed local artwork, not as the art itself. Otherwise none credible against Lantern Press in the US.
7. **Acquisition:**
   - Faire marketplace exposure plus founder outreach to shops (Faire Direct).
   - Newcomer outcomes on Faire are **[Unknown/blocked]**. The only first-year data are brand self-reports (Petty Paper, 70+ stores in a quarter), which are survivor anecdotes.
   - Trade shows cost more than the budget [Hypothesis: booth costs not verified].
8. **Capital and operations:**
   - Short-run inventory per design: Sticker Mule allows "as few as 10 per design" [Verified: stickermule.com/custom-stickers, 13 Oct 2026]; unit prices are client-rendered and could not be read [Unknown].
   - About $2k funds samples and a few hundred SKUs' first runs in one region.
   - From Israel this needs a destination-country printer that drop-ships case packs. Freight and returns are the friction.
   - No legal blockers beyond place-name trademarks: national-park logos and some park names are protected, e.g. Smokey Bear is licensed [Hypothesis].
9. **Labour:** Design and catalogue production automate well. Account acquisition and reorders are founder or rep time. Commission reps typically take about 15–20% [Hypothesis, not verified this phase].
10. **Unit economics [Hypothesis]:**
    - Sticker wholesale $3.50, minus 15% Faire, minus about $0.60 short-run cost and packing, leaves about $2.30 gross.
    - An active account averaging $100/month wholesale yields about $55–60 gross.
    - Track A ($3k/month) needs about 55–60 actively reordering accounts. Track B needs hundreds of accounts plus reps.
    - **Fit: Track A plausible only if reorder density holds. Track B weak.**
11. **Kill risks:**
    - Faire newcomer reality is like other marketplaces (a few accounts).
    - Short-run costs above about $1 per sticker or $3 per magnet.
    - Shops reject AI-assisted art.
    - Freight from or for an Israel-based operator.

### B2. Children's-artwork keepsake fundraisers run through schools and kindergartens, in a country without an established provider

1. **Concept:** Schools collect pupils' artwork. Parents buy that artwork printed on keepsakes (cards, tea towels, mugs, calendars, notebooks), with free ship-to-home or ship-to-school. The school or parent association keeps a share. Production is POD or made-to-order: no inventory, and the presale is funded by parents.
2. **Paying customer:** Parents, reached through the school, which owns the relationship. One deal brings 50–300 orders. Geography: a market not already served. **The UK and US are served**, so the target is something like DE/AT/NL/Nordics, or Israel subject to regulation.
3. **Model and prices:**
   - Parent pays retail, roughly €10–30 per item [Hypothesis: competitor prices not listed].
   - School share benchmarks: **Square 1 Art "standard profit is 33% (up to 38%)"**, with the profit check 10–14 days after completion [Verified: square1art.com/plan-a-fundraiser, 13 Oct 2026].
   - **My Child's Art 20% commission** [Verified: pta.co.uk/supplier/my-childs-art, 13 Oct 2026].
   - **Xmas4schools £1 per product** [search snippet from a school notice, 2025].
4. **Spending evidence:**
   - Square 1 Art: "more than 25 years … thousands of schools nationwide" [Verified: square1art.com, vendor claim, 13 Oct 2026]. Recurring school posts "Square 1 Art Projects 2023/2024/2025" (stmargaretstl.org) show yearly repeat [search snippets].
   - UK: My Child's Art claims "thousands of happy schools" and 35+ products, with six named school testimonials [Verified as vendor claim].
   - At least three UK providers coexist (My Child's Art, Xmas4schools, Art Projects for Schools), per school PTA notices from 2021–2025 [snippets].
   - Each provider's order volume is [Unknown].
5. **Competitors:**
   - US: Square 1 Art, plus others not checked.
   - UK: the three providers above.
   - Customer dislikes [Unknown]. Possible friction: physical artwork shipping, and the logistics of collecting art at one moment [Hypothesis].
   - Competition in DE/NL/Israel is **[Unknown]**. No search budget was left to check, and absence of results is not absence.
6. **Entry strategy:**
   - Country or language gap, if one exists.
   - Software advantage: phone-scan workflow where the teacher photographs the art and AI cleans it up, instead of shipping paper. Parent ordering by QR code. Local POD partner in the target country.
   - **Israel caveat:** the Ministry of Education restricts commercial activity in schools [Hypothesis; I recall Director-General circulars on this but did not verify]. Kindergartens and after-school programmes may be easier [Hypothesis].
7. **Acquisition:**
   - Parent-association (PTA/Elternbeirat) channels, school-supplier directories (the UK uses pta.co.uk supplier listings), and teacher word of mouth. Seasonal: autumn for Christmas, spring for Mother's/Father's Day.
   - Proven channel evidence exists for incumbents (directory listings, repeat school posts). **Newcomer evidence: the coexistence of three UK providers suggests the niche supports several entrants, but their volumes are unknown.**
8. **Capital and operations:**
   - Under $2k for a pilot: POD samples, scan-and-order web app, flyers.
   - POD costs per piece, e.g. Printful card $2.95, mug $6.75 [Verified via API, US prices]; an EU POD partner is needed in Europe.
   - Child-data and photo privacy (GDPR) applies to pupils' names on artwork.
   - From Israel this is operable remotely once a local POD partner and school contacts exist. Local language is needed.
9. **Labour:** Each school campaign needs a coordinator touchpoint; the rest (artwork processing, catalogue, payments, POD routing) automates. Growth runs through a regional ambassador on commission [Hypothesis].
10. **Unit economics [Hypothesis]:**
    - Average order €25, school 20–25%, POD + shipping about €10–12, payment about 3% → about €7–8 owner gross per order.
    - A 300-pupil school at 30% participation is about 90 orders, or about €650 per campaign.
    - Track A ($3k/month average) needs about 50–60 school campaigns a year.
    - Track B needs hundreds of schools a year and a team of ambassadors, which is how US incumbents scaled.
11. **Kill risks:**
    - The target country already has a provider.
    - Participation below 15%.
    - School rules on commercial activity (Israel especially).
    - Strong seasonality: about 70% of volume in Q4 [Hypothesis].

### B3. Presale ("petition") merch production for small game studios and mid-size creators, in categories Makeship doesn't make

1. **Concept:** The creator or indie studio owns the audience. The founder runs the campaign page, factory sourcing (China), QC, and US/EU 3PL fulfilment. Production starts only once presales clear the MOQ. The creator receives a share of net sales.
2. **Paying customer:** Fans of the creator, worldwide. The B2B relationship is with the creator or studio.
3. **Model (Makeship benchmark):**
   - MOQ pre-sales gate manufacturing; the creator is paid a percentage of net retail within 30 days [Verified: makeship.com/creator-terms-of-service, 13 Oct 2026].
   - Live MOQs on the current homepage: **200 for plush, 300 for hoodies and t-shirts, 500 for keychains and sweatpants, 3,000 for one large IP** [Verified: makeship.com page data, 13 Oct 2026].
   - The creator's percentage is not public [Unknown].
4. **Spending evidence:**
   - Makeship has "paid out $16M+ to Creators" [vendor claim, via search result of its company profile].
   - "Over 1,000 creators … over 600,000 products" by 2022 [Secondary: Wikipedia].
   - Where the sold counter is exposed, products show **215, 304, 308, 389, 520 and 1,098 sold** [Verified: 53 product pages parsed, 13 Oct 2026]. 47 of the 53 did not expose a count, so this is a biased, upper-leaning sample.
5. **Competitors and shift:**
   - Makeship dominates the plush-presale niche. Its 2026 homepage is now heavily **licensed big IP**: Palworld, Fullmetal Alchemist, Attack on Titan, Inuyasha, Among Us (Innersloth), Paradox Interactive, Dave the Diver, Valheim. Small creators appear alongside.
   - Merch platforms such as Fourthwall and Spring cover POD apparel. Their terms were not checked this phase.
   - Creator dislikes [Unknown].
6. **Entry strategy:** Categories Makeship's catalogue doesn't show: dice and playmats for tabletop creators, creator-branded consumables, or enamel-pin-heavy bundles. Or niches Makeship ignores, such as non-English creators (Spanish/Portuguese/German VTubers and streamers). **Credible only if a creator segment can be shown to be under-served; otherwise none credible.**
7. **Acquisition:**
   - Founder outbound to creators and studios. This is the low-yield founder sales Phase 6 warned about.
   - The channel that produces purchases is the creator's audience: the observed 215–1,098 units per campaign is the proof. Creator-side acquisition cost for a newcomer is [Unknown].
8. **Capital and operations:**
   - Presales fund production. Samples and prototypes cost about $300–800 each [Hypothesis].
   - Factory MOQs and QC are needed, plus a 3PL in the US/EU. Workable from Israel, which can run sourcing remotely.
   - IP licence and warranty paperwork per creator. Chargeback risk if a campaign is delayed.
9. **Labour:** Per-campaign project management is substantial. Templated page, ads and fulfilment automate. Revenue can outgrow hours only with a sourcing agent and a 3PL.
10. **Unit economics [Hypothesis]:**
    - 300 units × $35 = $10.5k gross.
    - Creator share 20–30% [Unknown; Makeship rate not public], landed cost about $8–10/unit, shipping subsidies and payment fees.
    - That leaves about $3–4.5k contribution per successful campaign before failed-campaign costs.
    - Track A needs about one successful campaign a month. Track B needs a roster.
    - **Fit: medium on economics, weak on acquisition.**
11. **Kill risks:**
    - Creators default to Makeship.
    - Failed campaigns burn sample costs.
    - Factory delays cause refunds.
    - IP disputes.

### B4. A made-to-order gift line built for corporate-gifting platforms and gifting studios (supplier, not agency)

1. **Concept:** Be the brand inside gifting platforms (Goody, Loop & Tie, Elfster, Wishlist) and gifting studios. These own HR/sales-team buyers, with one order covering hundreds of recipients. Product: personalised made-to-order items with the recipient's company and name, which the founder's automation can produce at scale.
2. **Paying customer:** Companies, through the platforms. US first.
3. **Model:** Wholesale or platform-margin pricing. Caftari says platforms buy at wholesale and margins are "relatively tight" [Verified: Modern Retail, 16 Dec 2024]. Goody's partner terms are not published [Verified: ongoody.com/partner, 13 Oct 2026, no terms shown].
4. **Spending evidence:**
   - Goody: "Trusted by 25,000+ companies"; Gong sent "800+ gifts" [vendor claims, Verified page, 13 Oct 2026].
   - Small direct-to-consumer brands' corporate share [Verified: Modern Retail, Dec 2024]:

     | Brand | Corporate share |
     |---|---|
     | Caftari (launched Nov 2023) | ~25% of H1-2024 revenue (via Loop & Tie, Elfster, Wishlist, hotels) |
     | Anecdote Candles | ~19% of sales, up from 7% |
     | Gardenuity | ~15% since 2017 |

5. **Competitors:** Every gifting category (candles, snacks, drinkware) is crowded. Platforms curate. Buyer complaints [Unknown].
6. **Entry strategy:** Personalisation at the recipient level that commodity brands can't do (a per-recipient engraved or printed item produced from a CSV). Otherwise none credible: a generic product has no reason to be picked.
7. **Acquisition:**
   - Platform listing plus gifting studios (Telescope-type agencies have "established relationships with suppliers" [Secondary: Shopify blog snippet]).
   - **Newcomer outcomes on gifting platforms are [Unknown].** Caftari is one positive anecdote (from launch to platform placements within about a year), but it is a survivor story.
8. **Capital and operations:**
   - Made-to-order personalisation via a US POD or engraving partner. About $2k covers samples and integration.
   - Platforms may require inventory commitments and fast SLAs [Unknown].
   - Ships from US partners, so it works from Israel.
9. **Labour:** Platform integration and personalisation automate. Platform relationship-building is founder time.
10. **Unit economics [Hypothesis]:**
    - Retail $40 personalised item; platform buys at 50–60% → $20–24.
    - POD/engraving plus shipping about $12–14, leaving about $8–10 per unit.
    - A single 300-recipient order is about $2.5–3k. Highly lumpy and Q4-seasonal.
    - Track A plausible if 1–2 large orders a month arrive. Track B unclear.
11. **Kill risks:**
    - Platform curation rejects new brands.
    - Thin margins after platform discounts.
    - Seasonal concentration.

### B5. Personalised pet-memorial keepsakes supplied through pet crematoria and vet practices

1. **Concept:** The crematorium or vet owns the grieving owner at the moment of purchase. Supply made-to-order keepsakes (photo-engraved plaques, nose- or paw-print jewellery, memory items) with a white-label ordering portal the crematorium resells through.
2. **Paying customer:** Pet owners, through crematoria and vets. UK/US.
3. **Model:** Wholesale to the crematorium, which marks up [margins Unknown].
4. **Spending evidence:**
   - Pet Cremation Services (UK) sells keepsakes and memorials online and from "our catalogue either at your veterinary practice", and runs a vet portal (pcsvets.co.uk). Prices are not shown on the listing page [Verified: pcsonline.org.uk/category/keepsakes, 13 Oct 2026].
   - Pets Remembered (UK) supplies "pet crematoriums, veterinary practices, human undertakers" and says it makes over 80% of items itself [snippet: madeinbritain.org].
   - Volume and price evidence: **[Unknown]**.
5. **Competitors:** Crematorium groups' in-house ranges plus specialist makers. Dislikes [Unknown].
6. **Entry strategy:** A white-label personalised range with photo-proof automation, aimed at independent crematoria without an in-house range [Hypothesis].
7. **Acquisition:** B2B outreach to crematoria (a finite, reachable list). Channel evidence that crematoria add new suppliers: none found.
8. **Capital and operations:** Made-to-order engraving or print partners. Low capital. Sensitive customer service. Israel market is tiny, so the target is UK/US.
9. **Labour:** Account sales are founder-led. Fulfilment automates.
10. **Unit economics:** [Unknown]. Too little price data to estimate honestly.
11. **Kill risks:**
    - Crematoria are loyal to existing suppliers or vertically integrated.
    - Low order volume per account.
    - **Evidence is too thin to rank highly.**

### B6. Club and association made-to-order merch stores outside the US (fundraising markup to the club)

1. **Concept:** Free online stores for sports clubs, choirs, scout groups and alumni associations. The club owns the members and promotes the store; items are POD; the club keeps a markup.
2. **Customer:** Members and parents, via the club. Target the EU/Israel.
3. **Model and benchmarks (US):**
   - SquadLocker: 5–15% markup, 100% to the organisation, payout once over $10, "we don't charge fees" [search summary of squadlocker.com blog; not opened].
   - Printful Quick Stores: free, markup set by the organisation, no minimums, monthly payout over $25, and **"currently available to sellers and shoppers in the US"** only [Verified: printful.com/quick-stores/online-stores-for-schools, 13 Oct 2026].
   - Custom Ink claims catalogue fundraisers return 40–50% to the school [vendor claim, snippet].
4. **Spending evidence:** US category proven (ASI 2018: leagues favour online stores because no inventory is held; tees, caps and hoodies sell best [snippet]). EU volume [Unknown].
5. **Competitors:**
   - EU: Spreadshirt's Spreadshop and team-kit suppliers' club shops very likely occupy this [Hypothesis, not verified this phase].
   - Israel: [Unknown].
6. **Entry strategy:** The US-only restriction on Printful Quick Stores is a gap only if EU tools are absent, which is unverified. Likely none credible.
7. **Acquisition:** Club-by-club outreach. Each club's members are a captive but small audience.
8. **Capital and operations:** Near zero (POD). Works from Israel.
9. **Labour:** Low per store once live. Acquisition is founder-led.
10. **Unit economics [Hypothesis]:** €8–10 owner gross per item at 30–40% POD margin. A 200-member club buying 0.5 items a year is about €1k a year. Track A needs about 40 active clubs.
11. **Kill risks:** Free incumbents (Spreadshop-style); tiny per-club volume. **Weak.**

---

## Killed ideas (and why)

| Idea | Why killed |
|---|---|
| Generic "become a Faire brand" (cards, stationery, gifts) via POD | Keystone + 15–25% commission + POD costs leave cents per unit (Printful card $2.95, sticker $2.50 vs ~$3.50 wholesale). 100k+ brands, and newcomer data unmeasurable (403). |
| US school spirit-wear / team stores | Free, entrenched tools: SquadLocker (no fees), Printful Quick Stores (free, POD), Custom Ink, Spirit Hero. No wedge. |
| UK children's-art keepsake fundraisers | At least three providers already: My Child's Art (20%), Xmas4schools (£1/item), Art Projects for Schools. The geography gap must be elsewhere (B2). |
| Generic Makeship clone for plush | Makeship has scale ($16M+ paid out, vendor claim) and now signs big licensed IP. Only category or language niches remain (B3). |
| Private-label supplements for practitioners | Inventory MOQs and regulatory or claims exposure exceed $2k. Practitioner dispensary platforms are incumbent [Hypothesis; not researched further]. |
| Trade-show-led wholesale launch (NY NOW, Spring Fair etc.) | Booth plus travel very likely exceeds the budget [Hypothesis; costs not verified]. |
| Israeli corporate holiday gifts (Rosh Hashanah/Pesach for workers' committees) | Voucher incumbents dominate employer holiday gifting [Hypothesis, unverified]. Also re-drifts to Israel-only. |
| Profession-themed paper goods for clinics/offices (e.g. dental notepads) | Only one self-reported Faire brand (Purrfect Little Art); practice-supply incumbents likely [Hypothesis]. Too thin to stand alone. |

## Ranking

| Rank | Idea | Why here |
|---|---|---|
| 1 | **B2 Children's-art keepsake fundraisers in an unserved country** | Institutional channel where one deal brings many presold orders; zero inventory; verified institutional shares (20–38%) and multi-decade incumbents. The geography gap is unverified. |
| 2 | **B1 Per-location souvenir lines for gift shops** | A verified large made-to-order incumbent (≥10,750 SKUs) proves the model. Margins only work with short-run production. Newcomer wholesale traction unmeasurable. Israel logistics drag. |
| 3 | **B3 Presale merch for under-served creator or studio niches** | Strong verified mechanics and per-campaign volumes (215–1,098 units where visible). Creator acquisition is founder sales against a dominant incumbent. |
| 4 | B4 Personalised gift line for corporate-gifting platforms | Real corporate spend shares (15–25% of small brands' revenue); platform terms and newcomer acceptance unknown. |
| 5 | B6 Club merch stores outside the US | Cheap to test but probably occupied. |
| 6 | B5 Pet-memorial keepsakes via crematoria | Real channel, almost no price or volume evidence. |

None of these has newcomer-outcome evidence comparable to the Phase 5–6 channel measurements. The distribution-borrowing mechanism is real in each case (schools, shops, creators, gifting platforms), but every one still needs **founder-led B2B acquisition of the intermediary**. That is the binding constraint Phase 6 identified.

## Top 3 for deep diligence: the decisive unverified assumption for each

1. **B2:** In at least one target market (Germany/Austria, Netherlands, Nordics, or Israeli kindergartens and after-school programmes):
   - no established artwork-keepsake fundraiser already serves schools at scale;
   - schools are permitted to run one;
   - **parent participation reaches at least about 20–25% per campaign.**

   Check next: local-language searches for competitors, PTA/Elternbeirat supplier directories, and Israeli MoE circulars on commercial activity.
2. **B1:** Short-run unit costs fall to at most about 20–25% of retail (stickers at most about $0.80, magnets at most about $1.50), **and** a new brand without trade shows can reach about 50+ reordering independent accounts within 12 months via Faire and Faire Direct. That second part is unmeasurable while Faire blocks fetching. The next step is a non-browser source of Faire brand review counts, or retailer-side surveys.
3. **B3:** A definable creator or studio segment (non-English streamers or VTubers, tabletop creators) is not served by Makeship or similar, will sign with an unknown producer, and **at least about 60% of its campaigns clear a 200–300 unit MOQ.**

   Check next: Makeship catalogue coverage by language or category (its page data is parseable), and the share of products exposing sold counts at or above MOQ.

## Sources (opened unless marked)

| Source | Status |
|---|---|
| makeship.com creator terms + homepage and 53 product pages (Next.js data) | Verified 13 Oct 2026 |
| lanternpress.com and products.json, pages 1–43 (bot wall from page 44) | Verified 13 Oct 2026 |
| api.printful.com/products/{534,358,656,568,19,433} | Verified 13 Oct 2026 |
| square1art.com and /plan-a-fundraiser | Verified 13 Oct 2026 |
| pta.co.uk/supplier/my-childs-art | Verified 13 Oct 2026 |
| printful.com/quick-stores/online-stores-for-schools | Verified 13 Oct 2026 |
| ongoody.com and /partner | Verified 13 Oct 2026 |
| pcsonline.org.uk/category/keepsakes | Verified 13 Oct 2026 |
| stickermule.com/custom-stickers (minimum 10 per design; prices not readable) | Verified 13 Oct 2026 |
| modernretail.co corporate-gifting article | Verified; published 16 Dec 2024 |
| eightx.co Faire take-rate analysis | Verified; published 5 Jul 2026 (secondary analysis) |
| 01net.it Faire release reprint | Verified; published 11 Jun 2026 |
| publishersweekly.com Faire article | Verified; published 7 Nov 2022 |
| faire.com | Blocked (403) |
| Makeship $16M+ payouts, SquadLocker terms, Xmas4schools £1/item, Pets Remembered, Faire brand self-reports | Search snippets only |

**WebSearch count: 8 of 8.**
