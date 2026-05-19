# Project Context for Claude Code

This is an AI-managed Obsidian knowledge base (Second Brain) following Karpathy's LLM Knowledge Base methodology. The vault schema — directory layout, file conventions, writing tone, compilation rules — is defined in `AGENTS.md`. Read and follow it before making any changes.

@AGENTS.md

## Workflows

Slash commands in `.claude/commands/` wrap the workflow definitions in `.agents/workflows/`. Available:

- `/ingest` — Nạp dữ liệu thô vào `raw/`
- `/compile` — Biên dịch `raw/` thành bài wiki
- `/ask` — Hỏi đáp trực tiếp trên vault
- `/save` — Lưu kiến thức từ hội thoại vào wiki
- `/cleanup` — Dọn dẹp, kiểm tra chất lượng wiki
- `/autoresearch` — Tự động nghiên cứu chủ đề
- `/breakdown` — Tách bài wiki lớn thành sub-topics

The workflow files in `.agents/workflows/*.md` are the source of truth for each command.
