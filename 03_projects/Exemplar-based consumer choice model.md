---
aliases:
    - GCM inspired analysis
    - EB-CCM
---

# Exemplar-based consumer choice model

Taking inspiration from the [[Generalised Context Model]]  the first iteration of this approach takes a look at the single option choice sets that I have done, including the [[Veridical task]], the [[Preferential task]] and the [[Attribute Map]] task.

Outlined roughly the approach is to set the exemplar to be (0, 0), that is price anchored to $max and quality or rating anchored to 0% or 0 stars. Then each individual option is "compared" to this anchor, and the GCM uses modelling to tease apart the:
* $w$ -  "weight" given to each attribute
* $d$ - "distance" metric form
* $s$ - "sensitivity" to distances in attribute space, and
* $\delta$ - the choice "offset" relative to the anchor

Some terms of use here are the distance between two exemplars, taken straight from [[Nosofsky]]'s [[Generalised Context Model]]

$$
d_{ij} = \left[\sum_{m=1}^Mw_m|x_{im} - x_{jm}|^r\right]^{1/r}
$$

however here we set the anchor, or the examplar being checked against to be the most likely to be rejected, or the highest price/lowest quality option - set to (0,0). This makes our distance expression for option $a$

$$
d_{a} = \left[\sum_{m = 1}^Mw_m.x_{am}^r\right]^{1/r}
$$

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

