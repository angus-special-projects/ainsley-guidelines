# Python general guidelines

These guidelines build on the core standards and apply to Python code in this repository.

# A new section

A new section here

## Project structure

- Organize code into small, focused modules.
- Keep package boundaries clear and avoid circular imports.
- Prefer explicit imports over wildcard imports.
- Place executable entry points in dedicated modules or scripts.

## Style and readability

- Follow PEP 8 where practical and keep formatting consistent.
- Use descriptive names for functions, classes, and variables.
- Keep functions short and favor early returns over deeply nested logic.
- Use docstrings for public modules, classes, and functions when the intent is not obvious.

## Pythonic practices

- Prefer standard-library solutions before adding dependencies.
- Use context managers for resources such as files, locks, and network connections.
- Prefer `pathlib` over manual string path manipulation.
- Use `dataclasses` for simple data containers.
- Keep mutable default arguments out of function signatures.

## Errors and logging

- Raise specific exceptions and preserve the original cause when useful.
- Use logging for operational visibility; avoid `print` in production code.
- Keep logs structured, informative, and free of secrets.

## Configuration

- Read configuration from environment variables or explicit config objects.
- Validate required settings at startup.
- Avoid hidden global state where the behavior depends on import order.

## Practical checklist

- [ ] Is the code easy to read and reason about?
- [ ] Are imports explicit and organized?
- [ ] Are resources managed safely with context managers?
- [ ] Are exceptions and logs helpful without leaking sensitive data?
- [ ] Is the design simple enough for future changes?

