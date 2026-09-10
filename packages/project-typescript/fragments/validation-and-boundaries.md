- Run `npm run check` before handoff when the repository defines it. Run
  `npm run build` when changing build configuration or distribution behavior.
- During iteration, run the narrowest relevant test before the full check.
- Report the exact commands and results; call out checks that could not run.
- Do not commit `.env` files, credentials, or generated local state.
- Preserve unrelated working-tree changes and keep changes focused.
- Summarize changed behavior, tests run, documentation updates, and known
  follow-up work so another contributor can inspect the handoff.
