---
aliases:
    - KL-divergence
---

# KL-divergence

A distance measure for how far a proposed probability distribution $Q$ is from the true probability distribution $P$.

Mathematically it is defined as:

$$
D_{KL}(P||Q) = \sum_{x \in X}P(x)\log\left(\frac{P(x)}{Q(x)}\right)
$$

A simple interpretation is that the distance measures the expected excess surprise from using $Q$ as a model when the true distribution is $P$

Always a non-negative real number, and equal to zero if (and only if) both $P$ and $Q$ are identical. It is not technically a distance (metric) as it does not satisfy the [[triangle inequality]], rather it is a divergence