---
name: brain-review
description: Perform a weekly or monthly Technical Brain review by organizing inbox items, checking note health, and creating a concise review. Use when the user says 周复盘, 月度复盘, 整理收集箱, 知识库体检, or wants regular knowledge-base maintenance.
---

# Review The Technical Brain

Default to a weekly review unless the user specifies monthly.

Resolve the Technical Brain root first: use the current Git root when it contains `HOME.md`; otherwise read `$HOME/.agents/technical-brain.json` and use its `repository_path`. Verify the path exists or tell the user to run `scripts/install-brain-skills.ps1` on Windows or `scripts/install-brain-skills.sh` on macOS/Linux from the cloned repository.

1. Read `<brain-root>/80-Reviews/知识库维护清单.md`, `<brain-root>/00-Inbox/收集箱.md`, `<brain-root>/HOME.md`, and recent Git changes.
2. Classify actionable inbox items. Distill only items with enough context; leave ambiguous items in place with a clearer question.
3. Check recent notes for missing metadata, broken links, duplicates, conflicts and stale claims.
4. Update domain indexes and `HOME.md` only where navigation materially improves.
5. Create a dated review from `<brain-root>/90-Templates/周回顾模板.md`; for monthly review, adapt the headings to the month.
6. Identify one next learning or maintenance priority.
7. Never invent progress or delete unresolved information silently.
8. Run `git diff --check` and verify relative Markdown links.
9. Summarize completed maintenance, remaining questions and the next priority.
