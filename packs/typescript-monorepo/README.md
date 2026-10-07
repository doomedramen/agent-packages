# TypeScript monorepo pack

This pack demonstrates separate guidance outputs. The root receives the
baseline, while `apps/web` receives project TypeScript workflow guidance.

Use it when the consumer wants application-local instructions without copying
root guidance into every nested output:

```sh
npx rulepacks init
npx rulepacks add github:doomedramen/agent-packages#packs/typescript-monorepo --ref main
npx rulepacks check
```

The consumer's local files stay beside their outputs:

- `.agents/project.md` for the root output
- `apps/web/.agents/project.md` for the web application output

Source license: MIT; see the repository root [`LICENSE`](../../LICENSE).
