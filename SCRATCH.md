# SCRATCH PAD

_Notes placed here should be cleaned out regularly into the appropriate places, or actioned upon and removed_


# Visualisation for fitting module

- Full thing downloadable.
- Upload data (num trials, num groups, num subjects)
- Vis:
    - Convergence metric (R < 1.01)
    - Group level parameters for learning rate and temperature (Median point and std dev around it)
    - Individual level parameters

![[Pasted image 20250528143728.png]]


# cpm

Luca was the person who I talked to


# Next steps in my career

What do I want to do if this job with Joe doesn't work out.

- Location - would be nice to stay in Newcastle region given Alisha loves her job.
- Field - Do I apply for grants, do I apply for a post-doc job in a local lab? How cloce to cognitive modelling does the position really have to be? Could I look at economic modelling, linguistic modelling, some other tangentially related field?
- Do i move out of academia and into industry? How flexible do I want my work and is academia that relevant to me longer term?

# Linear model reviewer response notes

- Need to reshape the pre-processed data to include the raw attribute values before running the linear model. __Still need to rerun the new script__
- The log-likelihood functions will also need adjustment in order to correctly apply the drift rates (with linear application to the attribute values) to calculate each individual likelihood of accept/reject.
-  Shoot a message to Guy about the new log-likelihood functions here. Should each architecture be rewritten using the linear function of the prices and ratings - that is - still keep the architectures, but instead of a H/L/D use a intercept/slope.