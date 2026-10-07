- Import named icons from `lucide-react` and keep the icon set tree-shakeable;
  do not import an entire icon namespace or add inline SVG copies without need.
- Treat decorative icons as hidden from assistive technology when adjacent
  text already names the action. Give icon-only controls an accessible name
  on the interactive element.
- Reuse project sizing and stroke conventions. Avoid using an icon's color or
  shape as the only carrier of status or meaning.
- Check the installed package for the exact icon export before changing icon
  names or adding dependencies.
