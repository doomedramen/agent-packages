- Use `tailwind-merge` to resolve conflicting Tailwind utility classes in
  caller-provided class names; it does not replace design-system decisions or
  validate arbitrary CSS.
- Preserve the order and intent of variants when composing classes.
- Check that the installed `tailwind-merge` version understands the project's
  Tailwind version and custom utility groups before relying on conflict
  resolution for custom tokens.
