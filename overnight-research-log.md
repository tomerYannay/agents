# Research log

## 2026-10-13 run 1 (Phase 6, step 6.1 discovery)
Persistence: `git push` -> 403 and GitHub MCP push_files -> 403 (Claude GitHub App has no write access to tomerYannay/agents). Work exists only in the local container commit until access is fixed. No `research` branch exists.

Discovery results (search budget ~3-10 per agent; prices mostly ASSUMPTION/UNKNOWN):
- A: GPSR EU-representative + label pack for non-EU sellers (EUR 150-500/yr, crowded); Amazon/Etsy suspension appeal writing (FreeeUp $300+$300 success; law firm $1,500); JDM proxy buying; killed pet-groomer/piano/homeschool/pilot apps.
- B: refurb label printers + consumables; refurb coffee machines; private-label dental/vet consumables; B2B compatible filter replenishment; discontinued-appliance parts; PPWR kits (overlap, weak).
- C: CBAM supplier-data pack for small EU importers (strongest of C); EUDR geolocation validation; NEMT claim-denial scrubber; FSMA 204 (deadline 2028, weak); aviation 8130-3 intake; cold-chain GDP reports.
- F: Poland KSeF last-mile for bookkeepers (micro-firm deadline 1 Jan 2027); EU Battery Passport data prep (18 Feb 2027); ZATCA wave-24 cleanup (marginal); Gulf WhatsApp back-office, LatAm customs (weak).
- D: KSeF bridge (WooCommerce/Allegro->KSeF; PL apps price 4.99-19 PLN/mo, weak); French PA-connector white-label for niche software vendors (SME issuing 1 Sep 2027; PA prices 9-40 EUR/mo); Belgian Peppol (killed, deadline passed); EU Battery Passport (DPP Hero $57-289/mo, per aggregator); CBAM declarant kit; EUDR small-operator (simplified, weak); EAA audits (killed).
- E: managed SOC2/ISO evidence-keeper for 10-50 person SaaS (managed SOC2 from $5k/mo, vCISO $3-5k/mo; undercut at $1.5-2.5k); done-for-you US sales-tax nexus filing for foreign sellers ($99-599/mo; $75/filing/state); Amazon account-health retainer ($500/mo, reinstatement $1-3.5k); denial-appeal factory for specialty practices; white-label review ops (price war); AP outsourcing to CPA firms (overlaps prior).

## Step 6.2 dedupe / shortlist (12) -- see next-phase-plan.md

## 2026-10-13 run 1 cont. -- Step 6.3 competitor/pricing checks (COMPLETE; 6-8 searches per group, no pages fetched; vendor-sourced prices)
- L1 SOC2 evidence-keeper: WEAK. Buyers pay (vCISO $1.5-5k/mo; platforms ~$7.5-25k/yr) but only a CPA firm can issue reports, trust crisis in category (Delve allegations Mar 2026), no auditor ties.
- L2 US sales-tax nexus for foreign sellers: WEAK-VIABLE. Real pain (TaxJar reg $299/state needs SSN/ITIN; big tools don't serve foreigners) but needs CPA/EA partner; Taxually/Commenda/Zenind already target it; channel/CPC unknown.
- L3 Amazon/Etsy appeals+prevention retainer: VIABLE-BUT-WEAK. Appeals $1.5-3.5k, prevention $500/mo (amazonsellers.attorney); no licence barrier; Fiverr $50 gigs commoditise low end; non-English channel unproven.
- L4 CBAM data pack: WEAK. ~90% of importers exempt (<=50t); software EUR 0-200/mo (Sustainability Cloud), Dubrink EUR 1,990-2,990/yr; certificate-date sources conflict.
- L5 Battery Passport prep: WEAK. 18 Feb 2027 still current; >=4 vendors live (DPP Hero $57-289/mo, PassportLab EUR149); manufacturer data hard to obtain.
- L6 KSeF last-mile: KILL. Incumbents bundle KSeF free; language barrier; micro date (1 Jan 2027) possibly deferred (bill unconfirmed).
- L7 French PA connector: WEAK. 137 registered PAs (Jul 2026); no white-label pricing found; SME issuing deadline 1 Sep 2027.
- L8 GPSR rep + labels: WEAK. Price floor EUR 139-199/yr/product type; needs EU legal entity for rep role; crowded.
- L9 Denial-appeal recovery: WEAK. Real leakage (35-60% of denials never appealed) but no pricing/channel evidence; HIPAA/BAA burden.
- L10 refurb label printers: KILL (physical, thin margin, LabelValue already has auto-order).
- L11 compressor filter replenishment: WEAK (crowded parts sellers; software-only layer has no proven buyer).
- L12 EUDR validation: KILL (free validators, light small-operator rules, regulatory churn).
Summary: no L-candidate clears the evidence bar on price+channel+new-entrant. Advance to 6.4 with L2, L3, L1, L9, L4, L7, L8, L5, L11 (L6, L10, L12 killed). Lesson: deadline-driven compliance themes mostly turn out already served by bundled/free tools or require local legal entities.

## 2026-10-13 run 2 -- Step 6.4 audit (in progress)
Cross-run continuity VERIFIED: run 2 loaded origin/research checkpoint (c8279d0) and resumed at 6.4.
- Auditor L2 (WebFetch DNS failed; search summaries only): Kintsugi $75/filing, ~$699-799/state/yr; Avalara $699-799/state/yr; foreign sellers can get EIN w/o SSN but states ask responsible-party SSN/ITIN; Anrok/Numeral/Zamp/Zenind already publish foreign-seller guides. POA/legal-filer, CPC, entrants UNKNOWN. Verdict WEAK-to-viable.
- Auditor L3: prices $300-4,000 flat (attorney $1.5-2.3k); very crowded (Fiverr, FreeeUp, law firms, ex-Amazon staff); appeals free to self-file; no demand/channel data; shared-access suspension risk. Verdict WEAK.
- Auditor L1: platform prices Secureframe from $7k/yr, Vanta ~$10k+, Drata ~$7.5k, Sprinto $4-8k (third-party est.); vCISO $1.5-5k/mo; non-CPA may sell readiness/evidence but operating controls creates AICPA independence problem; Delve allegations (class action 21 Apr 2026) add trust friction. WEAK.
- Auditor L9: no verified private contingency % (4-10% UNVERIFIED); crowded (R1, Aspirion); HIPAA BAA needed; no evidence small entrants win. WEAK.
- Auditor L4: definitive period began 1 Jan 2026, 50t threshold, certificates from 1 Feb 2027, first declaration 30 Sep 2027 (secondary sources; EC page not fetched). Competition UNKNOWN. Viable-but-unproven; previously found ~90% importers exempt.
- Auditor L7: Iopole (DGFiP-registered PA) already sells API white-label B2B2B to software vendors; 1 Sep 2026 obligation already passed. WEAK.
- Auditor H6 re-check: free incumbents Highlightly (free tier 100 req/day, RapidAPI) and BALLDONTLIE college baseball API; 64 Analytics $9.99-12.99/mo; NCAA ToS restricts; NO evidence any small API has paying customers => material downward evidence.
- Auditor H1: Etsy crowded (MidwestTech, CreatorSam, OffGridDevices, TerraNode); newest entrant OffGridDevices 29 sales/14 reviews since 2025; no correction warranted.
- Auditor monday.com: marketplace unreachable (DNS), install counts UNKNOWN; no correction.
- Tool limitation: WebFetch failed DNS in this run; all audit evidence is search-snippet level. Primary-page verification remains pending.
