# Scaling Plan

## Objective
Demonstrate scalability of TVB-based simulations and inference pipelines on GPU-based HPC systems.

## Experiments

### Strong Scaling
- Fixed workload
- Increase number of GPUs
- Measure runtime reduction and efficiency

### Weak Scaling
- Increase workload proportionally with GPU count
- Measure time stability and throughput

## Test Configurations
- 1 GPU
- 8 GPUs
- 32 GPUs
- 128 GPUs

## Metrics
- Runtime
- Speedup
- Efficiency
- GPU utilization
- Memory usage

## Expected Outcome
- Near-linear scaling for embarrassingly parallel components
- Identification of bottlenecks (communication vs compute)
- Quantitative evidence for EuroHPC proposal
