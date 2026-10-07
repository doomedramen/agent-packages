- Treat `@pikl-insurance/pikl-ui-admin` as the shared admin design system.
  Check its installed exports and existing usage before building a duplicate
  control or interaction.
- Prefer its form, table, dialog, tab, toast, and feedback components when
  they meet the requirement; use the package's supported props and composition
  patterns rather than styling its internals.
- Import shared styles and configure framework transpilation only as documented
  by the installed package and consuming application.
- Keep UI-library changes separate from product-specific data rules. Wrap a
  shared component when a product needs a stable domain-level interface.
- Verify keyboard, focus, and error behavior in the consuming app; a component
  being accessible in isolation does not prove the composed flow is accessible.
