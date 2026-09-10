- Read `README.md`, `package.json`, `tsconfig.json`, and nearby code before
  changing behavior.
- Keep production code in `src/` and follow the existing ESM, naming, and
  error-handling conventions when that layout exists.
- Preserve public APIs and package entry points unless the change explicitly
  requires a break.
- Add or update a focused regression test for each behavior change.
- Update documentation when commands, public behavior, or repository
  structure changes.
- Treat `dist/` and other build output as generated; edit the source and
  rebuild instead of editing generated files by hand.
