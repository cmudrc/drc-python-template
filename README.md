# design-research-python-template

`design-research-python-template` is a compact starter for typed Python
libraries. It borrows the shared project shape from
`design-research-agents` and `design-research-problems`, but keeps the initial
surface area small enough to customize quickly.

## Overview

This template includes:

- A `src/` layout package with a small public API and type marker
- `pyproject.toml` settings for packaging, Ruff, mypy, and pytest
- A `Makefile` with common development, docs, coverage, and release targets
- Basic Sphinx docs, a runnable example, and GitHub Actions workflows
- Contributor guidance in `AGENTS.md` and `CONTRIBUTING.md`

## Quickstart

Requires Python 3.12+.

```bash
python -m venv .venv
source .venv/bin/activate
make dev
make test
make run-example
```

For a frozen local environment, `make dev` installs `uv`, so you can generate
and use `uv.lock` immediately:

```bash
make lock
make repro
```

## Repository Shape

```text
.
|- .github/workflows/
|- docs/
|- examples/
|- scripts/
|- src/design_research_python_template/
|- tests/
|- AGENTS.md
|- CONTRIBUTING.md
|- Makefile
`- pyproject.toml
```

## Customizing The Template

Before using this as a real package, update:

- Project metadata in `pyproject.toml`
- Package and import names under `src/`
- The README, docs, and example script
- CI workflow names, deploy settings, and repository URLs

## Docs

Build the docs locally with:

```bash
make docs
```

The generated HTML output is written to `docs/_build/html/`.

## Contributing

See `CONTRIBUTING.md` for the local development workflow and contribution
expectations.
