# Day 15 - Parameter-Driven DVC Retraining

## Objective

Integrate `n_estimators` into the DVC pipeline so the train stage is re-executed when the parameter changes, demonstrating parameter-driven reproducibility.

## Tasks Completed

- Added a `params` declaration for `n_estimators` in the `train` stage of `dvc.yaml`
- Confirmed that `src/models/train.py` reads `n_estimators` from `params.yaml`
- Ran the full pipeline with `dvc repro`
- Updated `n_estimators` from `100` to a different value and ran `dvc repro` again
- Verified that only the `train` stage re-executed after the parameter change
- Confirmed that the updated value was recorded in `dvc.lock`
- Regenerated `models/model.pkl` from the new parameter value
- Noted that `dvc params diff` can be used to compare tracked parameter changes across commits

## Parameter Tracking

- Tracked parameter:
  - `n_estimators`
- Pipeline effect:
  - Changing the tracked parameter invalidates the `train` stage cache and triggers retraining

## Commands Used

```bash
cd /root/code/fraud-detection/

dvc repro

# Update params.yaml: n_estimators: 100 -> 200

dvc repro

dvc params diff
```
