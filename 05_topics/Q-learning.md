# Q-learning

A model free cognitive model of reinforcement learning, the general form of Q-learning has two parameters in the Q-value update function, the learning rate $\alpha$ and the discount parameter $\gamma$.

$$ Q(S_t,A_t) = (1 - \alpha)\cdot Q(S_{t-1},A_{t-1}) + \alpha\cdot\Bigl(R_t + \gamma\cdot\max_aQ(S_t,a)\Bigr)$$
There is also an additional parameter $\beta$ that controls how deterministically the actual action taken is, where

$$ p(A_t=a) = \frac{e^{\frac{Q^t_a}{\beta}}}{\sum_{a'\in{A}}e^{\frac{Q^t_{c'}}{\beta}}}$$

That is the probability of taking action $a$ is calculated using the softmax function with a temperature of $\beta$.

In the case of the simple 2-parameter reinforcement learning model for the start of the [[Hypatia Health]], we set $\gamma = 0$ , that is our agent (participant) is assumed to only focus on immediate rewards.