# Acceptance audit — 2026-11-22

Acceptance criteria come only from this repository's [ACCEPTANCE.md](../ACCEPTANCE.md). Final audit; local educational UI evidence is not evidence of a deployed autonomous research agent.

| Item | Source rule | Evidence | Disposition |
|---|---|---|---|
| PR #1 translation lacks evidence closer | §8 | Current checker rejects its body; #2 passes | Not fixable after merge by a new branch. New PR includes complete closer. |
| Missing executed QA and mobile interaction artifacts on #1 | §§2,4 | Unchecked render/navigation test plan; review comment adds no 390×844 artifact or walkthrough | Fixed prospectively: current index/four-module screenshots, quiz-selection still and animated WebP. Original merge-time absence remains. |
| README lacks status and next human action | §5 | Generic static-hosting instructions are not a status line | Fixed: LOCAL ONLY plus audit/evidence review and hosting next action. |

## Existing work

Baseline `8026efe5b612120011bd3ab304b013d3419b9467`; main was up to date before branching. Returned PRs #1 translation and #2 acceptance infrastructure were merged; their merge SHAs passed ancestry checks against origin/main. Reviewed README, base/footer, four modules, generated index, JS/CSS and build script. No product automated-test/linter suite is configured. Recent acceptance workflow successes are not browser QA. GitHub deployments were empty and Pages returned HTTP 404; unknown external hosting is not ruled out.

## Current verification

- `bash build.sh`: `Built index.html — open it in your browser.`
- `git diff --exit-code -- index.html`: exit 0; no module edits or generated index diff.
- `node --check main.js`: exit 0.
- Playwright Chromium, exactly 390×844: index → all four modules via nav dots → first quiz selection. Required target-in-viewport assertion passed after waiting for smooth scrolling to reach its destination. An initial fixed-delay assertion ran before module 4 arrived; a separate 2.5s diagnostic showed its y-position at approximately 0, disproving a broken navigation destination. No UI change was made.
- Stills and animated `interaction.webp` at `/home/ubuntu/audits/shots/autoresearch-course/`; PR body embeds them. These are viewport stills, not exhaustive paragraph captures.
- Final PR-body validation uses `python scripts/check_acceptance.py <body>`; result recorded in PR body.

## Coverage of all acceptance sections

- §1: inspected before minimal documentation edits; historical private planning/approval chronology is not assessable.
- §2: executed build/syntax/browser checks and fresh artifacts; no source-only completion claim. Full quiz scoring, every tooltip/definition and educational accuracy were not exhaustively checked.
- §3: translation/process PRs do not establish a bug-fix episode; navigation diagnostic required no product fix.
- §4: current four-module evidence supplied prospectively; cannot change original merge-time proof.
- §5: LOCAL ONLY with next human action; neither production deployment nor this branch's merge claimed. Historical ancestry checked; private approval/duplicate-intent history unavailable.
- §6: repository acceptance pointers and README/build commands reviewed. No unrelated criteria imported.
- §7: no historical stuck/bypass episode established; hosting remains explicitly unverified.
- §8: #1 historical failure retained; #2 passes; new PR supplies required eight-field closer.

Not fixable after merge: PR #1's contemporaneous missing closer and original QA evidence. No modules, UI behavior, acceptance rules, shared configuration or dependencies changed.
