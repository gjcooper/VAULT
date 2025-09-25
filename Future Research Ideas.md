# Ideas for future research

## Unformed thoughts

- Price Quality display that "switches" at some point during the task
    - See [[Peter Kvam]] talk
- [[Guy Hawkins]]'s timing threshold work, how does this apply to tasks where there is a time limit (short) on responses - think JP's work
- How does Serial self-terminating actually work? Looking at Criss and Cox's paper I was struck by the fact that for a serial self-terminating model, if we are accumulating evidence in serial, at what point do we <span id="stop"></span>**stop** accumulating evidence for the first attribute/option and *start* accumulating evidence for the second option. I presume it is some sort of racing accumulator racing between evidence in favour and evidence against, and if evidence against succeeds then the second alternative/option race starts accumulating?
- Consumer Choice preferences change as a function of friend network, Networks could be social networks, close friend networks etc.
- Deep RL NN model for learning features of the DCE. Early trials in a DCE where people learn the range of each feature, what an excellent option looks like, what a bad option looks like, and which ones are borderline.
- How do [[evidence accumulation models]] work with recognition memory???
- Can you predict worst choices from best choices and vice versa in best-worst discrete choice tasks?

## Priming and mapping the price/quality trade-off

- Start with a section that primes the participant with appropriate values for price and quality.
  - This could involve saying the range of prices and qualities typically seen in an area ([[Preferential task]])
  - Alternatively this could involve showing a list example hotels (prices and ratings for example) for participants to extract this information themselves.
- Next we run either a staircase approach as done in Pref SFT and/or a
2D boundary search approach where participants rate a selection of hotels one after another, and the attributes values are adjusted such that we try and map the boundary of the participants trade-off between price and rating.
- Maybe then set up a SFT like task after this based on the boundary as a whole. (not just a fixed point)

## 2D helicopter task

- Instead of a [[Helicopter Predictive Inference Task]] with the helicopter moving along one axis, perhaps a helicopter moving along 2 axes.
- Two possible tasks:
  - trying to catch a parcel again, drops from a 2D gaussian or similar. Wind could be constant, gusty, swirling. Mouse to control the location?
  - Perhaps you are controlling the helicopter and you need to try to drop to hit a target (food drops) and you have to infer the best location to account for wind.

## Framing of choices effects on response times

When a set of choices is framed as "Please accept options that meet some criteria" Does the patterns of response times change compared to peoples response times when given the framing of "Please reject options that do not meet the criteria"?

## Unbalanced effects of the $199 price points on thresholds.

When presented with prices that are just shy of a round number, do people show effect son thresholds or drift rates for price points on either side of the round number boundary.

### Decision Processes in Consumer Choice

Standard DCE with 3 alternatives and three attributes per option, two formats

| Option 1 | Option 2 | Option 3 |
| -------- | -------- | -------- |
| $150 | $500 | $80 |
| 65/100 | 85/100 | 45/100 |
| Beach | Beach | Skiing |

| Option 1 | Option 2 | Option 3 |
| -------- | -------- | -------- |
| \$\$ | \$\$\$\$ | \$ |
| \* | \*\*\* | \*\* |
| 🌅 | 🌅 | 🌄 + ⛷️ |

So we have a comparison of decision strategies between textual and pictorial representations of attribute information, use reaction time modelling to investigate the processing involved in the two conditions

### SFT in Consumer choice extension

- Extending the current experiment to a scenario with two alternatives, with a price and rating for each.

| Option 1 | Option 2 |
| -------- | -------- |
| \$\$\$ | \$\$\$\$ |
| \*\* | \*\*\* |

How do we manipulate salience?? We can adjust the difference between each attribute (\$\$ vs \$\$\$ is low, \$ vs \$\$\$\$ is high).

What is the correct response without a specific guideline here? For the above example Option 2 wins on rating, but loses on price - so no obvious winner.

