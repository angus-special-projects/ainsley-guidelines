# Ainsley Guidelines

This repository contains shared AI-assisted coding guidelines for the team.

The content is organized into small packages so that general standards can be reused across languages, while language-specific guidance stays focused and easy to maintain.

## Repository structure

- `mainifest.yaml` — top-level registry of guideline packages
- `core/` — shared standards that apply to every package
- `python/` — Python-specific guidance that builds on `core`
- `fastapi/` — FastAPI guidance that builds on `python`
- `go/` — Go guidance that builds on `core`

Each package has a `manifest.yaml` that defines its name, version, type and any dependencies.

## Available guidance

### Core

- `core/code-quality.md` — code quality, readability, structure, and maintainability
- `core/security.md` — security, sensitive data handling, and safe defaults

### Python

- `python/general.md` — Python project structure, style, and general practices
- `python/testing.md` — Python testing strategy and pytest conventions
- `python/typing.md` — Python typing conventions and type-hinting guidance

### FastAPI

- `fastapi/general.md` — API design, application structure, validation, and testing guidance

### Go

- `go/general.md` — package design, idioms, concurrency, and testing guidance

## How to use this repository

1. Start with the `core` guidance for baseline standards.
2. Apply the language package that matches the code you are writing.
3. If you are working in FastAPI, follow both the Python and FastAPI guidance.
4. Use the manifests to understand package versioning and dependencies.

## Contributing

- Keep guidance practical, concise, and easy to apply in reviews.
- Prefer adding or refining focused documents instead of making a single file too broad.
- Update the relevant package `manifest.yaml` if package metadata or dependencies change.

## Notes

- The repository currently uses `mainifest.yaml` at the root as the package registry.
- Package names and versions are intentionally simple so the structure can evolve over time.

