# Research methodology (frozen since Phase 3; applies to Phases 6–10 unchanged)

## Founder profile
- Israel-based; can sell internationally.
- Strong software, mobile, backend, AI tooling and automation (Claude Code); comfortable running AI agents.
- About $2,000 for initial experiments; part-time start; wants to own a profitable business, not sell dev hours; prefers low capital and the ability to delegate or automate founder labour.
- Track A: realistic route to $2–5k/month owner profit. Track B: route to $10–30k+/month owner profit. Track C (from Phases 1–5): service first, scalable later. These are objectives, not scoring targets.

## Process per phase
1. Research direction chosen by the Research Director from gaps and biases in earlier phases.
2. Six independent discovery agents (A Consumer/prosumer, B Physical/e-commerce, C Traditional/offline, D Niche software/digital/technical, E Distribution-first/existing spending, F Contrarian/emerging). Assignments may be adapted per phase.
3. Merge, remove duplicates and previously investigated ideas (see `opportunity-ledger.md`), shortlist about 12–15.
4. Independent Evidence Auditor (checks sources; separates market-wide revenue from new-entrant outcomes; re-checks earlier leaders).
5. Independent Red-Team Investor (why each would fail; hard blockers vs unverified concerns).
6. Rescore with the frozen rubric; about 5 finalists with deep dives and downside/base/upside owner-profit scenarios.
7. Phase report, cumulative leaderboard, ledger and checkpoint updated; local git commit.

## Frozen rubric (do not modify)
Each criterion is scored 0–5 and converted as score × weight / 5.

**Cash-Flow (100):** existing spending evidence 25 · speed to first sale 20 · capital and delivery feasibility 20 · margins 20 · independence from founder labour 15.

**Scalability (100):** market depth 15 · recurring revenue 20 · scalable acquisition 20 · operating leverage and delegation 20 · defensibility 15 · founder fit 10.

**Distribution (100):** customer clarity 20 · discoverability 20 · proven acquisition-channel evidence 30 · difficulty of first customers 15 · growth beyond founder outreach 15. Being listed in a directory or marketplace is not credited as a proven channel; since Phase 5, marketplace-wide payouts are not credited as channel evidence without new-entrant outcome data.

**Balanced** = 0.4 × Cash-Flow + 0.4 × Scalability + 0.2 × Distribution.
**Adjusted** = Balanced − evidence penalty (0–15; historically calibrated 6–14, mostly 9–14). Higher penalty = weaker or more contradicted evidence.
Gaps under about 5 points are noise.

## Evidence labels
[Verified: URL, date] · [Secondary: credible report] · [Anecdote / vendor claim] · [Hypothesis] · [Unknown].
Never fabricate revenue, demand, conversion, paid users, CAC or successful entrants. Search snippets are not verified primary-page evidence.

## Boundaries
Desk research only. No contacting prospects or customers, no purchases, no ads, no building or deploying products, no opening accounts, no signed-in browser or private accounts, no simulated interviews presented as real. No bypassing paywalls or access controls.

## Search management
- WebSearch quota is session-wide, finite and refills unpredictably. Per-phase caps per agent; shared log at `research-notes/search-log.txt` (one line per search) to avoid duplicates across agents and phases.
- Prefer WebFetch of primary pages and public JSON APIs (iTunes Search API, Apify Store API, Gumroad search JSON, JetBrains Marketplace API, Shopify `products.json`, etc.).
- Reddit, Etsy, eBay, Fiverr, Kickstarter, Walmart, Amazon often block automated fetching; report blocked sources rather than infer.

## Reconciliation rule (from Phase 8)
The evidence auditor and the red team score every new idea independently at criterion level. The final score for a new idea is the mean of the two reviewers' CF, Scal, Dist and penalty. With two reviewers this is the median. Half-steps are allowed, and every final score lies between the two reviewers' scores. Leader corrections are applied only as named criterion steps; dissents are recorded.
