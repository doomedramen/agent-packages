# TypeScript project pack

This pack composes [`global-baseline`](../../packages/global-baseline) and
[`project-typescript`](../../packages/project-typescript) into one project
output. It is a small, usable starting point for a TypeScript repository.

The pack assumes a consumer with a normal Git working tree. It does not add
framework rules, deployment instructions, skills, secrets, or local project
files. Add those through the consumer's `.agents/project.md` or another
reviewed package.

Install it from any project:

```sh
npx rulepacks init
npx rulepacks add github:doomedramen/agent-packages#packs/typescript-project --ref main
npx rulepacks check
```

Source license: MIT; see the repository root [`LICENSE`](../../LICENSE).
