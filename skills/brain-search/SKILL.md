---
name: brain-search
description: Search and synthesize existing knowledge from the Technical Brain repository without changing it. Use when the user says 查找, 搜索知识库, 我以前怎么决定的, 项目规范是什么, or asks a question that should be answered from personal notes first.
---

# Search The Technical Brain

Resolve the Technical Brain root first: use the current Git root when it contains `HOME.md`; otherwise read `$HOME/.agents/technical-brain.json` and use its `repository_path`. Verify the path exists or tell the user to run `scripts/install-brain-skills.ps1` on Windows or `scripts/install-brain-skills.sh` on macOS/Linux from the cloned repository.

1. Start with `<brain-root>/HOME.md` and the most relevant domain or project index.
2. Search filenames and Markdown content using `rg` with topic names, aliases and related technical terms.
3. Prefer verified notes. Clearly label draft, deprecated, conflicting or possibly stale content.
4. Synthesize the answer instead of dumping full files.
5. Link to the most relevant local notes using absolute clickable paths.
6. Do not modify repository files.
7. If no useful note exists, say so and suggest `$brain-capture` or `$brain-distill` as the next action.
