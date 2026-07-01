# Day 11 - Track Datasets with DVC

## Objective

Move a dataset from Git tracking to DVC, ensuring that large data files are versioned with DVC instead of Git.

## Tasks Completed

- Removed the dataset from Git tracking without deleting it from the local system
- Tracked the dataset using DVC
- Generated the `.dvc` pointer file for the dataset
- Generated `data/raw/.gitignore` to prevent Git from tracking the dataset
- Staged the DVC-generated files
- Committed the changes with the message `Track transactions dataset with DVC`

## Commands Used

```bash
cd /root/code/fraud-detection/

git rm --cached data/raw/transactions.csv

dvc add data/raw/transactions.csv

git add .

git commit -m "Track transactions dataset with DVC"