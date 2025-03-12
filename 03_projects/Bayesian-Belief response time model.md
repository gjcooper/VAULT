Closely related to the [[BPD Self-other social model]] this model incoporates response time predictions by using an evidence accumulation component to the model. Specifically the idea is to include a [[diffusion decision model|drift diffusion model]] component to the model that captures the response times.

There are a few possible places from the self-other, or Bayesian-belief model that could lead to incorporating a parameter from the belief model to drive the drift in the DDM.

One way could be just to look a a value difference between the current posterior and the generating model for the opponent, however [[Joseph Barnby]] has proposed that rather than a simple value difference a better start may be to look at a [[Kullbach-Leibler divergence|KL-divergence]] between the posterior and the generating model.

From SCRATCH -> KL-divergence between distributions feed into drift rate DDM and social cognition

## Model that inspired this work

Inspired by [[Lei Zhang]]'s work on incorporating the DDM into an [[reinforcement learning]] model.

So Lei's original model had:

$$
RT_t \sim \mathit{wfpt}(a,T,z, v)
$$
where $v$ changed as a function of the value difference in the RL task (simple [[Q-learning]] model) in one of two ways. In the linear scaling version the drift rate at time $t$, ie $v_t$ is:

$$
v_t = v_{s}(Q^t_c - Q^t_{ic})
$$
where $Q_c$ and $Q_{ic}$ are the Q-values for the correct and incorrect option, and $v_s$ is the drift scaling parameter.

There was also an additional nonlinear scaling version that introduced a new term $S$ such that now,

$$
v_t = S\left[v_{s}(Q^t_c - Q^t_{ic})\right]
$$
, and,

$$
S(x) = 2.\frac{v_{max}}{1 + e^{-x}} - v_{max}
$$

## Our proposed model(s)

Given a [[Kullbach-Leibler divergence|KL-divergence]] measure on the difference in the proposed posterior of the participants predicted distribution for their distribution at time point $t$ with the distribution at time point $t-1$, the drift rate at time point $t$ will be a scaled adjustment to this divergence.

That is given
$$
D_{\mathrm{KL}}(P_t||P_{t-1}) = \sum_t^sP^t(s)\log\left(\frac{P^t(s)}{P^{t-1}(s)}\right)
$$
and given the hypothesis that increased divergence will lead to slower response times (lower drift rates) we have the drift at time t ($v_t) equal to a scaled version of the $D_{\mathrm{KL}}$, such as,
$$
v_t = v_s\Big(D_{\mathrm{KL}}\left(P^t||P^{t-1}\right)^{-1}\Big)
$$
This would lead to a $D_{\mathrm{KL}}$ version of the model. We could similarly create another model that scales a standard entropy measure of the distribution $E$, so now $v_t$ would be:
$$
v_t = v_s\Big(E\left(P^t\right)^{-1}\Big)
$$
Other than drift, the typical boundary separation, non-decision time and bias would be freely estimated.

Along with a standard null model that disassociates the bayesian belief choice model from the response time model we would also add a practice effects model that scales an original drift value $v_o$ over time (either linearly of nonlinearly), so then
$$
v_t = v_s*v_o
$$
This could be modelled with $v_s$ going from $0 \leq x \leq \infty$ where a value == 1 shows no practice effects, and value < 1 shows a slowing down over time and a value > 1 shows a speeding up over time.

# Initial plans

Create the models and simulate from them to get some plots showing the expected patterns for different KL etc. The goal would be to get this working on a lot of the **Phase 2** data from places like the [[barnby2022knowing|Knowing me, knowing you: Interpersonal similarity improves predictive accuracy and reduces attributions of harmful intent]] project and other work from [[Joseph Barnby]] using a similar task but with adolescents.