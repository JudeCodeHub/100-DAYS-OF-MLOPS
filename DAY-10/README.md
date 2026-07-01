# Day 10 - Initialize Data Version Control (DVC)

## Objective

Initialize DVC (Data Version Control) in an existing Git repository to enable version control for datasets and machine learning artifacts independently of the source code.

## Tasks Completed

- Initialized DVC in the existing Git repository
- Generated the standard DVC configuration files
- Created the `.dvc/` control directory
- Created the `.dvcignore` file
- Staged all DVC-generated files in Git
- Committed the initialization with the message `Initialize DVC`

## Commands Used

```bash
cd /root/code/fraud-detection/

dvc init

git add .

git commit -m "Initialize DVC"