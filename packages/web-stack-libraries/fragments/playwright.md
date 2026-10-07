- Follow the repository's Playwright config, fixtures, page objects, and
  environment setup. Reuse its authentication and data lifecycle instead of
  creating a second login path.
- Prefer locators by role, label, and visible name. Keep selectors in existing
  page objects when that is the repository convention.
- Cover user-visible flows and important navigation or persistence behavior;
  keep assertions resilient to presentation changes while checking meaningful
  outcomes.
- Distinguish application failures from shared-backend, authentication, or
  infrastructure failures. Report retries and flaky behavior accurately.
- Do not put credentials in test source. Use the configured environment or
  secret store and avoid tests that mutate shared production data.
