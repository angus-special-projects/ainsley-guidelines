# Python testing guidelines

These testing practices support the Python package and should be used with the core code-quality standards.

## Test strategy

- Prefer fast, deterministic unit tests for most behavior.
- Add integration tests for boundaries such as databases, APIs, and file systems.
- Keep end-to-end tests focused on a few high-value workflows.
- Test behavior, not implementation details.

## Pytest conventions

- Use `pytest` as the default test framework.
- Follow arrange-act-assert structure where it improves readability.
- Use fixtures for shared setup, but keep them small and explicit.
- Parameterize related cases instead of duplicating tests.

## Good test properties

- Tests should be independent and order-agnostic.
- Avoid external network calls in unit tests.
- Mock only the boundary you control; do not over-mock internal behavior.
- Keep test data minimal and easy to understand.

## Async code

- Use async-aware test helpers for asynchronous code.
- Verify both success and failure paths.
- Keep event-loop interactions isolated and deterministic.

## Coverage and maintenance

- Focus on meaningful coverage rather than raw percentages.
- Update or remove brittle tests when the production code changes.
- Name tests clearly so the scenario and expected outcome are obvious.

## Checklist

- [ ] Are the tests deterministic and independent?
- [ ] Do they validate observable behavior?
- [ ] Are fixtures and mocks used sparingly?
- [ ] Are edge cases and failure paths covered?
- [ ] Would a new contributor understand what each test protects?

