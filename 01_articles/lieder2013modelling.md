---
cssclass: research_note
type: "journalArticle"
author: "Lieder, Falk; Daunizeau, Jean; Garrido, Marta I.; Friston, Karl J.; Stephan, Klaas E."
title: "Modelling Trial-by-Trial Changes in the Mismatch Negativity"
publication: "PLOS Computational Biology"
date: 2013-02-21
citekey: lieder2013modelling
aliases: 
    - "Modelling Trial-by-Trial Changes in the Mismatch Negativity"
---

# Modelling Trial-by-Trial Changes in the Mismatch Negativity

Lieder, F., Daunizeau, J., Garrido, M. I., Friston, K. J., & Stephan, K. E. (2013). Modelling Trial-by-Trial Changes in the Mismatch Negativity. _PLOS Computational Biology_, _9_(2), e1002911. [https://doi.org/10.1371/journal.pcbi.1002911](https://doi.org/10.1371/journal.pcbi.1002911)
[online](http://zotero.org/users/local/kZl3QdXV/items/7CKZTEMI) [local](zotero://select/library/items/7CKZTEMI) [pdf](file:///home/gjc216/Zotero/storage/JRB78VWZ/Lieder%20et%20al.%20-%202013%20-%20Modelling%20Trial-by-Trial%20Changes%20in%20the%20Mismatch%20N.pdf)
 


## My Thoughts

Comparing 13 different models of how the [[Mismatch Negativity|MMN]] signal might arise in [[EEG]] signals, this paper compares models of simple change detection, and more complex models that work on the free energy principle, like [[Active Inference]]. Some notable results were the marginal win of models based on prediction error, as papers like [[weber2020ketamine]] and [[hauke2023aberrant]] refer to and model with the [[HGF]]. When looking at families of models though the [[model adjustment]] models account for more variation in the trial-to-trial MMN signal than prediction error alone.

This is an older paper, and seems to take the approach of determining a trial-by-trial MMN amplitude and using that for model comparison, rather than looking at the entrie MMN distribution.
 
### Annotations

%% begin annotations %%

##### Imported on 2024-02-16 4:20 pm
>[!quote|#ffd400]
>Subject-specific subsets of the preselected electrodes were created by excluding those electrodes where the expected mismatch potential could not be detected in the subject’s average difference wave. [(p. 3)](zotero://open-pdf/library/items/JRB78VWZ?page=3&annotation=JPGXN7PD)

---
>[!quote|#a28ae5]
>isolates the deviance-specific potential. [(p. 3)](zotero://open-pdf/library/items/JRB78VWZ?page=3&annotation=MI9RNN8I)

---
>[!quote|#a28ae5]
>baseline correction [(p. 3)](zotero://open-pdf/library/items/JRB78VWZ?page=3&annotation=ERDPGMEY)

---
>[!quote|#a28ae5]
>Estimate each subject’s MMN peak latency [(p. 3)](zotero://open-pdf/library/items/JRB78VWZ?page=3&annotation=ZET2GE9N)

---
>[!quote|#a28ae5]
>Estimate each subject’s trial-wise MMN amplitudes by averaging his/her deviance-specific potentials over a +70 ms time window centered at his/her MMN peak latency. [(p. 3)](zotero://open-pdf/library/items/JRB78VWZ?page=3&annotation=VVS3RPGI)

---
>[!quote|#5fb236]
>Change detection hypothesis (Models M1-M3). A classical interpretation of the MMN is the change detection hypothesis, which assumes that the MMN indexes local physical changes in the sensory input [16,17]. This hypothesis comes in several flavours, each of which leads to different quantitative predictions. 1. The MMN indexes only whether or not a change has occurred. 2. The MMN indexes the absolute value of the change in a physical property of the sensory input (i.e., unsigned change). 3. The MMN indexes the difference in a physical property between the deviant and its predecessor (i.e., signed change). [(p. 4)](zotero://open-pdf/library/items/JRB78VWZ?page=4&annotation=K43QJ4BQ)

---
>[!quote|#5fb236]
>Neural adaptation is the process due to which the neural response to a stimulus or feature decreases with its repeated or prolonged presentation. According to the adaptation hypothesis, the MMN elicited by a change in sound frequency reflects the difference in the responsiveness of adapted and non-adapted frequency-specific neurons in auditory cortex [12]. [(p. 5)](zotero://open-pdf/library/items/JRB78VWZ?page=5&annotation=H5CANMJJ)

---
##### <span style="color: #2ea8e5">Screenshot</span>
![[meta/attachments/lieder2013modelling/image-6-x61-y424.png]]

---
>[!quote|#5fb236]
>The prediction error models assume that the MMN reflects the activity of neurons encoding precision weighted prediction errors on sensory inputs and hidden states. Roughly speaking, prediction errors are the difference between what is observed and what was predicted from previous experience according to the probabilistic mental model m. [(p. 9)](zotero://open-pdf/library/items/JRB78VWZ?page=9&annotation=KPJ4QSJZ)

---
>[!quote|#5fb236]
>The novelty detection models assume that the MMN reflects neuronal activity encoding surprisal (also known as ‘‘self-information’’ or ‘‘Shannon surprise’’) with respect to the conditional probability distributions describing the observer’s beliefs. Unlike prediction error, surprisal is an unsigned quantity, [(p. 9)](zotero://open-pdf/library/items/JRB78VWZ?page=9&annotation=J7LDDHVC)

---
>[!quote|#5fb236]
>The ‘‘model adjustment’’ models assume that trial-wise MMN amplitudes reflect adjustments of the parameters of the probabilistic mental model m; this is a formalization of the model adjustment hypothesis [19]. MMN amplitudes could reflect adjustments of different parameters (i.e., the categories’ mean frequencies, the expected sequence length, and the conditional transition probabilities) and in different ways (i.e., sensitive or insensitive to the sign of the adjustment). [(p. 9)](zotero://open-pdf/library/items/JRB78VWZ?page=9&annotation=W5YFEPC4)

---
>[!quote|#ffd400]
>The most plausible MMN theory was the model adjustment theory (w~0:70), followed by the prediction error theory (w~0:24). [(p. 11)](zotero://open-pdf/library/items/JRB78VWZ?page=11&annotation=VGQ8I2SG)

---
>[!quote|#5fb236]
>Instead, our results suggest that trial-by-trial changes in MMN amplitude are highly historydependent and represent an informative index of statistical learning as the recording session proceeds. [(p. 13)](zotero://open-pdf/library/items/JRB78VWZ?page=13&annotation=ZZM4HMJF)

---
>[!quote|#5fb236]
>Instead, our results support explanations postulating that the brain maintains and constantly updates an internal model of its environment. [(p. 14)](zotero://open-pdf/library/items/JRB78VWZ?page=14&annotation=A7V7KPDQ)

---
>[!quote|#ffd400]
>Our results supported model adjustment and, to a lesser extent, prediction error signalling, but not novelty detection, even though it computes an approximation to (Shannon) surprise. [(p. 14)](zotero://open-pdf/library/items/JRB78VWZ?page=14&annotation=UJBPHZZ8)

---%% end annotations %%

## Item Notes

#### Tags

##### Keywords

#subject/learning #subject/perception #subject/electroencephalography #subject/mismatch_negativity #subject/coding_mechanisms #subject/sensory_perception #subject/electrode_potentials #subject/perceptual_learning

##### Authors

#author/lieder_falk #author/daunizeau_jean #author/garrido_marta_i. #author/friston_karl_j. #author/stephan_klaas_e.

##### Publication

#pub/plos_computational_biology


%% Import Date: 2024-02-16T16:20:35.799+11:00 %%
