# bayesOpt

`bayesOpt` is a [[MATLAB]] function provided by the Statistics and Machine Learning toolbox that attempts to find values for a vector of variables that minimise the provided scalar objective function in a bounded domain.

The components of the domain can be real, integers or categorical. The minimisation has the following elements:
- A [[Gaussian process model]] of $f(x)$.
- A Bayesian update procedure to modify the process model at each new evaluation of $f(x)$.
- An acquisition function $a(x)$ that you maximise to determine the next point $x$ for evaluation.

## Algorithm
1. Evaluate $y_i = f(x_i)$ for `NumSeedPoints` points $x_i$ (if there are evaluation errors keep taking more points until you have enough).
2. Update the Gaussian process model of $f(x)$ to obtain a posterior distribution over functions $Q(f|x_i,y_i \mathrm{ for }i=1,...,t)$ 
3. Find a new point that satisfies the acquisition function $a(x)$
4. Repeat 2 and 3 until number of iterations/time/stopping criteria is met 