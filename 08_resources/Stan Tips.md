# Tips for using stan

## Phi and normal

Phi is a shortcut for the standard normal in stan (mean 0, sd 1). There also exists a `Phi_approx` that is faster for a subset of values. Phi runs the [[cumulative distribution function]] for the normal distribution. That is for a given value x it returns the probability that a value drawn from the distribution (X) is less than or equal to x.