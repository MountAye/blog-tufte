---
layout:      post
title:      ".mpipks-note | 10. Dimension Reduction"
keywords:   "mpipks-note"
excerpt:    "对高维数据的降维打击"
date:        2021-05-15
categories:  post
milestoneID: 40
---

> 第十讲是由校外邀请来的嘉宾来讲数据降维，所以课程网站上没有课件。时间轴和语音转录相对来说不那么有意义了。所以在听课的过程中做了如下笔记。

## Contents

- High dimensinoal data
- Dimensionality Reduction Methods
- Clustering (a discrete form of reduction)

## High Dimensional Data

data matrix X:n*m. 

n samples as rows, m columns as observables

How to visualize?
- m=1: list
- m=2: x-y plot

__Aim of dimension reduction: reduce the number of observables, while keeping relevant information.__

### Examples

Ferromagnetic Ising model of a 28*28 lattice, 50,000 samples. The 1st principal component scales with the magnetization. 

500,000 DNA sites of 3,000 humans. Projections onto the first 2 principal components givees a rough map of Europe

Fashion MNIST: 60,000 pictures of 784 (28*28) pixels. UMAP projections onto 2 dimensions 

## Linear dimension reduction

- Principal component analysis
- Non-negative matrix factorization
- Independent component analysis
- Factor analysis

### Principal component analysis

change of basis

__Aim:__ to find a transformation such that
- the components are uncorrelated
- ordered by the explained variability

__Math__:

$$ X^T X $$ is a $$m \times m$$ matrix. Eigen-decomposition gives $$(\lambda,W) $$ where $$W$$'s columns are eigen vectors sorted by $$\lambda$$

$$ T = X \cdot W $$ where  $$T$$ is the score onto principal components, and $$T^TT$$ is diagonal

$$ T_r = X \cdot W_r $$ where $$W_r$$ is a n*r matrix of the first r components

__Practice In `R`__: 

- Iris Dataset
- Pitures of Objects at Different Angles: 
- Swiss Roll: the transformed data almost have the same structure as the original data. This shows the limit of PCA due to linearity

[wikipedia - Nonlinear_dimensionality_reduction]()

### UMAP: uniform manifold approximation

__Assumptions__:
- uniformed distributeed on Riemann manifold
- Riemann metric is locally constant
- The manifold is locally conncected

__Results__:
- models the manifold with a fuzzy topological structure
- finds low dimensional projection of the data that has the cloest possible equivalent fuzzy topological structure 

__Simplex__
0-simplex: dot
1-simplex: line
2-simplex: triangle
3-simplex: 正四面体

__Problem__:

When the uniform distribution is not met, the result may not be what we like. To circumvent this, we need to define the local metric with the nearest neighbours.

__Finding a low dimensional representation__
- derive similar fuzzy topological representation of a low dimensional representation
- interpret edge weight s as proba
- minimize cross entropy
- [pair-code.github.io/understand_umap](pair-code.github.com/understand_umap)

__Practice in `R`__
- Swiss Roll becomes a 2-d ring
- Pictures at different angles are well seperated

## Clustering

### hierarchiral clustering
- metric
- linkage criterion / distance between clusters

### centroid base clustering (k-means)
- pre-specify number of clusters, k
- partition the data such that the squared distance to cluster mean position is minimal
- Lloyd algorithm
    - start with random centers
    - assign data to neatest center
    - compute new centers

### graph based-clustering
- graph representation of data
- partition the data such that modularity Q is optimized
- $$ Q = \sum_{i=1}^c e_{ii}-\gamma {a_i}^2, a_i = \sum_{j-1}^c e_{ij} $$.
    - $$ e_{ij} $$: fraction of links between cluster i and j
    - $$ \gamma $$: resulution

## Summary

Question: How to identify order in high-dimensinoal data?
- dimensionality reductuon to visualize high-dimensional data and to identify macroscopic observables
- clustering to identify discrete order in high dimensional data
- methods to se depending on the problem at hand
