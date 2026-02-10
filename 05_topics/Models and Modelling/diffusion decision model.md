---
aliases:
    - drift diffusion model
    - diffusion model
    - Wiener diffusion
    - DDM
---

The classic [[Roger Ratcliff]] diffusion model, and all its variants has had a large effect on the decision making literature, with many variants based on certain tasks and task requirements. It has variously been used to assist in many areas of decision making modelling. The paper [[ratcliff2016diffusion|Diffusion Decision Model: Current Issues and History]] covers the model in its standard form, along with areas of research it has been applied to.

The general concept is to assume that evidence is being accumulated over time, according to a diffusion drift rate. In the typical encoding of the model the responses are limited to a [[two-alternative forced choice]] response, with evidence accumulating towards one of two boundaries from some initial point.

The standard parameters are:
- The boundary separation parameter ($a$) that controls the amount of information required before triggering a response.
- The drift rate ($v$) which models the rate of information acquisition. Much of the academic work using the DDM attempts to explain behaviour through $a$ and/or $v$.
- There is also a non-decision time ($t_0$) which holds everything not directly part of the evidence accumulation process. This is generally said to be motor responses on the back end, and "raw" perception on the front end.
- There starting point parameter ($z$) that covers the location where the accumulation starts between 0 and $a$. Non-biased response are assumed to have a starting point of $a/2$.