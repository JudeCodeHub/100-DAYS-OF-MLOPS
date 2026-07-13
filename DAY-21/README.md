# Day 21 - Log Training Runs Using MLflow

## Objective

Record a machine learning training run using MLflow tracking server by logging parameters, metrics, and model artifacts.

## Tasks Completed

- Configured MLflow tracking URI to connect with the tracking server
- Logged model hyperparameters using `mlflow.log_params`
- Logged evaluation metrics using `mlflow.log_metric`
- Saved the trained sklearn model as an MLflow artifact
- Created a new run in the Default MLflow experiment
- Verified parameters, metrics, and artifacts through MLflow UI

## MLflow Run Details

Experiment:
- Default

Logged Parameters:
- n_estimators = 100
- max_depth = 5
- random_state = 42

Logged Metrics:
- accuracy = 0.75
- f1_score = 0.8571428571428571

## Commands Used

```bash
python3 /root/code/log_experiment.py