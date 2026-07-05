# Day 14 - Build a Reproducible DVC Pipeline

## Objective

Create a two-stage DVC pipeline to automate data processing and dataset splitting, ensuring reproducibility using `dvc repro`.

## Tasks Completed

- Defined a DVC pipeline using two stages:
  - `process_data` for cleaning raw transaction data
  - `split_data` for generating train/test datasets
- Configured dependencies and outputs for each stage
- Established proper stage chaining using DVC dependency tracking
- Executed the full pipeline using `dvc repro`
- Generated `dvc.lock` for reproducibility
- Verified pipeline structure using `dvc dag`

## Pipeline Stages

### 1. process_data

- Input:
  - `data/raw/transactions.csv`
  - `src/data/process_data.py`
- Output:
  - `data/processed/clean_transactions.csv`

### 2. split_data

- Input:
  - `data/processed/clean_transactions.csv`
  - `src/data/split_data.py`
- Output:
  - `data/processed/train.csv`
  - `data/processed/test.csv`

## Commands Used

```bash
cd /root/code/fraud-detection/

dvc stage add -n process_data \
  -d data/raw/transactions.csv \
  -d src/data/process_data.py \
  -o data/processed/clean_transactions.csv \
  python3 src/data/process_data.py

dvc stage add -n split_data \
  -d data/processed/clean_transactions.csv \
  -d src/data/split_data.py \
  -o data/processed/train.csv \
  -o data/processed/test.csv \
  python3 src/data/split_data.py

dvc repro
dvc dag
dvc status
