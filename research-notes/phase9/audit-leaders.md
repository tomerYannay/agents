# Phase 9 leader re-check (Leader Auditor, P9-AUDITL), 2026-10-13

Desk research only. I used public pages, public JSON and Wayback Machine snapshots. No browser tools, sign-ups or contact with anyone. Every request used a generic User-Agent, and no personal identifiers were sent.

- **WebSearch:** 4 of 8 used, each logged in `search-log.txt` as `P9-AUDITL`. Everything else came from curl and WebFetch.
- **Scripts:** `scratchpad/p6plus/P9-auditL/scripts/`. **Data:** `.../P9-auditL/data/`.
- **Scoring method:** the same as Phases 6–8. One step on a criterion is worth weight/5 points. A Cash-Flow or Scalability point moves Adjusted by 0.4; a Distribution point moves it by 0.2.
- **Penalty rule:** raised only where the decisive assumption is directly contradicted.

## Summary

| Leader | Was | Recommended | Change | Decisive finding |
|---|---|---|---|---|
| H6 College-baseball API | 52.2 | **52.2 (hold)** | 0 | No public licence route for regular-season NCAA stats exists. Both main sources (NCAA.com and SIDEARM school sites) limit content to noncommercial use. Yet paid college-stats APIs operate openly without claiming an NCAA licence: CFBD explicitly permits commercial use, and Highlightly sells paid NCAA baseball tiers. Genius Sports' exclusive covers official championship data to sportsbooks only. The terms risk is unchanged from what Phase 6 priced (penalty 13), and nothing new directly contradicts the assumption. |
| K8 Framer kit | 52.0 | **50.4** | −1.6 | First newcomer-level measure (still indirect): at most 649 accounts got any creator or affiliate payout in Dec 2025, against 7,359 creators listed now (about 9–13% even at best). Sampled 2026 creators have a median of 43 followers, and only 1 of about 290 sampled items is featured. Site-wide resource IDs suggest new supply is running at 2–3× the 2024–25 rate. **Speed to first sale −1.** |
| H1 Meshtastic kits | 51.2 | **51.2 (hold)** | 0 | Tindie (via Wayback, 67 Meshtastic listings from 21 sellers): about 90% of 2024–26 listings have 0 reviews. All 12 listings at $150+ have 0–1 reviews. The only "kit" listings are cheap dev kits, all with 0 reviews. No family kit exists. This is consistent with Phase 6's cut, and Tindie was never H1's planned channel. Etsy and Amazon were blocked this time. |
| M1 Sage 50 US/CA API | 49.6 | **49.6 (hold)**; downside 48.6 | 0 | A Wayback copy of the **Aug 2023 Sage NA Developer Partner Program** document confirms the programme covers Sage 50 US/CA ($350 sign-up, $250/year). It requires signing "the Developer Partner Program Agreement". The only archived NA agreement text is the "Medium Segment" version. It licenses add-ons sold to end users, bars using the software or tools "for the benefit of any third party", and lets Sage terminate for convenience on 90 days' notice. It does not mention a hosted API for vendors. The assumption is still unverified and leans adverse, but it is not directly contradicted. |

**Board effect:** H7 55.4 · H6 52.2 · H1 51.2 · monday and J7 50.8 · K13 50.6 · **K8 50.4** · UK MTD 50.2 · Israeli allocation 49.8 · **M1 49.6**.
- The top cluster below H7 is now 49.6–52.2, entirely inside the noise band.

---

## 1. H6: data rights for a paid college baseball/softball API (hold 52.2)

**Decisive assumption:** a newcomer may lawfully sell API access to college baseball and softball statistics taken from public NCAA, conference or school sources.

### Evidence
- **NCAA.com terms (last updated 21 Feb 2023)** [Verified: ncaa.com/tos, 2026-10-13]:
  - NCAA Content includes "statistics, updated scores".
  - Users may not "use for commercial purposes, or in any way exploit, any of the NCAA Content".
  - "no copying, redistribution, retransmission, publication, or commercial exploitation of downloaded material will be permitted without the express permission of Operator and the copyright owner."
  - This was already priced in Phase 6.
