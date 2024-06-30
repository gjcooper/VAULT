
https://soccrlab.shinyapps.io/reinforcementlearningshiny/



Tools to use:
- [Plumber](https://www.rplumber.io/) is a tool for creating an API directly from |function in R. It looks very promising.
- [**pointBlank**](https://rstudio.github.io/pointblank/index.html) as for input data validation?
- [renv](https://rstudio.github.io/renv/articles/renv.html) for R package dependencies
- Use [docker](https://www.docker.com/), a container system for everything else system related. The plumber package has some info about [integrating with docker](https://www.rplumber.io/articles/hosting.html#docker). There is more general information about integrating docker with R on [this blog](https://colinfay.me/docker-r-reproducibility/), including links to [rocker](https://rocker-project.org/) which has a list of pre-made docker images with R installed.
- [Fly](https://fly.io/) and [Render](https://fly.io/) for renting virtual machine? Led by Damien...


# Initial Plans

First things, getting a modularised RL 2-parameters model up and running.

## Ideas for RL models

- Add in discounting rate 


# Simulation
-  Add variable rewards to the simulation
-  Simulate multiple people from a group level distribution