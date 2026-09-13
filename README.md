# cursor-template-starter

A thin starter for [Cursor Projects](https://cursor.com) and [Codex](https://developers.openai.com/codex/guides/agents-md).

Chats forget. Progress lives in `STATUS.md`. This is an operating contract, not a product.

[English](#english) · [繁體中文](#traditional-chinese) · [简体中文](#simplified-chinese) · [日本語](#japanese)

---

<a id="english"></a>
## English

### How it works

1. Use this template.
2. Open the new repo as a Cursor Project, or open Codex in the folder.
3. Say: `This is a new project. Interview me first.`
4. Answer up to 5 questions. The agent writes `docs/PRODUCT.md`, `CONTEXT.md`, `specs/INDEX.md`, and `STATUS.md`.
5. Say `start` for the first feature. After that, say only the next task.
6. Before you leave: `wrap up` — that updates `STATUS.md` only.

A new session should read `AGENTS.md` and `STATUS.md`, then do only the Next item. Do not paste old chats. Do not scan the whole repo.

`wrap up` is not every message. Tiny edits do not belong in STATUS.

The ritual is the same for a video OS, an ERP, or a shop. Only folder names change.

### Files agents read

| File | Role |
|---|---|
| `AGENTS.md` | Coordinator rules |
| `STATUS.md` | One-page progress. Next is a single item |
| `docs/PRODUCT.md` | One-sentence product |
| `CONTEXT.md` | Vocabulary |
| `specs/INDEX.md` | Module list |

Working files are English on purpose, so any agent can follow them.

---

<a id="traditional-chinese"></a>
## 繁體中文

對話會消。進度留在 `STATUS.md`。這不是產品，是開工契約。

### 流程

1. 按 **Use this template** 開新 repo。
2. 用那個 repo 開 Cursor Project，或在該資料夾開 Codex。
3. 說：`This is a new project. Interview me first.`
4. 最多答 5 題。Agent 會寫 `docs/PRODUCT.md`、`CONTEXT.md`、`specs/INDEX.md`、`STATUS.md`。
5. 說 `start` 才做第一件。之後只講下一件。
6. 離開前說 `wrap up`（收工）─只改 `STATUS.md`。

新 session 只讀 `AGENTS.md` 和 `STATUS.md`，只做 Next 那一項。不要貼舊對話，不要掃整個 repo。

小修不寫進 STATUS。影片 OS、ERP、電商都用同一套儀式，只換模組名。

---

<a id="simplified-chinese"></a>
## 简体中文

对话会消。进度留在 `STATUS.md`。这不是产品，是开工契约。

### 流程

1. 点 **Use this template** 开新仓库。
2. 用那个仓库开 Cursor Project，或在该文件夹开 Codex。
3. 说：`This is a new project. Interview me first.`
4. 最多答 5 题。Agent 会写 `docs/PRODUCT.md`、`CONTEXT.md`、`specs/INDEX.md`、`STATUS.md`。
5. 说 `start` 才做第一件。之后只讲下一件。
6. 离开前说 `wrap up`（收工）—只改 `STATUS.md`。

新 session 只读 `AGENTS.md` 和 `STATUS.md`，只做 Next 那一项。不要粘贴旧对话，不要扫整个仓库。

小改不写进 STATUS。影片 OS、ERP、电商都用同一套仪式，只换模块名。

---

<a id="japanese"></a>
## 日本語

会話は消える。進捗は `STATUS.md` に残る。製品ではなく、動かし方の契約です。

### 流れ

1. **Use this template** で新しいリポジトリを作る。
2. その repo で Cursor Project を開く。またはそのフォルダで Codex を開く。
3. `This is a new project. Interview me first.` と言う。
4. 最大 5 問に答える。エージェントが `docs/PRODUCT.md`、`CONTEXT.md`、`specs/INDEX.md`、`STATUS.md` を書く。
5. 最初の機能は `start` と言ってから。以降は次の 1 件だけ話す。
6. 離れる前に `wrap up` — `STATUS.md` だけ更新する。

新しい session は `AGENTS.md` と `STATUS.md` だけ読み、Next の 1 件だけやる。古い会話は貼らない。リポジトリ全体を走査しない。

小さな修正は STATUS に書かない。動画 OS、ERP、EC も同じ流れで、モジュール名だけ変わる。

---

## License

MIT
