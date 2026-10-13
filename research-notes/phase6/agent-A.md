# Phase 6 — Discovery Agent A (Consumer & Prosumer, owned/direct acquisition)

Date: 2026-10-13 · WebSearch used: **8 of 8** (logged as P6-A in search-log.txt) · Scratch data: `scratchpad/p6plus/A/data/` (Skool discovery JSON sweeps, Substack leaderboard JSON)

## 0. Headline finding: a measurable newcomer channel for paid communities (and what it says)

The main new evidence this phase is **first-party newcomer data for paid communities**, taken from Skool's public discovery pages. Each listed group's `__NEXT_DATA__` JSON includes `createdAt`, `totalMembers`, price, billing interval and membership model. I pulled about 2,300 unique English groups across 34 hobby and life-event keywords (top 90 per keyword, "trending" sort), plus the top 240 trending groups in German, Spanish, Portuguese, Polish, Turkish and Italian. [Verified: skool.com/discovery JSON, fetched 2026-10-13.] Skool briefly returned HTTP 403 (rate limit) partway through. I stopped, waited and resumed at a slower rate. Nothing was bypassed.

**English, pure paid-subscription groups (membershipModel 2, monthly) created in the last 12 months: n = 454**
- Members: median **11**, p75 38, p90 87. 30% have 5 or fewer members.
- Implied MRR (price × members, an upper bound because some members may be comped or on trial): **84 (18.5%) ≥ $2k/month** and **33 (7%) ≥ $5k/month**. Median price is $25/month.
- Groups created more than 12 months ago have a median of about 60 members (survivorship).
- **Bias:** discovery shows "trending" groups, so dead groups are under-represented. The real newcomer distribution is worse than this.
- Third-party trackers are more optimistic but are built on the same upper-bound method. Profitable.app tracks 48.1k communities, 15.9k of them paid, with a modelled median MRR of $1,200 and 52.6% of paid groups above $1k (labelled an upper bound). [Verified: profitable.app/skool/stats, updated 2026-10-07.] RevenueGeeks reports a median of 205 members among the top-1,000 trending groups. [Secondary: search snippet.]

**By vertical (new pure-paid groups, last 12 months):**

| Vertical | n | Median members | Groups ≥ $2k implied MRR |
|---|---|---|---|
| Dog | 29 | 16 | 7 |
| Divorce | 14 | 35 | 6 |
| Menopause | 20 | 8.5 | 3 |
| Pregnancy | 9 | 11 | 1 |
| Postpartum | 16 | 5.5 | 0 |
| Baby sleep | 8 | 5.5 | 0 |
| Grief | 9 | 7 | 1 |

**Life-event communities underperform hobby or identity ones.** Members leave once the event passes.

**AI and Claude Code groups:**
- English, keyword "claude code" (top 60 of 662 matches): 28 new paid groups, median **48** members, 10 at ≥ $2k. Examples: "Claude Code Academy" 1,404 members × $97 (created Feb 2026); "Claude for Content Automation" 909 × $39 (Jun 2026).
- Spanish, keyword "claude": 12 new paid groups, median **136** members, 8 at ≥ $2k. Examples: "Agentic Engineers" 215 × $49; "Automatízate" 121 × $59; "Academia agentIA" 252 × $27.
- German "claude": 4 groups, median 12. Portuguese: 2 groups, median 8. Turkish: 7 groups, median 10. The exception in Turkish is "Rich Kids of Claude" with 272 × $29.

**Non-English generally (top 240 trending per language, all topics; new pure-paid median members):**

| Language | n | Median members |
|---|---|---|
| Spanish | 98 | 94.5 |
| German | 37 | 47 |
| Turkish | 83 | 34 |
| Polish | 31 | 19 |
| Portuguese | 33 | 8 |

These groups are dominated by make-money, AI, trading and self-improvement topics. Hobby and life-event groups in these languages are sparse and small. Examples: German dog groups "Hunderbar OnlyDogs" 250 × $90/yr and "One Team: Verstehe deinen Hund" 58 × $27; Spanish "Psicología Canina" 513 × $37; Polish "Mały Tenisowy Mistrz" 48 × $39. Brazil barely uses Skool (it runs on Hotmart/Kiwify), so the low Portuguese numbers are a platform artefact, not proof that demand is absent.

