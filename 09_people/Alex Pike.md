
## Notes from Alex

Some notes from my meeting with Alex in relation to the [[Hypatia Work]].

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