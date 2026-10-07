- Define schemas at untrusted input boundaries and infer TypeScript types from
  schemas where that avoids maintaining two sources of truth.
- Distinguish parsing from validation: use `parse` when failure should throw
  and `safeParse` when the caller needs to present or branch on issues.
- Keep coercion and defaults explicit. Do not silently transform user input
  unless the product contract calls for it.
- Reuse schemas for shared constraints, but keep request, environment, and
  persisted-data schemas separate when their accepted shapes differ.
- Test valid input, invalid input, optional fields, and boundary values that
  affect user-visible behavior.
