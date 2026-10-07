- Use `clsx` for conditional class values and follow the consuming project's
  shared composition helper when one exists.
- Keep conditions explicit and readable; prefer a variant map for a finite set
  of states instead of building class names from runtime fragments.
- Add focused tests when changing a shared class helper or a component's
  externally visible variant behavior.
