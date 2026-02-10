---
aliases:
    - Akaike information criterion
---

# Akaike information criterion

An estimator of prediction error. If we predict behaviour from two separate models, then look at the relative difference in prediction errors we can see which model better predicts the data.

$$ 
\mathrm{AIC} = 2k - 2\log(\hat{L})
$$
- $k$ is the number of parameters
- $\hat{L}$ is the maximum likelihood of the model.

For a set of models the one with the **lowest** $\mathrm{AIC}$ should be deemed the better fit of model to data.