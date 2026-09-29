# Agent rules

Works in Codex, Cursor Projects, and Claude Code. `STATUS.md` is the only source of truth for progress.

## Start of session

1. Read `STATUS.md`.
2. If it says `Setup: not done`, follow `docs/SETUP.md` instead of the rules below.
3. If there is no `STATUS.md` (existing project), create it from the current code and `git log`, move old HANDOFF / PROGRESS / log files to `docs/archive/`, then show the user the new Next and stop.
4. Otherwise work on the Next item. Read `docs/PRODUCT.md`, `CONTEXT.md`, or a spec only when the task needs it.

## Working

- Do the work yourself. Use parallel sub-agents only when the parts are independent and large enough to pay for the extra context. Each brief: goal, allowed paths, done-when. Paths must not overlap.
- Read the code the task touches. Widen only when dependencies or tests require it. Do not survey the whole repo.
- Ask only when missing information would change the result or scope, or when the action needs permission (destructive, publishing, spending). Otherwise proceed, verify, and report.
- One product goal at a time. Small fixes do not change Next. If the user switches goals before Next is done, record the unfinished item in Now so it is not lost.
- Before building a new feature, write a short spec in `specs/<module>.md` (goal, scope, done-when) and list it in `specs/INDEX.md`. Small fixes need no spec.
- Do not tidy or rewrite files the task did not name.
- In Cursor: if Shared Context disagrees with `STATUS.md`, follow `STATUS.md` and fix Shared Context.

## Progress files

- `STATUS.md` is the only progress file. Do not create HANDOFF, PROGRESS, LOG, or similar files.
- Overwrite STATUS; never append. Keep it under one page. Write it in the user's language.
- History, test output, and evidence go in commit messages and PR descriptions, not in markdown files.

## Wrap-up

`wrap up`, `update STATUS`, and `收工` are the same command. Also run it when Next is done. Do not update STATUS after every message.

Rewrite only these fields:

1. Updated: today's date
2. Now: three lines or fewer, including any unfinished goal that was set aside
3. Done: one line per finished capability; keep the latest 10, older ones live in git
4. Next: exactly one item, or "waiting for the user"
5. Do not repeat: at most 10; add only new pitfalls, remove ones that no longer apply

Then commit the files changed in this session locally, with a message that says what changed and how it was verified. Do not push unless the user asks. Tell the user the new Next in one line.
