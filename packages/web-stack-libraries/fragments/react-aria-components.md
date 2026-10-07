- Prefer React Aria Components for accessible interaction patterns when it is
  already part of the project's UI stack. Check the installed API and nearby
  components before creating a parallel primitive.
- Preserve the component's label, description, error, disabled, and validation
  relationships when composing fields. Prefer library-provided slots and
  render props to recreating ARIA state manually.
- Use the library's state and event contracts rather than reading DOM state or
  adding competing keyboard handlers.
- Test the interaction with keyboard and pointer input, and include the
  project's accessibility assertion for rendered UI.
