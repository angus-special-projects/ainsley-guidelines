# Go guidelines

These guidelines apply to Go code in this repository and build on the core standards.

## Package design

- Keep packages small and cohesive.
- Prefer simple package boundaries with clear responsibilities.
- Use exported identifiers only when they are part of the intended public API.
- Avoid circular dependencies by keeping lower-level packages independent.

## Style and idioms

- Follow standard Go formatting with `gofmt`.
- Favor straightforward code over clever abstractions.
- Use descriptive names and keep functions focused.
- Prefer composition over deep inheritance-style patterns.

## Error handling

- Return errors explicitly and handle them close to where they occur.
- Wrap errors with useful context where it helps debugging.
- Do not ignore returned errors.
- Use sentinel errors and custom types intentionally and sparingly.

## Concurrency

- Use goroutines and channels only when they simplify the design.
- Make shared state explicit and protect it carefully.
- Add timeouts and cancellation for long-running operations.
- Avoid blocking the main flow unnecessarily.

## Configuration and I/O

- Pass dependencies and configuration explicitly.
- Prefer `context.Context` for request-scoped operations.
- Keep file and network operations bounded and observable.
- Validate inputs at boundaries and fail fast on invalid data.

## Testing

- Write table-driven tests where they improve clarity.
- Keep tests deterministic and independent.
- Prefer testing exported behavior over implementation details.

## Checklist

- [ ] Is the package small and purpose-driven?
- [ ] Are errors handled consistently and explicitly?
- [ ] Is concurrency used only when it adds value?
- [ ] Are dependencies and configuration passed clearly?
- [ ] Are tests readable and reliable?
