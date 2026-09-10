# agents.md reference packages

Installable Git packages for [`@doomedramen/agents.md`](https://www.npmjs.com/package/@doomedramen/agents.md).

Each directory under `packages/` is a package. Its `agent.yaml` declares the
scope and destinations, and its `AGENTS.md` is the canonical instruction file.

## Project package

Run this from a TypeScript or Node.js repository:

```sh
npx @doomedramen/agents.md add github:doomedramen/agent-packages#packages/project-typescript
```

This installs project-scoped `AGENTS.md` guidance and a Claude Code
`CLAUDE.md` import adapter.

- [Manifest](packages/project-typescript/agent.yaml)
- [Instructions](packages/project-typescript/AGENTS.md)

## Global package

Review the file before installing it. Global instructions apply across every
repository used by the configured agent:

```sh
npx @doomedramen/agents.md add github:doomedramen/agent-packages#packages/global-baseline
```

This installs global Codex guidance at `~/.codex/AGENTS.md`, global Claude
guidance at `~/.claude/AGENTS.md`, and the Claude import adapter at
`~/.claude/CLAUDE.md`.

- [Manifest](packages/global-baseline/agent.yaml)
- [Instructions](packages/global-baseline/AGENTS.md)

The manifest sets the scope. The command has no global or project flag.

## Package layout

```text
packages/<name>/
├── agent.yaml
└── AGENTS.md
```

The package repository is intentionally Git-native. Tags or commit SHAs can be
used as Git refs when a consumer needs a stable revision.
