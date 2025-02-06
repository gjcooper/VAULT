
Observational data is the bane of causal inference, whereas the "gold standard" is a randomised control trial. Maybe instead of avoiding causal language, we want to state that our aims are to establish a causal link and then clearly state limitations.

In data science, we may want to describe a phenomena, predict future occurrences or establish causal links.

One "solution" is to use [[directed acyclic graphs]], drawing out our causal pathways. Can be shared to help with replication crisis etc. Visual tools that help represent causal relationships.

The DAG can include mediators (never control for otherwise close loop), instrumental variables. 

[[Collider Bias]] is a variable influenced by 2 or more variables. Say smoking and air pollution both converge on a lung disease node inthe graph. If we control for lung deisease we open up the graph and it looks like air pollution and smoking are correlated. The birthweight paradox is another example of this collider bias. One way if you get a non-intuitive result based on this is to run a sensitivity analysis.

[[Selection bias]] when sample used is not representative of target population. Using DAGs to visualise potential bias, and possibly inverse probabiity weighting to reqeight the sample to account for differential participation of attrition.

A tautological association is when a variable is used to explain itself, ie when part of the variable is used in both the exposure and outcome. Say per capita CO^2 emissions compared to GDP (which is also per capita)

## Matteo's section

[[Matteo Lisi]] The LIP paper in Nature about deactivation of the area not removing perceputal decision aking abilities.

The DAG provides a _blueprint_ defining the joint probability distributions over a set of variables.
For more complex graphs the technique of [[D-separation]] 

Automatic analysis of DAGs is possible with some tools such as [dagitty](https://www.dagitty.net/), which is also available as an R package.

