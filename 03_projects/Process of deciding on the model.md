# A loose collection of notes from meetings and high level ideas

## Notes from meeting Scott and guy

We use Multivariate normals, which are then transformed to positive,
scaling

The possible options for selecting between the models are:

  - Stick-breaking - bad priors for this though
  - Dirichlet process - exactly how to do this though was initially
    unsure.

## Plan for models

For each of the 7 models have a count parameter (named alpha from Cox
and Criss). Then enter a "master" log likelihood function, so instead of
calculating log likelihood for all 7 models, sample from dirichlet based
on count parameters (exp'd). This gives the winning model for this
particle. Then generate the log likelihood for this winning model.

    Start points for counts -> [1,1,1,1,1,1,1]
    prior for each count -> N(1, 2)
    
    ll() {
      x = exp(x)
      model = rdirichlet(1, counts)
      like = ddensity(model)
      }

Question - Can we store the model that wins? - This was not followed up
though.

*Planning for [[Modelling of Veridical and Preferential Choice]]*

Going into the output: [[Architecture of MultiAttribute Choice]] some changes were made. That is five architectures now, not the full seven. However the underlying principle here of using a dirichlet process