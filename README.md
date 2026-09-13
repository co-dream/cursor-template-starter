# cursor-template-starter

A lean starter contract for [Cursor Projects](https://cursor.com/blog/projects) and [OpenAI Codex](https://developers.openai.com/codex/guides/agents-md).

Chats forget. `STATUS.md` does not.

This is a workflow template, not a finished product.

## 30-second start

1. Click **Use this template** (enable Template repository in Settings first).
2. Open that new repo as a Cursor Project, or open Codex in the folder.
3. Say:

```text
This is a new project. Interview me first.
```

The agent asks up to 5 questions, then writes `docs/PRODUCT.md`, `CONTEXT.md`, `specs/INDEX.md`, and `STATUS.md`. After that you only say the next task. To freeze progress:

```text
wrap up
```

## Files the agent should read

| File | Role |
|---|---|
| `AGENTS.md` | Coordinator rules |
| `STATUS.md` | One-page progress. Next action must be a single item |
| `docs/PRODUCT.md` | One-sentence product |
| `info/` | Human manuals |

## Manuals

- [English](info/en.md)
- [繁體中文](info/zh-Hant.md)
- [简体中文](info/zh-Hans.md)
- [日本語](info/ja.md)

## License

MIT
