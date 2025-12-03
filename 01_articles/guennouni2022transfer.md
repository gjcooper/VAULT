---
cssclasses:
    - research_note
type: "journalArticle"
author: "Guennouni, Ismail; Speekenbrink, Maarten"
title: "Transfer of Learned Opponent Models in Zero Sum Games"
publication: "Computational Brain & Behavior"
date: 2022-09-01
citekey: guennouni2022transfer
aliases: 
    - "Transfer of Learned Opponent Models in Zero Sum Games"
---

# Transfer of Learned Opponent Models in Zero Sum Games

Guennouni, I., & Speekenbrink, M. (2022). Transfer of Learned Opponent Models in Zero Sum Games. _Computational Brain & Behavior_, _5_(3), 326–342. [https://doi.org/10.1007/s42113-022-00133-6](https://doi.org/10.1007/s42113-022-00133-6)
[online](http://zotero.org/users/7162438/items/9MNQWBPW) [local](zotero://select/library/items/9MNQWBPW) [pdf](file:///home/gjc216/Zotero/storage/B8NALG4P/Guennouni%20and%20Speekenbrink%20-%202022%20-%20Transfer%20of%20Learned%20Opponent%20Models%20in%20Zero%20Sum%20Games.pdf)
 

 
%% begin notes %%

## My Thoughts

A nice paper on the tansfer of learning about an opponents strategy into new contexts.

There are some interested results on repeated games against the same opponent here, using simple rock-paper-scissors (and variants of) games. A lot of the discussion revolves around the reasoning about an opponents strategy, which while not mentioned directly seems to coincide with [[Joseph Barnby]]'s work on tests of [[theory of mind]] that move away from the old sally-anne tasks.

Surprising the papers authors the results on the face of it show a simple [[reinforcement learning]] model as winning via model selection over the alterative iterative [[Cognitive Hierarchy theory]] - even though the reinforcement learning seem to not explain the improvement in participant performance across tasks (is RL does not allow for transfer of learning).

On diving deeper the authors use a hidden Markov model that allows for switching between the more complex Bayesian Cognitive Hierarchy model (at the start of a new game) and the simpler heuristic of an RL model.

#### Model fits

Fit to individual data using [[Maximum Likelihood]] estimation (MLE) in the DEoptim package.

%% end notes %%

### Annotations

%% begin annotations %%

##### Imported on 2025-11-06 10:34 am
>[!quote|#ffd400]
>[[Cognitive Hierarchy theory]] is based on similar principles, but rather than assuming an opponent always adopts a particular level-k strategy, they are assumed to adopt each of the level-k strategies with a particular probability (i.e.the opponent’s strategy is a mixture over pure level-k strategies). [(p. 327)](zotero://open-pdf/library/items/B8NALG4P?page=327&annotation=XB5C2B28)

---
>[!quote|#ffd400]
>As discussed in the introductory section on computational models, the self-tuning Experience-Weighted Attrac-tion (EWA) model combines two seemingly differentapproaches, namely reinforcement learning and belief learning [(p. 334)](zotero://open-pdf/library/items/B8NALG4P?page=334&annotation=YZCJSW56)

---
>[!quote|#ffd400]
>In what we call the [[Bayesian Cognitive Hierarchy]] (BCH) model, the participant attempts to learn the type of opponent they are facing through Bayesian learning. For present purposes, we assume participants consider the opponent could be either a level 0, level 1, or level 2 player, and start with a prior belief that each of these types is equally likely. [(p. 335)](zotero://open-pdf/library/items/B8NALG4P?page=335&annotation=L858H5X6)

---
>[!quote|#5fb236]
>DEoptim R package [(p. 335)](zotero://open-pdf/library/items/B8NALG4P?page=335&annotation=DYQH3MIH)

---
>[!quote|#ffd400]
>We use [[hidden Markov model]]s to test for strategy switching in participants’ play. In these models, the three strategies (RL, BCH with between-game transfer, and Nash) correspond to latent states which determine the overt responses (actions chosen). [(p. 337)](zotero://open-pdf/library/items/B8NALG4P?page=337&annotation=UU2KJY3Z)

---%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/artificial_intelligence #subject/bayesian_cognitive_hierarchy #subject/computational_economics #subject/game_theory #subject/hidden_markov_models #subject/learning_theory #subject/learning_transfer #subject/machine_learning #subject/model_theory #subject/opponent_modelling

##### Authors

[[Ismail Guennouni]] [[Maarten Speekenbrink]]

##### Publication

#pub/comput_brain_behav


%% Import Date: 2025-11-06T10:34:53.016+11:00 %%
