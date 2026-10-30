---
name: brain-help
description: List and explain the Technical Brain repository workflows. Use when the user asks what knowledge-management commands are available, types 帮助, 指令, 命令, 怎么记录, or wants to choose an operation before changing the repository.
---

# Technical Brain Help

Resolve the Technical Brain root before reading files:

1. Use the current Git root when it contains both `HOME.md` and `COMMANDS.md`.
2. Otherwise read `$HOME/.agents/technical-brain.json` and use its `repository_path`.
3. Verify the resolved directory contains `HOME.md`. If not, tell the user to run `scripts/install-brain-skills.ps1` on Windows or `scripts/install-brain-skills.sh` on macOS/Linux from the cloned Technical Brain repository.

Read `<brain-root>/COMMANDS.md` and present the six commands as a compact menu:

- `$brain-capture`：快速收集
- `$brain-distill`：知识沉淀
- `$brain-sync`：记忆同步
- `$brain-search`：知识查找
- `$brain-review`：定期复盘
- `$brain-help`：显示帮助

Do not modify repository files. End by asking the user to select one command only when their intended operation is still unclear.
