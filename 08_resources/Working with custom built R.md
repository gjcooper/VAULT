## Working with gcc R

An example PBS job script

```bash
#!/bin/bash

#PBS -P ut81
# Other PBS directives for walltime/mem etc
# tell PBS to let you have access to gdata
#PBS -l storage=scratch/ut81+gdata/ut81

#PBS -q normal
# Setup email notifications when the job is aborted(a), begins (b) or ends (e)
#PBS -M <Your email address>
#PBS -m abe

cd $PBS_O_WORKDIR
{
    source /etc/profile.d/modules.sh
    . ~/.bashrcmodule load R-ut81/4.3.2
    module load R-ut81/4.3.2

    Rscript --no-save --no-restore test.R

    qstat -xf $PBS_JOBID
} > output/test_4.3.self.out 2> output/test_4.3.self.err

exit 0

```
So the job script is the same as others (although mine may be weird), with a couple of additions. I am running my .bashrc file (the `. ~/.bashrc` line) in order to add the module files on `/g/data` to the list. I also request access to `/g/data` and `/scratch` storage in the PBS directives to be able to see the module files and custom R. And finally I make sure I load my custom R with `module load R-ut81/4.3.2`.

## Your bashrc file

Another thing that is necessary is to edit your .bashrc file

```bash
# .bashrc                                                         
#...
# The automatic contents of .bashrc that NCI create for you
# ...
# The location of user created modulefiles
prepend_path MODULEPATH /g/data/ut81/apps/modulefiles
```