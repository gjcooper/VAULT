# Assumptions for Decision Strategies

## Coactive architectures

### Frequency of Good and/or Bad Features Heuristic

[Montgomery and Svenson (1976)](#montgomery76) first introduced this
decision strategy, and described it as *Maximizing the number of
attributes with great attractiveness*, but it was also again described
as the *Frequency of Good and/or bad features heuristic* by [Alba and
Marmostein (1987)](#alba87).

The decision maker in this case is not directly comparing attributes
between alternatives, instead they are comparing them to some aspiration
level and then labelling each as either good (in which case
\(\mathit{frq}(a_{ij}) = 1\)), neutral (\(\mathit{frq}(a_{ij}) = 0\)) or
bad (\(\mathit{frq}(a_{ij}) = -1\)). The decision process itself is
described by one of three variants

1.  Choosing the alternative with the highest number of good attributes
2.  Choosing the alternative with the lowest number of bad attributes.
3.  Considering both good and bad attributes, i.e.
    \(\mathrm{max}_{j=1..n}[\sum_{i=1}^m \mathit{frq}(a_{ij})]\)

[[Equal Weight Heuristic]]
[[Weighted Additive Rule]]
[[Additive Difference Strategy]]
[[Majority of Confirming Dimensions Heuristic]]
[[s Heuristicor Bad Feature]]
## Self-terminating (Serial or Parallel)

### Compatibility Test

Coming from *Image theory* in [Beach and Mitchell (1978)](#beach87) and
formalised as *compatibility test* by [Beach in 1990](#beach90), this
decision strategy is one that operates by eliminating alternatives. The
general idea is that an alternative is eliminated if its attribute
levels violate the corresponding aspiration levels more than $k$
times, where $k$ is specific to the decision maker.

$\sum_{i=1}^m \mathit{asp}(a_{ij}) > k$

Nothing is specified what happens in a decision if no alternative meets
this threshold, or how to decide between each option if multiple ones
meet the threshold.

### Conjunctive Strategy

Originally discussed by [Coombs and Kao (1955)](#coombs55) the
conjunctive strategy is the special case of the compatibility test where
$k$ is fixed at 1, that is an alternative is removed if at least 1
attribute does not meet the aspiration level.

$$
\sum_{i=1}^m \mathit{asp}(a_{ij}) >= k
$$

### Satisficing Heuristic

Introduced by [H. Simon in 1955](#simon55) the *satisficing heuristic*
is a strategy whereby decision makers are assumed to consider
alternatives sequentially in the order in which they occur in the choice
task. The decision is made as soon as alternative is reached that meets
all aspiration levels ($\forall i\; \mathit{asp}(a_{ij}) = 0$)

In contrast to the conjunctive strategy the decision maker will stop
early at the first alternative that meets all aspiration levels.

### Satisficing-plus Heuristic

A variant to the Satisficing heuristic introduced by [Park
(1978)](#park78), this extends the satisficing heuristic to the
situation where decision makers only consider some subset of attributes,
of size $m^*$. They then choose the alternative that meets the
aspiration level on all $m^*$ of those attributes.

## Exhaustive (Serial or Parallel )

### Disjunctive Strategy

Another elimination strategy proposed by [Coombs and Kao
(1955)](#coombs55), this strategy complements the conjunctive strategy
as the decision maker will eliminate an alternative if all of its
attribute values do not meet their respective aspiration level.

$$
\sum_{i=1}^m \mathit{asp}(a_{ij}) = m
$$

This means that the disjunctive strategy, the compatibility test and the
conjunctive strategy all fall along a spectrum, by eliminating an
alternative if all, some or at least one attribute fails to meet the
aspiration level.

### Dominance strategy

Proposed by [Lee (1971)](#lee71) the *dominance strategy* is one where
the chosen alternative dominates all other alternatives. An alternative
$\mathit{alt}_k$ is said to dominate $\mathit{alt}_l$ if all
attribute values are as good or better. That is:

$$
\forall i \; v_i(a_{ik}) >= v_i(a_{il}) \land
       \exists i v_i(a_{ik}) > v_i(a_{il})
$$

If no alternative dominates the others, then no choice is made.

### Simple Majority Decision rule

This decision strategy is basically the same as the dominance strategy,
however the decision maker always chooses an alternative. The chosen
alternative is the one which has the highest number of dominating
attributes. Thus for alternatives A and B with A better on one
attribute, and B better on two attributes, then B is selected.

## Self-terminating and Serial

### Elimination by Aspect Strategy

Described by [Tversky (1972)](#tversky72) and also a variant, the
*Deterministic version of elimination by aspect strategy* in [Payne et
al. (1988)](#payne88) this strategy is one that operates over
attributes, where decision makers are assumed to sort attributes
$\mathit{attr}_i$ according to their weight $w_i$, or the importance
of the attribute to the decision maker. Then starting with the attribute
with largest weight alternatives will be iteratively removed if the
value of the $i\mathrm{th}$ attribute does not meet the aspiration
level. That is that $\mathit{asp}(a_{ij}) = 1$.

The strategy stops once there is only one alternative left (and does not
consider any more attributes), or if all attributes have been
considered. If the pool of alternatives still has more than one
alternative left then there is no specification for how to choose
between the remaining alternatives.

The deterministic version contrasts to the original version by Tversky
in which attributes are considered probabilistically.

### Lexicographic Heuristic

Decision makers in this strategy (proposed in [Tversky
(1969)](#tversky69)) also consider attributes in order of their weight,
and indeed for the current attribute under consideration the alternative
$\mathit{alt}_j$ whose attribute has the highest value is selected.
Highest value is:

$$
\mathit{max}_{j = 1..n} v_h(a_{hj})
$$

If more than one alternative is selected (say two or more alternatives
are equivalent on the most important attribute) then the remaining
attributes are iteratively considered until there is only one
alternative left.

### Minimum Difference Lexicographic Rule

Proposed as the *Lexicographic semiorder strategy* by [Luce
(1956)](#luce56), this strategy was also covered and renamed the
*minimum difference lexicographic rule* by [Montgomery and Svenson
(1976)](#montgomery76). This strategy is quite similar to the
lexicographic heuristic, however two attribute values $a_{ij}$ and
$a_{ik}$ are said to be equal if
$v_i(a_{ij}) - v_i(a_{ik}) < \Delta_i$, where $\Delta_i$ is a
threshold above which a decision maker notices a difference between two
attribute values

## References

  - Dawes R, Corrigan B (1974) Linear models in decision making. Psychol
    Bull 81(2):95–106
    <span id="-dawes74"></span><span id="dawes74" class="tag">dawes74</span>
  - Einhorn H, Hogarth R (1981) Behavioral decision theory: Processes of
    judgment and choice. Annu Rev Psychol 32:53–88
    <span id="-einhorn81"></span><span id="einhorn81" class="tag">einhorn81</span>
  - Dawes RM (1979) The robust beauty of improper linear models in
    decision making. Am Psychol 34:571–582
    <span id="-dawes79"></span><span id="dawes79" class="tag">dawes79</span>
  - Thorngate, W. (1980). Efficient decision heuristics. Behavioral
    Science, 25(3), 219-225.
    <span id="-thorngate80"></span><span id="thorngate80" class="tag">thorngate80</span>
  - Tversky A (1969) Intransitivity of preferences. Psychol Rev 76:31–48
    <span id="-tversky69"></span><span id="tversky69" class="tag">tversky69</span>
  - Fishburn PC (1970) Utility Theory of Decision Making. Krieger,
    Huntington
    <span id="-fishburn70"></span><span id="fishburn70" class="tag">fishburn70</span>
  - Todd P, Benbasat I (1991) An experimental investigation of the
    impact of computer based decision aids on decision making
    strategies. Inform Syst Res 2:87–115
    <span id="-todd91"></span><span id="todd91" class="tag">todd91</span>
  - Montgomery H, Svenson O (1976) On decision rules and information
    processing strategies for choices among multiattribute alternatives.
    Scand J Psychol 17:283–291
    <span id="-montgomery76"></span><span id="montgomery76" class="tag">montgomery76</span>
  - Payne JW (1976) Task complexity and contingent processing in
    decision making: An information search and protocol analysis. Organ
    Behav Hum Perform 16(2):366–387
    <span id="-payne76"></span><span id="payne76" class="tag">payne76</span>
  - Wright P, Barbour F (1977) Phased decision strategies: Sequels to an
    initial screening. In: Starr MK, Zeleny M (eds) Multiple criteria
    decision making. TIMS studies in the management sciences, vol 6.
    Elsevier Science Pub, Amsterdam, pp 99–109
    <span id="-wright77"></span><span id="wright77" class="tag">wright77</span>
  - Alba, J. W., & Marmorstein, H. (1987). The effects of frequency
    knowledge on consumer decision making. Journal of Consumer Research,
    14(1), 14-25.
    <span id="-alba87"></span><span id="alba87" class="tag">alba87</span>
  - Beach, L. R., & Mitchell, T. R. (1978). A contingency model for the
    selection of decision strategies. Academy of management review,
    3(3), 439-449.
    <span id="-beach78"></span><span id="beach78" class="tag">beach78</span>
  - Beach, L. R. (1990). Image theory: Decision making in personal and
    organizational contexts. John Wiley & Sons Incorporated.
    <span id="-beach90"></span><span id="beach90" class="tag">beach90</span>
  - Coombs, C. H., & Kao, R. C. (1955). Nonmetric factor analysis.
    University of Michigan. Department of Engineering Research.
    Bulletin.
    <span id="-coombs55"></span><span id="coombs55" class="tag">coombs55</span>
  - Simon H (1955) A behavioral model of rational choice. Quart J Econ
    69(1):99–118
    <span id="-simon55"></span><span id="simon55" class="tag">simon55</span>
  - Park CW (1978) A seven-point scale and a decision maker’s
    simplifying choice strategy: An operationalized satisficing-plus
    model. Organ Behav Hum Perform 21:252–271
    <span id="-park78"></span><span id="park78" class="tag">park78</span>
  - Lee WL (1971) Decision theory and human behavior. Wiley, New York
    <span id="-lee71"></span><span id="lee71" class="tag">lee71</span>
  - Tversky A (1972) Elimination by aspects: A theory of choice. Psychol
    Rev 79:281–299
    <span id="-tversky72"></span><span id="tversky72" class="tag">tversky72</span>
  - Payne JW, Bettman JR, Johnson EJ (1988) Adaptive strategy selection
    in decision making. J Exp Psychol Learn Mem Cognit 14(3):534–552
    <span id="-payne88"></span><span id="payne88" class="tag">payne88</span>
  - Luce D (1956) Semiorders and a theory of utility discrimination.
    Econometrica 24(2):178–191
    <span id="-luce56"></span><span id="luce56" class="tag">luce56</span>
