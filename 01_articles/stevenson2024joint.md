---
cssclass: research_note
type: "journalArticle"
author: "Stevenson, Niek; Innes, Reilly J.; Boag, Russell J.; Miletić, Steven; Isherwood, Scott J. S.; Trutti, Anne C.; Heathcote, Andrew; Forstmann, Birte U."
title: "Joint Modelling of Latent Cognitive Mechanisms Shared Across Decision-Making Domains"
publication: "Computational Brain & Behavior"
date: 2024-03-01
citekey: stevenson2024joint
aliases: 
    - "Joint Modelling of Latent Cognitive Mechanisms Shared Across Decision-Making Domains"
---

# Joint Modelling of Latent Cognitive Mechanisms Shared Across Decision-Making Domains

Stevenson, N., Innes, R. J., Boag, R. J., Miletić, S., Isherwood, S. J. S., Trutti, A. C., Heathcote, A., & Forstmann, B. U. (2024). Joint Modelling of Latent Cognitive Mechanisms Shared Across Decision-Making Domains. _Computational Brain & Behavior_, _7_(1), 1–22. [https://doi.org/10.1007/s42113-023-00192-3](https://doi.org/10.1007/s42113-023-00192-3)
[online](http://zotero.org/users/7162438/items/WMNUZJJB) [local](zotero://select/library/items/WMNUZJJB) [pdf](file:///home/gjc216/Zotero/storage/QFJXE2HD/Stevenson%20et%20al.%20-%202024%20-%20Joint%20Modelling%20of%20Latent%20Cognitive%20Mechanisms%20Sha.pdf)
 

 
%% begin notes %%

## My Thoughts

Some nice work here looking at using the [[PMwG]] package for joint model estimation on both _between-session_ runs of the same model, and _between-task_ runs of different models. For the _between-session_ joint modelling the PMwG does an admirable job for all tasks, with fairly high correlation between model parameters in the two sessions for all tasks except the [[RL-Rev]] task ([[reinforcement learning]] with reversal).
When looking at the _between-task_ joint modelling the number of parameters to estimate explodes (especially when you consider the estimation of the covariance matrix, i.e. number of covariance parameters = $N * (N-1)$ where $N$ is the number of group level parameters). To help with this they use a new hierarchical factor structure (an extension of PMwG) that models the loading of each group level covariance onto a predetermined number of factors.

The tasks include previously modelled work on reinforcement learning models with [[evidence accumulation models]] as the underpinning, with work by [[Steven Miletić]]. This includes the previously mentioned reversal RL as well as an RL task with [[Speed Accuracy trade-off]]. There are also two tasks with newly developed models, on called MSIT (Multi-source integration task) which uses combinations of [[Flanker task]] and [[Simon task]] stimuli together. The final task was a [[Reference back]] task that I still don't quite understand, it seems similar to an [[n-back task]], however there are different trials that indicate to the participant that they should perform a comparison (compare current trial to a previous trial) or reference trials where they should ?update? the reference stored in memory.



%% end notes %%

### Annotations

%% begin annotations %%

##### Imported on 2024-08-05 3:43 pm
>[!quote|#5fb236]
>whereas the accumulation process for valuebased decision-making may depend on subjective preference for alternate values (Ratcliff et al., 2016). [(p. 2)](zotero://open-pdf/library/items/QFJXE2HD?page=2&annotation=WNJ23FQG)

---
>[!quote|#5fb236]
>a reversal learning task (RL-Rev; Costa et al., 2015; Behrens et al., 2007; Mileti ́ c et al., 2021), [(p. 2)](zotero://open-pdf/library/items/QFJXE2HD?page=2&annotation=VPBXUFUR)

---
>[!quote|#5fb236]
>(4) a reinforcement learning speed-accuracy trade-off task (RL-SAT; Sewell et al., 2019; Mileti ́ c et al., 2021). [(p. 2)](zotero://open-pdf/library/items/QFJXE2HD?page=2&annotation=CEFP29DM)

---
>[!quote|#ffd400]
>We refer to this approach that explicitly accounts for relationships between parameters as the joint modelling covariance approach (Turner et al., 2017). [(p. 3)](zotero://open-pdf/library/items/QFJXE2HD?page=3&annotation=TPAF9AWJ)

---
>[!quote|#5fb236]
>Here   are the factor loadings and   describes the diagonal residuals of the variances. The exact details of this decomposition are described in Innes et al. (2022). [(p. 7)](zotero://open-pdf/library/items/QFJXE2HD?page=7&annotation=E3NZACQF)

---
>[!quote|#ffd400]
>Model comparisons were made using the Bayesian predictive information criterion (BPIC; Ando, 2007), rather than Bayes factor estimates using IS2, since in contrast to the joint models, the individual likelihoods were of main interest rather than the group-level distributions, in which case the BPIC is far more computationally efficient. [(p. 15)](zotero://open-pdf/library/items/QFJXE2HD?page=15&annotation=ZVBWH3GM)

---%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/decision-making #subject/cognitive_neuroscience #subject/bayesian_factor_analysis #subject/joint_modelling

##### Authors

[[Niek Stevenson]] [[Reilly J. Innes]] [[Russell J. Boag]] [[Steven Miletić]] [[Scott J. S. Isherwood]] [[Anne C. Trutti]] [[Andrew Heathcote]] [[Birte U. Forstmann]]

##### Publication

[[Computational Brain & Behavior]]

%% Import Date: 2024-08-05T15:43:27.493+10:00 %%
