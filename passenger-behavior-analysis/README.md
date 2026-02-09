# Passenger Behavior Analysis – Large-Scale Data Science Pipeline

This project presents an end-to-end **data science pipeline** developed to analyze
and classify passenger behavior from **large-scale telemetry data**.

The pipeline was designed with a strong emphasis on **scalability, parallel processing,
and performance optimization**, and is implemented in both CPU-parallel and
GPU-accelerated variants.

---

## Project Overview

The goal of this project is to process and analyze high-volume data in order to
extract meaningful behavioral patterns at scale.

Key objectives include:
- Cleaning and preprocessing multi-gigabyte raw data
- Applying custom logic to classify passenger behavior
- Performing spatial and temporal filtering
- Aggregating time-based metrics per user
- Producing analytical summaries and visualizations

The same core logic is executed using different computational backends to
highlight performance trade-offs.

---

## Notebooks

### 1. CPU Parallel Pipeline
**`cpu_parallel_pipeline.ipynb`**

- Full data preprocessing and aggregation pipeline
- CPU-based parallel execution using **Dask**
- Baseline implementation for large-scale processing
- Focuses on correctness, scalability, and reproducibility

---

### 2. GPU-Accelerated Pipeline
**`gpu_accelerated_pipeline.ipynb`**

- GPU-powered implementation of the core pipeline
- Uses **NVIDIA RAPIDS** libraries (cuDF, cuSpatial, CuPy)
- Refactors critical operations to be GPU-friendly
- Achieves significant speedup compared to the CPU pipeline

---

### 3. Data Processing & Visualization
**`data_processing_and_visualization.ipynb`**

- Aggregation and post-processing of pipeline outputs
- Creation of analytical plots and summaries
- Visualization of passenger behavior patterns
- CPU vs GPU output comparison

---

## Technologies Used

- Python
- Dask (CPU-based parallel processing)
- NVIDIA RAPIDS (cuDF, cuSpatial, CuPy)
- Pandas, NumPy
- Matplotlib

---

## Performance Perspective

This project demonstrates how the same data science workflow can be
significantly accelerated by selecting appropriate computation models.

By transitioning from CPU-parallel execution to GPU-accelerated processing,
the pipeline achieves **substantial reductions in execution time** while
preserving analytical correctness.

---

## Notes on Data and Privacy

All datasets, identifiers, and domain-specific details have been anonymized.
The focus of this repository is on **transferable data science and data engineering
techniques**, not on proprietary data or systems.
