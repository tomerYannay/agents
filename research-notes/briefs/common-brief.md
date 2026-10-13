# SHARED DISCOVERY-AGENT BRIEF (Phases 6–10). Read fully before any research.

Repo root: /Users/tomeryannay/Projects/agents
Read first: research-notes/research-methodology.md (rubric, evidence labels, boundaries) and research-notes/opportunity-ledger.md (everything already investigated; do NOT resubmit, rename or repackage anything in it unless the segment/model/channel is materially different and you say why).

## Founder
Israel-based; can sell internationally. Strong software/mobile/backend/automation/AI-assisted dev. About $2,000 test budget (flag anything needing more). Part-time start. Wants a profitable BUSINESS, not selling dev hours; prefers low capital and the ability to automate or delegate founder labour.
Track A = realistic $2–5k/month owner profit. Track B = route to $10–30k+/month owner profit. Do not favour SaaS, AI, subscriptions or any category in advance. AI is an execution advantage, not a product requirement.

## Hard lessons from Phases 1–5 (apply them)
1. Marketplace-wide payouts are NOT evidence a newcomer will sell. Phase 5 measured: median new Apify Actor had 1 monthly user; typical new Superhive add-on <10 sales in 2–3 months; new JetBrains paid plugins 10–133 downloads; most new Wix/WooCommerce apps 0 reviews; 2026 quilt apps 0–23 ratings; new CodeCanyon modules 1–16 lifetime sales. Open marketplaces are flooded by AI-built supply. Whenever you cite a channel, look for NEWCOMER outcomes (recent entrants' review counts, rank, sales badges), not just the leaders.
2. Competitors prove spending; do not auto-reject. But name a concrete entry strategy (segment, price, language/geo gap, better channel, better unit economics) or say "none credible". Do not manufacture differentiation.
3. Earlier phases leaned on: Israel-diaspora/affinity niches, low-capital digital products sold on marketplaces, and regulatory/compliance deadlines. Do not drift back into these without a strong reason.
4. A listed price is not proof of buyers. Seek transaction signals: sales counts, review velocity (reviews in the last 12 months), funded amounts, disclosed revenue, job/order volume, public filings, government statistics.
5. Distribution is decisive. Every promising idea needs a SPECIFIC acquisition mechanism plus evidence that the channel produces purchases for comparable offers, ideally for new entrants. Estimate acquisition cost only from evidence; otherwise mark [Unknown].

## Evidence rules
Labels: [Verified: URL, date accessed/published] / [Secondary: source] / [Anecdote or vendor claim] / [Hypothesis] / [Unknown]. Never invent customer counts, market size, revenue, conversion, CAC, margins, willingness to pay, or interviews. Search snippets are not verified pages — open the page (WebFetch) before labelling Verified. Absence of search results ≠ absence of competitors.

## Access rules (strict)
- Do NOT use any browser-automation tools (mcp__claude-in-chrome__* or any other browser), signed-in sessions or private accounts. Use only WebSearch, WebFetch, and Bash with curl/python for PUBLIC pages/APIs.
- Do not contact anyone, submit forms, sign up, purchase, or post anything. Do not bypass paywalls, logins, CAPTCHAs or robots blocks; if blocked, say so.
- Scripts and downloaded files go under the scratchpad directory: /private/tmp/claude-501/-Users-tomeryannay-Projects-agents/33458dff-96bb-4d90-98b6-5161ecb65c2e/scratchpad/p6plus/<phase>-<your-agent-id>/ (put downloaded data in a separate subfolder from scripts; run python with -I). Do not write into the repo except where your prompt says.
- Load web tools via ToolSearch "select:WebSearch,WebFetch".
- Never put the user's name, email address or any personal identifier into request headers (e.g., User-Agent), URLs, or payloads. If a site such as SEC EDGAR requires a contact User-Agent, use a generic one (e.g., `research-bot admin@example.com`) or skip the source and report it.

## Search budget (hard rule)
- Your WebSearch cap is stated in your prompt. Count your searches and report the count.
- Before each WebSearch, read research-notes/search-log.txt AND research-notes/search-log-phase5.txt; do not repeat a query already run. After each WebSearch append ONE line: `P<phase>-<AGENT> | query | key takeaway` with `echo ... >> /Users/tomeryannay/Projects/agents/research-notes/search-log.txt`.
- WebFetch on primary pages and public JSON APIs is not capped but be efficient. If WebSearch fails for quota, continue with WebFetch and disclose exactly what remained unverified.
- Roughly 50% discovery, 50% verifying demand/competition/newcomer outcomes for your best 3 ideas. Stop researching weak ideas early.

## Output (per opportunity, dense)
1. Name + one-line concept 2. Paying customer + geography 3. Model / how they pay / price 4. Spending evidence (transaction signals, sources, dates) 5. Competitors + what customers dislike 6. Entry strategy (or "none credible") 7. Acquisition mechanism + evidence the channel works, including NEWCOMER outcomes where measurable 8. Capital, inventory, delivery/ops requirements, Israel-based operability, legal/platform restrictions 9. Labour dependence: can revenue grow faster than founder hours? 10. Labelled rough unit economics (owner profit, not revenue); Track A/B fit 11. Main risks / what would kill it.

Target 6–8 genuinely distinct opportunities (quality over count) plus a short list of ideas you killed and why. End with: your ranking, top 2–3 for deep diligence, the decisive unverified assumption for each, and your WebSearch count. About 3,000–4,500 words. Return full findings as your final message (also save them to the file path given in your prompt).
