# Guide (English)

## What this is

A small template so coding agents can resume after the chat is gone.

You talk to one coordinator. It does not edit product files during daily work. On an empty project it asks up to 5 questions, writes the map files, then sends one worker at a time. Progress is one page: `STATUS.md`.

Works in Cursor Projects and Codex. The daily flow does not change if the product is a video OS, an ERP, or a shop. Only module names change.

## Start

1. Use this GitHub template.
2. Open a Cursor Project on that repo, or run Codex in the folder.
3. Say: `This is a new project. Interview me first.`
4. Answer up to 5 questions, or say `use your suggestions`.
5. When the four map files exist, say `start`.

## Daily

- `Change checkout shipping. Touch only checkout.`
- `Ask me 3 questions first. Write done-when into STATUS.`
- `wrap up` — update STATUS only. Do not edit other files.

Tiny edits do not belong in STATUS and do not need a Project.

## When chat memory disappears

Do not paste the old thread. A new session should read `STATUS.md`, `docs/PRODUCT.md`, and only the spec named by Next.
