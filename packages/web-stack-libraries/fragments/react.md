- Follow the installed React version's documentation and the host framework's
  rendering model; do not assume a client-only application.
- Keep components focused on rendering and interaction. Move reusable pure
  logic into ordinary functions and keep state close to the components that
  own it.
- Call Hooks unconditionally at the top level of components or custom Hooks.
  Keep effect dependencies complete and use effects for synchronization with
  external systems, not for values derivable during render.
- Prefer controlled, accessible interactions and semantic HTML. Preserve
  keyboard behavior, labels, focus, and form semantics when replacing native
  elements with custom components.
- Use stable keys from domain data for collections; do not use array positions
  when items can be inserted, removed, or reordered.
- Add or update tests for rendered states and user interactions using the
  project's established renderer and accessibility checks.
