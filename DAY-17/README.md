# Day 17 - Track and Compare ML Experiments with DVC

## Objective

Use DVC Experiments to run multiple model training configurations, compare their performance, and apply the best-performing experiment to the workspace.

## Tasks Completed

- Executed three DVC experiments with different `max_depth` values
- Trained the model for each experiment without modifying the pipeline code
- Compared experiment results using `dvc exp show`
- Identified the experiment with the highest `f1_score`
- Applied the best-performing experiment to the workspace

## Commands Used

```bash
dvc exp run -S max_depth=2
dvc exp run -S max_depth=6
dvc exp run -S max_depth=12

dvc exp show

dvc exp apply genic-pees
```

> Note: In this task, the workspace was already updated with the best experiment after running it, so `dvc exp apply` was optional.

## What I Learned

- How to run parameterized ML experiments using DVC Experiments
- How to compare multiple experiment runs using `dvc exp show`
- How to evaluate models using metrics such as `accuracy` and `f1_score`
- How to identify and promote the best-performing experiment to the workspace
- How DVC simplifies experiment tracking without creating multiple Git commits
