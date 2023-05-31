# Modelling Veridical and preferential DCE

## Ancillary Information

- [[Process of deciding on the model]]
- [[Data Prep for the modelling]]
- [[Multinomial Logit Models]]
- [[Architecture Recovery in Preferential dataset]]

## Current Model

3 Architectures implemented (IEX, IST and CB) using a dirichlet process
for the selection of model to estimate.

The t0 and A parameters are shared across all trial type, there are two threshold parameters, one for accept decisions and one for reject.  Finally there are 12 drift rates, for each attribute (price vs quality) and salience level (H, L, D) there is a drift rate for accepting and a drift rate for rejecting. The drift rates are then combined via the specified model for each trial, so a HD trial (High Price, Distractor Quality) would combine the drift rates for High Price (Accept and Reject) and Distractor Quality (Accept and Reject) in the way specified by the model selected by the dirichlet process.

There was a contaminate process also modelled (2% uniform over response
range, 0 to 4.5 seconds)

## Model recovery

The general idea is for each subject get median of posterior distribution of random effects (Except for alpha -\> (dirichlet counts), and then simulate data that matches size of real dataset.

How do we simulate alphas? We don't - Median of subj level pars, then simulate each of the different models shared across participants. How well do alphas recover?

Start with output we have, apply fn over samples, get median for each par for each subject. Store that array to call repeatedly. Generate 3 datasets. All same median subject level pars. Simulate data for each subject from IST model, and so forth for each of the 3 models.

## Serial Models?

Content from email from Guy Hawkins 23/10/2020

Use a data augmentation algorithm to estimate serial processing models

- Observe RT. Want to estimate parameters of two processes running in serial where t1 is the finishing time of the first process and t2 is the finishing time of the second process, where t1 and t2 are latent and t1 + t2 = RT is observed.
- \(\theta\) is a vector of parameters to be estimated from data and includes t0, t1, t2 (i.e., t1 and t2 are parameters to be estimated). Assume we have a density function for each of the latent component processes that generate t1 and t2, \(f(.|\theta)\) and \(g(.|\theta)\).
- Conditional updating scheme. Start with estimates of \(\theta_i\) and \(t1_i\), \(t2_i\). Let's call the augmented parameter vector \(\theta'_{i+1}\). Then, on each iteration
    - Propose \(\theta_{i+1} = \theta_i + metropolis jump\)
    - \(u1 = RT - t0_{i+1} - t2_{i+1}\), calculate \(like1 = f(u1|\theta_{i+1})\)
    - \(u2 = RT - t0_{i+1} - t1_{i+1}\), calculate \(like2 = g(u2|\theta_{i+1})\)
    - Return \(like1 * like2\) and use that to reject \(\theta'_{i+1}\)
- There is a separate t1 and t2 for each RT. Unlike other model parameters we don't estimate the full chains of t1 and t2. All we require is the current best estimate of t1 and t2. We condition on these current best estimates at each iteration, like expectation maximisation.

Serial models of multi-attribute choice:

- Say we have 2 options {1, 2} each described by 2 attributes {A, B} with levels {a1, a2, b1, b2}. Assume that the decision process is made up of 'attribute races' where some combination of winners across a set of independent and serial attribute races determine the chosen option. Denote \(a1>a2\) to mean that option 1 beat option 2 in the race for attribute A.
- Say option 1 is the observed choice. The model assumes this is due to option 1 winning both or either of the attributes races; it's not possible for option 1 to be chosen if it lost both attribute races.  So a choice of option 1 could be due to any of the following, where the likelihood of observing a choice of option 1 is the sum of the 3 likelihoods. Assume t1 and t2 are the times for attribute races A and B to finish, respectively, with u1 and u2 defined as above.
    - \(a1>a2\) & \(b1>b2\)
        - \(like1 = [ f(u1|\theta_{a1}) * (1-F(u1|\theta_{a2})) ] * [ f(u1|\theta_{b1}) * (1-F(u1|\theta_{b2})) ]\)
    - \(a1>a2\) & \(b2>b1\)
        - \(like2 = [ f(u1|\theta_{a1}) * (1-F(u1|\theta_{a2})) ] * [ f(u1|\theta_{b2}) * (1-F(u1|\theta_{b1})) ]\)
    - \(a2>a1\) & \(b1>b2\)
        - \(like3 = [ f(u1|\theta_{a2}) * (1-F(u1|\theta_{a1})) ] * [ f(u1|\theta_{b1}) * (1-F(u1|\theta_{b2})) ]\)
- The likelihood of observing choice of option 1 at time RT, conditioned on t1 and t2, is \(like1 + like2 + like3\).

Possible citation? Klauer & Kellen (2018). RT-MPTs: Process models for response-time distributions based on multinomial processing trees with applications to recognition memory. JMP.  <https://www.sciencedirect.com/science/article/pii/S0022249617301980>

## Decision strategies and their models

Here is the page with the latest organisation of [[assumptions for decision strategies]]
