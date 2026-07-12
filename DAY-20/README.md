# Day 16 - Set Up MLflow Tracking Server

## Objective

Configure and launch a local MLflow Tracking Server for experiment tracking using a SQLite backend store and artifact storage.

## Tasks Completed

- Configured MLflow with a SQLite backend database for storing experiment metadata
- Configured artifact storage location for MLflow model files and outputs
- Launched MLflow Tracking Server with external access support on port `5000`
- Verified the server status and accessed the Default experiment through MLflow UI

## MLflow Server Configuration

### Backend Store and Artifact Storage

Configured MLflow to use:

- Backend Store:
  - `/root/code/mlflow-backend/mlflow.db`

- Artifact Root:
  - `/root/code/mlflow-artifacts/`

The backend store manages experiment details, runs, parameters, and metrics, while artifact storage keeps models and other output files.

## Server Setup

Started MLflow server using:

```bash
nohup mlflow server \
--backend-store-uri sqlite:////root/code/mlflow-backend/mlflow.db \
--default-artifact-root /root/code/mlflow-artifacts \
--host 0.0.0.0 \
--port 5000 \
--allowed-hosts "*" \
--cors-allowed-origins "*" \
> /root/code/mlflow.log 2>&1 &
