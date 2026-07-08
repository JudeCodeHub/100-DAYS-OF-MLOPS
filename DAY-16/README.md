# Day 16 - Track Model Metrics Using DVC

## Objective

Configure DVC to recognize model evaluation metrics and enable metric tracking using `dvc metrics show` and `dvc metrics diff`.

## Tasks Completed

- Updated the DVC pipeline to track `metrics.json` as a DVC metric output
- Configured `metrics.json` with `cache: false` to keep metrics in Git for version comparison
- Updated the `train` stage to separate model artifacts and metric tracking
- Re-ran the complete pipeline using `dvc repro`
- Verified model performance metrics using `dvc metrics show`
- Enabled metric comparison across Git commits using `dvc metrics diff`

## Pipeline Stage Update

### train

- Input:
  - `data/processed/train.csv`
  - `src/models/train.py`

- Output:
  - `models/model.pkl`

- Metrics:
  - `metrics.json`

Example:

```yaml
train:
  cmd: python3 src/models/train.py
  deps:
    - data/processed/train.csv
    - src/models/train.py
  outs:
    - models/model.pkl
  metrics:
    - metrics.json:
        cache: false
```

## Metrics Tracking

The training stage generates:

```json
{
  "accuracy": 0.xx,
  "f1_score": 0.xx
}
```

DVC now recognizes these values as model evaluation metrics.

## Commands Used

```bash
cd /root/code/fraud-detection/

dvc repro

dvc metrics show

dvc metrics diff

dvc status
```

## Key Learnings

- DVC metrics allow tracking model performance over time
- Metrics should be declared using the `metrics` section in `dvc.yaml`
- `cache: false` keeps metric files in Git instead of DVC cache
- `dvc metrics diff` helps compare model improvements between experiments
- Combining Git and DVC provides reproducible ML experiment tracking
