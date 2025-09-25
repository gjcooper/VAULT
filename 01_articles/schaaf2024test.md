---
cssclasses:
  - research_note
type: journalArticle
author: Schaaf, Jessica V.; Weidinger, Laura; Molleman, Lucas; van den Bos, Wouter
title: Test–retest reliability of reinforcement learning parameters
publication: Behavior Research Methods
date: 2024-08-01
citekey: schaaf2024test
aliases:
  - Test–retest reliability of reinforcement learning parameters
---

# Test–retest reliability of reinforcement learning parameters

Schaaf, J. V., Weidinger, L., Molleman, L., & van den Bos, W. (2024). Test–retest reliability of reinforcement learning parameters. _Behavior Research Methods_, _56_(5), 4582–4599. [https://doi.org/10.3758/s13428-023-02203-4](https://doi.org/10.3758/s13428-023-02203-4)
[online](http://zotero.org/users/7162438/items/E9E767YC) [local](zotero://select/library/items/E9E767YC) [pdf](file:///home/gjc216/Zotero/storage/ILQGKUXF/Schaaf%20et%20al.%20-%202024%20-%20Test–retest%20reliability%20of%20reinforcement%20learning%20parameters.pdf)
 

 
%% begin notes %%

## My Thoughts

This is an important message about the test-retest reliability of reinforcement learning models, especially as us at [[Hypatia Health]] look to promote the use of [[reinforcement learning]] modelling as a way of moving towards more personalised medicine.

There are a number of things here, first I would like to learn more about the [[Intraclass Correlation Coefficient|ICC]] measure here used to indicate [[test-retest reliability]] as I don't know that I fully understand it.

Several of the calls for future directions definitely appeal to me, including metioning the integration of response times as a way of possibly adding extra reliability, one particular mention was [[Steven Miletić]]'s work on RL models with [[evidence accumulation models]] integrated. There was also a call to action of people wanting to use more advanced estimation methods, that made me think that throwing [[PMwG]] at the code, with its nice estimation of the covariance matrix directly could be a way of improving test-retest reliability.

%% end notes %%

### Annotations

%% begin annotations %%

##### Imported on 2024-09-25 12:43 pm
>[!quote|#5fb236]
>computational psychiatry (Adams et al., 2016; Friston et al., 2014; Huys et al., 2011, 2016; Maia & Frank, 2011; Montague et al., 2012; Paulus et al., 2016; Petzschner et al., 2017; Stephan et al., 2017; Wang & Krystal, 2014). [(p. 4583)](zotero://open-pdf/library/items/ILQGKUXF?page=4583&annotation=5PII788B)

---
>[!quote|#5fb236]
>However, in order to use individual model parameters for cognitive phenotyping, there are still several key challenges to be met (Eckstein et al., 2021; Patzelt et al., 2018; Stephan et al., 2017). [(p. 4583)](zotero://open-pdf/library/items/ILQGKUXF?page=4583&annotation=LTUQH3SV)

---
>[!quote|#ffd400]
>However, good test–retest reliability was found in a predictive-inference task in which learning rates were derived directly from observed predictions (Loosen et al., 2022; reliabilities ranging from .74 to .82). [(p. 4583)](zotero://open-pdf/library/items/ILQGKUXF?page=4583&annotation=G8E3PEXX)

---
>[!quote|#5fb236]
>oftenused learning tasks in computational psychiatry and aging research (see Fig. 1): a two-armed bandit task (Frank et al., 2004; Pessiglione et al., 2006) and a reversal learning task (Cools et al., 2002; Schlagenhauf et al., 2014) [(p. 4583)](zotero://open-pdf/library/items/ILQGKUXF?page=4583&annotation=JIB549F8)

---
>[!quote|#5fb236]
>group-level precision values between 2 and 600 (Steingroever et al., 2014) [(p. 4587)](zotero://open-pdf/library/items/ILQGKUXF?page=4587&annotation=NXEWWUCV)

---
>[!quote|#ffd400]
>The first striking result is that the parameter reliability and agreement for the MLE fitted models is extremely poor for all parameters, except for inverse temperature (τ) in the dual RL kDU model (see Table 2). Although, at least for the dual RL model, reliability and agreement are better for MAP and hBayes, for all parameters except the τ, reliability and agreement still qualify as poor. [(p. 4589)](zotero://open-pdf/library/items/ILQGKUXF?page=4589&annotation=C8G6JTDN)

---
>[!quote|#ffd400]
>As such, these results suggest that the hBayes method outperforms the other methods when estimating the parameters of more complex models. [(p. 4589)](zotero://open-pdf/library/items/ILQGKUXF?page=4589&annotation=MZB5U98D)

---
>[!quote|#ffd400]
>earning data set and whether this held for the bandit task. To do so, we fitted joint hBayes models with and without a parameter for the correlation between parameters (αgain, αloss, κ, and τ) across time points to data from the two learning tasks and assessed their model fit. [(p. 4593)](zotero://open-pdf/library/items/ILQGKUXF?page=4593&annotation=P5UGLY6H)

---
>[!quote|#ffd400]
>Specifically, the stochastic nature of the feedback in both tasks and the choice-dependent reversal rule in the reversal learning task may have affected task dynamics. [(p. 4594)](zotero://open-pdf/library/items/ILQGKUXF?page=4594&annotation=CBE547UN)

---
>[!quote|#ffd400]
>A second possibility is that participants truly differed across time points, due to either trait-like or state-like factors. [(p. 4595)](zotero://open-pdf/library/items/ILQGKUXF?page=4595&annotation=588AE4ML)

---
>[!quote|#ffd400]
>Future studies are advised to estimate individual learning strategies, for example, by using mixture modeling (e.g., Bartlema et al., 2014; Schaaf et al., 2019),  to assess how stable these strategies are across time points, and whether they change during the task. [(p. 4595)](zotero://open-pdf/library/items/ILQGKUXF?page=4595&annotation=I49DEWB7)

---
>[!quote|#ffd400]
>First, identifiability could be further improved, for example by increasing the number of administered trials (e.g., Shahar et al., 2019) or by jointly modeling multiple data sources (e.g., response times or neural data; Ballard & McClure, 2019; Fontanesi et al., 2019; Miletić et al., 2021; Pedersen et al., 2017; Shahar et al., 2019; Turner et al., 2013, 2016). [(p. 4595)](zotero://open-pdf/library/items/ILQGKUXF?page=4595&annotation=UHEDFD82)

---
>[!quote|#ffd400]
>We also invite them to use our dataset if they believe they have analytical tools at their disposal that may allow for better estimates that result in higher reliability (https://osf.io/pe23t/). [(p. 4596)](zotero://open-pdf/library/items/ILQGKUXF?page=4596&annotation=IBDWMBHS)

---%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/computational_modeling #subject/reinforcement_learning #subject/computational_phenotyping #subject/computational_psychiatry #subject/test–retest_reliability

##### Authors

[[Jessica V. Schaaf]] [[Laura Weidinger]] [[Lucas Molleman]] [[Wouter van den Bos]]

##### Publication

#pub/behav_res


%% Import Date: 2024-09-25T12:43:15.384+10:00 %%
