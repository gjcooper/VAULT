# Elimination by Aspect Strategy

Described in [[tversky1972elimination]] and also a variant, the *Deterministic version of elimination by aspect strategy* in [Payne et al. (1988)](#payne88) this strategy is one that operates over attributes, where decision makers are assumed to sort attributes $\mathit{attr}_i$ according to their weight $w_i$, or the importance of the attribute to the decision maker. Then starting with the attribute with largest weight alternatives will be iteratively removed if the value of the $i\mathrm{th}$ attribute does not meet the aspiration level. That is that $\mathit{asp}(a_{ij}) = 1$.

The strategy stops once there is only one alternative left (and does not consider any more attributes), or if all attributes have been considered. If the pool of alternatives still has more than one alternative left then there is no specification for how to choose between the remaining alternatives.

The deterministic version contrasts to the original version by Tversky in which attributes are considered probabilistically.

Closely allied with the [[Lexicographic Heuristic]], but rather than a fixed prior ordering of attributes, the choice process is probabilistic