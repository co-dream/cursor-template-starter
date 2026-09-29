# cursor-template-starter

A thin starter for [Codex](https://developers.openai.com/codex/guides/agents-md), [Cursor Projects](https://cursor.com), and [Claude Code](https://claude.com/claude-code).

Chats forget. Progress lives in one page: `STATUS.md`. This is an operating contract, not a product.

[English](#english) · [繁體中文](#traditional-chinese) · [简体中文](#simplified-chinese) · [日本語](#japanese)

---

<a id="english"></a>
## English

### Why this exists

Every new chat with a coding agent starts from zero. People fix this by pasting old chats or keeping long handoff logs, and both burn tokens and confuse the agent. This template keeps it simple:

- Start: say one sentence. The agent interviews you, writes the map files, and starts building.
- Work: say only the next task.
- Wrap up: say `wrap up` or `收工`. Only `STATUS.md` changes.

### Start a new project

1. Click **Use this template** on GitHub to create your repo (or clone it).
2. Open the repo in Codex, Cursor Project, or Claude Code.
3. Say: `This is a new project. Interview me first.`
4. Answer up to 5 questions, or say `use your recommendations`. It also asks whether to keep the MIT `LICENSE`.
5. The agent writes `docs/PRODUCT.md`, `CONTEXT.md`, `specs/INDEX.md`, and `STATUS.md`, replaces this README with one for your product, removes template-only files, then starts the first feature.

### Add it to an existing project

1. Copy `AGENTS.md` into your repo root. If you already have one, merge the rules instead of overwriting it.
2. For Claude Code: copy `CLAUDE.md`, or add the line `@AGENTS.md` to your existing `CLAUDE.md`.
3. Open a new chat and say: `Read AGENTS.md and set up STATUS.md for this project.` The agent writes `STATUS.md` from your code and git log, and moves old HANDOFF / PROGRESS / log files to `docs/archive/`.

### Daily use

- `Change checkout shipping. Touch only checkout.`
- `New feature: export to PDF. Ask me if anything is unclear.`
- `wrap up` / `收工` — before you leave. The agent rewrites `STATUS.md` and commits locally. Not after every message; tiny edits do not belong in STATUS.

In a new chat, do not paste old chats. The agent reads `STATUS.md` and picks up from Next.

### What the agent will do

- Read `STATUS.md` first, then only the files the task needs. No whole-repo scans.
- Do the work itself. Split into sub-agents only when the parts are independent.
- Ask only when missing information would change the result, or before deleting, publishing, or spending money.
- Work on one goal at a time. `STATUS.md` has exactly one Next item. Small fixes do not change it; a goal set aside half-done is noted so it is not lost.
- Write a one-page spec before a new feature. Small fixes skip it.
- Overwrite `STATUS.md` in your language, never append. History and test evidence go in git commits and PRs.
- At wrap-up, commit locally with what changed and how it was verified. It does not push unless you ask.

### Files

| File | Role |
|---|---|
| `AGENTS.md` | Rules for the agent. Codex and Cursor read it automatically |
| `CLAUDE.md` | Points Claude Code at `AGENTS.md` |
| `STATUS.md` | One-page progress. The only progress file |
| `docs/SETUP.md` | First-time interview. Deleted after setup |
| `docs/PRODUCT.md` | What the product is, who it is for, what is out of scope |
| `CONTEXT.md` | Vocabulary |
| `specs/` | `INDEX.md` module list, plus one short spec per feature |

Rule files are English on purpose, so any agent can follow them. `STATUS.md` is written in your language. The flow is the same for a video OS, an ERP, or a shop; only module names change.

---

<a id="traditional-chinese"></a>
## 繁體中文

### 為什麼做這個 repo

每開一個新對話，coding agent 都由零開始。常見做法是貼舊對話或寫很長的交接檔，兩者都浪費 token，也令 agent 分不清哪些仍然有效。這個 template 令流程保持簡單：

- 開工：講一句話。Agent 先問你幾條問題，寫好地圖檔，然後直接開始做。
- 做事：只講下一件。
- 收工：說 `wrap up` 或「收工」。只改 `STATUS.md`。

### 開新項目

1. 在 GitHub 按 **Use this template** 建立你的 repo（或直接 clone）。
2. 用 Codex、Cursor Project 或 Claude Code 打開那個 repo。
3. 說：`This is a new project. Interview me first.`
4. 最多答 5 題，或說「用你的建議」。Agent 亦會問你是否保留 MIT `LICENSE`。
5. Agent 會寫好 `docs/PRODUCT.md`、`CONTEXT.md`、`specs/INDEX.md`、`STATUS.md`，把這份 README 換成你產品的說明，刪除 template 專用檔案，然後開始做第一個功能。

### 用在現有項目

1. 把 `AGENTS.md` 複製到你的 repo 根目錄。如果已經有，把規則合併進去，不要直接覆蓋。
2. 用 Claude Code 的話：複製 `CLAUDE.md`，或在現有的 `CLAUDE.md` 加一行 `@AGENTS.md`。
3. 開新對話，說：`Read AGENTS.md and set up STATUS.md for this project.` Agent 會按程式碼和 git 記錄寫 `STATUS.md`，並把舊的 HANDOFF／PROGRESS／log 檔搬到 `docs/archive/`。

### 日常用法

- `改結帳運費，只動 checkout。`
- `新功能：匯出 PDF。有不清楚的先問我。`
- `wrap up`／「收工」──離開前才說。Agent 會重寫 `STATUS.md` 並在本機 commit。不用每句都說，小修不寫進 STATUS。

開新對話時不要貼舊對話。Agent 會讀 `STATUS.md`，從 Next 接手。

### Agent 會怎樣做

- 先讀 `STATUS.md`，再只讀這次任務需要的檔案，不會掃整個 repo。
- 自己動手做。只有工作可以拆成互不相關的部分時，才分給 sub-agent。
- 只在資料不足會影響結果，或要刪除、發布、花錢之前才問你。
- 一次只做一個目標；`STATUS.md` 只有一個 Next。小修不改 Next；中途擱置的目標會記下，不會遺失。
- 新功能開工前先寫一頁規格；小修不用。
- `STATUS.md` 用你的語言寫，每次覆寫，不累加。歷史及測試證據放在 git commit 和 PR。
- 收工時在本機 commit，寫明改了甚麼及怎樣驗證。你沒要求就不會 push。

### 檔案

| 檔案 | 用途 |
|---|---|
| `AGENTS.md` | Agent 的規則，Codex 和 Cursor 會自動讀取 |
| `CLAUDE.md` | 讓 Claude Code 讀 `AGENTS.md` |
| `STATUS.md` | 一頁進度，唯一的進度檔 |
| `docs/SETUP.md` | 首次訪問，設定完成後刪除 |
| `docs/PRODUCT.md` | 產品是甚麼、給誰用、不做甚麼 |
| `CONTEXT.md` | 用語表 |
| `specs/` | `INDEX.md` 模組清單，另每個功能一份短規格 |

規則檔刻意用英文，方便任何 agent 跟從；`STATUS.md` 用你的語言寫。影片 OS、ERP、電商都用同一套流程，只換模組名。

---

<a id="simplified-chinese"></a>
## 简体中文

### 为什么做这个 repo

每开一个新对话，coding agent 都从零开始。常见做法是粘贴旧对话或写很长的交接文件，两者都浪费 token，也让 agent 分不清哪些仍然有效。这个 template 让流程保持简单：

- 开工：讲一句话。Agent 先问你几个问题，写好地图文件，然后直接开始做。
- 做事：只讲下一件。
- 收工：说 `wrap up` 或「收工」。只改 `STATUS.md`。

### 开新项目

1. 在 GitHub 点 **Use this template** 创建你的仓库（或直接 clone）。
2. 用 Codex、Cursor Project 或 Claude Code 打开那个仓库。
3. 说：`This is a new project. Interview me first.`
4. 最多答 5 题，或说「用你的建议」。Agent 也会问你是否保留 MIT `LICENSE`。
5. Agent 会写好 `docs/PRODUCT.md`、`CONTEXT.md`、`specs/INDEX.md`、`STATUS.md`，把这份 README 换成你产品的说明，删除 template 专用文件，然后开始做第一个功能。

### 用在现有项目

1. 把 `AGENTS.md` 复制到你的仓库根目录。如果已经有，把规则合并进去，不要直接覆盖。
2. 用 Claude Code 的话：复制 `CLAUDE.md`，或在现有的 `CLAUDE.md` 加一行 `@AGENTS.md`。
3. 开新对话，说：`Read AGENTS.md and set up STATUS.md for this project.` Agent 会按代码和 git 记录写 `STATUS.md`，并把旧的 HANDOFF／PROGRESS／log 文件移到 `docs/archive/`。

### 日常用法

- `改结账运费，只动 checkout。`
- `新功能：导出 PDF。有不清楚的先问我。`
- `wrap up`／「收工」——离开前才说。Agent 会重写 `STATUS.md` 并在本地 commit。不用每句都说，小改不写进 STATUS。

开新对话时不要粘贴旧对话。Agent 会读 `STATUS.md`，从 Next 接手。

### Agent 会怎样做

- 先读 `STATUS.md`，再只读这次任务需要的文件，不会扫整个仓库。
- 自己动手做。只有工作可以拆成互不相关的部分时，才分给 sub-agent。
- 只在信息不足会影响结果，或要删除、发布、花钱之前才问你。
- 一次只做一个目标；`STATUS.md` 只有一个 Next。小改不改 Next；中途搁置的目标会记下，不会丢失。
- 新功能开工前先写一页规格；小改不用。
- `STATUS.md` 用你的语言写，每次覆写，不追加。历史及测试证据放在 git commit 和 PR。
- 收工时在本地 commit，写明改了什么及怎样验证。你没要求就不会 push。

### 文件

| 文件 | 用途 |
|---|---|
| `AGENTS.md` | Agent 的规则，Codex 和 Cursor 会自动读取 |
| `CLAUDE.md` | 让 Claude Code 读 `AGENTS.md` |
| `STATUS.md` | 一页进度，唯一的进度文件 |
| `docs/SETUP.md` | 首次访谈，设置完成后删除 |
| `docs/PRODUCT.md` | 产品是什么、给谁用、不做什么 |
| `CONTEXT.md` | 术语表 |
| `specs/` | `INDEX.md` 模块清单，另每个功能一份短规格 |

规则文件刻意用英文，方便任何 agent 遵循；`STATUS.md` 用你的语言写。影片 OS、ERP、电商都用同一套流程，只换模块名。

---

<a id="japanese"></a>
## 日本語

### なぜこの repo があるか

コーディングエージェントは新しいチャットのたびにゼロから始まる。古い会話を貼ったり長い引き継ぎファイルを書いたりすると、token を浪費し、どれがまだ有効かエージェントが迷う。この template は流れを単純に保つ：

- 開始：一文言う。エージェントが質問し、地図ファイルを書いて、そのまま作り始める。
- 作業：次の 1 件だけ話す。
- 終了：`wrap up` または「收工」。`STATUS.md` だけ更新する。

### 新しいプロジェクトを始める

1. GitHub で **Use this template** を押してリポジトリを作る（または clone する）。
2. その repo を Codex、Cursor Project、または Claude Code で開く。
3. `This is a new project. Interview me first.` と言う。
4. 最大 5 問に答える。または「おすすめで」と言う。MIT `LICENSE` を残すかも聞かれる。
5. エージェントが `docs/PRODUCT.md`、`CONTEXT.md`、`specs/INDEX.md`、`STATUS.md` を書き、この README をプロダクト用に置き換え、template 専用ファイルを削除してから、最初の機能を始める。

### 既存のプロジェクトに入れる

1. `AGENTS.md` をリポジトリのルートにコピーする。既にある場合は上書きせず、ルールを統合する。
2. Claude Code の場合：`CLAUDE.md` をコピーするか、既存の `CLAUDE.md` に `@AGENTS.md` の 1 行を足す。
3. 新しいチャットで `Read AGENTS.md and set up STATUS.md for this project.` と言う。エージェントがコードと git log から `STATUS.md` を書き、古い HANDOFF／PROGRESS／ログを `docs/archive/` に移す。

### 毎日の使い方

- `チェックアウトの送料を変更。checkout だけ触って。`
- `新機能：PDF 書き出し。不明点があれば先に聞いて。`
- `wrap up`／「收工」— 離れる前だけ。エージェントが `STATUS.md` を書き直し、ローカルで commit する。毎回は不要。小さな修正は STATUS に書かない。

新しいチャットでは古い会話を貼らない。エージェントが `STATUS.md` を読み、Next から続ける。

### エージェントの動き方

- まず `STATUS.md` を読み、その作業に必要なファイルだけ読む。リポジトリ全体は走査しない。
- 自分で作業する。互いに独立した部分がある時だけ sub-agent に分ける。
- 情報不足が結果に影響する時、または削除・公開・支払いの前だけ質問する。
- 一度に一つの目標だけ。`STATUS.md` の Next は常に 1 件。小さな修正では変えない。途中で置いた目標は記録し、失わない。
- 新機能の前に 1 ページの仕様を書く。小さな修正は不要。
- `STATUS.md` はあなたの言語で毎回上書きし、追記しない。履歴とテスト証拠は git commit と PR に残す。
- 終了時に、変更内容と検証方法を書いてローカルで commit する。頼まれない限り push しない。

### ファイル

| ファイル | 役割 |
|---|---|
| `AGENTS.md` | エージェントのルール。Codex と Cursor は自動で読む |
| `CLAUDE.md` | Claude Code に `AGENTS.md` を読ませる |
| `STATUS.md` | 1 ページの進捗。唯一の進捗ファイル |
| `docs/SETUP.md` | 初回インタビュー。設定後に削除 |
| `docs/PRODUCT.md` | 何を作るか、誰のためか、何をしないか |
| `CONTEXT.md` | 用語集 |
| `specs/` | `INDEX.md` のモジュール一覧と、機能ごとの短い仕様 |

ルールファイルはどのエージェントでも従えるよう、あえて英語。`STATUS.md` はあなたの言語で書く。動画 OS、ERP、EC も同じ流れで、モジュール名だけ変わる。

---

## License

MIT
