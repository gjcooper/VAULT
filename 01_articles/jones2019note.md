---
cssclasses:
    - research_note
type: "journalArticle"
author: "Jones, Pete R."
title: "A note on detecting statistical outliers in psychophysical data"
publication: "Attention, Perception, & Psychophysics"
date: 2019-07-14
citekey: jones2019note
aliases: 
    - "A note on detecting statistical outliers in psychophysical data"
---

# A note on detecting statistical outliers in psychophysical data

Jones, P. R. (2019). A note on detecting statistical outliers in psychophysical data. _Attention, Perception, & Psychophysics_, _81_(5), 1189–1196. [https://doi.org/10.3758/s13414-019-01726-3](https://doi.org/10.3758/s13414-019-01726-3)
[online](http://zotero.org/users/7162438/items/CVCGP353) [local](zotero://select/library/items/CVCGP353) [pdf](file:///home/gjc216/Zotero/storage/KWDFPHUN/Jones2019_Article_ANoteOnDetectingStatisticalOut.pdf)
 

 
%% begin notes %%

## My Thoughts

A short but nice comparison on various methods of [[outlier]] detection in psychophysical data. There are eight various methods discussed with both [[parametrc vs non-parametric methods|parametric and non-parametric]] methods discussed. These range from a simple SD method where a value is an outlier if it lies more that $\lambda$ deviations from the mean through to the winning method $\mathbf{S_n}$, which marks an outlier if the data point if the median distance of the point from all other points is greater that $\lambda$
times the median absolute distance of every point from every other point. [[MATLAB]] code is provided for an implementation of $\mathbf{S_n}$.

My thoughts on this paper more closely align with the final discussion point on whether the implement outlier removal in the first place. From the modelling perspective I would much rather add another model of behaviour to the analysis that at the very least has a small likelihood of spurious responses. Even better would be to have a contrasting model of behaviour that catches the dynamics or people not performing the task as expected.

%% end notes %%

### Annotations

%% begin annotations %%
%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/cognitive_neuroscience #subject/statistics

##### Authors

[[Pete R. Jones]]

##### Publication

#pub/attention_perception_and_psychophysics


%% Import Date: 2026-04-15T13:21:52.035+10:00 %%
