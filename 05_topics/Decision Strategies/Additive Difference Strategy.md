---
aliases:
    - Additive difference model
    - Addition of utility differences
    - ADD
---
# Additive Difference Strategy


Originally proposed in [Tversky's 1969 paper](#tversky69) for 2 alternatives it was extended to \> 2 alternatives and rebranded the *Additive difference model* in [Payne (1976)](#payne76), as well as being covered in [Montgomery and Svenson (1976)](#montgomery76) as the *Addition of [[utility]] differences rule*.

The framework for this decision process is to take pairs of alternatives and compute the utility difference between the pair. If the utility of the first alternative is higher, it is kept and the second alternative is discarded and replace by one of the remaining alternatives not yet considered. This continues until all alternatives have been considered and there is a final winner.

$$
\mathit{diff}(\mathit{alt}_k, \mathit{alt}_l) =
        \sum_{i=1}^m w_i[v_i(a_{ik}) - v_i(a_{il})]
$$
