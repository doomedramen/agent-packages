- Use generated Protobuf-ES descriptors and message types from their published
  package exports. Do not hand-edit generated output or duplicate wire types
  in application code.
- Follow the installed major version's message construction, presence, enum,
  and serialization APIs; do not assume plain JSON objects preserve protobuf
  semantics.
- Keep transport mapping at the RPC boundary and convert to domain types only
  when the application needs a stable model independent of the wire contract.
- Regenerate from the source schema using the repository's pinned toolchain
  when contract generation is owned by the current repository.
- Test optional fields, enum values, and compatibility-sensitive mappings at
  the boundary where they affect application behavior.
