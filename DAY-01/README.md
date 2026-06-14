# Day 01 - Python Environment Setup for ML

## Objective

Set up a Python virtual environment and install essential machine learning libraries.

## Tasks Completed

- Created a virtual environment named `ml-env`
- Activated the virtual environment
- Installed:
  - numpy
  - pandas
  - scikit-learn
  - matplotlib
- Generated a `requirements.txt` file using `pip freeze`

## Commands Used

```bash
python3 -m venv /root/code/ml-env
source /root/code/ml-env/bin/activate
pip install numpy pandas scikit-learn matplotlib
pip freeze > /root/code/requirements.txt
```

## What I Learned

- Creating Python virtual environments with `venv`
- Managing dependencies with `pip`
- Generating reproducible environments using `requirements.txt`