One factor to consider would be the extent to which we are measuring perception processes in our reaction times compared to actual decision processes. Does anyone have any ideas on how we can disambiguate these??

### SFT in Consumer choice extension

- Extending the current experiment to a scenario with two alternatives, with a price and rating for each.

| Option 1 | Option 2 |
| -------- | -------- |
| \$\$\$ | \$\$\$\$ |
| \*\* | \*\*\* |

How do we manipulate salience?? We can adjust the difference between each attribute (\$\$ vs \$\$\$ is low, \$ vs \$\$\$\$ is high).

What is the correct response without a specific guideline here? For the above example Option 2 wins on rating, but loses on price - so no obvious winner.

One factor to consider would be the extent to which we are measuring perception processes in our reaction times compared to actual decision processes. Does anyone have any ideas on how we can disambiguate these??

## [[Multidimensional Scaling]] related

#### RT as a measure of object similarity

Transform RT to a similarity measure. Use this transformed RT to use in multidimensional scaling. Alternatives closer to each other are harder to discriminate.
JP might want in on this??

## [[Preferential Choice]] related

### Preferential Choice for others

An investigation into reasoning about other people's preferences.

Implication for consumer choice (gift giving) but also making health decision for others.

[[Tin Nguyen]] has a nice approach using a [[Discrete Choice Experiments]], where the estimated values on a range of attributes are used as a proxy for a "friend" that you are making decisions on behalf of. Feedback on the choice your friend would make vs what you make is given, with the goal of you changing your decision weights to match the friends decisions. Discussion were had in our local [[reinforcement learning]] group as to whether an RL model could capture this learning behaviour.

I wonder whether Tin has thought about any insight measures - that is some kind of survey after the fact to see if the participant can rank the attributes by importance or say anything else about this "friend"?

### Preferential choice by groups

How does individual strength of preference drive the final decision.

How does time remaining for a decision drive the willingness to compromise on our preferences.

## Sensitivity to context

### Sensitivity to Instructions:
A task (preferential) with variable rewards

- 1. Rewarded based on randomly selected RT, with fast and slow RT's rewarded lowly, and close to median rewarded highly
- 2. Rewarded based on consistency? One selected trial is rewarded base on how consistent the choice is with the thresholds ?Catch Trial?
- 3. Rewarded based on speed? One selected trial is rewarded based on the speed of the choice.
- Speed Accuracy tradeoff comparison and Optimum time investment check

### Sensitivity to Content

A task wich attempts to map participants familiarity with variability in the market.
ie. Hotels in CBD, medium variability


## Self-other representation of beliefs

With respect to violations of a persons representation of others. Given a model $\bar{\theta^o}$ of some others internal beliefs, what happens with a significant violation of the others policy. Does this effect change based on the "location" of the others policy before the violation, or with the direction of the violation. That is how forgiving are we of infrequent violations? [[barnby2023theory]]

## Choice after offset of visual stimulus

A lot of attention based preferential choice literature has a hypothesis that increased attention leads to > preferences and higher likelihood of choosing. There are some (see [[bhatnagar2022metaanalysis]]) conflations here between overall fixation time and last fixation. What if we instructed participants to only respond after the offset of the visual stimulus? That is last fixation is on a "Respond now" message. You may get memory effects, you could vary the offset time, or even have it triggered by fixations on specific targets. Nope - reading on it seems this has already been done


# Trialwise parameter estimates

What would happen if we first estimate a parameter distribution (using a Bayesian MCMC technique) for a participant and then estimated a trial specific parameter estimate. That is either by repeatedly sampling from the posterior for each trial, or by sampling from a normal centred on the median of the posterior in some sort of importance sampling way. For large experiments this could be extremely prohibitive - but perhaps this could be possible. I'm thinking of possible links to Guy/Scotts modelling where the parameters are assumed to come from 2+ separate distributions with a defined switch between each of the distributions.