---
aliases:
    - LEX
---

# Lexicographic Heuristic

Decision makers in this strategy (proposed in [Tversky (1969)](#tversky69)) also consider attributes in order of their weight, and indeed for the current attribute under consideration the alternative $\mathit{alt}_j$ whose attribute has the highest value is selected. Highest value is:

$$
\mathit{max}_{j = 1..n} v_h(a_{hj})
$$

If more than one alternative is selected (say two or more alternatives are equivalent on the most important attribute) then the remaining attributes are iteratively considered until there is only one alternative left. (Uses [[attribute value]] directly)