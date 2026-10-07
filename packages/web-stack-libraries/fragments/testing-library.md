- Test components through accessible roles, names, labels, and visible
  behavior. Avoid selectors tied to implementation details when a user-facing
  query is available.
- Use `user-event` for realistic keyboard and pointer interactions; use
  `fireEvent` only when the event itself is the behavior under test.
- Await interactions and asynchronous UI updates. Assert the resulting state
  instead of implementation calls when practical.
- Use the project's configured DOM environment and cleanup setup. Keep each
  test isolated and avoid depending on execution order.
- Include accessibility assertions when the project provides a shared helper;
  automated checks supplement, but do not replace, accessible queries and
  interaction coverage.
