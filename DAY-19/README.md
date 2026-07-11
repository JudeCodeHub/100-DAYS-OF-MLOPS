# Day 19 - Complete a Production DVC Pipeline

## Objective

Complete an end-to-end DVC pipeline by fixing an existing stage, adding model training and evaluation stages, reproducing the pipeline, pushing artifacts to remote storage, and creating a versioned production release.

## Tasks Completed

- Fixed the misconfigured `preprocess` stage in `dvc.yaml`
- Added the `train` stage with parameter tracking from `params.yaml`
- Configured the `train` stage to generate `model.pkl`, `test_split.csv`, and `metrics.json`
- Added the `evaluate` stage to generate `evaluation.json`
- Declared `metrics.json` and `evaluation.json` with `cache: false`
- Executed the complete pipeline using `dvc repro`
- Pushed DVC-tracked artifacts to the SeaweedFS remote using `dvc push`
- Committed all pipeline changes to Git
- Tagged the completed pipeline release as `v1.0`

## Commands Used

```bash
cd /root/code/ml-pipeline

cp scripts-staging/train.py scripts/
cp scripts-staging/evaluate.py scripts/

dvc repro

dvc push

git add .
git commit -m "Complete DVC production pipeline"

git tag v1.0
```

## What I Learned

- How to build a complete multi-stage DVC pipeline
- How to add training and evaluation stages to an existing pipeline
- How to track hyperparameters using `params.yaml`
- How to record metrics and evaluation reports as Git-tracked outputs with `cache: false`
- How to push DVC artifacts to remote object storage
- How Git tags can be used to mark production-ready ML pipeline releases
