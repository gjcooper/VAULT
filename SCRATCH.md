# SCRATCH PAD

_Notes placed here should be cleaned out regularly into the appropriate places, or actioned upon and removed_


Descriptive/statistical analysis for studies 2 and 3, did the manipulation work? In the HH/LL cells did they accept more than in distractor cells? Maybe instead of 3x3 ANOVA use something like an attribute specific logistic regression

For th two option case does the _difference_ in attribute levels predict choice

## shower thoughts

Should we add win-stay lose-shift outputs to displays?

## Used response sections hypatia

data.trials
data.choice_prop
data.mean_reward

# Notes from Alex

- Variational Bayes easily done in stan when have the model written. Much faster, but no guarantee of model converence like MCMC.
- CmdStanR executables created that are interfaced with R, rather than within R
- Classic task papers:
    - [[pizzagalli2008reduced|Pizzagalli SDT with bias affected by rewards]]
    - [[hird2024movement|Hird's review article on exercise and depression that links to several effort-based reward tasks]]
    - Volatility tasks: [[pulcu2017affective|A volatility RL task that independently manipulates win/loss probability]]
    - Cambridge cognition: https://cambridgecognition.com/intra-extra-dimensional-set-shift-ied/
    - Explore-exploit task: https://www.sciencedirect.com/science/article/pii/S0010027717303359
    - https://elifesciences.org/articles/11305
 
### Confusion matrix, recovery from simulation scatterplot??

- to recover reward and punishment learning rates properly it may be best to have reward and punishment rates anti-correlated
- reward sensitivity and inverse temperature are confusable.
- model confusability.
- Claim that Subset of people who have no Model of the environment in the two-step task, would need to show model recoverability.

## project idea

Using Jess's work on separating out response style from true distributions, does this change the [[test-retest reliability]] of typical psychiatric battery tests like depression scales etc. These typically have high reliability compared to behavioural tasks, important for individual differences research, but works this call it into question.

## Climate change talk

Collective risk social dilemma sounds like an interesting task.

## Trial by trial predictions

In the [[Exemplar-based consumer choice model|GCM inspired analysis]] trial by trial predictions, it would be interesting to know (especially where the logistic regression (LR) analysis wins) where the wins predominate. For instance if my model predicts trials 75% correctly and the conjunctive method predicts 80% correctly, does the model [[AMADM]] evenly split its misses vs the LR conjunctive being completely correct on accept but missing majority of rejects?

- Roger Shepard universal law generalisation. 
- Hendrickson et al 2019. Categorisation and generalisation.


Zototen

## Writing up PhD things

- 26/02/25 - Chase up in a week or two about the CBB paper
- For the third content chapter of my thesis - the [[Exemplar-based consumer choice model|GCM inspired analysis]], I would like to write this up into a paper. To start with it might be a good idea to extract out the chapter and start shaping it into a paper. Then we can assess what might need to be worked on in order to turn it from thesis chapter to viable paper.
- Two ideas for the content chapter -> paper are listed below:
    - The current work on logistic regression coparisons for the model estimate the [[logistic regression]] independently for each attribute and then combine the cut points (thresholds) into decision rules like [[Conjunctive Strategy]], [[Disjunctive Strategy]] and [[Frequency of Good and-or Bad Features Heuristic]]. If instead I estimate the regression on both attributes at the same time, with an additional interaction term then perhaps we can compare participants interaction effect terms with the curvature terms of my model. Subsets of people (especially in the preference task) that show different patterns of predicted behaviour should exhibit different curvature and matching regression interaction terms. (This would be similar to a [[Random Utility Model]] approach)
    - Another avenue to investigate could be to link this work to the [[context effects]] work in decision making. If we take estimated parameters from the two-option choices in the third task and simulate responses to options designed to elicit context effects (attraction etc) do we see predicted behaviour matcging those same context effects as a natural consequence of the [[AMADM]] model?
- There is also the work I put together for the CogSci paper on the [[Attribute Map]] project which I could at some point work on.


# Newcastle Permanent Innovation Accelerator Program Launch

- Select early career researchers to give tools for developing ideas into the community.
    - Translational impact
    - Commercialisation pathway
- How it works
    - 12 week curated program with HMRI
    - initial pitch assessment, build up skills
- Who is it for. Healthcare innovations for real world impact
- $20k in seed funding to accerlate their research.
- Specialist training, networking opportunities.
- Chance to compete for $200k award to further develop their research.
- Continued access to HMRI's network
- EOI opens 17 March 2025 - Program commences May 2025.
- hmri.org.au/accelerator

I should reach out to Murray Cairns and Michael breakspear about the clinical applications.

## Podcast recommendations

- wicked movie 
- half life 2 (remade)
- Ludwig tv show
- the rest is history podcast 
- time is the playground albumn
# Switching prod servers

- ssh into new server
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