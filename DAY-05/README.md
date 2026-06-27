# Day 05 - ML Pipeline Automation with Makefile

## Objective

Fix and standardize a broken Makefile to automate the full ML workflow including setup, data processing, training, testing, and cleanup.

## Tasks Completed

- Fixed Makefile indentation issue (TAB instead of spaces)
- Corrected pipeline execution order
- Added missing `data` step into full pipeline
- Added `.PHONY` to prevent file/target conflicts
- Implemented full automation using `make all`

## Makefile Pipeline Stages

- setup → creates virtual environment and installs dependencies  
- data → runs data preprocessing  
- train → trains the ML model  
- test → runs unit tests  
- clean → removes cache and generated files  
- all → runs full pipeline in correct order  

## Command Used

```bash
cd /root/code/fraud-detection/
make all
