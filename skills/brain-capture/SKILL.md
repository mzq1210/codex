---
name: brain-capture
description: Quickly capture raw ideas, links, questions, observations, and conversation fragments into the Technical Brain inbox. Use when the user says 收集, 先记一下, 稍后整理, 放进收集箱, or wants to preserve information without deciding its final category.
---

# Capture To Inbox

Resolve the Technical Brain root first: use the current Git root when it contains `HOME.md`; otherwise read `$HOME/.agents/technical-brain.json` and use its `repository_path`. Verify the path exists or tell the user to run `scripts/install-brain-skills.ps1` on Windows or `scripts/install-brain-skills.sh` on macOS/Linux from the cloned repository.

1. Read `<brain-root>/00-Inbox/收集箱.md`.
2. Extract the content to preserve from the current user message and relevant conversation context.
3. Append one concise unchecked item under `待整理` using:

```text
- [ ] YYYY-MM-DD [类型] 内容；来源：对话 / URL / 文件
```

4. Preserve facts, open questions and source links. Do not copy the entire chat.
5. Do not classify the item into a permanent directory.
6. Never save secrets, credentials, private production data or unnecessary personal information.
7. Report the captured item and file path briefly.

If the message contains nothing identifiable to capture, ask one concise question before writing.
