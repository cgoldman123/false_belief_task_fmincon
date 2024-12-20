# README

## **Note: This repository is currently under development.**  
**Do not use this code in its current state. Features and functionality are incomplete and subject to change.**

---

## Model Fitting for Theory of Mind (False Belief) Task

This repository contains MATLAB and Python scripts for modeling, fitting, and analyzing **False Belief Task (FBT)** data using advanced computational models. The scripts support parameter estimation, hierarchical modeling, and batch processing for subject-level and group-level analyses.

---

## Repository Files

### MATLAB Scripts

1. **`FBT_run_models.m`**  
   - Main script for model fitting across multiple configurations.  
   - Iterates over parameter settings (`alpha`, `beta`, `delta`, `lambda`) and outputs results in `.csv` and `.mat` formats.  
   - Includes visualization of model fit performance.

2. **`FBT_config.m`**  
   - Configuration script for FBT model fitting.  
   - Defines parameter bounds, priors, and input data paths.  
   - Supports both local and Prolific datasets.

3. **`FBT_llfun.m`**  
   - Model-specific likelihood function for agent-specific learning in FBT.  
   - Calculates posterior probabilities, subject beliefs, and predicted responses.  
   - Supports both Maximum Likelihood (ML) and Maximum a Posteriori (MAP) estimation.

4. **`emfit_CMG.m`**  
   - Expectation-Maximization (EM) fitting script for FBT models.  
   - Includes functionality for computing subject- and group-level parameter estimates, Bayesian model comparison, and plotting belief trajectories.

---

### Python Scripts

1. **`runall_FBT.py`**  
   - Automates batch fitting of FBT models using Slurm.  
   - Dynamically creates result directories and logs.  
   - Configures parallel processing across subjects.

---

### Usage

1. **MATLAB Workflow:**
   - Edit `FBT_config.m` to specify parameter bounds and data paths.  
   - Run `FBT_run_models.m` to fit models and visualize results.

2. **Batch Processing with Python:**
   - Modify `runall_FBT.py` to define subject lists and results directory.  
   - Execute to submit Slurm jobs for parallelized fitting.

---

### Dependencies

- **MATLAB:** Required for core model fitting and analysis.  
- **Python 3.x:** Used for job automation and directory management.  
- **Slurm:** Needed for high-performance batch processing.

---
