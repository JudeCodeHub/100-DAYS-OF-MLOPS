# Day 04 - Standardizing Project Structure

## Objective

Bring the ML project at `/root/code/fraud-detection/` in line with the team's project structure conventions, including correct directories, empty `__init__.py` files for Python packages, required dependencies, and a standard `README.md`.

## Tasks Completed

- Inspected the existing project layout at `/root/code/fraud-detection/`.
- Created missing directories (`data/raw`, `data/processed`, `models/`, `notebooks/`, `src/data/`, `src/features/`, `src/models/`, `src/utils/`, `tests/`, `configs/`).
- Created an empty `__init__.py` file in every subdirectory under `src/` so they are recognized as Python packages.
- Created `requirements.txt` listing `scikit-learn`, `pandas`, `numpy`, and `mlflow` (one per line).
- Updated the `README.md` file to begin with the heading `# fraud-detection`.
- Removed files and folders that did not match the required standard tree layout.

## Commands Used

```bash
cd /root/code/fraud-detection/

# Create the required directories
mkdir -p data/raw data/processed models notebooks src/data src/features src/models src/utils tests configs

# Create __init__.py files for Python packages
touch src/data/__init__.py src/features/__init__.py src/models/__init__.py src/utils/__init__.py

# Specify dependencies
echo -e "scikit-learn\npandas\nnumpy\nmlflow" > requirements.txt

# Initialize README.md
echo "# fraud-detection" > README.md
```

## What I Learned

- How to structure a standard Machine Learning project layout.
- The importance of `__init__.py` files for defining Python packages in Python.
- How to manage and list dependencies in `requirements.txt`.
- Ensuring consistency across team projects for easier collaboration and maintenance.
