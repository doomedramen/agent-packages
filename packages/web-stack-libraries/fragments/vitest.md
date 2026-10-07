- Follow the repository's Vitest configuration for environment, setup files,
  aliases, test discovery, and coverage. Do not add a competing test runner or
  duplicate global setup.
- Keep pure logic tests in the configured unit-test scope. Use the configured
  DOM environment only for tests that render browser components.
- Mock at the module or service boundary with the existing Vitest patterns;
  avoid mocks that reproduce the implementation instead of checking behavior.
- Cover normal outcomes and meaningful error, empty, loading, and boundary
  states. Update coverage allowlists or thresholds when the repository uses
  them.
- Run the focused test while iterating and the repository's full test command
  before handoff when requested or required by its workflow.
