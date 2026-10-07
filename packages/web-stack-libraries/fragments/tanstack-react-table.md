- Treat TanStack React Table as a headless state and row-model library. The
  application remains responsible for semantic table markup, labels, focus,
  empty states, and responsive presentation.
- Use the installed version's APIs and define stable column definitions and
  row identifiers from domain data.
- Add only the row models needed for the requested sorting, filtering,
  pagination, grouping, or visibility behavior; keep controlled state in one
  clear owner.
- Preserve URL or server state only when that is an existing product pattern.
  Avoid duplicating table state between the table instance and unrelated
  component state.
- Test sorting, pagination, empty data, and relevant keyboard interaction in
  the rendered table.
