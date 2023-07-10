# OHBM Australia talks

## DTI Processing

Talk by *Maxime Descoteaux.*

### Good practices

* Inspect your data, look at your bvals, bvecs, look at animated GIF of your DWI
* DWI Preprocessing:
* Denoising Rician?)
* Eddy current correction - remember to rotate bvecs
* Remove outliers (subject motion, physiological noise etc)
* Distortion artifact reduction - using reverse phase encoded b0 via something like topup.
* Quality check (QC) your DTI and ODF directions (dcm2niix is a good converter) Look at underlying directions not just FA map.
* Inspect you fODF (crossing fibres)
* ACT (Anatomically constrained tractography),
* A new better solution, SET (Surface Enhanced tracking), using a cortical mesh to launch and finish tracking, reduces gyral bias and improves connectivity.
* Probabilistic tracking is well regarded, maybe not quite standard

### Caveats and warnings

- Challenge calibrating fiber response function in group studies
- Challenge for ACT are pathology (lesions etc)
- SET improves seeding termination, but still have 30%+ cortex unreached by streamlines.
- Probabilistic tracking has a challenge of false positives.
- Beware push button solutions

## Resting State fMRI

Talk by *Catie Chang*

Why is Resting state tricky, signals are mixtures of neural and unrelated noise, which can covary.

Focussed on artifact reduction techniques

- Postprocessing to remove head motion, regress out motion parameters, use multivariate approaches such as ICA. Best is to reduce/remove head motion in the scanner itself.
- Caridac and respiratory effects, TR should be low, look at fundamental frequecies and second order (use something like RETROICOR, needs physiological recordings). PESTICA can be used to get data-driven estimates of physio cycles. Spatial ICA can be used if no Physiological signals recorded.
- Can be overlap and covariation between physiological and RS networks
- Global signal regression is controversial, can distort true correlations, contains contributions from multiple processes (neural, physiological etc which could effect scans differently)
- Tissue-based regressors may be better, but has it's own controversies.
- Temporal ICA (Glasser et al 2018)
- Reproducible pipelines, like fmriprep help somewhat.

## Noise in fMRI - Best practices in data acquisition

Talk by *Saskia Bollman*

Noise can be iid, ie scanner electronics and random water motion, but BAD noise comes from head motion etc:

- Head motion, reduce in scanner as much as possible, slow drifts are unavoidable but motion spikes/head jerks introduce large artifacts.
- Imaging Acceleration noise, higher acceleration leads to larger artifacts, can get signal leakage (adjacent voxels activated when they shouldn't be)
- Physiological noise - pre-whitening with FAST is good, but still should regress out physiological signals. Depending on the effect and use of noise reduction techniques, lower TR is not necessarily better.

###### Tags

#dailyNote