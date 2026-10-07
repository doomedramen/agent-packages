- Confirm the installed Next.js version and read its matching documentation
  before changing framework code. Prefer documentation shipped in the local
  `node_modules/next/dist/docs/` when available; use the official docs as a
  secondary reference.
- Follow the repository's routing model and colocated conventions. In the App
  Router, keep server components as the default and add a client boundary only
  where browser state, event handlers, or client-only APIs require it.
- Keep secrets and privileged data access on the server. Do not import
  server-only modules into client components; use supported server actions or
  route handlers as the boundary.
- Check version-specific request APIs and route conventions. In Next.js 15 and
  later, request APIs such as `cookies()`, `headers()`, `draftMode()`, and
  dynamic route `params` / `searchParams` are asynchronous.
- Treat framework-managed output as generated. Change source, configuration,
  or supported extension points instead of editing `.next/` output.
- Validate behavior with the repository's typecheck, tests, and build commands
  when relevant; report which checks ran.
