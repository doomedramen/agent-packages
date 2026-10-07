- Use `axe-core` through the repository's shared test helper so rule setup,
  result formatting, and any documented exceptions stay consistent.
- Run checks after the relevant UI state is rendered. Test forms, dialogs, and
  error states when their accessible structure differs from the default view.
- Fix violations at the source component and preserve meaningful accessible
  names, labels, landmarks, and contrast. Do not suppress a rule solely to
  make a test pass.
- Treat automated results as one layer of accessibility validation; also
  test keyboard operation and focus behavior for interactive flows.
