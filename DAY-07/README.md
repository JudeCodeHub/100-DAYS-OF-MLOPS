# Day 07 - Python Packaging with pyproject.toml and Wheel Distribution

## Objective

Convert the fraud detection ML project into a properly packaged Python distribution that can be built and installed as a reusable library using `setuptools` and `wheel`.

## Tasks Completed

- Reviewed and corrected `pyproject.toml`
- Fixed project metadata to match packaging standards
- Ensured package name matches module structure (`fraud_detection`)
- Updated versioning to `0.1.0`
- Set Python requirement to `>=3.10`
- Added required dependencies (`scikit-learn`, `pandas`, `numpy`)
- Configured setuptools to find packages under `src/`
- Added proper `[build-system]` configuration for wheel building

## pyproject.toml Fixes

- Added build system configuration:
  - setuptools >= 61.0
  - wheel support enabled
- Standardized project metadata for packaging compliance
- Ensured correct source directory mapping

## Commands Used

```bash
cd /root/code/fraud-detection
python3 -m build
