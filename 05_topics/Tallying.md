---
aliases:
    - Weighted Tallying
    - Unit-weight Linear Model
    - Weighted Linear Model
---

## Overview

From [[gigerenzer1996reasoning]], Tallying is just summing up the number of positive cues, so for alternatives $a$ and $b$ choose $a$ if:

$$
\sum_{i=1}^na_i > \sum_{i=1}^nb_i
$$

If the tally's are equal then guess.

Also $a_i$ and $b_i$ are $1$ if the cue value is positive, and $0$ otherwise.

## Variants

_Weighted Tallying_ is a variant of this where each $a_i$ is weighted according to its ecological validity $v_i$, ie choose a if:

$$
\sum_{i=1}^na_iv_i > \sum_{i=1}^nb_iv_i
$$

The _Unit-Weight Linear Model_ is another variant, and is related to the weighted linear models such as the [[Equal Weight Heuristic]]. Here the decision rule is the same as for base tallying, but the cue values are either 1 if positive, or -1 if negative.

The _Weighted Linear Model_ is a combination of weighted tallying and the unit-weight linear model in that is combines the weighted aspect of weighted tallying, and the impact of negative cue values.