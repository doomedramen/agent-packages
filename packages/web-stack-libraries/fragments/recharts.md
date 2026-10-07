- Use the installed Recharts version and the project's existing chart
  components, color tokens, and formatting helpers.
- Keep chart data transformation and domain formatting outside presentation
  where practical. Handle empty, incomplete, and large data sets explicitly.
- Provide a useful title or accessible description and do not rely on color
  alone to distinguish series. Keep labels, tooltips, and legends consistent
  with the displayed data.
- Avoid coupling application logic to undocumented SVG or DOM structure.
- Verify responsive sizing and interaction in the browser; chart layout can
  depend on its rendered container dimensions.
