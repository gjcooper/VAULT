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

https://www.figma.com
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

### Process(es) for working with [[AWS]].

#### Access using aws-cli
- Install aws cli tool locally
- Access using IAM, in the AWS console, create the IAM user.
    - For the IAM user create an access key (not currently doing external SSO - which is recommended but overkill for now).
    - Record the Access Key ID, and Access Key Secret (won't be able to retrieve this after the fact.
    - In `aws configure` use the recorded ID and secret. Currently setting default region to eu-west-2 and the default output to json.
> [!note]
> IAM Identity Center seems to be all about setting up identity management by interfacing with external identity providers such as Google Workspace etc. I have not currently done this due to the simple nature of our org at the moment.


#### Pushing new [[docker]] images to AWS
- Register the local docker install with AWS: `aws ecr get-login-password --region eu-west-2 | docker login --username AWS --password-stdin 954976308939.dkr.ecr.eu-west-2.amazonaws.com` - This should only need to be done once.
- tag the local testing version of the docker image with an AWS specific tag: `docker tag hypatia_health:v0.0.0.9007 954976308939.dkr.ecr.eu-west-2.amazonaws.com/hypatia/backendbeta:v0.0.0.9007`
- push the new docker image `docker push 954976308939.dkr.ecr.eu-west-2.amazonaws.com/hypatia/backendbeta:v0.0.0.9007`

### Lightsail with ECR

Lightsail is the service to run a VM, ECR is the Elastic Container Registry (Where the docker image/containers are stored)

https://docs.aws.amazon.com/en_us/lightsail/latest/userguide/amazon-lightsail-container-service-ecr-private-repo-access.html

I may want to reconsider the options to not use the Lightsail container stuff as doing it manually may be difficult.

### Register lightsail docker with aws

- `aws configure` add newly generated key id and secret
-  `docker pull 954976308939.dkr.ecr.eu-west-2.amazonaws.com/hypatia/backendbeta:v0.0.0.9007`


Article for docker/certbot: https://mindsers.blog/en/post/https-using-nginx-certbot-docker/



Needs to be run every 3ish months?
```bash
docker compose run --rm certbot renew
```

## New processes

For **dev** build hypatiahealth using devtools::build(), after bumping version if necessary. Then a docker compose build followed by `docker compose push`. Note that if it has been a while and the SECRET KEY for aws has been rotated then it may be necessary to rerun `aws configure` and put in new keys. The `aws ecr` step from above will also be necessary.

Then log onto the dev server and do the following:
- If access key expired redo `aws configure` and `aws ecr` step.
- `VERSION="0.0.1.9005" docker compose pull`
- pull latest changes via github, rebase dev version nginx settings
