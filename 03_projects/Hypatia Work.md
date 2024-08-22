---
aliases:
    - Hypatia Health Beta app
    - Hypatia Health beta
---

https://soccrlab.shinyapps.io/reinforcementlearningshiny/

Hypatia Email account - health.hypatia@gmail.com

Tools to use:
- [Plumber](https://www.rplumber.io/) is a tool for creating an API directly from |function in R. It looks very promising.
- [**pointBlank**](https://rstudio.github.io/pointblank/index.html) as for input data validation?
- [renv](https://rstudio.github.io/renv/articles/renv.html) for R package dependencies
- Use [docker](https://www.docker.com/), a container system for everything else system related. The plumber package has some info about [integrating with docker](https://www.rplumber.io/articles/hosting.html#docker). There is more general information about integrating docker with R on [this blog](https://colinfay.me/docker-r-reproducibility/), including links to [rocker](https://rocker-project.org/) which has a list of pre-made docker images with R installed.
- [Fly](https://fly.io/) and [Render](https://fly.io/) for renting virtual machine? Led by Damien...
- [Valve](https://valve.josiahparry.com/) looks promising as a way to distribute Plumber API calls over multiple processes.


# Initial Plans

First things, getting a modularised RL 2-parameters model up and running.

## Ideas for RL models

- Add in discounting rate 
- Look into the [[softmax]] function for the [[stan]] code


# Simulation
-  Add variable rewards to the simulation
-  Simulate multiple people from a group level distribution

## Potential Customers

- [[Private companies relevent to HypatiaHealth]]

## Accessing VM

ssh to machine, ubuntu 18.171.136.168