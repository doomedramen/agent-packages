- Confirm the installed Tailwind CSS major version and follow its matching
  configuration and CSS entry-point model; v4 uses CSS-first configuration and
  framework-specific integration packages.
- Reuse the project's design tokens and component conventions instead of
  introducing one-off colors, spacing values, or parallel styling systems.
- Keep class names statically discoverable by the configured scanner. Avoid
  constructing utility names from runtime fragments; map data values to
  complete, explicit class strings instead.
- Keep responsive, state, and dark-mode variants readable. Extract a component
  or shared token when a class list becomes difficult to review.
- Verify styles in the actual build pipeline after changing Tailwind config,
  plugins, source scanning, or global CSS imports.
