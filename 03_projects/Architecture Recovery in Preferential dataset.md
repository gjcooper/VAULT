# Recovery of Preferential architecture

I have previously run the architecture recovery (where I simulate using
each of the 5 processing architectures and then try to recover them) for
both Veridical and Preferential datasets. The Veridical looked nice
(which you saw at OzMathPsych) and the Preferential was also promising,
but with confusion between two of the models.

Here is what the original veridical recovery looked like:

:\! feh \~/mcce/results/Veridical/ArchRecovery\_2022-02-09.png&

And here is the original Preferential architecture recovery plots.

:\! feh \~/mcce/results/Preferential/ArchRecovery\_2022-03-30.png&

Part of the model estimation is a 2% contaminant process component, but
in the first runs of the recovery, the simulated data did not include
any simulated contaminant responses. I have added that in, and when
rerunning the Veridical dataset, the new recovery estimates look
slightly less strong but still good (as expected).

:\! feh \~/mcce/results/Veridical/ArchRecovery\_2022-03-09.png&

I have a problem with the new Preferential recovery though with
individual recovered architectures that are not consistent within each
simulated dataset, and group level estimates that are misattributed.
There is also some cleaning I have done to the raw data between the two
recovery attempts that may be affecting it in some unforeseen way. At
the meeting, we can look through some trace plots, and discuss some
possibilities for directions to take (epsilon/n.particles changes in the
sampler, longer burn-in runs etc)

:\! feh \~/mcce/results/Preferential/ArchRecovery\_2022-03-09.png

## Traces for parameters

From the most recent estimation run

theta\_mu

:\! evince
/home/gjc216/mcce/results/Preferential/theta\_mu\_trace\_2022-03-10.pdf
&

well specified parameter

:\! evince
/home/gjc216/mcce/results/Preferential/v\_acc\_p\_H\_randeff\_trace\_2022-03-10.pdf
&

poorly specified parameter

:\! evince
/home/gjc216/mcce/results/Preferential/v\_rej\_p\_H\_randeff\_trace\_2022-03-10.pdf
&

## Older estimation run

theta\_mu

:\! evince
/home/gjc216/mcce/results/Preferential/theta\_mu\_trace\_2022-03-30.pdf
&

well specified parameter

:\! evince
/home/gjc216/mcce/results/Preferential/v\_acc\_p\_H\_randeff\_trace\_2022-03-30.pdf
&

poorly specified parameter

:\! evince
/home/gjc216/mcce/results/Preferential/v\_rej\_p\_H\_randeff\_trace\_2022-03-30.pdf
&

## Last minute discovery

\> df %\>% mutate(longrt = ifelse(rt \>= 10, "long", "short")) %\>%
group\_by(longrt) %\>% summarise(minrt = min(rt), maxrt = max(rt), count
= n())

1.  A tibble: 2 × 4 n()) longrt minrt maxrt count \<chr\> \<dbl\>
    \<dbl\> \<int\>

1 long 10.0 6803. 788 2 short 0.35 10.0 84183

\> df %\>%

> mutate(longrt = ifelse(rt \>= 10, "long", "short")) %\>%

group\_by(subject, longrt) %\>% summarise(minrt = min(rt), maxrt =
max(rt), count = n()) %\>% ungroup() %\>% filter(longrt == "long") %\>%
summarise(min = min(count), max = max(count), mean = mean(count))

1.  A tibble: 1 × 3ount)) min max mean \<int\> \<int\> \<dbl\>

1 1 49 8.76

### Meeting

Check random choice Every trial 2 percent prob, instead of 2 percent
