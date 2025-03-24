---
aliases:
    - GCM inspired analysis
    - EB-CCM
---

# Exemplar-based consumer choice model

Taking inspiration from the [[Generalised Context Model]]  the first iteration of this approach takes a look at the single option choice sets that I have done, including the [[Veridical task]], the [[Preferential task]] and the [[Attribute Map]] task.

Outlined roughly the approach is to set the exemplar to be (0, 0), that is price anchored to $max and quality or rating anchored to 0% or 0 stars. Then each individual option is "compared" to this anchor, and the GCM uses modelling to tease apart the:
* $w$ -  "weight" given to each attribute
* $r$ - "distance" metric form (curvature)
* $s$ - "sensitivity" to distances in attribute space, and
* $\delta$ - the choice "offset" relative to the anchor

Some terms of use here are the distance between two exemplars, taken straight from [[Nosofsky]]'s [[Generalised Context Model]]

$$
d_{ij} = \left[\sum_{m=1}^Mw_m|x_{im} - x_{jm}|^r\right]^{1/r}
$$

however here we set the anchor, or the exemplar being checked against to be the most likely to be rejected, or the highest price/lowest quality option - set to (0,0). This makes **our** distance expression for option $a$

$$
d_{a} = \left[\sum_{m = 1}^Mw_m.x_{am}^r\right]^{1/r}
$$

One note here is that the [[AMADM]] model (Adaptive Multi-Attribute Decision Model (AMADM)) does not use the distance metric as defined for a [[Minkowski distance metric]], instead it allows r to vary freely as long as it is positive ($r > 0$). This means that it does not satisfy the triangle inequality, thus making it a [[quasi-metric]].
## Response Probability

Given current estimates for $w$, $r$, $s$ and $\delta$, the probability of an accept response is

$$
\begin{aligned}
X &\sim N(\mu, \sigma) \\
& \\
F(x) &= P(X < \delta + s.d_a)
\end{aligned}
$$
This is in the case when presented a single option, and the choice is whether to accept or reject.

## For a choice between two options

Given two options are being presented, how does this decision making change from a categorical type decision to a preferential choice.

Well perhaps what we do is using the same underlying representation, use some choice rule like the [[Luce choice axiom|Luce Choice rule]] to combine the response functions into a probability of choosing one option over the other.

So - again with the "exemplar" or "anchor" $p$ set to the most undesirable option, for instance in the two attribute case $p = (0, 0)$ we drop the $\delta$ and $s$ parameters from the single option model. We keeping the $w$ weight and the $r$ distance metric form and add a new sensitivity parameter $\gamma (\geq0)$. The new parameter $\gamma$ controls how sensitive to this difference in individual option "values" people are. If $\gamma = 0$ then people are not at all sensitive to the representational values and are essentially guessing. As $\gamma$ increases the probability of selecting the option is increasingly more deterministic.

So for options $a$ and $b$, the probability of choosing $a$ is:


$$
P(a;a,b) = \dfrac{d_a^\gamma}{d_a^\gamma + d_b^\gamma}
$$
where $d_a$ and $d_b$ are the distances of options $a$ and $b$ from the anchor point $p$


### Original framing for the approach

[[Anchor]], psychological space, new approach for the preferential choice exhibited in the [[Preferential task]] (couched in well established psych theories about [[how people represent options]])

#### Thought for the day

I wonder whether for [[Exemplar-based consumer choice model|EB-CCM]], or other preferential data, a scatter plot (or similar) of price/memory, price/rating on the x/y axes, and then colour representing the RT could elucidate the pattern I would expect of more "difficult" choices (closer to a participants "boundary" being slower)?

## Trial by trial predictions

In the [[Exemplar-based consumer choice model|GCM inspired analysis]] trial by trial predictions, it would be interesting to know (especially where the logistic regression (LR) analysis wins) where the wins predominate. For instance if my model predicts trials 75% correctly and the conjunctive method predicts 80% correctly, does the model [[AMADM]] evenly split its misses vs the LR conjunctive being completely correct on accept but missing majority of rejects?

- Roger Shepard universal law generalisation. 
- Hendrickson et al 2019. Categorisation and generalisation.

## From meeting 20-08-03 (YMD)

Shepard 89' about exponential decay as function for similarity to psychological distance

LME4 - log scale for RT to reduce skew - fulfill assumptions of lme