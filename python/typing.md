# Python typing guidelines

These typing conventions build on the general Python and core standards.

## General approach

- Add type hints to public functions, methods, and data structures.
- Prefer explicit types when they improve readability and tool support.
- Keep types accurate and up to date as code changes.
- Use typing to clarify intent, not to overcomplicate simple code.

## Common preferences

- Use built-in generic syntax such as `list[str]` and `dict[str, int]`.
- Prefer `X | None` for optional values when the project targets modern Python.
- Use `Callable`, `Iterable`, `Sequence`, and `Mapping` when a broader interface is appropriate.
- Use `Protocol` for structural contracts and `TypedDict` for dictionary-shaped records.

## Practical rules

- Avoid `Any` unless the boundary is genuinely dynamic.
- Use `cast()` sparingly and only when the runtime behavior justifies it.
- Narrow types with guards, validation, and explicit branches instead of assertions alone.
- Keep overloads and advanced typing features for APIs that truly need them.

## Tooling

- Keep the code compatible with the repository’s chosen type checker.
- Resolve type errors close to the source rather than suppressing them broadly.
- Prefer small, local refinements over broad, hard-to-maintain annotations.

## Checklist

- [ ] Are public APIs annotated clearly?
- [ ] Are types specific enough to be useful?
- [ ] Is `Any` avoided unless necessary?
- [ ] Are casts and advanced typing features used carefully?
- [ ] Will the annotations help readers and tooling alike?

