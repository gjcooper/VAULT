# Thoughts and notes for probability on finite sets

This takes a general overview on probability for finite sets as an intuitive introduction to probabiity theory. Terms covered here include some simple set theory, which i think I am familiar enough with from back in high school and later.

Some interesting terms that have popped up though are things like [[measurement theory]], which seems to be about the allocation of some continuous value $M$ to each of the elements of a finite set. The _interesting_ part though is when $0 < M < \infty$, that is when $M$ is finite. When this is the case the allocation of $\{m_1, m_2, ..., m_N\} = M$ to a finite set with $N$ elements can be rewritten to allocate the proportions of $M$.

That is instead of $m_n$ to each element of the set $X$ we can instead allocate $p_n = \frac{m_n}{M}$. with $0 \leq p_n \leq 1$ and the $\sum_{n=1}^N p_n = 1$. If this holds then we call the collection $\{p_1, p_2, ..., p_N\}$ a **simplex**.

A proportional measure $\pi$ such as this is also known as a _probability distribution_. 

When working with subsets, particularly for a probability distribution $\pi$, the probability distribution for the special subsets $\theta$ (the empty set) is zero, and the probability distribution for the full set $X$ is one.

If we have two more _disjoint_ subsets, then a nice feature is that for the _union_ of those subsets, the measure defined on them satisfies _additivity_, and for probability distributions, if we have a subset $\textrm{x}$ and its complement $\textrm{x}^c$ then a nice property is that $\pi(\textrm{x}^c) = 1 - \pi(\textrm{x})$.