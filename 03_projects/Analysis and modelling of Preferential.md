# Code walkthrough of preferential

## Troubleshooting Notes

Troubleshooting the processing of data from Raw to Model for the [[Preferential task]]. Closely aligned with the [[Modelling of Veridical and Preferential Choice]], but a flow state interpretation of the preprocessing and modelling as in 03/03/2023.

### Raw Data

Stored as JSON, has fields for the key\_press (integer code for L=90, R=191), accept (whether pressed left when left key corresponds to accept, etc.) and hand - the response hand mapping.

### Preprocessing Steps

- Read in raw data from JATOS file (RES: A tibble with every event recorded by jsPsych)
- Filter "sft" trials, select useful columns, create factors from some cols (RES: A tibble with sft trials)
- Remove data from one duplicate participant (somehow did part of the task a second time)
- Remove participants data that did not complete at least 3/4 blocks (RES: 165 participants data)
- Remove one row with NA for rt
- Remove participants with more than 20% of their responses less than 350ms (as consistency in the HH cell drops below 70% with short responses)
    - **consistency** refers to whether they accept an option that we expect them to based on their thresholds (better price and rating than threshold). (RES: 138 participants data)
- Remove all trials with RT less than 350ms and all trials with RT > 10s
- Remaining consistency graph shows about 75%+ consistency for all cells except HD (20%) and LD (41%), that is when rating is a distractor but price is high or low than they are more likely to accept than reject.
- Remove participants with consistency in HH and DD cells at least 75% (RES: 121 participants data)
- Reorganise data as follows:
  - Select SFT only columns
  - Mutate rt to seconds
  - subject is factor column of sonaID
  - Accept is 2 for true and 1 for false.
  - Split cell_name into two columns, level for price (H/L/D) and
    level for rating (H/L/D)
  - Augment with labels for each row giving resulting drift
    parameter name. That is four new columns (v_acc_p, v_rej_p,
    v_acc_r and v_rej_r filled with par names for each
    accumulator. An example would be for a trial from the HL cell
    would get v_acc_p = v_acc_p_H, v_rej_p = v_rej_p_H,
    v_acc_r = v_acc_r_L and v_rej_r = v_rej_r_L
- Save to an RDS file

### Model input

- Read in preprocessed data, setup output and modelling settings
- Input specific parameterisation for the model
- Set priors for model (mean = 1 for dirichlet/alpha, 0 otherwise, variance = 2 for dirichlet/alpha, 1 otherwise)
- Create dirichlet function by filling in "global" variables like probability of contaminant, min and max RT (as per preprocessing).
- Some extra details on the Dirichlet function are:
  - Applies a transform to the parameter values being tested, Transforms include:
      - std: exponentiate input parameters.
      - reduced: Take exponent of all parameters except drifts, then v_rej_p = beta0_p - beta1_p * v_acc_p and v_rej_r = beta0_r - beta1_r * v_acc_r
      - reduced_more: Same as reduced except beta0_p == beta0_r
      - For all three b_acc = sampled b_acc + A and b_rej = sampled b_rej + A
  - Test for alpha < 0.01 or > 100, and if so return very small ll
  - Sample from Dirichlet with alpha parameter values as shape parameters. (Gets probability weights for each architecture.
  - Sample from architectures according to weighting from Dirichlet
  - Pass architecture loglikelihood function, transformed parameters and data to the model\_wrapper which:
      - Creates a drifts tibble with 4 columns, each a row is the correspond trial from the data, the actual parameter value for the appropriate drift rate for the cell (Acc and Rej for Price and Rating)
      - Gets a list of accept trials (accept == 2) and reject trials (accept == 1)
      - gets rts, drift rates and other parameters in an argument list
      - If there are some accpets for that participant, call the model with the accept arg list
      - If there are some rejects call the model with the reject arg list
      - return combination of accept and reject model results (trialwise log-likelihoods)
  - Add contaminants -\> .98 \* trial\_ll + .02 \* dunif(data$rt, min\_rt, max\_rt)/2
  - Return sum(log(pmax(ll\_contam\_mixture, 1e10)))
- Create and run sampler with priors/dirichlet function, data and parameter list.

_Analysis Note from 2023-08-21_
Reading the [[fific2010logicalrule|logical rules paper]] from [[Mario Fific]], I am struck by some possibly useful approaches. One - for the preferential work in particular - would be to take the response times to the H cells and compare them to the L cells, such that the expected response times would be LL > LH/HL > HH.