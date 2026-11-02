# Development

## Prerequisites

- [uv](https://docs.astral.sh/uv/) installed
- Python >= 3.10 (see `.python-version` for the pinned version)

## Setup

```bash
uv sync
```

This creates `.venv` and installs the dependencies from `pyproject.toml` / `uv.lock`.

## Run

```bash
uv run langchain-course
```

Expected output: `Hello from langchain-course!`

Alternatives:

```bash
uv run python -c "from langchain_course import main; main()"

# or with the venv activated
source .venv/bin/activate
langchain-course
```

## Dependencies

```bash
uv add <package>       # add a dependency
uv remove <package>    # remove a dependency
uv lock --upgrade      # upgrade locked versions
```

## Project layout

```
pyproject.toml                 # project metadata, dependencies, entry point
src/langchain_course/          # package source
  __init__.py                  # main() entry point
```

The `langchain-course` command is defined under `[project.scripts]` in `pyproject.toml` and points to `main()` in `src/langchain_course/__init__.py`.
