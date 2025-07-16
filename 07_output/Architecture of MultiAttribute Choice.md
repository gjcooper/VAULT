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

Intercept and scale for modelling requested in comment 1 by Reviewer 1. bCould mean negative mean drift rate. Investigate how the likelihood would change. Parameters would be constrained much more. This would assume linear scaling. There is a lot of cases where the scaling would not be linear (inverted U on price perhaps) and we did not want to build those assumptions into the model (this is why we chose our method).

R1C2 wanted more individual PP plots for choice proportions and more on RTs. Show more than the means in the RT figures. For cells with little data (include per cell anyone who has at least 5 responses for the infrequent responses - and only medians) maybe not visualise and justify based on lack of data. Distributional RT plots, accepts and rejects should perhaps be split by accept/reject and have median + x quantiles.

For the individual participant version (supplement) each person would have one of the two halves (Acc or Rej condition). Just running the code up to one step before.

R2 RT comments. Use Marley/Hawkins inspired likelihood of LBA where probabilities are integrated across time. This would be **very** slow but not too difficult. Or I could reqrite the likelihood to collapse and run the same call twice per cell (Only call the integrate for each accept/reject response type).