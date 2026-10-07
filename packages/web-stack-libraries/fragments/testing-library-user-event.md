- Use `@testing-library/user-event` for realistic keyboard and pointer
  interactions. Use lower-level event dispatch only when the event itself is
  the behavior under test.
- Await user interactions and let the component process the full interaction
  sequence before asserting the resulting UI.
- Prefer queries by role, name, and label so tests exercise the same semantics
  available to users and assistive technology.
