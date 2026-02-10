---
aliases:
    - LBA
---

# Linear Ballistic Accumulator

Work from [[Scott D. Brown]], [[Andrew Heathcote]], an evidence accumulation model that assumes drift rate variability, where each individual race is a drift sampled from a distribution of mean drift and standard deviation. Comparable in use to the [[diffusion decision model|drift diffusion model]], but analytically simpler.

Has been used in a range of applications, such as perceptual tasks, preferential tasks, risky gambles, memory and many more.

Used in my [[Architecture of MultiAttribute Choice]] work as the underlying framework on which the elementary decision processes are based on single attribute (or combined attribute) processing.

One benefit of the LBA model over the standard DDM is that it is relatively simple to set up a choice between > 2 options. The standard DDM assumes a single diffusion process from some starting value towards one of two boundaries. However the LBA treats this typical [[two-alternative forced choice|2AFC]] response type as a race between two accumulators, whichever accumulator reaches its specific threshold first becomes the response.

The means that 3+ response options are easily modelled with the addition of more accumulators (linked to those responses).