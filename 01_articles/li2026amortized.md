---
cssclasses:
    - research_note
type: "preprint"
author: "Li, Chengkun; Vehtari, Aki; Bürkner, Paul-Christian; Radev, Stefan T.; Acerbi, Luigi; Schmitt, Marvin"
title: "Amortized Bayesian Workflow"
date: 2026-02-17
citekey: li2026amortized
aliases: 
    - "Amortized Bayesian Workflow"
---

# Amortized Bayesian Workflow

Li, C., Vehtari, A., Bürkner, P.-C., Radev, S. T., Acerbi, L., & Schmitt, M. (2026). _Amortized Bayesian Workflow_ (arXiv:2409.04332; Version 3). arXiv. [https://doi.org/10.48550/arXiv.2409.04332](https://doi.org/10.48550/arXiv.2409.04332)
[online](http://zotero.org/users/7162438/items/IID83I4F) [local](zotero://select/library/items/IID83I4F) [pdf](file:///home/gjc216/Zotero/storage/EBGLEGIY/Li%20et%20al.%20-%202026%20-%20Amortized%20Bayesian%20Workflow.pdf)
 

 
%% begin notes %%

## My Thoughts

Preprint behind [[BayesFlow]] software.

Amortised (computation is front-loaded during training, fast inference with new datasets).

Steps:
- Step 0, train on simulated data from a model
- Step 1, Use Amortised Bayesian Inference, check whether new dataset is sufficiently similar to simulated datasets using metrics such as Mahalanobis distance. If bad, move to
- Step 2: Use Pareto-Smoothed Importance Sampling, use Pareto-k to check whether fits are improved. If not, move to
- Step 3: Use a full MCMC (they use ChEES-HMC) to run full inference.


What is this useful for? Large company - many, many datasets with short timeframe for analysis - think Netflix running simple model on consumer behaviour looking to provide real-time suggestions type stuff. Might not be the best for hierarchical modelling.

#### How do they know this?

#### What would I need to believe to accept this argument?

#### What questions does this raise that aren’t addressed?

%% end notes %%

### Annotations

%% begin annotations %%
%% end annotations %%

---
## Item Notes

##### Note added on 2026-08-03 10:12 am

Comment: Accepted in Transactions on Machine Learning Research

---
#### Tags

##### Keywords

#subject/computer_science_-_machine_learning #subject/statistics_-_machine_learning

##### Authors

[[Chengkun Li]] [[Aki Vehtari]] [[Paul-Christian Bürkner]] [[Stefan T. Radev]] [[Luigi Acerbi]] [[Marvin Schmitt]]

##### Publication




%% Import Date: 2026-08-03T15:04:08.705+10:00 %%
