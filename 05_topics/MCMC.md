---
aliases:
    - Markov Chain Monte Carlo
---


There are many different variants of MCMC, with slightly different properties for each. One addition to this landscape is our addition, the [[PMwG|Particle Metropolis within Gibbs]] package I helped to create during my time at the University of Newcastle.

A property of a successfully implemented model with MCMC is the guarantee that is will converge to the true estimate given enough time. This **enough time** though leaves a lot of room for incorrect estimates, especially given compute time constraints in real life.

One discussion I have recently read in this regard is about [[biased inferences]], in a blog by [[Michael Betancourt]] (available at [his blog](https://betanalpha.github.io/assets/case_studies/divergences_and_bias.html#3_a_non-centered_eight_schools_implementation))