- Consume `@pikl-insurance/pas-contracts` through its published service and
  message exports. Treat generated files as read-only in consumer projects.
- Use the package's generated service descriptors with Connect clients and its
  generated message types for request and response shapes; avoid local copies
  of service definitions or hand-maintained wire interfaces.
- Keep application validation and user-facing domain outcomes in the
  consuming application. A generated contract type does not replace input
  validation or authorization.
- Check the installed package version and available exports before depending
  on a new service or field. Contract changes belong in the schema-owning
  repository and should follow its compatibility checks.
- Handle protobuf presence and enum semantics using the generated API rather
  than assuming every field behaves like a plain JavaScript object property.
