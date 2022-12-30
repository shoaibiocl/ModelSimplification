# ModelSimplification

## ABSTRACTION - parametric
The abstraction function is to be used when the code block to replace the abstracted subsystem needs to be generated. The output from the parent 
simulation should go as input to the abstraction function. The function fits standard probability distributions available with Scipy library and 
return the best fitting distributions along with the corresponding P values. It will also print the code block corresponding to the best fitting distribution 
to be used in the metasimulation model. 
Additionally, it yields five best-fitting probability distributions based on sum-squared errors (SSEs) using the Fitter Python library and
prints the code block based on the SSE estimate.

The user must use the abstraction(data) function by passing the length of stay table as argument, to generate the code blockn. The input data should be the length of stay values stored in an array/list collected across a single simulation replication.

Further, in case none of the standard probability distributions seem to fit well (P value < 0.05), the function prompts the user to use non-paramateric function for estimating probability density. 

## ABSTRACTION - non-parametric

This function is developed to estimate the probabilty density of the length of stay data generated and collected from the parent simulation model. It used kernel density estimation available on Scikit-Learn package. The output from the function can directly be used to replace the abstracted system in the parent model. 

## KL-Divergence - Outcome validation

The _KLDivergence(data2, data2)_ method was developed to automate the outcome validation exercise. The method requires inputs of the overall length of stay values from the parent and child models. It then converts it to probability distributions and compares the ditsributions. In effect, the diversion of one probability ditribution from the other is measured and reported.  
