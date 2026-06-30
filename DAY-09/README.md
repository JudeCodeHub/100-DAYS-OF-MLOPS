# Day 09 - Custom ML Project Template with Cookiecutter

## Objective

Design and fix a Cookiecutter-based ML project template that can generate standardized machine learning project structures with dynamic dependencies and metadata.

## Tasks Completed

- Reviewed and corrected the Cookiecutter template structure
- Fixed `cookiecutter.json` to properly define project variables
- Implemented Jinja-based conditional logic in `requirements.txt`
- Fixed dynamic templating in `README.md`
- Ensured template supports multiple ML frameworks:
  - scikit-learn
  - pytorch
  - tensorflow
- Validated required directory structure for generated projects
- Successfully generated a working ML project using Cookiecutter

## Template Features Implemented

- Dynamic project name injection
- Dynamic author injection
- Python version configuration
- ML framework-based dependency selection
- Standard ML project structure:
  - data/
  - models/
  - src/
  - tests/

## Commands Used

```bash
cd /root/code/mlops-template/

cookiecutter /root/code/mlops-template/ -o /root/code/ --no-input project_name=churn-model ml_framework=sklearn
