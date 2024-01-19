---
src: https://github.com/CooperAcademia/reviews/blob/master/CBB/Limits_on_Predictability_of_Risky_Choice_Behavior/my_comments.md
date: 22/12/23
hash: daf8ba3
---

# General Notes


* Limits on Predictability of Risky Choice Behavior, paper shares title with authors cognitivesciencesociety.org article (ICCM 2020?)
* ~ 50% common lines between the two "papers"

## Notes to me

* Certainty equivalence (Farquhar - State of the art)
* Prediction tournaments (Erev - A choice prediction competition (2010), From anomalies to forecasts (2017))
* Stochastic nature risky choices (Bhatia - Noisy preferences in risky...)
* Need to cover MSE vs correlation vs P_Agree again as well as Kappa
	* MSE: Mean squared distance between prediction and observed R-rate across problems
	* correlation: Pearson correlation between predicted and observed R-rate
	* P_Agree: Do observed and predicted R-rate both fall below or above 0.5, if so then 1, else 0
	* Kappa: Individuals consistent proportion - prob of random agreement / 1 - prob of random agreement.

Luce et al 1965:
> Eight of the subjects were twice rerun after periods varying from a few days to
> several weeks, and two of these were run a fourth time. Bounds for these
> remeasured utility curves were, in general, quite similar to those determined
> in the initial session. This evidence is encouraging, particu- larly in the
> light of the concern expressed by several investigators that experimentally
> determined utility curves are temporally unstable.

## Notes on the paper

## Overall impression


# Author comments

This manuscript demonstrates a fresh approach to accuracy when predicting risky choices, particularly aggregate measures of responses to certainty equivalence problems. The paper introduces previous work predicting choices in prediction tournaments. These tournaments were designed to test the predictive ability of models of risky choice and encourage the development of improved models. I appreciate the attempt to determine the upper limits to prediction in this context, rather than just striving for better predictions with no sense of the end goal. 

The manuscript presents a method to experimentally determine a limit on the predictive ability of models using a test-retest task. Participants responded to a set of problems taken directly from previous prediction tournaments over a few sessions. A subset of problems in the later sessions repeats choice problems from the first session. The correlation between repeated items at different time points provides an upper limit to how accurate predictions on the same problem set can be. The manuscript compares this prediction limit to past and current performance on a set of cognitive or statistical models.

## Major comments

While I agree with the manuscript that understanding the limits of our ability to predict risky choices rather than continually chasing better predictions is warranted, I have a few concerns with the work currently presented.

Section 2.2 (Page 4, Line 32): An additional test would have been to see problems repeated on the same day/same sitting as a test of within-session variability vs within-person variability. It was unclear from the cited works whether any pre-existing data could be used to calculate an analogous prediction limit based on repeated choice problems in the same sitting. However, if possible, this could be an excellent addendum and enable readers of the manuscript to get some sense of the variability across longer and shorter timescales. To be specific, I do not think an extra experiment is warranted here; however, if there is already existing data that could answer this question, an analysis of that data along these lines would be appreciated.

In section 2.2.1, the manuscript states: "As we mentioned above, the winner of the first DFD tournament was the logistic regression model". This model is not mentioned anywhere else in the paper, so this should probably be expanded and given more detail.

In Section 4.3 (Page 13, Line 28), The manuscript mentions that prediction limits "may vary slightly across datasets" whilst stating that the prediction limit calculated in the manuscript is a point estimate. As mentioned above, an estimate of the prediction limit from data where choice problems were repeated within-session would help justify this judgement. In the absence of this, some method of estimating the variability of this prediction limit would help. Perhaps bootstrapping a confidence interval or other similar method could give some confidence in the precision of the limit.

## Minor comments

In section 2.3, Page5, Line 30 - the manuscript mentions a participation fee. Were the participants charged a fee to participate in the task? If this is incorrect, I suggest rewording this to indicate that the participants were paid a base rate of 100 INR, which was then scaled as the subsequent sentence indicates.

In section 2.4 (Page 6, Line 18), I would suggest detailing the three possible outcomes, which I presume correspond to Safe (Medium), Risk (High) and Risk (Low)?

Section 3.1.1 (Page 8 Line 40) The manuscript states that the differing model performance is "formally surprising"; however, as you indicate in section 4.3, aspects such as "problem selection, population characteristics, and experiment protocol variations" could affect the R-rates across problems. I would suggest some indication that possible causes of this issue will be discussed in a later section.

Section 4.3 In this section you define a new acronym (PL) and then use it once more in the section. I would suggest removing the acronym and just use the full wording (prediction limit) throughout.

In section 5 (General Discussion), the manuscript makes a point that "The choice of number of participants is entirely arbitrary, and variations in this number across datasets makes it difficult to compare results across them due to differential quantization of R-rates". As R-rates are sensitive to the number of participants, and the number of participants is higher in the Technion Estimation and Technion Competition datasets, perhaps the aggregate measures are more stable in the tournament data than in the current experimental data. This point could be mentioned in earlier discussions about differing model performance.

# Editor comments

I quite like the approach outlined in the paper, comparing previous predictions to a theoretical maximum limit on the predictive power based on test-retest of the same individuals on exactly the same problems seems a novel way to approach this question.

I would like to see some improvements to the manuscript, particularly some attempt to assess the precision in the estimated prediction limit.