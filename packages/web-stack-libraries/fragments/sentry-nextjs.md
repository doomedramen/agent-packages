- Follow the installed `@sentry/nextjs` setup for the framework version and
  runtime. Keep server, edge, and browser instrumentation in their supported
  entry points.
- Capture actionable errors with useful context while excluding credentials,
  tokens, personal data, and request bodies that are not safe to send.
- Avoid reporting the same handled failure at multiple layers. Preserve the
  original error and user-facing behavior when adding telemetry.
- Treat source-map upload, tunnels, cron monitors, and build plugins as
  deployment and cost decisions; change them only when the application needs
  the behavior.
- Verify instrumentation in the target runtime and build configuration rather
  than relying only on unit tests.
