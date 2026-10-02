# FastAPI guidelines

These guidelines apply to FastAPI services in this repository and build on the Python and core standards.

## API design

- Design endpoints around resources and use clear, consistent paths.
- Choose HTTP methods and status codes that match the intended action.
- Keep request and response models explicit.
- Return predictable error shapes so clients can handle failures reliably.

## Application structure

- Keep routers, schemas, services, and infrastructure concerns separated.
- Put business logic in service layers rather than in route handlers.
- Use dependency injection to make components easy to test and replace.
- Keep route functions small and focused on request/response handling.

## Validation and serialization

- Use Pydantic models for request and response validation.
- Validate incoming data at the boundary and reject invalid payloads early.
- Avoid leaking internal objects directly when a public schema is more appropriate.
- Keep serialization rules explicit for dates, enums, and optional values.

## Errors and middleware

- Raise HTTP errors with clear messages and appropriate status codes.
- Centralize error handling where possible.
- Use middleware intentionally for cross-cutting concerns such as tracing, metrics, and auth.
- Ensure error responses do not expose secrets or implementation details.

## Async behavior

- Use async endpoints when the work is I/O bound and the dependencies support async.
- Keep blocking work off the event loop.
- Be deliberate about background tasks, timeouts, and retries.

## Testing

- Test routers, dependencies, and validation rules.
- Prefer endpoint tests that exercise the public contract.
- Mock external services at the boundary.

## Checklist

- [ ] Are endpoints intuitive and resource-oriented?
- [ ] Are request and response schemas explicit?
- [ ] Is business logic separated from route handlers?
- [ ] Are errors handled consistently and safely?
- [ ] Are async and blocking workloads used appropriately?
