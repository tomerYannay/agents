# Phase 6 Report -- Regulation-driven and B2B service opportunities (2026-10-13)

Method: frozen Phase 3 rubric (CF/Scal/Dist, weights 0.4/0.4/0.2, evidence penalty 0-15). Six discovery agents (A-F) -> ~40 raw ideas -> 12 shortlisted (L1-L12) -> pricing/competitor checks (6.3) -> independent audit (6.4) -> independent red team (6.5) -> scoring (6.6).
Phase purpose: counter Phase 1-5 biases (Israel/diaspora affinity, low-capital digital marketplace products, software tilt) by looking at deadline/regulation-driven B2B spend and services with existing budgets.

## Evidence limits (read first)
- All prices come from vendor pages or third-party roundups seen only as search snippets. WebFetch failed DNS in this run, so NO primary page was fetched in 6.4. Everything is "secondary". Primary verification is pending.
- No customer contact, no purchases, no simulated interviews. Willingness-to-pay for a new entrant is UNKNOWN for every candidate.
- The red team noted that near-uniform penalties (11-14) compress differences; gaps under ~5 points are noise. Treat results as tiers.

## Killed in 6.3: L6 KSeF last-mile, L10 refurb label printers, L12 EUDR validation (reasons in overnight-research-log.md).

## Audited candidates (verified facts, secondary)
- L2 US sales-tax for foreign sellers: Kintsugi $75/filing, ~$699-799/state/yr; Avalara $699-799/state/yr. Foreign sellers can get an EIN without SSN but states ask a responsible-party SSN/ITIN; Anrok/Numeral/Zamp/Zenind already publish foreign-seller guides. POA/legal-filer rules UNKNOWN (gate: needs CPA/EA partner).
- L1 SOC2/ISO evidence-keeper: platforms $4-25k/yr (Secureframe from $7k), vCISO $1.5-5k/mo. Only a CPA signs reports; operating a client's controls creates AICPA independence conflict. Delve allegations (class action Apr 2026) raise buyer scepticism of AI-driven providers.
- L3 Amazon appeals: $300-4,000 flat; hugely crowded; self-filing is free; no demand or channel data.
- L8 GPSR EU rep + labels: EUR 139-199/yr/product type, crowded, needs EU entity.
- L9 denial recovery: no verified contingency rate (4-10% unverified); R1/Aspirion etc.; HIPAA BAA; no evidence small entrants win.
- L4 CBAM: definitive period since 1 Jan 2026, 50t threshold, certificates from 1 Feb 2027, first declaration 30 Sep 2027 (secondary sources); ~90% of importers exempt; competition UNKNOWN.
- L7 French PA connector: Iopole already sells white-label API to software vendors; 1 Sep 2026 deadline passed.
- L5 Battery Passport, L11 filter replenishment: weak (see log).

## Red-team adjustments applied (documented)
L3: CF 69->60, Dist 58->50 (Fiverr floor, free self-filing, no demand data). L1: Scal 57->51, Dist 47->44 (independence conflict caps leverage/defensibility; Delve trust friction). L8: CF 56->52 (EU entity capital). L9: CF 51->45 (slow contingency cash, BAA). L2 unchanged but POA/ITIN feasibility is a hard GATE. Services score modestly on Scalability for real: they do not scale beyond founder/partner hours.

## Phase 6 scores (CF / Scal / Dist -> Balanced - penalty = Adjusted)
| Opp | CF | Scal | Dist | Balanced | Pen | Adjusted |
|---|---|---|---|---|---|---|
| L2 US sales-tax for foreign sellers | 58 | 55 | 55 | 56.2 | 12 | **44.2** |
| L1 SOC2 evidence-keeper | 61 | 51 | 44 | 53.6 | 13 | **40.6** |
| L3 Amazon appeals retainer | 60 | 37 | 50 | 48.8 | 12 | **36.8** |
| L8 GPSR rep + labels | 52 | 42 | 46 | 46.8 | 11 | **35.8** |
| L4 CBAM data pack | 52 | 41 | 42 | 45.6 | 12 | **33.6** |
| L9 Denial-appeal recovery | 45 | 50 | 38 | 45.6 | 13 | **32.6** |
| L11 filter replenishment | 46 | 37 | 38 | 40.8 | 12 | 28.8 |
| L7 French PA connector | 42 | 45 | 34 | 41.6 | 12 | 29.6 |
| L5 Battery Passport | 46 | 38 | 35 | 40.6 | 12 | 28.6 |

Finalists (about five, "least bad", not strong): L2, L1, L3, L8, L4 (L9 a close sixth, within noise).

## Prior-score correction (material new evidence): H6 college-baseball data API
Original: CF 75 / Scal 66 / Dist 64 -> Balanced 69.2 - pen 12 = **57.2**.
New evidence (6.4): free incumbents Highlightly (free tier 100 req/day) and BALLDONTLIE; 64 Analytics $9.99-12.99/mo; NCAA ToS restricts reuse; zero evidence that any small college-baseball API has paying customers (channel evidence was only CFBD, football).
Corrected: CF 65 / Scal 58 / Dist 50 -> Balanced 59.2 - pen 14 = **45.2**. (Red team argued even lower, ~40-42; kept 45.2 since the premium JUCO/NAIA niche is unaddressed but unproven.)
H1 Meshtastic: re-check found crowded Etsy and newest entrant ~29 sales/14 reviews since 2025; no correction (54.6) but flagged. monday.com Israeli invoicing: marketplace unreachable; unchanged (52.0), still pending manual check.

## Comparison with prior leaders
No Phase 6 opportunity approaches the Phase 3-5 leaders (H7 56.6, H1 54.6, K13 53.6). Best new, L2 (44.2), ranks below the top ~20. Conclusion: Phase 6 did NOT find a superior business. Regulation-driven themes were mostly already served by bundled/free tools, incumbents with API white-labels, or require local licensed entities. L2 is worth a cheap gating check only (POA/ITIN feasibility with a CPA/EA; foreign-seller demand), which needs future external validation (no contact done).

## Needed validation (not done: no contact allowed)
L2: can a non-CPA operate via POA; CPA/EA partner willingness; foreign-seller willingness to pay above $75/filing. H6: NCAA data rights. monday: manual marketplace check.

## Lessons for Phase 7
- Supply-side pricing (vendor pages) proves incumbents' existence not entrant demand; treat as supply evidence.
- Licensing/entity gates (CPA, HIPAA, EU rep) are binary blockers: check them first.
- Services on a part-time founder do not score on scalability; prefer productized/automated delivery.
