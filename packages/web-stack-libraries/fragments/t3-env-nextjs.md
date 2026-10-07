- Define server and client variables explicitly in the environment schema.
  Only values intended for browsers should be placed in the public-variable
  section or use the framework's public prefix.
- Keep secrets server-only and validate required configuration at startup or
  at the established lazy boundary. Never add secret values to source,
  generated instructions, logs, or client bundles.
- Use the installed `@t3-oss/env-nextjs` API and matching Zod version; inspect
  the existing `createEnv` setup before adding another environment parser.
- Keep test values in test configuration and document variable names and
  purpose without documenting their secret values.
- Test missing, malformed, and valid values at the environment boundary.