**Substack check:** I pulled the top-125 paid leaderboards for 8 consumer categories through Substack's public API. [Verified: substack.com/api/v1/category/public/{id}/paid, 2026-10-13.]
- New publications do reach these leaderboards (Food & Drink: 24 publications under 24 months old have "thousands of paid subscribers"). On inspection, though, they are creators importing existing audiences: "The Home Edit Group Chat" has 298k free subscribers, Byron Talbott is a YouTuber, and several are doctors with a media presence.
- Non-English publications are 2–7 of 125 per category.
- **Conclusion:** on Substack and Skool, the paying channel is the creator's own audience (YouTube, Instagram, TikTok). The platform is a billing layer, not an acquisition channel. A founder with no face or audience does not acquire customers here unless he partners with someone who has an audience. This shapes A2 and A3 below.

---

## A1. Elterngeld & family-benefits concierge for international parents in Germany ⭐ (top pick)

1. **Concept:** A fixed-fee, remote advisory and application service that optimises and files Elterngeld (parental allowance), plus Kindergeld and Mutterschaftsgeld, for parents in Germany who are not comfortable in bureaucratic German (English, Turkish, Arabic, Russian, Ukrainian, Polish, Spanish speakers). It runs on an AI-assisted intake and calculator, with a qualified German advisor reviewing every case.
2. **Paying customer and geography:** Expecting parents living in Germany. There were 654,241 live births in 2025. [Verified: destatis.de Geburten page, fetched 2026-10-13.] The share born to foreign-national parents is [Unknown] (Destatis has the table, but I did not extract it).
3. **Model and price:** One-time packages. Incumbent prices:
   - Elterngeldexperten: €179 advice / €279 application service / €329 plus. [Verified: elterngeldexperten.de, 2026-10-13]
   - Elterngeldhelden: €169 / €249 / €299, and already offered in German, English and Italian. [Verified: elterngeldhelden.de, 2026-10-13]
   - In January 2024 Finanztest put commercial advice-only packages at €120–149. [Verified: test.de/Elterngeldberatung-im-Test-5942423-0, published 2024-02-01]

   Prices have risen about 20–40% in under 3 years.
4. **Spending evidence:**
   - Stiftung Warentest/Finanztest tested 8 advisers, 4 of them commercial (Einfach Elterngeld, Elterngeldexperten, Elterngeld.net, Elterngelden), across 40 consultations. Its verdict: "Im Test überzeugen vor allem kommerzielle Anbieter", and specialist advice can be worth "Tausende Euro". [Verified: test.de, above]
   - Elterngeldexperten claims 25,000+ families served. [Vendor claim]
   - A test.de reader reports that Einfach Elterngeld raised its base price to €139 and is "oft ausgebucht", i.e. often booked out. [Anecdote] That hints at a capacity constraint.
   - The commercial category is documented. Volume per provider is not verified.
5. **Competitors and what customers dislike:** There are 4+ commercial specialists. Free advice is available from AWO, Caritas, Diakonie and pro familia, and from the Elterngeldstellen themselves (§14 SGB I). Free providers scored worse in the test. Weaknesses I can see: German-first service, booked-out capacity [Anecdote], and only Elterngeldhelden offers English/Italian. I found no Turkish, Arabic, Russian or Ukrainian provider, but absence from my fetches is not proof that none exist.
6. **Entry strategy:**
   - **Language and segment:** non-German-speaking and mixed-nationality couples. They also have harder cases: foreign income, cross-border employment, self-employment, EU coordination (Regulation 883/2004).
   - **Throughput:** AI intake (document upload, payslip parsing, scenario calculator across Basis/Plus/Partnerschaftsbonus month allocations) cuts adviser time per case.
   - **Pricing:** match €249–299, with a cheaper "check my own application" tier at about €99.
7. **Acquisition mechanism:**
   - High-intent search ("Elterngeld Beratung", "parental allowance Germany help", the same terms in Turkish and Arabic).
   - Expat Facebook groups and forums for international parents.
   - Referral partnerships with English-speaking midwives (Hebammen), birth-prep course providers and relocation firms.

   Channel evidence: the incumbents' existence and claimed volume rely on search. CAC is [Unknown], and newcomer outcomes are [Unknown]. Google Ads CPCs for "Elterngeld Beratung" were not checked (no public source within budget).
8. **Capital, ops, operability:**
   - Under $2k to test (landing pages in 3 languages, a calculator, a small ads test).
   - Delivery needs a German-qualified Elterngeld adviser. These are freelance or trained ex-Elterngeldstelle staff; Elterngeldberatung.de even sells adviser training, which points to a labour pool.
   - Operable remotely from Israel.
   - **Legal:** whether paid Elterngeld application help is an unlicensed Rechtsdienstleistung under the RDG is [Unknown]. Commercial GmbHs operate openly and Stiftung Warentest evaluated them without flagging legality, which is reassuring but not proof.
   - GDPR: sensitive data (income, health/birth), so a DPA and EU hosting are needed. Finanztest checked providers' privacy policies.
