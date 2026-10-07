- Use `@axe-core/playwright` at the repository's established page or component
  boundary and keep the shared accessibility helper as the single assertion
  seam where one exists.
- Run checks after the relevant UI state is rendered. Exercise dialogs,
  menus, validation errors, and other states separately when their accessible
  structure differs.
- Fix violations at the source component and preserve meaningful accessible
  names, labels, landmarks, and contrast. Do not suppress a rule solely to
  make a test pass.
- Treat automated axe results as one layer of accessibility validation; also
  test keyboard operation and focus behavior for interactive flows.
- If a rule must be disabled for a documented reason, scope the exception to
  the smallest target and explain the limitation in the test.
