# DBSCAN Clustering from Scratch (PyTorch)

This repository contains a custom implementation of the **DBSCAN (Density-Based Spatial Clustering of Applications with Noise)** algorithm using **PyTorch**. The goal is to demonstrate how DBSCAN can be implemented without relying on high-level clustering libraries, giving insight into how the algorithm works internally.

## Features

- Full DBSCAN implementation using **tensor operations**
- Supports **Euclidean distance**
- Includes **noise detection** and **cluster expansion**
- Synthetic dataset generation with `sklearn.datasets.make_blobs`
- Visualization of clustering results using `matplotlib`

## Background

DBSCAN is a density-based clustering algorithm that groups together points that are closely packed while marking as outliers the points that lie alone in low-density regions.

It requires two parameters:
- `eps`: radius of neighborhood around a point
- `minPts`: minimum number of points required to form a dense region

## Implementation Details

- **Distance Function**: Computes pairwise Euclidean distances using vectorized PyTorch.
- **Neighbor Retrieval**: For each point, retrieve neighbors within `eps`.
- **Clustering Logic**: Core algorithm to assign clusters or noise labels based on density criteria.

## Visualization

The notebook visualizes clustered data using `matplotlib`. Data is generated with blobs and injected with uniform noise.

> To see the result, check the final plot in the notebook or export it using:
> ```python
> plt.savefig("dbscan_clusters.png")
> ```