9. **Labour dependence:** Each case needs a human. Revenue scales with adviser hours, but advisers can be contractors and AI cuts minutes per case. The founder's own hours do not have to scale.
10. **Unit economics:**
    - [Hypothesis] €269 average ticket; 2 adviser-hours at €45 = €90; payment fees, tools and support ≈ €20; CAC unknown. With CAC at €60 [Hypothesis], about €100 contribution per case.
    - Track A ($2–5k/month profit) needs about 20–45 cases/month. That is plausible given 654k births a year.
    - Track B ($10–30k) needs 100–300 cases/month plus cross-sell (Kindergeld, Elternzeit planning, tax-class switch timing). Possible only if CAC stays low; incumbents with 25k+ families show the ceiling is real.
11. **Risks / killers:**
    - The RDG ruling.
    - The state digitises further (ElterngeldDigital already exists) or simplifies the benefit. Income cap cuts from April 2025 remove high earners (over €175k).
    - Paid-search CAC above about €120.
    - Advisor quality: errors cost families thousands, which creates liability.
    - The founder lacks German, so he is dependent on partners.

## A2. Native-language "AI agents / Claude Code for operators" paid community, Spanish first (founder = technical expert, native co-host = face)

1. **Concept:** A paid Skool-style community plus monthly cohort sprints teaching non-developers (small-business owners, marketers, freelancers) to build automations and agents with Claude Code, n8n and similar tools. Spanish is the first market. The founder writes the curriculum, templates and live builds; a native-speaking co-host fronts the content.
2. **Paying customer and geography:** Spanish-speaking prosumers and solo operators in Mexico, Colombia, Argentina, Chile and Spain. English is a fallback.
3. **Model:** $29–59/month membership, with an optional $300–600 cohort.
4. **Spending evidence:**
   - Skool data shows 12 new pure-paid Spanish "claude" groups with a median of 136 members, 8 of them at ≥ $2k implied MRR; examples are "Agentic Engineers" 215 × $49 (May 2026) and "Automatízate" 121 × $59 (May 2026).
   - English "claude code": 28 new groups, median 48 members.
   - Turkish "Rich Kids of Claude" has 272 × $29. German has DE "Die KI Community" 165 × $97, and Portuguese has "IA para Negócios" 140 × $80.

   [Verified: Skool discovery JSON, 2026-10-13; member counts are an upper bound on payers.]
5. **Competitors:** Many, and the field is growing fast. Spanish has at least 12 new paid groups in a year, and English is saturated (662 matching groups). Customer complaints I could not verify; generic "make money with AI" communities have a churn reputation. [Hypothesis]
6. **Entry strategy:** **Technical depth plus language.** Most competitors are marketers reselling prompts; the founder is a real builder. A vertical angle (e.g., "AI agents for Spanish-speaking real-estate agents" or "...for accountants") would separate it from generic groups. Credible only with a native co-host.
7. **Acquisition mechanism:** The co-host's YouTube/TikTok/IG channel, plus Skool discovery as a secondary channel. Evidence: top new Spanish groups reach 100–250 paying-ish members in 4–6 months. There is no evidence that a faceless operator reaches these numbers. CAC is [Unknown].
8. **Capital and ops:** Under $1k (Skool $99/month Pro plan + 2.9% fee [Secondary: skillscouter via search]). The founder can work remotely from Israel. Legal: consumer-protection rules on income claims.
9. **Labour:** Weekly live sessions and content keep it labour-dependent. Recorded curriculum and templates give partial leverage, and the co-host carries the audience work.
10. **Unit economics:**
    - [Hypothesis] 150 members × $45 = $6.75k MRR.
    - Minus 50% co-host revenue share, 3% platform fee and about $300 in tools gives roughly $3k owner profit, which is Track A.
    - Track B needs 600+ members; few new groups get there (Claude Code Academy at 1,404 is the outlier).
11. **Risks:**
    - Finding a co-host who already has an audience; this is the whole channel.
    - The AI-education fad fading, and monthly churn (the data shows median ages of about 5 months, so retention is unknown).
    - Tooling changes making the curriculum obsolete.
    - Reputational association with "get rich with AI".

## A3. Operator-partner for hobby/identity paid communities (dog behaviour first)

