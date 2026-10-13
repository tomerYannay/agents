# Persistence protocol (canonical branch: `research`)
Start of every run: `git fetch origin research`; read research-state.json, next-phase-plan.md, research-exclusions.md, cumulative-leaderboard.md from `origin/research` (merge `origin/research` into the session branch first: `git merge origin/research`).
Work on the session branch. End of run: commit, `git push -u origin <session-branch>`, open a PR targeting `research` (only research files), merge it if permitted, then verify `git ls-remote origin research` contains the final commit. If merge is not permitted, report the blocker; do not claim continuity.
Log of persistence tests is in research-state.json `persistence`.
