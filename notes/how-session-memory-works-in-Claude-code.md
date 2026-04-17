# 2026-04-16

## What I Learned

1. Claude Code's memory system is just local Markdown files. `MEMORY.md` is a one-line index that gets auto-loaded every session, and individual memory files are only pulled via `Read` when the topic matches. There is no database, no API sync, and nothing uploaded to Anthropic. I can delete or edit the files by hand at any time.
2. Memory scope is per-project. The path embeds my project directory, so Career-Ops memories do not leak into other projects.
3. Career-Ops `deep` mode generates a 6-axis research prompt tailored to my CV before I ever apply. It covers AI strategy, recent moves, engineering culture, challenges, competitors, and candidate angle, and I can run it without committing to a full A-G evaluation.
4. The auto-pipeline flow (`Playwright fetch -> A-G scoring -> tracker TSV -> token log`) caught two independent kill signals on the Liberty Mutual req in under a minute: an expired deadline (`2026-04-03`, passed 13 days ago) and a comp ceiling below my comp floor.
5. Memories can be staleness-flagged automatically. I saw the tag `<system-reminder>This memory is 7 days old</system-reminder>` and learned Claude is expected to verify live files before asserting old memory content as fact.

## What I Applied

- Ran `/career-ops deep` for Liberty Mutual Senior Data Engineer to generate a custom research prompt before deciding whether to fetch and score.
- Fetched the JD via Playwright instead of WebFetch, which is mandatory per career-ops `CLAUDE.md` set-up for job opening verification.
- Marked Liberty Mutual as `SKIP` in the tracker and saved a `feedback` memory so future scans will not surface them again, turning one bad evaluation into a permanent filter.
- Updated the `MEMORY.md` index manually to point to the new feedback file so future sessions load the skip rule.

## What Was Confusing

- I initially assumed memory was some hosted cloud service on anthropic cloud. It took asking directly to realize it is just files on my disk that I fully control.
- The difference between `MEMORY.md` (index, auto-loaded) and individual memory files (body, loaded on demand) was not obvious from the surface behavior.
- It was unclear why a `SKIP` entry still gets a full A-G report written. It turns out the report is archival, useful for future reference if the role reposts at a higher comp, not a signal to apply.

## Next Thing to Try

- Pipe the next JD paste into `oferta` (score-only, no PDF) instead of auto-pipeline to save about `15K` tokens on borderline candidates, then only escalate to full auto-pipeline when score is `>= 4.0`.
- Build a small script that greps `MEMORY.md` plus the memory directory to audit what Claude "knows" about me, and treat it like a dotfile I version in its own repo.
- Try a project-type memory capturing my TN visa timeline (deadline, employer change constraints) so it surfaces in every evaluation automatically.
