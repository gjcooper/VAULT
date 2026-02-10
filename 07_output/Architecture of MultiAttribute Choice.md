---
aliases:
    - veridical choice modelling paper
---

# Processing architectures of multiattribute choice

## Overview

- Brief recap of decision strategies, taking from [[payne1993adaptive]], [[pfeiffer2012fundamentals]] and [[riedl2008identifying]]
- Alternative [[process tracing]] including [[Mouselab]], [[Active Information Search]], and [[Eye tracking for process tracing]].
- Overview of process-tracing methods, by [[riedl2008identifying]] and [[schulte-mecklenbeck2017processtracing]]
- The problems of interpreting estimation of model parameters when estimated using participant average responses, rather than individual responses, as outlined in [[estes1956problem]], [[estes2005risks]], [[estes2002traps]] and [[heathcote2000power]]
- A couple of mentions of the [[cooper2019investigating]] paper to bump cites
- Some discussion of sequential sampling models, drawing on [[ratcliff2016diffusion]]
- Adding to SSM approaches to preferential choice, other methods include: [[krajbich2011multialternative]] and [[busemeyer1993decision]]
- Some work on visual fixations on [[binary-attribute choice]] is the [[fisher2017attentional]] paper that looks at combinations of aversive and appetitive foods as a single option that people are asked to accept or reject.
## Decision strategies

Mentioned and referenced the [[Conjunctive Strategy]], [[Disjunctive Strategy]] and [[Satisficing Heuristic]] for non-compensatory strategies, and the [[Frequency of Good and-or Bad Features Heuristic]] and [[Weighted Additive Rule]] for compensatory strategies. Probably need to look into complete vs selective strategies a bit more and think more on single option variants of other strategies.


# Reviews meeting

Intercept and scale for modelling requested in comment 1 by Reviewer 1. Could mean negative mean drift rate. Investigate how the likelihood would change. Parameters would be constrained much more. This would assume linear scaling. There is a lot of cases where the scaling would not be linear (inverted U on price perhaps) and we did not want to build those assumptions into the model (this is why we chose our method).

R1C2 wanted more individual PP plots for choice proportions and more on RTs. Show more than the means in the RT figures. For cells with little data (include per cell anyone who has at least 5 responses for the infrequent responses - and only medians) maybe not visualise and justify based on lack of data. Distributional RT plots, accepts and rejects should perhaps be split by accept/reject and have median + x quantiles.

For the individual participant version (supplement) each person would have one of the two halves (Acc or Rej condition). Just running the code up to one step before.

R2 RT comments. Use Marley/Hawkins inspired likelihood of LBA where probabilities are integrated across time. This would be **very** slow but not too difficult. Or I could reqrite the likelihood to collapse and run the same call twice per cell (Only call the integrate for each accept/reject response type).


## References of note

- [[broder2003bayesian|Bayesian strategy assessment in multi-attribute decision making]]
- [[corbin1974random|Random utility models with equality: An apparent, but not actual, generalization of random utility models]]
- [[eidels2010converging|Converging measures of workload capacity]]
- [[gigerenzer2001simple|Simple heuristics that make us smart]]
- [[gilbride2004choice|A Choice Model with Conjunctive, Disjunctive, and Compensatory Screening Rules]]
- [[heathcote2000power|The power law repealed: The case for an exponential law of practice]]
- [[lee2016bayesian|Bayesian outcome-based strategy classification]]
- [[lee2023risky|Risky decisions are influenced by individual attributes as a function of risk preference]]
- [[manzini2014stochastic|Stochastic Choice and Consideration Sets]]
- [[murre2023how|How averaging individual curves transforms their shape: Mathematical analyses with application to learning and forgetting curves]]
- [[oh2016satisficing|Satisficing in split-second decision making is characterized by strategic cue discounting.]]
- [[lee2019understanding|Understanding the complexity of simple decisions: Modeling multiple behaviors and switching strategies]]
- [[lee2004evidence|Evidence accumulation in decision making: Unifying the “take the best” and the “rational” models]] Marrying [[Take the Best]] and rational models of decision making.
- [[schulze2021who|Who you know is what you know: Modeling boundedly rational social sampling.]] Details/comparison to my latent mixture approach.
- [[pachur2017how|How the twain can meet: Prospect theory and models of heuristics in risky choice]]. Some latent mixture approaches here, but also the intersection of different models of decision making being integrated.