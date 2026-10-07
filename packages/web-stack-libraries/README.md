# Web stack libraries

Reusable implementation guidance for projects that use the listed web
application libraries. Each fragment focuses on library-specific boundaries,
common failure modes, and version-aware documentation lookup; consumers can
exclude fragments they do not use.

Audience: TypeScript web applications using one or more of these libraries.

Assumptions: consumers verify installed versions, existing project conventions,
and framework integration before applying a pattern. The guidance describes
library usage and does not prescribe a project's architecture, commands,
credentials, or deployment process.

Exclusions: no PAS product rules, secrets, service URLs, test credentials,
project-specific commands, or claims that every listed library fits every app.

Source license: MIT; see the repository root [`LICENSE`](../../LICENSE).

Install the package and exclude fragments your project does not use:

```sh
npx rulepacks init
npx rulepacks add github:doomedramen/agent-packages#packages/web-stack-libraries --ref main
npx rulepacks edit
npx rulepacks check
```
