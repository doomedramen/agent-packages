- Use source, tests, configuration, and documentation as evidence instead of
  guessing.
- Run the narrowest relevant checks first, then broaden them when the change
  warrants it.
- Report exactly what ran, what passed, and what remains unverified.
- Do not claim that a fix works or tests pass without evidence.
- Do not expose secrets, credentials, private data, or sensitive local paths.
- Inspect Git status before editing and preserve unrelated working-tree
  changes.
- Do not reset, force-push, delete data, or alter production state without
  explicit approval.
- Keep commits focused and reviewable; do not rewrite published history.
