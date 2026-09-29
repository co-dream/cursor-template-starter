# First-time setup

Read this only when `STATUS.md` says `Setup: not done`.

1. Do not scan the repo or start product work yet.
2. Ask at most 5 questions in one message. Give your recommended answer with each.
   1. One sentence: what is this product?
   2. Who is it for?
   3. What is explicitly out of scope?
   4. What is the smallest unit of change? (one shot / one module / one document / one checkout step)
   5. What is the first feature to ship?

   In the same message, ask whether to keep `LICENSE` (MIT, currently © co-dream) under the user's name, or remove it.
3. After the user answers (or says "use your recommendations"), write these once:
   - `docs/PRODUCT.md`
   - `CONTEXT.md`: keep the Shared section; replace the video example with this product's terms
   - `specs/INDEX.md`: module list. Do not create empty module folders; git does not keep them
   - `README.md`: replace the template README with a short one for this product
   - `STATUS.md`, in the user's language: remove `Setup: not done`; Next is the first feature
4. Remove template-only files: `info/`, `CONTRIBUTING.md`, this file, and `LICENSE` if the user chose to remove it.
5. Recap in three lines, then start the first feature (spec first) unless the user asked to review first.
