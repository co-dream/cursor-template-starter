# First-time setup

Read this only when `STATUS.md` says `Setup: not done`.

Existing project: if the user says to skip the interview, rewrite `STATUS.md` from the current code and git log (remove `Setup: not done`), then stop. Move old HANDOFF / PROGRESS / log files to `docs/archive/`.

1. Do not scan the repo or start product work yet.
2. Ask at most 5 questions in one message. Give your recommended answer with each.
   1. One sentence: what is this product?
   2. Who is it for?
   3. What is explicitly out of scope?
   4. What is the smallest unit of change? (one shot / one module / one document / one checkout step)
   5. What is the first feature to ship?
3. After the user answers (or says "use your recommendations"), write these once:
   - `docs/PRODUCT.md`
   - `CONTEXT.md` (glossary only)
   - `specs/INDEX.md` (module list)
   - empty folders only for named modules
   - `STATUS.md`: remove `Setup: not done`; Next is the first feature
4. Recap in three lines, then start the first feature unless the user asked to review first.
