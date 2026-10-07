# Direct package consumer

This is a small consumer project that selects the public
[`project-typescript`](../../packages/project-typescript) package directly.
The generated files and lockfile are committed so the result can be inspected
without installing anything first.

From this directory, verify the committed state with:

```sh
npx rulepacks check
```

The configuration uses the public GitHub source with `ref: main` for a simple
walkthrough. The lockfile pins the exact source commit. For a production
consumer, replace `main` with a reviewed tag or commit before committing the
configuration.

This fixture is intentionally small: the package supplies standing guidance,
while `.agents/project.md` supplies facts specific to this example project.
