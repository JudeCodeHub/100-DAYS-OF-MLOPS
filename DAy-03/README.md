# Day 03 - Reproducible Dependencies with uv and Lockfiles

## Objective

Audit and correct the dependency specification, then generate a fully pinned lockfile using `uv` so the environment can be reproduced consistently.

## Tasks Completed

- Audited the `requirements.in` file and corrected the dependency specification
- Verified the required package names and version constraints
- Kept only the necessary top-level dependencies in the input file
- Navigated to the project directory
- Compiled the dependency specification into a pinned `requirements.txt` lockfile using `uv`

## Commands Used

```bash
cd /root/code/fraud-detection/
uv pip compile requirements.in -o requirements.txt
```

## What I Learned

- How to use `uv` to manage Python dependencies
- The difference between direct dependencies and transitive dependencies
- How to generate reproducible environments with pinned package versions
- How lockfiles help prevent dependency drift across deployments
