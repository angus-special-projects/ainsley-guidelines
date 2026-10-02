# Code quality

This document defines the baseline code-quality standards for the repository. It applies to every package unless a language-specific document overrides it.

## Principles

- Prefer clear, simple, maintainable code over clever implementations.
- Keep functions small and focused on one responsibility.
- Name things for intent, not implementation details.
- Avoid duplication; extract shared behavior when it improves clarity.
- Make dependencies explicit and keep side effects contained.
- Fail fast with useful error messages and safe defaults.

## Writing code

- Use consistent formatting and let automated formatters handle style.
- Keep control flow easy to follow; reduce nesting where possible.
- Prefer immutable data where practical.
- Avoid unnecessary abstraction until a pattern is proven useful.
- Add comments only when they explain why, not what the code already says.

## Error handling

- Handle expected failures close to the source.
- Do not swallow exceptions or return ambiguous sentinel values.
- Include context in errors so failures are actionable.
- When retrying, keep the retry policy explicit and bounded.

## Reviews and maintainability

- Every change should be easy to review in small, logical increments.
- Keep public APIs stable unless a breaking change is intentional and documented.
- Choose names, structure, and module boundaries that make future changes easier.
- If code becomes difficult to explain, refactor it before it spreads.

## Checklist

- [ ] Is the code easy to read without extra explanation?
- [ ] Are responsibilities separated clearly?
- [ ] Are errors handled explicitly and safely?
- [ ] Is the solution free of unnecessary duplication?
- [ ] Would a teammate understand the intent quickly?