1. **Concept:** The founder becomes the operating partner (funnel, membership tech, onboarding automation, email, analytics, churn prevention, AI course production) for credentialed hobby experts who already have small audiences: dog trainers, menopause clinicians, sailing instructors, divorce coaches. He takes a 30–50% revenue share of the paid community he launches with them.
2. **Customer:** The end payers are hobbyists (dog owners etc.), US/UK first, then Spanish and German. The founder's "customer" is the expert partner.
3. **Model:** $25–60/month memberships plus one-off courses. The founder's share is a percentage of revenue.
4. **Spending evidence (Skool, new groups in the last 12 months):**
   - Dog: 29 groups, 7 at ≥ $2k implied MRR. Examples: "Understand the Dog™" 321 × $55 (Jun 2026, 18 reviews); "Dog Mama Academy" 156 × $83 (Mar 2026); "Oscar Mora Dog Training" 109 × $35 (Jan 2026).
   - Divorce: 6 of 14 at ≥ $2k.
   - Menopause: "The Menopause Rebellion" 234 × $197 (Jun 2026).
   - Spanish "Psicología Canina" 513 × $37.

   [Verified: Skool JSON 2026-10-13.] The flip side: a median of 11–16 members means most launches fail.
5. **Competitors:** Agencies and "Skool operators" already offer this (I saw no counts, but the category is known). [Hypothesis] Experts dislike agencies that bill upfront and leave; a revenue-share model aligns incentives.
6. **Entry strategy:** Pick partners using public data. An expert whose YouTube/IG audience is large relative to what they currently monetise is a candidate, and the founder can score this with scripts on public data. Start in the dog vertical, which has the best newcomer stats. Founder fit is high on the automation side.
7. **Acquisition mechanism:** Partner acquisition is direct outreach (founder labour). End-customer acquisition is the partner's owned audience. The evidence that this channel converts comes from the vertical top performers above. That newcomers *with* an operator do better is [Hypothesis].
8. **Capital and ops:** Minimal capital. Operable from Israel. Contracts are needed (revenue share, IP).
9. **Labour:** Medium to high per partner at launch, then lower. Each partner is roughly a 3–6-month build. Revenue can outgrow hours only with a repeatable playbook across 5+ partners.
10. **Unit economics:** [Hypothesis] Per successful partner: 150 × $45 = $6.75k MRR, 40% share = $2.7k. With 1 in 3 launches succeeding (consistent with the 18.5% ≥ $2k base rate among visible newcomers, lifted by partner selection), the founder needs 3 launches to reach Track A. Track B needs 4–8 successful partners.
11. **Risks:** It slides into agency or service work, which conflicts with the founder's preference. Partners leave once the community works. Success rates are low and could be lower than the visible data suggests. Dependence on Skool (fee changes, discovery changes).

## A4. Online MPU preparation for non-native-German drivers (Germany)

1. **Concept:** Structured online preparation for the medical-psychological assessment (MPU) needed to regain a driving licence. Delivered in Turkish, Russian, Arabic, Polish or Ukrainian, with an AI-built self-study module plus sessions with licensed traffic psychologists (Verkehrspsychologen).
2. **Customer and geography:** Residents of Germany who lost their licence (44% over alcohol, about 21% over drugs/medication).
3. **Model and price:**
   - ADAC: individual sessions from about €100/hour; MPU itself €400–800; total cost €1,350 (points) to €2,200–2,850 (alcohol, drugs). [Verified: adac.de MPU-Kosten, 2025-10-21]
   - Packages: TÜV SÜD from €900; group courses €600–800, individual €1,000–1,500. [Secondary: search snippets of tuvsud.com and allianzdirect.de; tuvsud.com returned 403 to WebFetch]
4. **Spending evidence:**
   - 70,135 MPUs in 2025 (−7%), with 38% judged unfit. [Verified: autohaus.de, 2026-08-24, citing BASt] 2024 had 75,257 [Secondary: search snippet], the third straight decline.
   - Failures generate repeat preparation.
   - [Hypothesis] Implied prep spend is in the tens of millions of euros a year.
5. **Competitors:** TÜV SÜD Pluspunkt, DEKRA and similar, plus many independent psychologists. ADAC warns about dubious providers promising a guaranteed pass, so customers distrust the category. Foreign-language supply is [Unknown].
6. **Entry strategy:** Language-specific offers plus a trust-first approach (no pass guarantees, transparent pricing, installments). This is a thin but real wedge.
7. **Acquisition:** High-intent search and community word of mouth. CAC is [Unknown]. Newcomer evidence: none.
8. **Ops and legal:** Requires accredited psychologists; abstinence proofs come from labs. Remote delivery is possible. Advertising claims in this sector are heavily scrutinised.
9. **Labour:** High; it is fundamentally session-based.
10. **Economics:** [Hypothesis] A €900 package with about 50% going to the psychologist gives €450 gross per client. Ten clients a month is about Track A. Track B is unlikely.
11. **Risks:** Shrinking market. Heavy dependence on psychologist partners. Reputational association with the category. The founder cannot quality-check delivery in the language.

