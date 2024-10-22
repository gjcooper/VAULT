

## Useful ssh/scp commands  

### SCP copy via multi-hop ssh

a la https://sshmenu.sourceforge.net/articles/transparent-mulithop.html

```bash
scp -o ProxyCommand="ssh gjc216@psych.newcastle.edu.au nc sri16132 22" gjc216@sri16132:/home/gavin/Analysis/VCFS2014/tbss/results/meanFA/A0370CA_FA_prep_warp_merged_masked_mean.nii ./meanFA.nii
```

### Multi-hop ssh
  
```bash
ssh -At gjc216@jumpgate.newcastle.edu.au ssh sri16132
```

or, for X-11 forwarding

```bash
ssh -AXt gjc216@jumpgate.newcastle.edu.au ssh -X sri16132
```