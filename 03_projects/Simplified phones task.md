# Simplified Phones task

This task is designed to act as a link between simpler binary choice (single option, double attribute) analyses for the [[Exemplar-based consumer choice model|EB-CCM]], and more complex stimuli like the [[Multidimensional Scaling Phones|MDS Phones]] task with > 1 option and > 2 attributes.

The initial goal of this task is to interleave short blocks of trials with one of two possible trial types, either:
- a single option and two attributes, with instructions similar to "Please choose whether you would consider this phone (Accept) or not (Reject)".
- two options and two attributes, with instructions similar to "Please choose the option you prefer between the two shown below".

Other design aspects are that the order of attributes should be stable for each participant, but randomly chosen between participants. The order of block presentation (Single, Double, Single, Double, ...) should be alternating, but the first presented block should be counterbalanced between participants.

Initial pilots will use 150 trials each of the single option and double option types, to see how long it will take. The single option trials will be randomly sampled from the price and memory attribute values (minus the 1000Gb memory phone due to the fact that this phone does not match the exponentially increasing pattern from the other phone memory values). The double option trials will be sampled randomly from pairwise combinations of the single option stimuli. See https://github.com/CooperAcademia/SimplifiedPhones2023/blob/main/design_scripts/attribute_investigation.Rmd for an investigation of this effect.

## Some relevant meeting notes

2023-07-19
In a quick meeting with Guy we discussed the values chosen to form the options for the [[Simplified phones task]]. Elements we discussed were whether to use the real phones as a defined subset of the phones selected as options (No). We also discussed the double option trials and whether they are sampled purely randomly from all possibilities or if they are based on the option chosen for the single option case.

2023-08-03
Thoughts during analysis of the [[Simplified phones task]] initial data.
- I probably want to put in a block number for each trial as this will help with some possible analysis avenues.
- Analysis for the parameter estimates of the ML method of recovering [[Exemplar-based consumer choice model|GCM inspired analysis]] to see if there are bimodal groups, or whether a single normal distribution over people would be sufficient.
