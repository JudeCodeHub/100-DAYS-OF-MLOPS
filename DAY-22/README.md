# Day 22 - Register MLflow Experiments for Team Projects

## Objective

Create two separate MLflow experiments for new ML projects and tag each one with the correct owning team.

## Tasks Completed

- Opened the MLflow UI for the running tracking server on port `5000`
- Registered a new experiment named `fraud-detection`
- Added a non-empty experiment description for `fraud-detection`
- Tagged `fraud-detection` with `team=ml-platform`
- Registered a new experiment named `churn-prediction`
- Tagged `churn-prediction` with `team=analytics`
- Verified both experiments appear in the MLflow UI experiment list
- Confirmed the experiment descriptions and tags are visible on each experiment page

## MLflow Experiment Details

### fraud-detection

- Description: Fraud detection project for monitoring suspicious activity and model performance.
- Tag:
 	- `team = ml-platform`

### churn-prediction

- Description: Churn prediction project for identifying customers at risk of leaving.
- Tag:
 	- `team = analytics`

## Verification

Both experiments were created separately from the Default experiment and the seeded `legacy-models` experiment was left unchanged.
