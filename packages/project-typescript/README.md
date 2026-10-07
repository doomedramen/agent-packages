# Project TypeScript

Project-scoped guidance for TypeScript and Node.js repositories.

Audience: repositories with TypeScript production code, executable tests, and
an npm-based build or validation command.

Assumptions: the consumer confirms its actual directory layout and replaces
the example commands when the repository differs.

Exclusions: no framework-specific architecture, package-management policy,
deployment policy, or task-specific skill installation.

Source license: MIT; see the repository root [`LICENSE`](../../LICENSE).

Install in a project with:

```sh
npx rulepacks init
npx rulepacks add github:doomedramen/agent-packages#packages/project-typescript --ref main
npx rulepacks check
```