---

## Ideas killed (with reason)
- **Paid flight-deal alerts in non-English markets (PL/BR/MX):** The local leaders are free and ad/affiliate-funded. Fly4free has about 100k newsletter subscribers and about 1M Facebook followers with no paid tier [Verified: fly4free.pl, 2026-10-13]. Melhores Destinos is free, since 2008 [Verified: melhoresdestinos.com.br]. Paid alert services surfaced only in the US (Going, 2M+ travellers, paid count undisclosed [Verified: going.com/about]; Thrifty Traveler $89.99/yr). There is no evidence local users will pay.
- **US marriage name-change kits:** MissNowMrs claims 500k brides since 2007 [Vendor claim, verified page]. HitchSwitch sells $49.99–129.99 tiers and partners with The Knot and WeddingWire [Verified: hitchswitch.com]. Incumbents own the channel. In ES, LatAm and much of the EU, the custom (name change on marriage) or the process does not create the same demand. No credible entry.
- **Life-event communities (pregnancy, postpartum, baby sleep, grief) by a newcomer:** Skool newcomer medians are 5.5–11 members, with 0–1 groups at ≥ $2k per vertical. Taking Cara Babies shows the money is in one-off classes from a credentialed creator ("1M+ sold" [Vendor claim]). Localising it needs a credentialed local expert, which makes it a sub-case of A3.
- **Mexican US-visa DS-160 / interview prep:** Volume is high, but the US government says no external expediters are authorised. Paid help sells at MXN 500–3,000 (about $25–160). [Verified: cuantomecuesta.com/mx/visa-americana, Apr 2026; elimparcial.com 2026-02-20] There is strong scam stigma and the DS-160 is free. Thin price and trust problems make it a poor bet.
- **Substack hobby newsletter by a faceless founder:** New entrants on the paid leaderboards bring existing audiences, and non-English publications are 2–7 of 125. There is no channel for a newcomer without an audience.
- **Brazil infoproducts (Hotmart/Kiwify):** Proven spending, but acquisition is the creator's Instagram plus paid traffic, and the market is native-Portuguese and crowded. Same partner dependence as A3, at higher CAC. Not investigated further.
- **German Einbürgerung/driving-theory prep:** Exam prep is excluded by the ledger ("licensure exam-prep"). Skipped.

## Ranking
1. **A1 Elterngeld concierge for international parents (DE):** Verified spending (category tested by Stiftung Warentest, rising prices, a 654k-births/yr flow), high-intent search acquisition, labour that can be delegated to contractors. Gaps: RDG legality, CAC.
2. **A2 Spanish-language AI-operator community:** Best founder fit and verified newcomer outcomes in the exact niche. Depends on a co-host and a fad.
3. **A3 Operator-partner for hobby communities:** Good measured base rates, low capital, but drifts towards services.
4. **A4 MPU prep in foreign languages:** Real spending, but a shrinking market, heavy labour and partner dependence.

The scope yielded 4 credible opportunities rather than 6–8. The others did not survive the newcomer-channel test, and I chose not to pad the list.

## Top picks for deep diligence and the decisive unverified assumption
- **A1:** That paid Elterngeld application help by a non-lawyer company is lawful under the RDG, **and** that search or expat-community CAC stays below about €100 per case for non-German-speaking parents. Next checks: the RDG/BSG position (BSG cases on benefit-application assistance); Destatis births by mother's nationality; Google Ads Keyword Planner CPCs (needs an account, so out of scope here).
- **A2:** That a Spanish-speaking co-host with an existing audience of at least 20–50k will partner on a revenue share, and that monthly churn stays below about 10%. Next check: score Spanish YouTube/TikTok AI-education creators by audience against monetisation (public data).
- **A3:** That operator involvement lifts the success rate meaningfully above the roughly 18% visible base rate. Next check: track the same Skool cohort (saved JSON) again in 60–90 days to measure growth or death of 2026 groups. This is a cheap, repeatable newcomer-velocity measurement and also improves the evidence for A2.

**WebSearch count: 8 / 8.** Blocked sources: Trustpilot (403 for all 5 attempts), tuvsud.com (403), Skool (temporary 403 rate limit; resumed later at a slower rate, no bypass).
