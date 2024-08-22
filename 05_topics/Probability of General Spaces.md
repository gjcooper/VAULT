# Extending probability to general spaces

With finite sets a measure could be definedf on a subset by summing up all of the allocations of measures to the included elements. This fortunately does extend to sets with a countably infinite number of elements, such as the integers. Element-wise allocations on finite and countable infinite sets are known as **mass functions** and the corresponding probabilities as **probability mass functions**. On an ordered set (again take the integers) this can be easily visualised as a sequence of vertical bars stacked next to each other.

However when we move to uncountably infinite sets such as the real numbers, the approach of using sums breaks down. Up to here https://betanalpha.github.io/assets/chapters_html/probability_on_general_spaces.html#consistent-allocations

### Allocation over all subsets

Luckily in most realistic cases (say the two dimensional real plane $\mathbb{R}^2$) we can use countable additive measures to get a consistent allocation of a measure to subsets. For illustration take a disc on the on the 2D real plane. A crude approximation to the disc can be achieved by a single rectangular subset. A more accurate approximation comes about by the disjoint union of many different rectangular subsets within the bounds of the disc, and a countably infinite number of rectangular subsets can reconstruct the disc without error.

Many uncountably infinite spaces feature disjoint subsets ($\mathrm{x}_1 \cup \mathrm{x}_2 = \emptyset$) that exhibit _sub-additivity_  ($\mu(\mathrm{x}_1 \cup \mathrm{x}_2) < \mu(\mathrm{x}_1) + \mu(\mathrm{x}_2)$) or _super-additivity_  ($\mu(\mathrm{x}_1 \cup \mathrm{x}_2) > \mu(\mathrm{x}_1) + \mu(\mathrm{x}_2)$). These pathological subset can be proven to exist, but we can't typically construct them from explicit conditions. These _non-constructive_ objects tend not to be considered in practical applications of [[measurement theory]].

### $\sigma$-Algebras

A $\sigma$-algebra is a way to consistently filter out subsets from the power set. We can always filter the power set by removing certain subsets. A $\sigma$-algebra is any collections of subsets that is closed under complements, countable unions and countable intersections (the three set operations). A set equipped with a $\sigma$-algebra is known as a **measurable space**.

One useful way to generate $\sigma$-algebras is  to generate them by repeatedly applying the three set operations to an initial collection of subsets. Once we are generating no new subsets on each iteration the $\sigma$-algebra is defined.

If we have a topological space then the defining topology is a natural collection of subsets that we can use to generate the $\sigma$-algebra. The $\sigma$-algebra generated on a topology is known as a _Borel_ $\sigma$-algebra. Measurability of the subsets of a measurable subset is not guaranteed.

### Measures and Probability Distributions

A **measure** is a function from the $\sigma$-algebra to the extended positive real line that is countably additive. A set equipped with a $\sigma$-algebra and a measure i.e. ($\mathrm{X}, \mathcal{X}, \mu$) is known as a measure space. A function $\pi$ on any measurable space that maps to the closed unit interval $[0, 1]$ is a **probability distribution**. The axioms defining the properties of probability distributions are known collectively as the _Kolmogorov axioms_.

The usual rules of probability theory come from countable additivity, the disjoint nature of subset and its complement and more.

### Probability distributions in practice

Due to the impossibility of allocated exhaustively on infinite subsets, probability distributions are typically defined algorithmically.

## Uniform Measures

In the case of discrete measurable spaces we can define a _counting_ measure, that is each element (or atomic subset) of $X$ is assigned a unit allocation.

For non finite sets though this becomes more dificult. With an appropriate ordering, and if the space has an algebra, metric and topology we can construct closed interval subsets. Think an interval on the real line). A _Lebesgue measure_ is one where every such interval is allocated a measure directly equal to its length. The total Lebesgue measure is infinitely large and thus cannot be normalised into a probability distribution.

The Lebesgue measure can be easily extended to multivariate real spaces.

### Applications

Thus far everything has been mathematical, however interpretation is possible when we use these concepts to model something like:
- Physical distributions (mass, electrical charge etc)
- Populations (the properties of individuals from a larger population.)
- Frequencies of repeated events.
- Uncertainty about information