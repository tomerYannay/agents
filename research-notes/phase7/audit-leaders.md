# Phase 7 leader re-check (Evidence Auditor, P7-AUDIT-L), 2026-10-13

Scope: newcomer and channel test on UK MTD prep (#2, 52.6), J1 Hebrew/Russian memoir books (#6, 51.0) and H10 ketubot (#9=, 50.6). The method is the same as the Phase 6 leader corrections: named criterion steps worth weight/5 points each. Wider market spending is not credited as channel evidence unless there is data on how new entrants did.

WebSearch: **10 of 10 used**, all logged as `P7-AUDIT-L`. Two of them were Hebrew queries, and both came back with English-only results because the search engine is US-only. The rest of the work was WebFetch and curl on public pages. Data and scratch files are in `scratchpad/p6plus/P7-auditL/data/`.

**Blocked sources:**
- Etsy, The Knot and Thingtesting returned 403.
- Shopify `products.json` returned 429 or 406 on the ketubah domains I guessed.
- The Xero App Store renders with JavaScript, so it can't be parsed.
- CIPP returned 403.
- I found no gov.uk page with MTD ITSA statistics (404).

**About the baselines:** the earlier reports never published criterion-level steps for these three leaders. The baseline steps below are reconstructions that reproduce the published CF/Scal/Dist totals exactly; they are not the original working. Only the **deltas** are recommendations, and each delta can be traced to a source.

Step values: CF: spending 5, speed 4, capital 4, margin 4, labour 3. Scal: depth 3, recurring 4, acquisition 4, leverage 4, defensibility 3, fit 2. Dist: clarity 4, discoverability 4, proven channel 6, first customers 3, beyond founder 3.

---

## 1. UK MTD white-label quarterly prep (52.6)

### Verified facts
- **Uptake is real and ongoing:**
  - More than 570,000 had signed up for MTD for Income Tax.
  - More than 436,000 had filed their first quarterly update by the 7 Aug 2026 deadline.
  - HMRC's August 2025 estimate was about 864,000 taxpayers in scope.
  - There are no penalty points for late quarterly updates in 2026-27. Points apply from 6 Apr 2027, with a £200 fine at 4 points.
  - The £30k threshold applies from April 2027 and £20k from April 2028.
  - [Verified: rossmartin.co.uk/sme-tax-news/9073-436-000-file-under-making-tax-digital-for-income-tax, page updated 12 Aug 2026, accessed 2026-10-13]
  - HMRC starts signing up non-registered taxpayers from September 2026 [Secondary: ICAEW and IAB headlines in search snippets; not opened].
- **The letting-statement pain point is real:**
  - Agents send monthly or annual PDF statements, sometimes with only a net figure. HMRC wants gross rent with fees shown as expenses, so the figures must be split.
  - The landlord, not the agent, carries the legal responsibility.
  - **But the NRLA already sells a fix:** "NRLA Portfolio" offers bulk upload of digital statements, and Tax'd is its MTD software partner.
  - [Verified: nrla.org.uk/news/making-tax-digital-are-you-and-your-agent-on-the-same-page, published 12 Feb 2026]
- **Offshore outsourcers already sell this exact work to practices:**
  - **Outbooks** offers MTD setup, categorisation into HMRC categories, digital attachments, all four quarterly updates, year-end support and an internal review before submission. It positions this for "accounting and bookkeeping practices that want to deliver MTD work for their clients". No prices are published. It claims "20,000+ end clients" and "33,000+ self-assessments per year" (vendor claim). [Verified: outbooks.co.uk/services/making-tax-digital/ and outbooks.co.uk, accessed 2026-10-13]
  - **QX Accounting** says it handles quarterly MTD ITSA returns and runs an "MTD Query Hub" and an "MTD Readiness Score". It claims "1,100+ dedicated accountants" and 22 years in business. Its tax-preparation pricing page says "Starting at Just £30*" with no MTD price. [Verified: qxaccounting.com/uk and /uk/pricing/tax-preparation/, accessed 2026-10-13]
- **Incumbent software is automating the prep step itself:**
  - **Sage** announced the "UK's first MTD for Income Tax Agent" on 24 Sep 2025. It segments clients by complexity, organises client information, chases documents and flags issues. It shipped through Sage Copilot from October 2025. [Verified: gpa.net/blogs/emea-1/uk-sage-announces-first-mtd-ai-agent, accessed 2026-10-13]
  - **ANNA Money** raised £10M of growth debt (Jan 2026) for an "MTD-ready solution designed to automatically prepare and submit these digital updates once a business account is connected". It reports 50k+ monthly SMB users and £30M ARR (vendor claim). [Verified: thefintechtimes.com/anna-money-secures-10m-…, 26–27 Jan 2026]
- **HMRC software list:**
  - The gov.uk compatible-software page no longer lists products; it points to a finder tool instead.
  - The "in development" section was removed on 13 Jul 2026.
  - Free products exist for simple tax affairs.
  - [Verified: gov.uk/guidance/find-software-thats-compatible-with-making-tax-digital-for-income-tax, updated 13 Jul 2026]
- **Price signals:** Xero's 11 Jun 2026 pricing guide gives no rates ("no standard rate") [Verified]. No white-label per-client MTD price was found anywhere.

### Unknowns
- No newcomer outcome of any kind: how many practices a new or foreign MTD-prep provider has won, its review counts, or app-partner data. The Xero App Store can't be parsed.
- No ICAEW or ACCA survey giving the share of firms that outsource. Only vendor-quoted ACCA 2024 "belief" statistics turned up (snippets).
- No white-label price. No split between agent-filed and self-filed updates.
- Whether HMRC still restricts production credentials for new products. This is moot for an upstream-prep model.

### Assessment
- **Demand is stronger than in Phase 2.** The mandate is live and 436k quarterly updates have been filed.
- **The entry wedge is now occupied from three sides:**
  - offshore outsourcers that already market MTD quarterly work to practices at scale;
  - AI automation inside the incumbent software (Sage agent, ANNA);
  - the landlord association's own bulk statement-upload product.
- The first quarterly cycle passed without a new entrant, and practices have already chosen their 2026-27 workflows.
- The next demand step is the 2027 £30k wave. Because there are no penalty points this year, urgency is lower.
- A new entrant gets nothing measurable from any observed channel. The Phase 3 note still holds: "no evidence that cold email from a foreign AI provider reaches UK practices".

### Recommended rescoring

Reconstructed baseline steps:
- CF: 3, 3, 4, 3, 2 = 61
- Scal: 5, 5, 2, 3, 1, 4 = 66
- Dist: 5, 3, 2, 2, 3 = 59

Changes:

| Criterion | Change | Points | Reason |
|---|---|---|---|
| Defensibility | 1→0 | −3 | Sage's MTD agent and ANNA's automatic preparation automate the prep step; Outbooks and QX sell the same service to practices. Same logic as Phase 3, where allocation verification got defensibility 0 because vendors already do it. |
| Proven channel | 2→1 | −6 | Consistent with the H6, H1 and K8 corrections in Phase 6. What was credited before was evidence that outsourcers exist, not newcomer outcomes. Two searches and 6 fetches found no newcomer data. Large incumbents (20k end clients; 1,100 staff) hold the offshore lane. |
| Spending evidence | hold | 0 | The 436k filings measure workload, not purchases of outsourced prep. List prices are not transactions (Phase 6 rule, K13). |
| Market depth, recurring | hold (already 5) | 0 | Confirmed: 864k in scope now, more in 2027 and 2028. |
| Speed to first sale | hold | 0 | Late joiners and auto sign-up give a window before Nov 2026 and Feb 2027, but no evidence either way. |
| Penalty | 10→11 | −1 | Phase 2's "largest unproven assumption" (practices would pay a foreign AI-first provider despite offshore bookkeepers and client-side apps) is now partly contradicted: those alternatives are verified, live and targeting the same task. That is the same kind of contradiction that moved H1's penalty from 6 to 7. |

**Result:** CF 61, Scal 63, Dist 53 → Balanced 60.2 → penalty 11 → **Adjusted 49.2** (was 52.6).

If the penalty stays at 10, the score is 50.2. I recommend 11, because the contradiction concerns the entry wedge rather than competition in general, so it is not double-counted with defensibility.

---

## 2. J1 Hebrew/Russian voice-to-hardcover memoir books (51.0)

### Verified facts
- **MyStories (MyHeritage) now has the core J1 feature set:**
  - Users "record or write"; speech is turned into text by AI.
  - An AI editor keeps the storyteller's voice.
  - "Every recorded story comes with a QR code in the printed book. Scan to hear the voice."
  - Recordings work from desktop, phone or tablet.
  - The membership includes a year of questions, one hardcover book and "global free shipping on the first copy".
  - [Verified: mystories.com; mystories.com/frequently-asked-questions; help.mystories.com/en/articles/13430082, accessed 2026-10-13]
  - At the Feb 2025 launch it was English only, LTR only, had no audio and cost $99. [Verified: blog.myheritage.com/2025/02/introducing-mystories-…, 6 Feb 2025] So the product has closed the audio gap in about 18 months.
- **Languages:**
  - The FAQ says "available in 10 languages": Danish, Dutch, Finnish, French, German, Italian, Norwegian, Portuguese (Brazil), Spanish and Swedish.
  - "MyStories only supports left-to-right text formatting at this time."
  - Users may reply in an unsupported language.
  - Russian is not listed. Hebrew is not supported, because it is RTL.
  - [Verified: mystories.com/frequently-asked-questions, accessed 2026-10-13]
- **Hebrew is being prepared.** The live mystories.com HTML contains a Crowdin language switcher with the comment "Add Hebrew if test parameter is present" (`test-heb=1`). Its language data includes `he-il` / "עברית", and there is a `?lang=he` page and a Hebrew help-guide link. This is site-interface localisation in testing, not proof of RTL book printing. The sitemap was last modified 2026-10-04. [Verified: curl of mystories.com and ?lang=he, 2026-10-13; saved in data/he.html]
- **Remento:** Speech-to-Story supports English and Spanish, with "more languages on the way soon". It ships to the US, Canada, the UK, Ireland, Australia and New Zealand; Israel is not listed. [Verified: remento.co/faq, accessed 2026-10-13]
- **Storyworth:**
  - English and Spanish interface. "Stories can be written and viewed in any language", and its "printing software supports most but not all languages".
  - Phone and landline recording.
  - Extra books cost $39 (black and white) or $79–99 (colour).
  - It prints in the US and Europe; customs may apply.
  - Unchanged from Phase 4. [Verified: welcome.storyworth.com/faq, accessed 2026-10-13]
- **No Hebrew or Russian voice-to-book competitor surfaced** in two Hebrew searches and one Russian search. The search engine is US-only and weak for Hebrew, so this is **unknown, not absent**.
  - The Russian results showed interview-based family-book studios with about a 5-month process [Secondary: sostav.ru blog snippets], plus fill-in gift books from Eksmo.

### Unknowns
- Whether MyStories' Hebrew test includes RTL book printing, and when it would launch.
- Whether Cyrillic replies print correctly in MyStories or Storyworth. If they do, the Russian gap is mostly language-of-questions only.
- Israeli prices and competitors.
- Any newcomer outcome for a non-English memoir service (orders, reviews), or any Israeli acquisition cost.

### Assessment
- **Hebrew RTL is still a real gap today.** It is verified as unsupported by all three major services.
- **The defensible window is visibly closing:**
  - The Israeli-owned incumbent has already added voice, QR codes, 10 languages and global free shipping.
  - It is testing Hebrew localisation of its site.
- **The Russian gap is weaker than assumed.** Both MyStories and Storyworth accept text in other languages, and Russian is left-to-right.
- Channel evidence is still US-only and category-wide, with no newcomer data.

### Recommended rescoring

Reconstructed baseline steps:
- CF: 3, 3, 4, 4, 3 = 68
- Scal: 3, 1, 3, 4, 2, 4 = 55
- Dist: 4, 3, 3, 3, 3 = 64

Changes:

| Criterion | Change | Points | Reason |
|---|---|---|---|
| Defensibility | 2→1 | −3 | MyStories added voice, QR codes and global shipping after launch and is testing Hebrew (verified code flag). The only verified differentiator left is RTL Hebrew printing. |
| Proven channel | 3→2 | −6 | Storyworth's and Remento's review volumes are category-wide US evidence. Under the Phase 5–6 standard (H7, J7, K8) this is not credited without newcomer outcomes, and none were found for any non-English or Israeli memoir offer. |
| Market depth | hold | 0 | The Russian gap is weaker, but I am not cutting depth as well, to avoid stacking on the same finding. I flag it for the red team. |
| CF criteria | hold | 0 | No new transaction evidence either way. |
| Penalty | hold at 11 | 0 | Phase 4's decisive assumption ("MyStories does not produce Hebrew RTL books") is **confirmed as of today**. The threat to it is already scored under defensibility. Net: no change. |

**Result:** CF 68, Scal 52, Dist 58 → Balanced 59.6 → penalty 11 → **Adjusted 48.6** (was 51.0).

---

## 3. H10 Ketubot (50.6)

### Verified facts
- **Ketubah.com:**
  - "Our team's been doing this for almost 30 years."
  - "Trusted by thousands of couples worldwide."
  - Rush orders are offered.
  - The homepage gives no artist count and no artist-submission programme.
  - It runs on WooCommerce.
  - [Verified: ketubah.com, accessed 2026-10-13]
  - The "75+ artists" figure from Phase 3 was not re-confirmed on the homepage.
- **Newcomer example: Love Letters Ketubahs**
  - Founded Sep 2024 and launched Oct 2024, according to a search snippet from Thingtesting, which showed "no reviews yet" (403 when fetched).
  - Its own Wix site lists giclée prints from $420 with free worldwide shipping and custom text and translation.
  - It shows one unattributed press quote, "Bestseller" labels and no review count or sales claim.
  - [Verified: lovelettersketubahs.com, page dated 3 Oct 2026, accessed 2026-10-13]
  - About two years after launch, it shows no measurable traction signal.
- **Other signals (search snippets only; Etsy and The Knot returned 403):**
  - Jennifer Raichman's Etsy shop: about 4,394 sales and 1,039 reviews. She is an incumbent.
  - Studio Shoshan: "a handful" of early-2026 reviews.
  - Ink with Intent: 46 reviews on The Knot and Best of Weddings 2020–23. Its own site is WooCommerce.
  - Several Etsy shops have reviews dated mostly 2017–2024. [Secondary: search snippets]

### Unknowns
- Etsy sales and review velocity for shops opened in 2024–26. This is the decisive measurement, and it is blocked.
- Shopify review counts. None of the domains I guessed exposed `products.json`.
- Ketubah.com's current artist count, and whether it takes new artists.
- Google Shopping is not accessible.

### Assessment
- What Phase 3 credited as channel evidence (an Etsy shop with about 1.5k sales, unverified) is incumbent evidence.
- The newcomer signals available are thin and point the same way as Phase 5: a 2024 entrant with a polished site and worldwide shipping shows no visible reviews or sales claims, while established artists hold the review base.
- No new contradiction of the Ketubah.com incumbency beyond what Phase 3 already scored.

### Recommended rescoring

Reconstructed baseline steps:
- CF: 3, 4, 5, 4, 3 = 76
- Scal: 2, 1, 3, 4, 1, 3 = 47
- Dist: 5, 5, 3, 2, 1 = 67

Changes:

| Criterion | Change | Points | Reason |
|---|---|---|---|
| Proven channel | 3→2 | −6 | The credited Etsy sales are incumbent outcomes. The only checkable newcomer (Love Letters, 2024) shows no reviews or traction. Same standard as H7, J7, K8 and H6. |
| Defensibility | hold at 1 | 0 | Already low. Nothing new found. |
| Penalty | hold at 12 | 0 | Evidence is weak (snippets, blocked Etsy) but not newly contradicted. I don't raise the penalty for blocked sources; that would double-count the channel cut. |

**Result:** CF 76, Scal 47, Dist 61 → Balanced 61.4 → penalty 12 → **Adjusted 49.4** (was 50.6).

---

## Summary

| Leader | Changes | CF / Scal / Dist | Balanced | Penalty | Adjusted |
|---|---|---|---|---|---|
| UK MTD prep | Defensibility −1 (−3), Proven channel −1 (−6), penalty +1 | 61 / 63 / 53 | 60.2 | 10→11 | **49.2** (was 52.6) |
| J1 memoir books | Defensibility −1 (−3), Proven channel −1 (−6) | 68 / 52 / 58 | 59.6 | 11 | **48.6** (was 51.0) |
| H10 ketubot | Proven channel −1 (−6) | 76 / 47 / 61 | 61.4 | 12 | **49.4** (was 50.6) |

**What did not change, and why:**
- **No upward moves.** The only positive evidence was MTD uptake (436k filings) and the confirmed NRLA pain point. Those measure workload, not purchases from a supplier like this founder, so under the K13 rule they earn no credit.
- **J1's decisive assumption.** It is still true today, so I did not raise its penalty.

**Effect:** all three fall inside the noise band and land around #11–16 on the cumulative board.

**Decisive unverified assumption for each:**
- **MTD:** a UK practice will route quarterly prep to a new foreign provider, despite Outbooks, QX, Sage's agent and NRLA Portfolio.
- **J1:** the window before MyStories ships Hebrew RTL books is long enough to build an Israeli customer base; plus Israeli acquisition cost.
- **H10:** Etsy review velocity for ketubah shops opened in 2024–26 (blocked here; needs a manual check).

**Searches used: 10/10** (logged as P7-AUDIT-L in research-notes/search-log.txt).
