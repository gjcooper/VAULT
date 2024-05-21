---
cssclass: research_note
type: "journalArticle"
author: "Schlossmacher, Insa; Lucka, Felix; Peters, Antje; Bruchmann, Maximilian; Straube, Thomas"
title: "Effects of awareness and task relevance on neurocomputational models of mismatch negativity generation"
publication: "NeuroImage"
date: 2022-11-01
citekey: schlossmacher2022effects
aliases: 
    - "Effects of awareness and task relevance on neurocomputational models of mismatch negativity generation"
---

# Effects of awareness and task relevance on neurocomputational models of mismatch negativity generation

Schlossmacher, I., Lucka, F., Peters, A., Bruchmann, M., & Straube, T. (2022). Effects of awareness and task relevance on neurocomputational models of mismatch negativity generation. _NeuroImage_, _262_, 119530. [https://doi.org/10.1016/j.neuroimage.2022.119530](https://doi.org/10.1016/j.neuroimage.2022.119530)
[online](http://zotero.org/users/local/kZl3QdXV/items/B3BAAXZJ) [local](zotero://select/library/items/B3BAAXZJ) [pdf](file:///home/gjc216/Zotero/storage/FD5DKETK/Schlossmacher%20et%20al.%20-%202022%20-%20Effects%20of%20awareness%20and%20task%20relevance%20on%20neuroco.pdf)
 


## My Thoughts

The application here is again single trial EEG, with [[Hierarchical Gaussian Filter|HGF]], with some possible application to our [[HGF analysis of MMN]], especially considering the application in this paper is also to [[Mismatch Negativity|MMN]].

One "major" note here is that the way EEG data is combined with the modelling seems quite different to the approaches of [[weber2020ketamine]] or [[hauke2023aberrant]] as they seem to model whole brain spatial measures derived from the EEG (I think) where here the single trial EEG is transformed to a single? number using a previously applied clustering algorithm to get an appropriate time window (and possibly selection of electrodes), and then from the peak and average around the peak of the mismatch waveform is used as input to the modelling.
 
### Annotations

%% begin annotations %%

##### Imported on 2024-02-09 4:53 pm
>[!quote|#ffd400]
>Computational modeling offers a unique way to investigate the underlying mechanisms by comparing predictors stemming from different models with single-trial ERP estimates [(p. 2)](zotero://open-pdf/library/items/FD5DKETK?page=2&annotation=TM7DLVQ2)

---
>[!quote|#ffd400]
>Preprocessing of the EEG data was performed using the FieldTrip toolbox (Oostenveld et al., 2010) in MATLAB. [(p. 3)](zotero://open-pdf/library/items/FD5DKETK?page=3&annotation=WB6MHY6Z)

---
>[!quote|#ffd400]
>For the oddball contrasts, trials of each subject were averaged separately for deviants and standards. We used the standard stimuli prior to deviants for the standard average allowing us to average equal amounts of stimuli per condition. [(p. 3)](zotero://open-pdf/library/items/FD5DKETK?page=3&annotation=NBUGZEJQ)

---
>[!quote|#ffd400]
>Individual single-trial amplitudes were extracted using the results of the cluster-based permutation. All electrodes included in the significant vMMN cluster were averaged and an individual difference wave was computed for each participant and phase. Then, the largest negative peak of the difference wave during the time window of the significant cluster (150 – 350 ms) was determined. [(p. 4)](zotero://open-pdf/library/items/FD5DKETK?page=4&annotation=5C3WUKNX)

---
>[!quote|#ffd400]
>single-trial estimates (y) were computed as the average amplitude ± 25 ms around the peak, i.e., the time window amounted to 50 ms. All artifact-free trials were used for the single-trial analysis, i.e., in contrast to the ERP analysis, we included all standard trials. [(p. 5)](zotero://open-pdf/library/items/FD5DKETK?page=5&annotation=AZ4J9NSA)

---
>[!quote|#5fb236]
>We based our computational modeling approach on Lieder et al. (2013), [(p. 5)](zotero://open-pdf/library/items/FD5DKETK?page=5&annotation=3IPNGC6S)

---
>[!quote|#5fb236]
>The precision-weighted prediction error predictor (pwPE) was derived using the freely available HGF toolbox (Mathys, 2011; Stefanics et al., 2018; Weber et al., 2020), which can be downloaded from http://www.translationalneuromodeling.org/tapas. [(p. 5)](zotero://open-pdf/library/items/FD5DKETK?page=5&annotation=C4XP7RYF)

---
>[!quote|#ffd400]
>tapas_hgf_binary_config, tapas_gaussian_obs and tapas_quasinewton_optim_config (TAPAS release 3.2/HGF version 5.3). [(p. 5)](zotero://open-pdf/library/items/FD5DKETK?page=5&annotation=MQMDAC9A)

---
>[!quote|#ffd400]
>This procedure allowed the HGF to fit the pwPE with an appropriate decay similar to the parameters of the adaptation model. [(p. 5)](zotero://open-pdf/library/items/FD5DKETK?page=5&annotation=YRRFNDB4)

---%% end annotations %%

## Item Notes

#### Tags

##### Keywords



##### Authors

#author/schlossmacher_insa #author/lucka_felix #author/peters_antje #author/bruchmann_maximilian #author/straube_thomas

##### Publication

#pub/neuroimage


%% Import Date: 2024-02-09T16:54:03.894+11:00 %%
