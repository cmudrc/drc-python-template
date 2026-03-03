# drc-python-template

`drc-python-template` is a compact starter for typed Python
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
├── AGENTS.md
├── CONTRIBUTING.md
├── LICENSE
├── Makefile
├── README.md
├── docs
│   ├── api.rst
│   ├── conf.py
│   ├── dependencies_and_extras.rst
│   ├── drc.png
│   ├── index.rst
│   └── quickstart.rst
├── examples
│   ├── README.md
│   └── basic_usage.py
├── pyproject.toml
├── scripts
│   ├── check_coverage_thresholds.py
│   ├── check_docs_consistency.py
│   └── check_google_docstrings.py
├── src
│   ├── design_research_python_template
│   └── drc_python_template
├── tests
│   ├── test_core.py
│   └── test_public_api.py
└── uv.lock
```

- `.github/workflows/` contains the GitHub Actions definitions for CI and docs publishing.
- `docs/` contains the Sphinx source files for the package documentation.
- `examples/` contains small runnable scripts that demonstrate the public API.
- `scripts/` contains repository maintenance and validation helpers used by `make`.
- `src/drc_python_template/` contains the installable Python package code.
- `tests/` contains the pytest suite that protects the public behavior.
- `.gitignore` defines which local caches, virtualenvs, and build outputs stay untracked.
- `.pre-commit-config.yaml` provides an optional pre-commit hook that runs the local CI gate.
- `.python-version` pins the preferred reproducible Python interpreter version.
- `AGENTS.md` documents repository-specific guidance for coding agents and contributors.
- `CONTRIBUTING.md` documents the human contributor workflow and quality checks.
- `LICENSE` contains the repository's software license.
- `Makefile` provides the standard local commands for setup, linting, testing, docs, and releases.
- `README.md` is the top-level overview and quickstart guide for the repository.
- `pyproject.toml` defines package metadata, dependencies, and tool configuration.
- `uv.lock` pins the reproducible dependency graph used by `make repro`.

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
