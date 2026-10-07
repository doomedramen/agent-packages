- Test components through accessible roles, names, labels, and visible
  behavior. Avoid selectors tied to implementation details when a user-facing
  query is available.
- Await asynchronous UI updates and assert the resulting state instead of
  implementation calls when practical.
- Use the project's configured DOM environment and cleanup setup. Keep each
  test isolated and avoid depending on execution order.
- Include accessibility assertions when the project provides a shared helper;
  automated checks supplement, but do not replace, accessible queries and
  interaction coverage.
