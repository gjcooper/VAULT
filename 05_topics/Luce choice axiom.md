---
aliases:
    - Luce Choice rule
---

# Luce Choice Rule


$$
P_S(x) = \dfrac{v(x)}{\sum_{y \in S}v(y)}
$$

Where $S$ is the set of options under consideration, such that $P_S(x)$ is the probability of choosing option $x$ from set $S$. $v(x)$ is the response strength associated with option $x$.

The article [[luce1977choice|The choice axiom after twenty years]] gives and overview of applications, and the encyclopedia entry [[pleskac2015decision|Decision and Choice: Luce's Choice Axiom]] gives a nice introduction.

From the article [[pachur2022strategy|Strategy selection in decisions from givens: Deciding at a glance?]] there is the slightly adapted form of the Luce Choice Axiom with "sensitivity", that is the amount the choice is driven by the ratio vs guessing.

In the case of a choice between two options ($A$ and $B$) that differ by the weighted sum of attribute values (with attrs $i = 1..n$) this can be written as

$$
p(A; A, B) = \dfrac
{(\sum_{i=1}^na_i^Aw_i)^\gamma}
{(\sum_{i=1}^na_i^Aw_i)^\gamma +
    (\sum_{i=1}^na_i^Bw_i)^\gamma}
$$

