# TypeScript monorepo consumer

This is a small consumer project that selects the public
[`typescript-monorepo`](../../packs/typescript-monorepo) pack. The pack writes
one root output and a separate `apps/web` output; it does not copy root
guidance into the nested application.

From this directory, verify the committed state with:

```sh
npx rulepacks check
```

Inspect these generated files:

- `AGENTS.md` — root baseline guidance
- `apps/web/AGENTS.md` — application workflow guidance
- `agents.lock` — the locked recipe and member commits

The configuration uses `ref: main` for a simple walkthrough. Replace it with a
reviewed tag or commit before adopting the pattern in a production repository.
