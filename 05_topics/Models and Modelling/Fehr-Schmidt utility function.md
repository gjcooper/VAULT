The Fehr-Schmidt Utility Function is a utility function that attempts to capture the utilities in human behaviour, particularly when the humans involved are averse to inequality. Particularly captures how people feel 

One formulation of the function is as follows:

$$
\begin{eqnarray}
U_i(x) = &X_i& \\
&-& \frac{\alpha_i}{n-1}\sum{max(X_j-X_i, 0)} \\
&-& \frac{\beta}{n-1} \sum{\max(X_i-X_j, 0)}
\end{eqnarray}
$$
So $X_i$ is the classic consumption utility (how much money does person $i$ get).
The second term captures the effect of other people getting more money that person $i$. Particularly the parameter $\alpha_i$ is the importance weight that person $i$ places on the inequality between themselves and others when other people have more money than themselves.
Similarly the third term captures the influence of other people having less money than person $i$, with parameter $\beta_i$ the importance weight on the inequality between themselves and others that have less.

For most people the expected values for weights are $\alpha_i > \beta_i$, that is most people place more importance on others having more than themselves as opposed to themselves having more than others when thinking about inequality.