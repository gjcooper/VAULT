---
aliases:
    - MCD
---

# Majority of Confirming Dimensions Heuristic

Also a pairwise decision strategy, however [[utility]] values are not
assigned, rather the decision maker decides whether they prefer
$a_{ik}$ over $a_{il}$. The difference between two alternatives is
the sum of the number of "wins" for all attributes (the winning
alternative won the majority of the attribute comparisons). This
strategy was first described in [Wright and Barbour (1977)](#wright77).

$$
\mathit{diff}(\mathit{alt}_k, \mathit{alt}_l) = 
        \sum_{i=1}^m D(a_{ik}, a_{il}),
$$     
where

$$
\begin{aligned}
D(a_{ik}, a_{il}) &= 1 \quad &\mathit{if} \quad v_i(a_{ik}) > v_i(a_{il}), \\
    D(a_{ik}, a_{il}) &= -1 &\mathit{if} \quad v_i(a_{ik}) < v_i(a_{il}), \\
    D(a_{ik}, a_{il}) &= 0 &\mathrm{otherwise}
\end{aligned}
$$