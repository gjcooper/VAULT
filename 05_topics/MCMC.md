---
aliases:
    - Markov Chain Monte Carlo
---


There are many different variants of MCMC, with slightly different properties for each. One addition to this landscape is our addition, the [[PMwG|Particle Metropolis within Gibbs]] package I helped to create during my time at the University of Newcastle.

A property of a successfully implemented model with MCMC is the guarantee that is will converge to the true estimate given enough time. This **enough time** though leaves a lot of room for incorrect estimates, especially given compute time constraints in real life.

One discussion I have recently read in this regard is about [[biased inferences]], in a blog by [[Michael Betancourt]] (available at [his blog](https://betanalpha.github.io/assets/case_studies/divergences_and_bias.html#3_a_non-centered_eight_schools_implementation))

## Families of MCMC

There are a large number of variations of MCMC algorithms, with most (if not all) being specialisations of the _Metropolis-Hastings_ algorithm. The Metropolis-Hastings algorithm was itself a generalisation of the first algorithm developed, the Metropolis-within-Gibbs sampler from Metropolis, Rosenbluth and Teller in 1953. Some general families of MCMC algorithms include [[Gibbs sampling]], [[Metropolis-Hastings]], [[slice sampling]], [[Hamiltonian Monte Carlo]] and many more.

A popular sampler recently (implemented by [[stan]] and [[pymc]]) is the [[No U-Turn Sampler]] or NUTS for short. This sampler is an extension of the [[Hamiltonian Monte Carlo]] sampler.

Samplers that are better able to handle the correlation between parameters and larger numbers of parameters are [[population MCMC samplers]] which include the [[PMwG|Particle Metropolis within Gibbs]] sampler and the [[Differential Evolution MCMC sampler]].
## Properties of Markov chains

A Markov chain is Markovian when the current iteration depends only on the previous iteration. Any dependance on the history of the chains removes this Markovian property.