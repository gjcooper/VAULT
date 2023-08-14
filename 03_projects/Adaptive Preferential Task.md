# Adaptive Preferential Task

The adaptive preferential task is designed to alleviates flaws from the [[Preferential task]], where estimation of the trade off between price and rating was either poor, or shifted throughout the task.

In this version I am using the [[jsQuestPlus]] JavaScript library to select stimulus values that provide the best evidence of the trade off between these two attribute levels. The hope is that then stimulus selection for the 9 cells of the task will better elucidate the response time variation that I need for the modelling. that is, each target trial with a price and rating value selected in relation to the current best estimate of the trade off between these two attributes should better reflect the in the participants threshold.

>[!Important]
> Note, the function that turns a stimulus value for price/rating into an accept/reject response needs to be specified. Let's talk to Guy about that.

My initial attempt at a function to convert stimulus values to probability of accept will be to leverage the [[Random Utility Model]], as this seems custom built for this approach.