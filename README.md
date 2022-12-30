# ModelSimplification

The abstraction method is to be used when the code block to replace the abstracted subsystem needs to be generated. The output from the parent 
simulation should go as input to the abstraction method. The method will fit standard probability distributions available with Scipy library and 
return the best fitting distributions along with the P values. It will also print the code block corresponding to the best fitting distribution 
to be used in the metasimulation model. 
Additionally, the method also yields five best-fitting probability distributions based on sum-squared errors (SSEs) using the Fitter Python library. It also 
prints the code block based on SSE estimate.

The used must use the abstraction(data) method for code block generation. the data should be length of stay values stored in an array/list collected across a single simulation replication.
