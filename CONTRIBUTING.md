# Contributing to Mycelium

Thanks for your interest in contributing to Mycelium! This document covers the guidelines for contributing to any repository in the mycelium-io organization.

## Getting Started

1. Fork the repository
2. Clone your fork locally
3. Create a feature branch from `main`
4. Make your changes
5. Run tests and linting
6. Submit a pull request

## Development Setup

```bash
cd fastapi-backend
uv sync --group dev
```

## Running Tests

```bash
# Unit tests (SQLite, no external dependencies)
uv run pytest tests/

# Integration tests (requires AgensGraph)
DATABASE_URL=... uv run pytest tests/
```

## Code Style

- Python 3.12+
- Format with `ruff format`
- Lint with `ruff check`
- Type hints are expected for public APIs

## Pull Requests

- Keep PRs focused — one feature or fix per PR
- Write descriptive commit messages
- Add tests for new functionality
- Update documentation if behavior changes
- Ensure CI passes before requesting review

## Issues

- Use the issue templates when available
- Search existing issues before opening a new one
- Include reproduction steps for bugs
- Be specific about expected vs actual behavior

## Architecture Decisions

For significant changes to architecture or new features, open an issue for discussion before writing code. This helps align on approach and avoids wasted effort.

## License

By contributing, you agree that your contributions will be licensed under the MIT License.
