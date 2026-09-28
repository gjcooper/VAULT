---
cssclasses:
    - research_note
type: "preprint"
author: "Howard, Zachary L; Miletic, Steven; Matzke, Dora; Heathcote, Andrew"
title: "Truncation and Censoring for Racing Evidence Accumulation Models"
citekey: howardtruncation
aliases: 
    - "Truncation and Censoring for Racing Evidence Accumulation Models"
---

# Truncation and Censoring for Racing Evidence Accumulation Models

Howard, Z. L., Miletic, S., Matzke, D., & Heathcote, A. (n.d.). _Truncation and Censoring for Racing Evidence Accumulation Models_.
[online](http://zotero.org/users/7162438/items/YA9NAYUV) [local](zotero://select/library/items/YA9NAYUV) [pdf](file:///home/gjc216/Zotero/storage/NS9ZQXLS/Howard%20et%20al.%20-%20Truncation%20and%20Censoring%20for%20Racing%20Evidence%20Accumulation%20Models.pdf)
 
%% begin notes %%

## My Thoughts

Reasonably simple methods (now integrated into [[EMC2]]) to account for censored data in [[evidence accumulation models]]. Censoring is the missing data you might get when there is a respone window cutoff for participants beyond which a response is not recorded. Even with missing responses at ~ 1% these can lead to biased estimates of evidence accumulation parameters (as shown in simulation studies in this paper). Instead if you account for censoring (and truncation where data are removed at long and short timescales in data pre-processing) then the actual generating parameters can be recovered.

This paper also includes some tutorial based work on EMC2, which I have not read in detail.

[[Zachary L Howard]] came along to journal club to present and a large part of his motivation for this work is trying to account for missing responses in the [[Detection Response Task|DRT]]. It looks as if this approach might not be perfectly suited to that case because a good predictor of this approaches validity is a data-informed approach where the response time distribution shows a distinct cutoff at the upper end (long tail with sharp cutoff). However in the DRT it is often the case that most responses at at the very short timescale, and the response time distribution is basically zero well before the cutoff.
 
%% end notes %%

### Annotations

%% begin annotations %%

##### Imported on 2026-09-14 12:01 pm
>[!quote|#5fb236]
>(Luce, 1986, e.g., responses faster than .15-.2 second are neurally implausible [(p. 14)](zotero://open-pdf/library/items/NS9ZQXLS?page=14&annotation=SD2RQ6WA)

<br>
>[!quote|#5fb236]
>In their study Damaso et al. (2022) also found a clear examples of a few participants who were failing to respond with an equal probability across all experimental conditions.  Rather than excluding these participants they modelled missing responses as due to a mixture of the sorts of evidenceaccumulation-based processes addressed here and a “contaminant” process characterised by a single probability parameter. [(p. 14)](zotero://open-pdf/library/items/NS9ZQXLS?page=14&annotation=XWEXM2LA)

<br>
>[!quote|#5fb236]
>Simulation-based calibration (SBC) studies involve fitting a large number of simulated data sets (automated by the run_sbc function) from a binary-choice paradigm. We used binary choice to include the DDM; similar results were found for different numbers of choices in race models. [(p. 20)](zotero://open-pdf/library/items/NS9ZQXLS?page=20&annotation=HQ9Y9WET)

<br>%% end annotations %%

---
## Item Notes

---
#### Tags

##### Keywords



##### Authors

[[Zachary L Howard]] [[Steven Miletic]] [[Dora Matzke]] [[Andrew Heathcote]]

##### Publication




%% Import Date: 2026-09-14T12:01:14.881+10:00 %%
