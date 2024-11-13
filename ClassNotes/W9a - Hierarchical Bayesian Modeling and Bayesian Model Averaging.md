## Outline 
- nested data - what it is and why does it matter? 
- Hierarchical bayesian models in brms
- Bayesian model averaging - GLMs

## Nested Data 
> the most used models Bayesian or frequentist assume **condition IID** - every observation does not overly depend on data in other observations 

- conditional IID
	- conditional on the model and data all observations are identically and independently distributed
	- rare that interesting data is conditionally IID 
	- violation of conditional IID is **bad**!! 

## Simpson's Paradox
Also known as the aggregation paradox 
- when the overall trend looks nothing like the actual within group trends 
- can lead to completely incorrect conclusions 

Other consequences:
- inflated standard errors 
- reduction in power 
- poor generalibility

## Hierarchical Bayes Regression 
