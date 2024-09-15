# Priors Review
Priors represent our prior knowledge about the phenomena under study
- they are probability distributions assigned to each parameter in a model that represent our prior beliefs about the location and uncertainty of the parameter

There are many **"classifications" of priors**
- *conjugate priors* - priors that result in the posterior being from the same distribution family 
- *informative priors* - priors that have something to say 
	- go to previous dataset look at previous results
- *weakly/unformative priors* - priors without much information given

***Key points: a posterior represents a compromise between data and the priors***

# Placenta Previa 
> is a condition in which the placenta is located low in the uterus; blocks vaginal delivery

Question: are male or female births more likely to have placenta previa?
- early study found that out of 980 PP births, 437 were make

## The likelihood
437/980 female births we are interested in the proportion of female births relative to male births. 
	- is it higher than .485 which is the proportion of female births in overall population 

*What's a reasonable likelihood for this data? *
- parameter of interest is a proportion
- data is # of female vs male 
**binomial distribution! **

 