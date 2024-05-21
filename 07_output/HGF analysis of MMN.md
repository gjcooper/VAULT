# HGF of MMN

For [[Juanita Todd]] et al, in particular the application of HGF to MMN data (DP200102346). [[HGF Aging Juanita]].

The general idea to to take single trial data from a static [[Mismatch Negativity|MMN]] sequence for different age cohorts, filtering and removing trials with significant artifacts and then fitting the HGF to the remaining sequence.

We are taking inspiration from papers such as [[weber2020ketamine|Ketamine Affects Prediction Errors about Statistical Regularities: A Computational Single-Trial Analysis of the Mismatch Negativity]], 

### Outline of approach

Currently adapted from [[weber2020ketamine]], previous JTodd MMN research and other papers applying HGF to MMN.

#### EEG data approach

##### Record Data (DONE)

##### Visually check data
- Read data into EEGLAB from CNT
- Plot (Channel Data (Scroll)) and record any visually _bad_ channels.
-  

##### Automated Preprocessing

- Record EEG
- Filter data (high/low) and downsample to 256Hz
- Epoch (Can't see any baseline correction)
- Reject all trials overlapping with eyeblinks.
- Artifact rejection (based on deviation from prestimulus baseline)
- Channels with > 20% rejected trials rejected marked as bad and interpolated for sensor-level stats

#### Modelling approach

- Multivariate HGF with matrix $\mathbf{X}_2$ being the transition probabilities between tones and $x_3$ being the volatility, or degree to which $\mathbf{X}_2$ changes from trial to trial.
- Set subject specific perceptual parameters
    - $\kappa = 1$, as the strength of coupling between second and third level is arbitrary.
    - $\omega$ (learning rate independent of volatility estimation) and $\nu$ (speed of change in volatility) were estimated using a surprise-minimising Bayesian observer for all participants (no participant responses to estimate on)
    - Additional starting values of individuals beliefs, ($\mu_2$, $\sigma_2$, $\mu_3$ and $\sigma_3$) were also estimated.
    - Default priors for all values were taken from the tapas toolbox, specifically `tapas_fitModel` and the `tapas_bayes_optimal_whatworld` function.
- As each sequence was slightly different due to subject specific EEG preprocessing there were slightly different parameters per person.
> [!note]
> This last point can probably be relaxed for us as we had a fixed sequence

#### Statistical analysis

- EEG Data converted to smoothed scalp images
- Precision-weighted prediction errors from models served as regressors in a GLM of trialwise EEG for each participant (after removing entries corresponding to rejected trials)
- Random-effects group analysis, using one-sample t-tests as second-level models. Also used F tests to silmultaneously examine pos and neg relations of EEG amplitudes with compuatational trajectories.
- FWE correction



Notes from other papers on HGF/single trial - see:
- [[weber2020ketamine]]
- [[hauke2023aberrant]]

