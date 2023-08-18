---
aliases:
    - Maximizing the number of attributes with great attractiveness
---
# Frequency of Good and/or Bad Features Heuristic

[Montgomery and Svenson (1976)](#montgomery76) first introduced this decision strategy, and described it as *Maximizing the number of attributes with great attractiveness*, but it was also again described as the *Frequency of Good and/or bad features heuristic* by [Alba and Marmostein (1987)](#alba87).

The decision maker in this case is not directly comparing attributes between alternatives, instead they are comparing them to some aspiration level and then labelling each as either good (in which case $\mathit{frq}(a_{ij}) = 1$), neutral ($\mathit{frq}(a_{ij}) = 0$) or bad ($\mathit{frq}(a_{ij}) = -1$). The decision process itself is described by one of three variants

1.  Choosing the alternative with the highest number of good attributes
2.  Choosing the alternative with the lowest number of bad attributes.
3.  Considering both good and bad attributes, i.e.     $\mathrm{max}_{j=1..n}[\sum_{i=1}^m \mathit{frq}(a_{ij})]$