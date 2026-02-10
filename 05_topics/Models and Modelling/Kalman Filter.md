---
aliases:
    - Bayesian Learner
---

# Kalman Filter

Sometimes known as the Bayesian Learner model the Kalman Filter is an alternative to the [[Q-learning]] model that assumes that a learner keeps track not just of the mean of the outcome distribution, but also the uncertainty about that estimate.

This leads to a trialwise learning-rate, with a higher learning rate when the uncertainty about an outcome is higher.