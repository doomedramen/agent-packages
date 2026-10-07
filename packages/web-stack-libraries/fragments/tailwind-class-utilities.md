- Use `clsx` for conditional class values and the project's shared helper for
  composing them; avoid introducing a second helper with different semantics.
- Use `tailwind-merge` only to resolve conflicting Tailwind utilities in
  caller-provided class names. It does not replace design-system decisions or
  validate arbitrary CSS.
- Preserve the order and intent of variants when composing classes, and add a
  focused test when a shared class helper or variant API changes.
- Check that the installed `tailwind-merge` version understands the project's
  Tailwind version and custom utility groups before relying on conflict
  resolution for custom tokens.
