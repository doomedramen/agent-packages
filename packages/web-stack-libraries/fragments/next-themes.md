- Place the theme provider at the application boundary expected by the host
  framework and keep the provider's configuration aligned with the CSS theme
  tokens.
- Avoid rendering a theme-dependent control with a different server and first
  client result. Gate stored-theme-dependent UI until mount or render a stable
  neutral state.
- Use the library's theme and system-preference APIs instead of maintaining a
  second theme value in component state or storage.
- Check the installed library's hydration guidance before suppressing hydration
  warnings; suppression should not conceal mismatched markup.
- Test theme switching, system preference, and persisted selection when these
  behaviors are user-facing.
