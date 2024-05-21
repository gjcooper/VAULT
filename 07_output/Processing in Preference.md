Individual differences for attribute processing in preferential choice

# Introduction

Much of attribute and option processing for preferential multiattribute choices has relied in aggreagate measures.

When looking at individual differences between approaches one method used has been process tracing, typically using eye tracking, mouse movements or the order of revealed information

These methods suffer from artificial restrictions on the processing (obscuring information) or situations (eye tracking is expensive).

One approach that has been developed recently has looked at the underlying processing of attribute information from a series of veridical choices on simple stimuli.

We extend this hear to the context of free preferential choices for a comparable set of stimuli sampled from a realistic range of prices and hotel ratings.

# Experimental Task

## Individual thresholds

For the task each participant was given one of two tasks in order to develop a personalised threshold of the tradeoff between the price of a hotel and its rating.

One subset manipulated a slider stimulus to determine the highest price and lowest rating they would accept.

The other subset of participants made s series of choices whether to accept or reject a hotel, for which the price and rating was increased/decreased in steps until a staircase algorithm settled on a threshold for the tradeoff between price and rating.

The mean of the sliding scales, or the mean of the last 8 staircase reversals was then used in the second stage of the task to determine the individuals threshold.

## Main task

The main part of the study then commenced, where participants were given a series of choices to either accept or reject examples of Hotels.

Each hotel could vary in price along a realistic range of values from $100 to $450 and in rating from 6.5 to 9.0
For the calculation of the attribute levels these ranges were normalised to the range [0,1]

For each hotel the two attributes (Price and Rating) were varied according to the following cells:

* A High value attribute was sampled from a normal distribution centred 0.15 (on the normalised range) in the positive direction for that attribute type (.15 cheaper for price, and .15 higher value for rating)
* A Low value attribute was sampled from a normal distribution centred 0.05 (on the normalised range) in the positive direction for that attribute type.
* A Distractor attribute was sampled from a normal distribution centred 0.1 (on the normalised range) in the negative direction for that attribute type (0.1 more expensive for price, and 0.1 lower for rating)
* The standard deviation for each distribution was set at 0.025, and the distribution was truncated at 2SD

These manipulations gave 9 cells to inform our model, from easy choices (HH [both attributes high] and DD [both attributes distractor]) through to harder decisions (LD [price low, rating distractor}).

# Descriptive results

Describe sanity checks and data cleaning, aggregate measures by cell types, cleaning of long and short responses.

Describe participant pool and results of cleaning


# Modelling of individual responses

Model run and fit in a hierarchical bayesian framework using the PMwG package.

Reference model recovery of simulation (probably appendix)

Global results, most people using Max Winner model, few people using Coactive model

This means that people are utilising all information for both accept and reject responses, but they differ in how efficiently they integrate this information into the final choice.

Drift rate differences between price and rating, how do they differ across attribute type.

Thresholds across response type, what do those differences mean.


# Participant demographics

How does group membership correlate with demographic information (can I even get demographic info??)


# Discussion

What are the limits in terms of number of choices per person for this technique??

Categorisation of people into groups could provide customer specific strategies for the presentation of information to consumers.

How would this be extended to multiple options? For forced choice it could be the difference between attribute levels, but how would a neither option work.


# From the associated mindmap

### Structure of Paper
- Information Processing in multi-attribute consumer choice
  - Decision strategies in the literature (see [[assumptions for decision strategies]])
  - Approaches to discriminating between decision strategies (see [[process tracing]], [[Random Utility Model|RUM]])
- 5 Models of Information processing in 2 attribute choice (taken from [[SFT of DCE]])
  - Parallel SFT Inspired models (Parallel Self terminating, Parallel Exhaustive)
  - Parallel SFT complements (First Past the Post, Maximal Information Decisions)
  - The SFT inspired Coactive model
- Modelling Information Processing (looking at you [[Linear Ballistic Accumulator|LBA]])
  - LBA for complex decision making
  - LBA for Information Processing
- LBA for multi-attribute choice
- Dirichlet selection between models (see [[Dirichlet process]]]] and [[navarro2006modeling|Modeling individual differences using Dirichlet processes]])
  - Possible approaches to choosing between IP models in individuals data
  - The dirichlet process
- Veridical Choice Data (from [[Veridical task]])
  - Experiment review
  - Show
  - Fitting the model to Veridical Data
  - Results
  - Discussion
- Preferential Choice Data (from [[Preferential task]])
  - Experiment Design/Rationale
  - Methods
  - Summary results showing thresholding procedure had reasonable effect
  - Modelling results
  - Discussion
- General Discussion
  - Veridical vs Preferential
  - Limitations and Opportunities

### Appendices
- Estimation approach, Implementation?
- Model Recovery
- Parameter Recovery
### Notes
- Accept mostly using one strat, reject using the other
  - Selective Influence
  - Is the model really doing what I say it is doing
- Following a similar approach (Intro)
  - Link verbal descriptions of the information processing with the decision strategies
  - Follow on to 2 attr 1 option
- Maybe swap 2 or 3  or drop LBA from 2?
  - LBA is just the tool used. (Could have been other accumulation ...)
  - Approach taken is to swap 2 and 3 as well as dropping LBA specifics
- Check on reject condition (whether that was run)