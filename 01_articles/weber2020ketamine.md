---
cssclasses:
  - research_note
type: journalArticle
author: Weber, Lilian A.; Diaconescu, Andreea O.; Mathys, Christoph; Schmidt, André; Kometer, Michael; Vollenweider, Franz; Stephan, Klaas E.
title: "Ketamine Affects Prediction Errors about Statistical Regularities: A Computational Single-Trial Analysis of the Mismatch Negativity"
publication: The Journal of Neuroscience
date: 2020-07-15
citekey: weber2020ketamine
aliases:
  - "Ketamine Affects Prediction Errors about Statistical Regularities: A Computational Single-Trial Analysis of the Mismatch Negativity"
---

# Ketamine Affects Prediction Errors about Statistical Regularities: A Computational Single-Trial Analysis of the Mismatch Negativity

Weber, L. A., Diaconescu, A. O., Mathys, C., Schmidt, A., Kometer, M., Vollenweider, F., & Stephan, K. E. (2020). Ketamine Affects Prediction Errors about Statistical Regularities: A Computational Single-Trial Analysis of the Mismatch Negativity. _The Journal of Neuroscience_, _40_(29), 5658–5668. [https://doi.org/10.1523/JNEUROSCI.3069-19.2020](https://doi.org/10.1523/JNEUROSCI.3069-19.2020)
[online](http://zotero.org/users/local/kZl3QdXV/items/UJ9QXQD4) [local](zotero://select/library/items/UJ9QXQD4) [pdf](file:///home/gjc216/Zotero/storage/GPXXZBPY/Weber%20et%20al.%20-%202020%20-%20Ketamine%20Affects%20Prediction%20Errors%20about%20Statistic.pdf)
 


## My Thoughts

This approach seems to be what we want for the [[Hierarchical Gaussian Filter|HGF]] analysis of the primacy data. We will clean the EEG data, but then separately fit the HGF using [[tapas]] to the data sequence. Then somehow combine the optimal HGF fits with the ERP data.
 
Provides some resources for thinking about the [[HGF analysis of MMN]]
### Annotations

%% begin annotations %%
##### Imported on 2023-08-23 11:57 am
>[!quote|#ffd400]
>We rejected all trials overlapping with eye blink events, as detected by a thresholding routine on the vertical EOG channel, which was created from subtracting the activity of two additional electrodes that were attached infraorbitally and supraorbitally to the left eye. Finally, an artifact rejection procedure was applied using a thresholding approach on all EEG channels to detect problematic trials or channels. Trials in which the signal recorded at any of the channels exceeded 80mVrelativetothe prestimulus baseline were removed from subsequent analysis, and channels in which .20% of trials had to be rejected were marked as bad and subsequently interpolated for sensor-level statistics. [(p. 5660)](zotero://open-pdf/library/items/GPXXZBPY?page=5660&annotation=VJVKGVPS)

---
>[!quote|#ffd400]
>To estimate these parameters, we used the MATLAB function tapas_fitModel from the HGF toolbox (version 4.0), distributed as part of TAPAS (release version 1.6) with the tapas_ bayes_optimal_whatworld function as a pseudoresponse model. [(p. 5660)](zotero://open-pdf/library/items/GPXXZBPY?page=5660&annotation=5QRTSKD6)

---
>[!quote|#ffd400]
>Specifically, we defined “standards” and “deviants” as those trials with the 10% lowest and 10% highest precision-weighted PEs, respectively, according to our model. [(p. 5661)](zotero://open-pdf/library/items/GPXXZBPY?page=5661&annotation=VJUVNSPW)

---%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/schizophrenia #subject/predictive_coding

##### Authors

#author/weber_lilian_a. #author/diaconescu_andreea_o. #author/mathys_christoph #author/schmidt_andré #author/kometer_michael #author/vollenweider_franz #author/stephan_klaas_e.

##### Publication

#pub/j_neurosci


%% Import Date: 2023-08-23T11:57:26.539+10:00 %%
