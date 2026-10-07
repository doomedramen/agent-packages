- Follow the repository's Connect transport and generated service conventions.
  Use the installed `@connectrpc/connect` APIs and the transport appropriate
  to the runtime; do not assume a browser transport is safe for server-only
  credentials.
- Keep RPC clients behind a small service or gateway boundary. Centralize
  transport configuration, interceptors, authentication, deadlines, and
  error translation rather than recreating them per feature.
- Keep internal tokens and privileged service calls on the server. Never pass
  credentials through client props, browser code, or request payloads.
- Treat Connect errors by status code and map expected failures to explicit
  domain outcomes. Do not turn every failure into an empty success response.
- Test the gateway boundary with the project's established mocks and cover
  success, expected service errors, and unexpected failures.
