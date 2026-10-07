# Global baseline

Stable defaults for coding-agent work across repositories. The package is
destination-neutral: its schema 2 manifest contains fragments, not v1 global
targets. The consumer chooses project or global scope and the agent
destinations.

Audience: individuals and teams that want a small, conservative baseline
before adding project-specific guidance.

Assumptions: the user reviews the generated guidance and keeps repository- or
service-specific commands in the project package or local consumer file.

Exclusions: no project architecture, framework rules, task-specific skills,
credentials, or automatic priority claims.

Source license: MIT; see the repository root [`LICENSE`](../../LICENSE).

Install globally with:

```sh
npx rulepacks init --global --agents claude-code,codex
npx rulepacks add github:doomedramen/agent-packages#packages/global-baseline --ref main --global
npx rulepacks check --global
```
