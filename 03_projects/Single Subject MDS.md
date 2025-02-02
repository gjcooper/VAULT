# Notes on Single Subject MDS

Guy's analysis on similarities/distances for Jess's Honours project seems mistaken, need to chat with Guy about his approach.

analysis-Jess.Rmd seems to show:

```R
# normalise similarity ratings to [0-1] interval
sim <- sim / max(sim, na.rm=T)
# assume distance is negative exponential function of similarity
dist <- -log(sim)
# finally, calculate mean similarity and distance
av_sim <- sim %>% apply(1:2, mean, na.rm=TRUE)
av_dist <- dist %>% apply(1:2, mean, na.rm=TRUE)
```

- Normalise similarity ratings across all participants data (sim)
- Calculate distances (dissimilarities) from normalised data (dist)
- calculate average similarity by mean over sim
- calculate average distances (dissimilarities) by mean over dist

smacof exp method seems to show:

``` R
# Pass in an already averaged similarity matrix s
dissimilarity <- -log(s/max(s))
```

- For group/global MDS pass an already calculated average similarity matrix, ideally passed into as.dist
- smacof::sim2diss(method="exp") calls -log(s/max(s)) on this object, with s converted to matrix
- So order is average across participants -\> normalise -\> distance conversion
- order of your work is normalise -\> distance conversion -\> average across participants