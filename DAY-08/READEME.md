# Day 08 - Code Quality Enforcement with Pre-Commit Hooks

## Objective

Set up and correct a pre-commit configuration to automatically enforce code quality checks before every Git commit using standardized hooks.

## Tasks Completed

- Reviewed and fixed `.pre-commit-config.yaml`
- Ensured all required hooks were configured:
  - trailing-whitespace
  - end-of-file-fixer
  - check-yaml
  - ruff (linting)
  - black (formatting)
- Corrected repository sources and hook IDs
- Added missing `rev` fields for all hook repositories
- Installed pre-commit hooks into the Git repository
- Executed hooks across all tracked files

## Hooks Configured

- **pre-commit-hooks**
  - trailing whitespace removal
  - end-of-file normalization
  - YAML validation

- **ruff**
  - Python linting and style checks

- **black**
  - Automatic Python code formatting

## Commands Used

```bash
cd /root/code/fraud-detection/

pre-commit install
pre-commit run --all-files
