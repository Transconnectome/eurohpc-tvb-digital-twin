# GPU Hour Justification

## Purpose
This document provides the computational rationale for requesting approximately 1,000,000 GPU-hours for EuroHPC access.

## Scientific Workload
The project performs large-scale personalized whole-brain simulations using The Virtual Brain (TVB) framework. Each model is parameterized by subject-specific structural connectivity and fitted or evaluated against empirical neural and behavioral data.

## Workload Decomposition
The total workload can be decomposed as:

```text
Total GPU-hours = N_subjects × N_parameter_sets × GPU_hours_per_simulation
```

A representative target allocation is:

```text
N_subjects = 1,000
N_parameter_sets = 500
GPU_hours_per_simulation = 2
Total = 1,000 × 500 × 2 = 1,000,000 GPU-hours
```

## Parallelization Strategy
The workload is highly parallelizable at multiple levels:

1. Subject-level parallelism
2. Parameter-set parallelism
3. GPU acceleration within simulation and inference kernels
4. Independent replicate simulations for uncertainty estimation

This makes the workload suitable for large GPU partitions on EuroHPC systems.

## Why EuroHPC Is Required
Conventional institutional clusters are insufficient because the scientific objective requires simultaneous exploration of subject-level variability, high-dimensional model parameters, and uncertainty estimates at population scale.

EuroHPC resources are required to:

- Reduce wall-clock time from months to days or weeks
- Enable population-scale personalized simulations
- Support large-scale Bayesian or machine-learning-based inference
- Generate reproducible scaling evidence for future extreme-scale access

## Benchmark Targets
Initial scaling tests will evaluate:

- 1 GPU
- 8 GPUs
- 32 GPUs
- 128 GPUs

Metrics:

- Runtime per simulation
- GPU utilization
- Memory footprint
- Throughput per GPU
- Strong scaling efficiency
- Weak scaling efficiency

## Allocation Strategy
The requested 1M GPU-hours should be treated as a production-scale Regular Access target after preliminary Benchmark or Development Access has established feasibility and scaling behavior.
