# Analysis differences between projects

This is to record analysis choices and their differences when two projects are working on the same datasets.

## [[SFT of DCE]] and [[Architecture of MultiAttribute Choice]]

When filtering on accuracy the python code in the SFT analysis for the special issue on Systems Factorial Technology there are additional steps.

For the SFT analysis I remove NaN responses, remove all responses < 300ms and all responses > 95% quantile for each individuals data as part of the #preprocessing. It is after these steps that I check for accuracy (according to the instructions in the [[Veridical task]]) of at least 80% accuracy to each of the four possible trial categories, price/rating alone, double target and double distractor.

However for the MCCE analysis I only remove NaN responses before checking accuracy.

This change results in one less participant meeting the accuracy criteria for the MCCE modelling (as their slow responses are higher in errors)

This has been updated in the code to match as of 10/08/23