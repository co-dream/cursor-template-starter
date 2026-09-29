# Guide (English)

## What this is

A small template so coding agents can resume after the chat is gone.

You talk to one lead chat (Codex, Cursor Project, or Claude Code). It does the work itself and splits independent parts to sub-agents only when that pays off. On an empty project it asks up to 5 questions, writes the map files, then starts the first feature. Progress is one page: `STATUS.md`.

The daily flow does not change if the product is a video OS, an ERP, or a shop. Only module names change.

## Start

1. Use this GitHub template.
2. Open the repo in Codex, Cursor Project, or Claude Code.
3. Say: `This is a new project. Interview me first.`
4. Answer up to 5 questions, or say `use your recommendations`.
5. The agent writes the map files and starts the first feature.

## Daily

- `Change checkout shipping. Touch only checkout.`
- `wrap up` — rewrites STATUS and commits locally (no push).

Tiny edits do not belong in STATUS.

## When chat memory disappears

Do not paste the old thread. A new session reads `STATUS.md`, then only what the Next item needs.

## Keep it lean

- `STATUS.md` is overwritten, never appended. No HANDOFF or PROGRESS files.
- History and test evidence go in git commits and PR descriptions.
