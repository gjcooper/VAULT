# Particle Metropolis within Gibbs

The pmwg is an R package that implements an [[MCMC]] sampler using something analogous to a particle filter. Each sample has both group level and random effects (individual subject level) parameter estimates generated multiple times (one for each "particle"). Then each particle is assessed using the log likelihood for the model under investigation, and then a weighted random sample from all particles is chosen as the seed for the next sample.

Each particle is drawn from a multivariate normal distribution centred around the previous winning particle.