---
cssclass: research_note
type: "journalArticle"
author: "van Geen, Camilla; Gerraty, Raphael T."
title: "Hierarchical Bayesian models of reinforcement learning: Introduction and comparison to alternative methods"
publication: "Journal of Mathematical Psychology"
date: 2021-12-01
citekey: vangeen2021hierarchical
aliases: 
    - "Hierarchical Bayesian models of reinforcement learning: Introduction and comparison to alternative methods"
---

# Hierarchical Bayesian models of [[reinforcement learning]]: Introduction and comparison to alternative methods

van Geen, C., & Gerraty, R. T. (2021). Hierarchical Bayesian models of reinforcement learning: Introduction and comparison to alternative methods. _Journal of Mathematical Psychology_, _105_, 102602. [https://doi.org/10.1016/j.jmp.2021.102602](https://doi.org/10.1016/j.jmp.2021.102602)
[online](http://zotero.org/users/7162438/items/GBLG4DMX) [local](zotero://select/library/items/GBLG4DMX) [pdf](file:///home/gjc216/Zotero/storage/DK629KXJ/1-s2.0-S0022249621000742-main.pdf)
 

 
%% begin notes %%

## My Thoughts

This ties in quite nicely with my [[Architecture of MultiAttribute Choice]] paper, as the strengths of hierarchical estimation of a cognitive model is something stressed in my paper.

There is also a nice easy introduction to the [[Q-learning]] model (with $\alpha$ learning rate and $\beta$ _inverse decision temperature_). I think the approach used in a lot of this paper of estimating on 3/4 of the data and then getting log-likelihoods on the remaining quarter sounds interesting, but I'm not sure how viable it would be for my work, as the complexity of my model means I want every scrap of data used in estimation. Luckily, the winning approach in this case seems to be fully hierarchical, with all data used in the estimation.

A lot of talk here about the priors used in the modelling, which is definitely sommehting I should be more considerate of in my own work.

Regarding the work on the [[Hypatia Work|Hypatia Health Beta app]] , therte are a number of good resources here in terms of data that could be used for testing, informed priors, and specifications of the models. 
%% end notes %%

### Annotations

%% begin annotations %%

##### Imported on 2024-07-26 6:27 pm
>[!quote|#ffd400]
>n this review, we will narrow the scope even further, to those RL models that describe how humans (and other organisms) learn behavioral policies from rewards [(p. 2)](zotero://open-pdf/library/items/DK629KXJ?page=2&annotation=JAM8S6JB)

---
>[!quote|#5fb236]
>The learning rate (α) determines the extent to which prediction error will play a role in updating an action’s value. [(p. 2)](zotero://open-pdf/library/items/DK629KXJ?page=2&annotation=Q37YHLTM)

---
>[!quote|#5fb236]
>This tendency is governed by an inverse temperature parameter (β) whose magnitude determines the impact of value on choice. [(p. 2)](zotero://open-pdf/library/items/DK629KXJ?page=2&annotation=K89E5CD7)

---
>[!quote|#5fb236]
>In the context of RL models, different combinations of parameter values can sometimes fit a subject’s data similarly well. If this is the case, differences between these plausible sets of parameters will in part be due to noise, and are unlikely to replicate out-of-sample. [(p. 2)](zotero://open-pdf/library/items/DK629KXJ?page=2&annotation=P2QXGX7S)

---
>[!quote|#ffd400]
>We used the data from Gershman (2015) – available at https: //github.com/sjgershm/RL-models – to fit this model. The dataset consists of choice behavior from 205 participants pooled across five different studies, each consisting of four 25-trial blocks. In all five studies, participants were instructed to choose one of two colored buttons, based on which one they believed had a higher expected reward. [(p. 3)](zotero://open-pdf/library/items/DK629KXJ?page=3&annotation=9GSUQJGJ)

---
>[!quote|#5fb236]
>Accordingly, the hyperpriors on individual learning rates (contained in the αn vector), inverse temperatures, intercepts, and stickiness (contained in the βn matrix) were specified as follows: αn ∽ Beta (0.5, 0.5) βn ∽ N (0, 52) This approach essentially fits separate reinforcement learning models to each subject, and only constrains these estimates with weakly informative hyperprior distributions. It is perhaps the most common method for fitting reinforcement learning models in the literature (Davidow et al., 2016; Daw, 2011; Dezfouli & Balleine, 2013; Niv et al., 2015, 2012). [(p. 6)](zotero://open-pdf/library/items/DK629KXJ?page=6&annotation=U2SISH4T)

---
>[!quote|#ffd400]
>Given the prevalence of these methods, the extraction of reliable parameter estimates is crucial: the strength of a study’s conclusions is contingent on the stability of the estimated parameters (but see Wilson and Niv (2015) for an interesting counterpoint) [(p. 9)](zotero://open-pdf/library/items/DK629KXJ?page=9&annotation=C43CZKW3)

---%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/bayesian_statistics #subject/model_comparison [[reinforcement learning]]

##### Authors

[[Camilla van Geen]] [[Raphael T. Gerraty]]

##### Publication

[[Journal of Mathematical Psychology]]


%% Import Date: 2024-07-26T18:27:20.751+01:00 %%
