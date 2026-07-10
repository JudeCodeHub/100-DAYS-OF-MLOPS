# Day 18 - Version Datasets and Models with Git Branches and DVC

## Objective

Use Git branches and DVC to manage multiple versions of datasets and trained models, allowing easy switching between project versions while maintaining reproducibility.

## Tasks Completed

- Tagged the current project state as `v1.0`
- Created a new Git branch named `v2-improved`
- Updated the tracked dataset with the improved dataset version
- Re-tracked the dataset using DVC
- Re-ran the DVC pipeline to regenerate processed data and retrain the model
- Committed the updated dataset and model on the `v2-improved` branch
- Switched back to the `main` branch and restored the original dataset and model using DVC

## Commands Used

```bash
git tag v1.0

git checkout -b v2-improved

cp data/raw/transactions_v2.csv data/raw/transactions.csv

dvc add data/raw/transactions.csv

dvc repro

git add .
git commit -m "Update dataset to v2 and retrain model"

git checkout main

dvc checkout

dvc status
```

## What I Learned

- How Git branches can manage different versions of an ML project
- How DVC tracks datasets independently from Git
- How retraining a model creates a version tied to a specific dataset
- How to restore previous datasets and models by switching Git branches and using DVC
- How Git and DVC work together to provide reproducible ML workflows
