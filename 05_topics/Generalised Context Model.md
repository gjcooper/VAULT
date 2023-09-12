---
aliases:
    - GCM
---

# The Generalised Context Model

This model was developed by Nosofsky, and is outlined in detail in [[nosofsky2011generalized|The generalized context model: an exemplar model of classification]].

The rough summary of this approach is that memory for objects is done in relation to exemplars in each category of object type.

The distance between two objects is given by:
$$
d_{ij} = \left[\sum_{m=1}^Mw_m|x_{im} - x_{jm}|^r\right]^{1/r}
$$
The similarity then between  $i$ and $j$ then is

$$
s_{ij} = e^{-cd_{ij}^p}
$$

And finally the probability that an item $i$ is classified into the category $J$ is

$$
P(J|i) = \dfrac{b_\mathfrak{J}\left[\sum_{j=1}^nV_{jJ}s_{ij}\right]^\gamma}
{\sum_{K=1}^{K_N}b_K\left[\sum_{k=1}^nV_{kK}s_{ik}\right]^\gamma}
$$
