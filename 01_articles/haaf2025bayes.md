---
cssclasses:
    - research_note
type: "journalArticle"
author: "Haaf, Julia M.; Klaassen, Fayette; Rouder, Jeffrey N."
title: "Bayes Factor vs. Posterior Predictive Model Assessment: Insights from Ordinal Constraints"
publication: "Computational Brain & Behavior"
date: 2025-09-01
citekey: haaf2025bayes
aliases: 
    - "Bayes Factor vs. Posterior Predictive Model Assessment: Insights from Ordinal Constraints"
---

# Bayes Factor vs. Posterior Predictive Model Assessment: Insights from Ordinal Constraints

Haaf, J. M., Klaassen, F., & Rouder, J. N. (2025). Bayes Factor vs. Posterior Predictive Model Assessment: Insights from Ordinal Constraints. _Computational Brain & Behavior_, _8_(3), 493–502. [https://doi.org/10.1007/s42113-025-00240-0](https://doi.org/10.1007/s42113-025-00240-0)
[online](http://zotero.org/users/7162438/items/WNCKDXL8) [local](zotero://select/library/items/WNCKDXL8) [pdf](file:///home/gjc216/Zotero/storage/KVIQAVCG/Haaf%20et%20al.%20-%202025%20-%20Bayes%20Factor%20vs. Posterior%20Predictive%20Model%20Assessment%20Insights%20from%20Ordinal%20Constraints.pdf)
 

 
%% begin notes %%

## My Thoughts

Haaf et al discuss the appropriate tools to use when comparing cognitive models. In particular they focus on un-intuitive results from model selection techniques such as the [[WAIC]], [[DIC]] and [[Leave One Out Cross Validation]]. These three tools are methods of [[posterior predictive model selection]] that use posterior estimates to make predictions about new data, and then compare that to existing data.

These methods all create issues when selecting between a nested model. For example when selecting between a model that assumes a positive value for a parameter and one that places no constraints on that same parameter. In this case, even when the estimate for the parameter in both models is high, the case for selecting the positive model over the unconstrained model approaches approaches 0. (As a difference say between each models WAIC) 
#### How do they know this?

It is never (as far as I can tell) explicitly stated,  but my impression is they ran simulations with different parameter values, extracting model fits and model selection criteria on values along a spectrum.

#### What would I need to believe to accept this argument?

I find it bvelievable as is, however running the simulations myself would help.
#### What questions does this raise that aren’t addressed?

[[Bayes Factor]]s can be expensive - especially when there is no analytical solution for the cognitive model. Are there other options that do not include this bias, or other ways to correct this bias that do not require the full Bayes Factor calculations.

%% end notes %%

### Annotations

%% begin annotations %%
%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/bayes_factor #subject/bayesian_inference #subject/ordinal-constrained_inference #subject/watanabe-akaike_information_criterion

##### Authors

[[Julia M. Haaf]] [[Fayette Klaassen]] [[Jeffrey N. Rouder]]

##### Publication

#pub/comput_brain_behav


%% Import Date: 2026-01-05T15:40:07.670+11:00 %%
