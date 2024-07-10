## Undirected Network Models

Gaussian graphical model

From a multivariate normal $\mu$ and $\sigma$ you can get partial correlations from the precision matrix $K = \sigma^{-1}$

$$
pcor(i, j) = - \frac{K_{ij}}{\sqrt{K_{ii}} * \sqrt{K_{jj}}}
$$