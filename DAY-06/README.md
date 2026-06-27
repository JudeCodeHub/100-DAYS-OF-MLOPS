# Day 06 - Code Quality Enforcement with Ruff and Black

## Objective

Fix and standardize the project so it passes automated code quality checks using `ruff` and `black`, ensuring consistent formatting and linting across the ML codebase.

## Tasks Completed

- Reviewed existing `pyproject.toml` configuration
- Configured `ruff` lint rules to include:
  - E (pycodestyle errors)
  - F (pyflakes errors)
  - W (warnings)
  - I (import sorting)
- Set both `ruff` and `black` line length to 120
- Fixed formatting issues across `src/` using `black`
- Resolved linting issues detected by `ruff`
- Ensured consistent import ordering and code style compliance

## Configuration Changes

- Updated `pyproject.toml`:
  - Set `line-length = 120` for both `black` and `ruff`
  - Added proper `[tool.ruff.lint]` rule selection

## Commands Used

```bash
cd /root/code/fraud-detection/

ruff check src/
black --check src/
black src/