- **stats.ncaa.org** returns 403 to automated requests (as in Phase 6). Its own terms could not be read [Blocked].
- **SIDEARM Sports terms (last updated 11 Apr 2023)** [Verified: sidearmsports.com/terms-of-service, linked from fightingillini.com footer, 2026-10-13]:
  - SIDEARM is a LEARFIELD subsidiary that powers most school athletics sites.
  - "The contents of the Services … are intended for your personal, noncommercial use".
  - "The Services shall be used only in a noncommercial manner."
  - **New:** the per-school box-score and stats source is also under noncommercial terms.
- **StatBroadcast:** homepage and /terms return 403 to curl [Blocked]. A search found no SIDEARM or StatBroadcast data-licensing programme (P9-AUDITL #2).
- **Official NCAA data licensing goes to sportsbooks only:**
  - Genius Sports is "the exclusive distributor of official NCAA data feeds to sportsbooks" in an authorised gaming-licensee programme through 2032.
  - "This agreement only impacts championship events and not regular-season games" [Verified: cbssports.com, 30 Apr 2025; BusinessWire release of 25 Apr 2025 returned 403].
  - So there is a licence route for official championship data to sportsbooks, and **no visible licence route for a hobbyist or analyst API**. Nor does this deal bar one.
- **How existing paid APIs operate:**
  - **CFBD / Rad Sports Analytics terms (effective 12 Aug 2026)** [Verified: collegefootballdata.com/terms, 2026-10-13]:
    - "Commercial use is permitted. Your subscription tier determines your API usage quota".
    - Prohibits users redistributing API data.
    - Disclaims "team, conference … names as trademarks; logos; player names or likenesses".
    - Bars representing data "as official data from the NCAA, a conference, a school".
    - **It claims no NCAA licence.** It operates openly as a paid API with 3,600+ Patreon supporters and 21,000+ users (homepage).
  - **Highlightly terms (updated 24 Jul 2026)** [Verified: highlightly.net/terms]: data is "sourced from publicly available data, authorised data feeds, and official developer APIs". It sells paid NCAA baseball tiers ($7.99–44.99, Phase 6). It names no NCAA licence.
  - **sportsdataverse:**
    - `baseballr-data` (pushed 2026-10-13) and `softballR` (2026-10-12) still scrape NCAA data daily in public [Verified: GitHub API].
    - `collegebaseballdata.com` is still "Launching Soon" [Verified].
- **Legal background** [Secondary/general knowledge, not legal advice]: US courts generally treat game facts as uncopyrightable (Feist; NBA v. Motorola). The exposure is breach of website terms and anti-scraping measures, not copyright in the stats.

### Reading
- The assumption is **not cleanly true**. Every primary source's terms say noncommercial, and no licence is on offer.
- It is also **not directly contradicted**. Several paid college-stats APIs operate openly on public-facts sourcing, and no enforcement against them was found. Not finding enforcement is not proof of safety.
- The SIDEARM terms add a second primary source with the same restriction Phase 6 found at NCAA.com. That is the same risk type, already priced by Phase 6's 12→13 penalty.
- **Operational note (not scored):** stats.ncaa.org blocks automated clients, and StatBroadcast returns 403. H6's pipeline must not bypass access controls. The free sportsdataverse pipeline works, but how it gets past these blocks was not checked.

### Recommendation
- **No step change. Penalty stays at 13. Adjusted 52.2.**
  - CF 75, Scal 59, Dist 58.
  - Balanced = 0.4×75 + 0.4×59 + 0.2×58 = 30 + 23.6 + 11.6 = 65.2.
  - Adjusted = 65.2 − 13 = 52.2.
- **Trigger for a cut:** evidence of the NCAA, a conference or LEARFIELD acting against a stats API or scraper. That would take the penalty to 14–15 (51.2–50.2).
- **Confidence:** medium on the facts; low on legal risk.

---

## 2. K8: Framer Marketplace newcomer outcomes (52.0 → 50.4)

**Decisive assumption (Phase 5):** a new creator's functional template reaches 20 or more sales or referrals within 60 days.

### Evidence
- **No per-item sales, remix or install counts are public.**
  - Template pages show only publish and update dates, the licence and a Remix button.
  - Plugin pages show no usage counts.
  - Creator pages embed follower counts, each resource's `publishedAt`, `featuredAt` and `price`, and like counts on launch posts. No sales fields exist [Verified: framer.com page payloads, 2026-10-13].
- **Supply** [Verified: framer.com/marketplace/sitemap/*.xml, 2026-10-13]: 12,625 templates, 1,137 plugins, 7,359 creator profiles.
- **Supply growth proxy (site-wide resource IDs vs creation month, from the sample):**

  | Median resource ID | Created |
  |---|---|
  | 45,988 | Jul 2024 |
  | 54,069 | Jul 2025 |
  | 57,232 | Oct 2025 |
  | 67,568 | Jun 2026 |
  | 75,040 | Oct 2026 |

  - That is about 670 new IDs a month in Jul 2024–Jul 2025, about 1,480 a month in Oct 2025–Oct 2026, and about 1,870 a month in Jun–Oct 2026: **2–3×**.
  - IDs cover all resource types and may include unpublished drafts, so this is a [Proxy].
- **Payout concentration:**
  - Framer's December payout was **$784K to 649 affiliates**, up from $267K to 312 a year earlier. This is Dec 2025 vs Dec 2024. It is labelled affiliates/creator program and does not separate template sales [Secondary: createwith.com, 11 Feb 2026, citing Framer's LinkedIn post].
  - Even if every paid account were a marketplace creator, at most 649 of today's 7,359 creators (8.8%) were paid that month. Creator counts were lower in Dec 2025, so the true share is perhaps up to about 13%.
  - The mean is about $1,200 per paid account, skewed by top earners.
- **Random creator sample:** n = 202 of 7,359 profiles (seed 20261013), crawled at 1 request/second. Results by cohort are in the table below. Cohort = year of the earliest published resource on the profile's first page, which skews toward recent years.

  [Verified: framer.com creator-page payloads, 2026-10-13]

  | Cohort | Creators | Median followers | 90th-percentile followers | Share with a paid template | Share with a featured item | Median likes on best launch post |
  |---|---|---|---|---|---|---|
  | 2022–24 | 10 | 64 | 181 | 70% | 0% | 27.5 |
  | 2025 | 13 | 53 | 173 | 77% | 8% | 41 |
  | **2026** | **61** | **43** | **152** | **69%** | **0%** | **10** |

  - All 202 sampled creators: median 29 followers, 90th percentile 152.
  - 84 of 202 had a published template, plugin or component on their profile's first page.
  - Of about 290 sampled items, **1 was featured**.
  - 288 templates: 50% paid, median price $49.
  - 181 of the 288 templates were published in 2026.
  - Paid templates are the norm among newcomers, so supply competes on price as well as volume.

- **Self-reports (anecdotes, not representative):**
  - One creator's best month was $2,832.69.
  - "Total commissions from one landing page template, 4 months, zero marketing" (amount not readable).
  - Framer community posts surfaced by search (P9-AUDITL #4).

### Reading
- There is still no direct newcomer sales count.
- The best available bounds point the same way as every other open marketplace measured:
  - at most about 9–13% of listed creators got any payout in a month;
  - the typical 2026 newcomer has tens of followers and no featuring;
  - supply is growing 2–3× year on year.
- Reaching 20 or more sales or referrals within 60 days therefore looks like a top-decile outcome, not the base case.
- K8's Cash-Flow score (84) is the highest in the top cluster. It assumed near-zero capital **and** a fast first sale. The second half is not supported.

### Recommendation
- **Speed to first sale −1 (CF −4).**
  - CF 84 → 80. Scal 56, Dist 45.
  - Balanced = 0.4×80 + 0.4×56 + 0.2×45 = 32 + 22.4 + 9 = 63.4.
  - Penalty stays at 13: no direct contradiction, because no sales counts exist.
  - **Adjusted 50.4.**
- **Not cut:** proven channel. Phase 6 already cut it for the uncreditable payout total, and cutting it again on bounds rather than counts would double count.
- **Lighter alternative for reviewers:** first-customer difficulty −1 instead (Dist −3), giving **51.4**.
- **Confidence:** low–medium. The measures are bounds and proxies, but all point the same way.

---

## 3. H1: Meshtastic kit newcomer outcomes (hold 51.2)

**Decisive assumption:** a $349–449 pre-paired family kit (3 handhelds plus a repeater) converts through Amazon search, YouTube preparedness creators and mesh Discords.

### Evidence
- **Blocked sources:**
  - Tindie live pages return 403 (Cloudflare) to both curl and WebFetch.
  - Etsy returns 403 (bot challenge) to both.
  - Amazon search now serves a JavaScript bot-verification page. It worked in Phase 6.
  - None was bypassed.
- **Tindie via Wayback:**
  - The Wayback CDX index lists 67 unique Tindie product URLs containing "meshtastic", from 21 sellers.
  - I fetched the latest archived copy of each (50 of 67 were captured in May 2026).
  - Tindie product pages show a review count and dated reviews, **but no sold counts**. "Sold out since <date>" is the only sales trace.
  - Listing date is proxied by the first archive capture, which is a late bound.
  - Results [Verified: web.archive.org snapshots of tindie.com/products/*, fetched 2026-10-13]:

    | First captured | Listings | Median reviews | Share with 0 reviews | Max reviews |
    |---|---|---|---|---|
    | 2021–23 | 7 | 1 | 43% | 4 |
    | 2024 | 27 | 0 | 89% | 6 |
    | 2025 | 23 | 0 | 91% | 3 |
    | 2026 | 10 | 0 | 100% | 0 |

  - Only 20 reviews across all 67 listings.
  - The most-reviewed listing is Neil Hao's Station G2 ($109, 6 reviews). Several of his units show repeated "sold out" dates, so reviews clearly undercount sales.
  - **$150+ listings (12):** 11 have 0 reviews and 1 has 1. Examples: SpecFive Spectre and MeshClip at $434.99, S5 Beacon variants at $179, almattor solar node at $175, Armachat Flip at $199.
  - **"Kit" listings (3):** FemtoFox dev kits and a T3S3 kit at $36.99, all with 0 reviews. No family or multi-handheld kit is listed.
  - Prices were parsed from the first price on each page and may be wrong for multi-variant items; the $999 and $6.30 values look like parsing errors.
- **Crowd Supply** search for "meshtastic" [Verified, 2026-10-13]:
  - Four campaigns mention it: IronEar 143 backers, AkiraConsole 452, HaloMax 19, WeatherXM D2 1,109.
  - None is a family kit, and none is a Meshtastic-first consumer kit.

### Reading
- Tindie newcomers selling higher-priced Meshtastic devices show almost no visible traction. That matches Phase 6's Amazon finding: branded $150+ communicators had 0–39 ratings.
- Tindie review rates are low even for sellers who sell out, so this is a weak negative.
- Tindie was not H1's planned channel. The decisive Amazon and YouTube conversion question could not be re-measured this phase because of the blocks.
- The evidence is consistent with Phase 6's proven-channel cut. It adds no new contradiction.

### Recommendation
- **No step change. Penalty stays at 7. Adjusted 51.2.**
  - CF 61, Scal 49, Dist 71.
  - Balanced = 24.4 + 19.6 + 14.2 = 58.2.
  - Adjusted = 58.2 − 7 = 51.2.
- **Note:** H1's Distribution score (71) is the highest of any leader, and it now rests on no measured newcomer conversion at the kit's price point anywhere.
- **Trigger for a cut:** if a later phase can read Amazon again and finds $300+ Meshtastic bundles with under about 20 ratings and no "bought" badges, cut proven channel −1 (Dist −6, giving **50.0**).
- **Confidence:** low–medium.

---

## 4. M1: Sage North America partner terms via Wayback (hold 49.6)

**Decisive assumption:** Sage's developer terms permit a hosted Sage 50 US/CA API that is resold to, or used by, third-party software vendors.

### Evidence
- **Wayback CDX index of PDFs on developer.sage.com** (12 entries): the only partner-programme PDFs are the NA "Developer Partner Program" brochure and "DevPartnerProg_Agreement.pdf", under both /100-us/guides/ and /300/guides/.
  - The **"Sage NA Tech Partner Program.pdf" (Mar 2025) cited in Phase 8 is not archived**.
  - There are no captures under /50-us/ or /50-ca/.
  - The live site returns 403.
- **"Developer Partner Program, August 2023, Sage North America"** [Verified: web.archive.org/web/20230924045731/…/100-us/guides/Sage NA Developer Partner Program.pdf]:
  - "The products included under this program are Sage 50 US/CA, Sage 100, Sage 300, and Sage X3".
  - Benefits include a "Not-for-resale copy of the Sage product for development purposes" and the SDK.
  - Eligibility:
    - "Must complete a formal application and submit for approval";
    - "Must complete the Developer Partner Program Agreement";
    - must pay fees;
    - products "must add functional value to" Sage 50 US/CA and the other listed products.
  - **Fees:** Sage 50 US/Canada (Category 1) is **$350 sign-up and $250 annual renewal**, with 1 free support case. Sage 100 and 300 cost $2,000.
  - Acceptance is "at the sole discretion of Sage".
  - Sage cites "nearly 3.2 million" NA SMB customers across all products [vendor claim].
- **"DevPartnerProg_Agreement.pdf"** [Verified: web.archive.org/web/20240427043142/…/100-us/guides/DevPartnerProg_Agreement.pdf; 11 pages; footer "Development Partner Program and license terms & conditions **Sage Medium Segment products** ©2022"]:
  - **Purpose:** tools "to develop add-on software modules … ('User Applications') to operate only in conjunction with and as a compliment to Sage's proprietary software".
  - **§3.1.1:** licence "solely to develop and test the User Applications and to demonstrate the Licensed Software in connection with Developer's efforts to sell end user licenses to the User Applications".
  - **§3.1.2:** Tools may be used "for development purposes only and not for production purposes".
  - **§3.3.2:** no "sublicense, transfer, sell, lend, rent, lease" of the Licensed Software or Tools, and Developer "shall not use, or allow others to use, the Licensed Software or Tools for the benefit of any third party."
  - **§3.3.4:** no circumventing "technological measures to prevent direct database access", and no "conversion functionality that converts end user data … to a competing product or service".
  - **§3.5:** no right to sell or distribute the Licensed Software "only under separate agreement".
  - **§10 (new vs Phase 8):** Sage may terminate "upon 90 days' written notice, for any reason, solely for Sage's convenience". After that, Developer has "no right to create or distribute any new User Application".
- **Search** (P9-AUDITL #3): no Sage 50-specific developer agreement surfaced. Only the same agreement, old Act! SDK licences and Sage 50 end-user EULAs. A 2015 Sage 50 EULA copy returned 404.
- **Unified-API vendors:**
  - Codat's Sage 50 integration is "Sage 50 Accounts (UK & Ireland)" only [Verified: docs.codat.io].
  - Rutter's sitemap lists only Sage Business Cloud Accounting and Sage Intacct [Verified: rutter.com/sitemap.xml].
  - No hosted US/CA Sage 50 API vendor was found that would show the model is tolerated.

### Reading
- **Confirmed:** Sage 50 US/CA developers join the same NA programme and sign "the Developer Partner Program Agreement". This makes it more likely, though still unverified, that Sage 50's terms follow the archived template. That template is labelled Medium Segment, not Sage 50.
- **The template's model** is add-ons sold as end-user licences to Sage customers. A per-company connector that the Sage 50 customer installs fits that model. A hosted API whose paying customers are third-party SaaS vendors is not contemplated.
- **Adverse clauses:** "for the benefit of any third party", "not for production purposes" for Tools, and anti-conversion (adverse for migration-tool buyers). Whether "for the benefit of any third party" reaches the end user's own Sage 50 copy, as opposed to the developer's not-for-resale copy and SDK, is ambiguous.
- **New platform risk:** termination for convenience on 90 days' notice.
- **Status:** still unresolved and leaning adverse, but **not directly contradicted**. There is no Sage 50 text, and the template is silent on hosted vendor-facing APIs. Phase 8's trigger for a higher penalty (the Sage 50 agreement carrying the same §3.3.2/§3.5 wording without a resale addendum) is not met.

### Recommendation
- **No step change. Penalty stays at 12. Adjusted 49.6.**
  - CF 68, Scal 60, Dist 52.
  - Balanced = 27.2 + 24 + 10.4 = 61.6.
  - Adjusted = 61.6 − 12 = 49.6.
- **Downside reading:** if a reviewer treats the confirmed single NA agreement plus the §3.1.1/§3.3.2 purpose limits as a direct contradiction of the vendor-facing model, the penalty goes 12 → 13, giving **48.6**.
- **Not re-proposed:** the red team's Phase 8 defensibility 1→0 (48.4). The 90-day termination clause supports it, but it is the same platform-dependence risk Phase 8 already weighed.
- **Positive (not scored):** entry cost is confirmed low ($350, then $250 a year).
- **Confidence:** medium on the documents; low on how they apply to the M1 model. Only Sage, under a signed application, can resolve it.

---

## Decisive unverified items after this audit
- **H6:** whether the NCAA, conferences or LEARFIELD enforce noncommercial terms against stats APIs or scrapers.
- **K8:** actual per-template sales for 2025–26 creators. Framer publishes none.
- **H1:** Amazon or YouTube conversion for $300+ multi-node bundles. Amazon, Etsy and Tindie were all blocked live this phase.
- **M1:** the Sage 50 US/CA agreement text and any SaaS/hosted addendum.

## Searches (4 of 8, logged as P9-AUDITL)
1. NCAA–Genius Sports official data rights. Exclusive to sportsbooks, championships only, through 2032.
2. SIDEARM/StatBroadcast terms. No data-licensing programme found.
3. Sage 50 SDK/developer agreement. No Sage 50-specific text found.
4. Framer creator payouts. Dec payout $784K to 649 affiliates.

Sources:
- [NCAA.com terms](https://www.ncaa.com/tos)
- [SIDEARM terms](https://sidearmsports.com/terms-of-service)
- [CBS Sports on NCAA/Genius](https://www.cbssports.com/betting/news/ncaa-strikes-data-and-logo-agreement-with-sportsbooks)
- [BusinessWire NCAA–Genius 2032](https://www.businesswire.com/news/home/20250425480652/en/NCAA-and-Genius-Sports-Expand-Partnership-Through-2032) (403)
- [CFBD terms](https://collegefootballdata.com/terms)
- [Highlightly terms](https://highlightly.net/terms)
- [createwith Framer December payouts](https://www.createwith.com/tool/framer/updates/december-creator-payout-total-surpasses-780k)
- [Framer marketplace sitemap](https://www.framer.com/marketplace/sitemap.xml)
- [Sage NA Developer Partner Program, Aug 2023 (Wayback)](https://web.archive.org/web/20230924045731/https://developer.sage.com/100-us/guides/Sage%20NA%20Developer%20Partner%20Program.pdf)
- [Sage DevPartnerProg Agreement (Wayback)](https://web.archive.org/web/20240427043142/https://developer.sage.com/100-us/guides/DevPartnerProg_Agreement.pdf)
- [Sage community thread 227809](https://communityhub.sage.com/ca/sage_50/f/general-discussion/227809/developer-license-to-support-integration/554843)
- [Codat Sage 50 docs](https://docs.codat.io/integrations/accounting/sage50/accounting-sage50)
- Tindie product pages via [Wayback CDX](https://web.archive.org/cdx/search/cdx?url=tindie.com/products/&matchType=prefix)
- [Crowd Supply search](https://www.crowdsupply.com/search?q=meshtastic)
