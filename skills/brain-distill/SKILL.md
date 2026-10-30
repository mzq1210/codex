---
name: brain-distill
description: Distill conclusions from a conversation, inbox item, project event, or source material into structured Technical Brain notes. Use when the user says 沉淀, 整理成笔记, 加入第二大脑, 记录这个结论, or wants reusable knowledge rather than a raw capture.
---

# Distill Knowledge

Resolve the Technical Brain root first: use the current Git root when it contains `HOME.md`; otherwise read `$HOME/.agents/technical-brain.json` and use its `repository_path`. Verify the path exists or tell the user to run `scripts/install-brain-skills.ps1` on Windows or `scripts/install-brain-skills.sh` on macOS/Linux from the cloned repository.

1. Read `<brain-root>/HOME.md`, the nearest domain or project index, and search for existing notes on the same topic.
2. Decide the smallest correct destination:
   - reusable knowledge: `<brain-root>/10-Knowledge/`
   - diagnosed issue or incident: `<brain-root>/20-Problems/`
   - project-only context or convention: `<brain-root>/30-Projects/`
   - architecture: `<brain-root>/40-Architecture/`
   - decision and trade-off: `<brain-root>/50-Decisions/`
   - learning plan or log: `<brain-root>/60-Learning/`
3. Use the closest template from `<brain-root>/90-Templates/` and remove irrelevant empty sections.
4. Separate confirmed facts, inference and personal decisions. Mark unverified or mutable claims as `status: draft`.
5. Record versions, applicable boundaries, validation evidence and sources where available.
6. Update the nearest index. Add to `HOME.md` only when the note is important enough for top-level navigation.
7. Remove the source inbox item only after its useful content has been fully preserved.
8. Never store secrets or raw chat transcripts.
9. Run `git diff --check` and verify new relative Markdown links.
10. Report created or updated notes briefly.
