# Public v2 agent packages

This repository contains real, reviewable Git sources for
[`@doomedramen/agents.md`](https://github.com/doomedramen/agents.md). Every
package uses the schema 2 fragment format. Every pack is a schema 2 recipe.

The examples are deliberately ordinary Git content: no registry, account, or
hosted service is required. Pin a branch, tag, or commit when adopting a
source in a real project.

## Quick start: one project package

From a TypeScript or Node.js repository:

```sh
npx @doomedramen/agents.md init
npx @doomedramen/agents.md add github:doomedramen/agent-packages#packages/project-typescript --ref main
npx @doomedramen/agents.md edit
npx @doomedramen/agents.md check
```

This creates and verifies a project `AGENTS.md`, a Claude Code import adapter,
an `agents.yaml` configuration, an immutable `agents.lock`, and a local
`.agents/project.md` file for repository-specific notes.

Review the source before adopting it:

- [`project-typescript` manifest](packages/project-typescript/agent.yaml)
- [`project-typescript` package README](packages/project-typescript/README.md)
- [fragment sources](packages/project-typescript/fragments/)

## Quick start: a shareable pack

The `typescript-project` pack composes the baseline and TypeScript packages
into one root output:

```sh
npx @doomedramen/agents.md init
npx @doomedramen/agents.md add github:doomedramen/agent-packages#packs/typescript-project --ref main
npx @doomedramen/agents.md check
```

Pack source and member commits are recorded separately in `agents.lock`.
Removing the pack removes only its contribution; a direct selection of one of
its member packages remains independent.

- [`typescript-project` recipe](packs/typescript-project/agents.yaml)
- [`typescript-project` pack README](packs/typescript-project/README.md)

## Quick start: a monorepo pack

The `typescript-monorepo` pack demonstrates one root output and one nested
output:

```sh
npx @doomedramen/agents.md init
npx @doomedramen/agents.md add github:doomedramen/agent-packages#packs/typescript-monorepo --ref main
npx @doomedramen/agents.md check
```

It writes root guidance and separate `apps/web/AGENTS.md` guidance. Local
context stays next to each output, so application-specific notes do not leak
between packages.

- [`typescript-monorepo` recipe](packs/typescript-monorepo/agents.yaml)
- [`typescript-monorepo` pack README](packs/typescript-monorepo/README.md)

## Committed consumer examples

The repository also includes two small consumers with generated output,
immutable locks, and local project context:

- [`examples/direct-project`](examples/direct-project) selects one package
  directly.
- [`examples/typescript-monorepo`](examples/typescript-monorepo) selects the
  nested-output pack.

Run `npx @doomedramen/agents.md check` from either directory to verify its
committed state. The example applications are intentionally tiny; the point is
to make source selection, locking, local additions, and output boundaries
visible.

## Global guidance

The same destination-neutral package can be selected globally. The consumer
chooses the registered agent destinations; the package manifest does not write
legacy v1 targets:

```sh
npx @doomedramen/agents.md init --global --agents claude-code,codex
npx @doomedramen/agents.md add github:doomedramen/agent-packages#packages/global-baseline --ref main --global
npx @doomedramen/agents.md check --global
```

Review global output carefully. It applies to every repository using those
agent destinations.

## Repository layout

```text
packages/<name>/
├── agent.yaml                 # schema 2 package manifest
├── README.md                  # audience, assumptions, exclusions, license
└── fragments/*.md             # focused reusable guidance

packs/<name>/
├── agents.yaml                # schema 2 pack recipe
└── README.md                  # selected outputs and usage
```

Keep fragments focused. Package README files describe intended audience,
assumptions, exclusions, and source licensing. Packs may use relative members
inside this repository; consumers lock the recipe and every member separately.

## Contributing

1. Edit or add a focused fragment.
2. Update its schema 2 manifest and README.
3. Inspect the rendered result in a consumer project.
4. Commit the package or pack, then use its commit or a reviewed ref in
   downstream `agents.yaml` files.

Do not add task-specific skills, credentials, generated consumer state, or
legacy v1 destination declarations to this repository.

Source license: MIT. See [`LICENSE`](LICENSE).
