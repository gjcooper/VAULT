# EEG Script issue

For the [[Perceiving is believing]] [[MMN]] project [[Mattsen Yeark]] is having some problems with the [[eeglab]] script for processing the data.

## Current problems with the script 8/8/23

#### Channels for Artifact rejection

Line 97. What I would like is for this process to ignore the HEO and VEO channels. What makes this complicated is that the input is a channel range and the number of channels will change with each participant based on the cleaning process. Sometimes HEO and VEO themselves might get removed….

#### Mastoid referencing

Line 124. What I would like is a line of code here that looks for M1 and M2 labels and makes those channels the basis of the reference. If it can only find one of them, then it will use just one of them. If it can’t find either it should spit out a warning of some kind in a text document (if possible). That way I can run the whole script and look back over it at the end and see who was excluded.

#### Grand Average

The grand average function (pop_gaverager)  requires all participants to have the same number of channels. One way to work around this is to interpolate channels that get removed (with the exception of the mastoids) remove the mastoids from the correction procedure and artifact rejection (so they never get removed) and then at the end during GA remove them all together (since we won’t need the mastoids at that point). Might sound a bit convoluted but I can explain my rational at a later date.  A few other interesting suggestions here https://sccn.ucsd.edu/pipermail/eeglablist/2017/012909.html and here https://www.morrislabpc.org/info/data-processing-pipeline/

 