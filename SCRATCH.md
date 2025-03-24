# SCRATCH PAD

_Notes placed here should be cleaned out regularly into the appropriate places, or actioned upon and removed_


Descriptive/statistical analysis for studies 2 and 3, did the manipulation work? In the HH/LL cells did they accept more than in distractor cells? Maybe instead of 3x3 ANOVA use something like an attribute specific logistic regression

For the two option case does the _difference_ in attribute levels predict choice

## shower thoughts

Should we add win-stay lose-shift outputs to displays?

[[AMADM papers]]

# Switching prod servers

- Reboot if needed
- ssh back into new server
- aws configure
- aws ecr get-login-password --region eu-west-2 | docker login --username AWS --password-stdin 954976308939.dkr.ecr.eu-west-2.amazonaws.com
- git clone https://github.com/Hypatia-Health/hypatia_app_beta_backend.git
- cd into `~/hypatia_app_beta_backend/src`
- VERSION="0.0.8.9000" docker compose pull
- Switch static IP to new server
- Log back in and cd to `~/hypatia_app_beta_backend/src`
****- switch nginx.conf to `nginx.conf.http-api`
- `VERSION="0.0.1.9005" docker compose up -d`
- `docker compose run --rm  certbot certonly --webroot --webroot-path /var/www/certbot/ -d api.hypatia.health`
- Switch nginx.conf back to `nginx.conf.full-api`
- VERSION="0.0.8.9000" docker compose restart
- **Remember to turn on https networking in AWS Lightsail console**

## Hypatia future notes

Sayidda lived experience

project coordinator, ux, front end backend based in WA.