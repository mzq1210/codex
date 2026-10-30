---
name: brain-sync
description: Incrementally synchronize cross-project standards and durable collaboration preferences from Codex memory into the Technical Brain. Use when the user says 同步记忆, 同步长期记忆, or 检查新增记忆. Exclude rules, business facts, and state that apply only to a specific project.
---

# Synchronize Codex Memory

Resolve the Technical Brain root first: use the current Git root when it contains `HOME.md`; otherwise read `$HOME/.agents/technical-brain.json` and use its `repository_path`. Verify the path exists or tell the user to run `scripts/install-brain-skills.ps1` on Windows or `scripts/install-brain-skills.sh` on macOS/Linux from the cloned repository.

1. Locate the current Codex memory registry and its referenced notes when accessible.
2. Read `<brain-root>/80-Reviews/Codex长期记忆迁移记录.md` and search the repository for already migrated topics.
3. Compare sources and select only new or materially changed standards that are reusable across multiple projects, such as general engineering principles, framework-independent practices, and durable collaboration preferences.
4. Exclude repository paths, business rules, table or field details, feature behavior, project architecture, current implementation state, and any convention that applies only to one named project. Do not generalize a project-specific observation without independent reusable evidence.
5. Do not copy internal indexes, raw rollout logs, raw chat transcripts, volatile command state, secrets or personal data.
6. Route reusable technical standards to `<brain-root>/10-Knowledge/` and collaboration preferences to `<brain-root>/AGENTS.md`. Do not write to `<brain-root>/30-Projects/` during this workflow.
7. If the user explicitly asks to preserve a specific project's knowledge, treat that as a separate capture or distillation request rather than part of memory synchronization.
8. Update the migration record with the date, standards migrated, and project-specific topics intentionally skipped.
9. Do not modify or delete the source Codex memories.
10. Run `git diff --check` and verify new relative Markdown links.
11. Report added, updated and skipped topics briefly.

If Codex memory is not accessible in the current environment, report that limitation without fabricating a sync.
