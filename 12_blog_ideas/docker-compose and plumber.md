# Setting up nginx, plumber and letsencrypt

Folloing the advice of https://www.digitalocean.com/community/tutorials/how-to-secure-a-containerized-node-js-application-with-nginx-let-s-encrypt-and-docker-compose and trying to update it for specific [[Hypatia Health]] stuff, so plumber instead of nodejs etc.

## Editing the dockerfile for the plumber app

### Adding a user (instead of root)
The dockerfile is still built around the rstudio plumber image, however now to add extra security I am running the backend as a new `app` **user**.

This requires jumping through some hoops to get the packages installed to the correct user library.