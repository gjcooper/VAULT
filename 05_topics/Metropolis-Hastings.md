# Metropolis Hastings

An algorithm that is the basis/general for a lot of [[MCMC]].

Given a target distribution $p(\theta)$ for which we don't know the [[normalising constant]].

The algorithm is as follows:

1. Select an initial value for $\theta$, $\theta_0$
2. For $i = 1, \ldots, m$, repeat
    1. Draw a candidate $\theta^* \propto q(\theta^*|\theta_{i-1})$ 
    2. Compute $\alpha$ using Eqn 1
    3. If $\alpha\geq1$ then accept $\theta^*$ and set $\theta_i \leftarrow \theta^*$, if however $0<\alpha<1$ accept $\theta^*$ and set $\theta_i\leftarrow\theta^*$ with probability $\alpha$ or reject $\theta^*$ and set $\theta_i\leftarrow\theta_{i-1}$ with probability $1 - \alpha$


Eqn 1:
$$
\alpha =
\frac{g(\theta^*) /q(\theta^*|\theta_{i-1})}{g(\theta_{i-1})/q(\theta_{i-1}|\theta^*)} =
\frac{g(\theta^*)q(\theta_{i-1}|\theta^*)}{g(\theta_{i-1})q(\theta^*|\theta_{i-1})}
$$

The candidate generating distribution $q$ can either be an approximation of $p(\theta)$, or in the case of **Random Walk Metropolis-Hastings** we can draw from a normal distribution centred on the previous iteration and get some gains in calculations of the $\alpha$, that is we get to cancel out the $q$ terms.

The desired [[acceptance rate]] varies depends on the actual algorithm being used. If $q$ is an approximation of $p$ then we want a high acceptance rate (it is a good approximation). For random walk Metropolis-Hastings we want an acceptance rate perhaps between about 25-50%. This means our step size is tuned well enough to cover the space, without getting wasted draws outside the high density regions of $p$.