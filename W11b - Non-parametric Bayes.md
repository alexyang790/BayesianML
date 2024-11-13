> Bayes for infinite dimensional problems

# Outline 
- what is non parametric bayes 
- infinite mixture models via the Chinese restaurant process 
- gaussian process models 

# Parametric Bayes
**parametric model** - a model with a fixed number of parameters
- any given regression model has a fixed number of features (and parameters)
- a finite mixture models have a fixed number of mixtures 
- LDA/QDA has a fixed number of classes 
# Non parametric Bayes 
> models that grow and change with increasing amounts of data 

warning: non-parametric is poorly defined 
- it can refer to models that do not assume parametrized distributions
	- Wilcoxian Sign Rank Test

Non-parametric Bayesian Models are ones where the structure is not specified a priori
- we are going to cheat a little where we define certain aspects of the model 

# Mixture Models and Latent Variables 
**Data augmentation** - propose unobserved (latent) variables to explain your data 

# Simple Gaussian Mixture Model 
[insert slides later]

# Infinite mixture models 
Mixture models 
- specify k components 
- automatically classify observations into classes/components 

**Big question: how many components??**
- hard question 
- important to get right

# Chinese restaurant process
Consider a restaurant with infinite tables and group style seating
- customers enter look around and choose a table
	- an occupied table with probability related number of occupants 
	- the next unoccupied table with probability related alpha
- this process produces a finite number of occupied tables 
	- alpha (concentration parameter) increases number of occupied tables 

# Stick breaking process 
[insert slides]

# Infinite mixture models 
A mixture model with an infinite number of potential classes 
- with a strong tendency for classes to be empty 

Conceptual difference is in how to model an infinite number of classes? 
- class membership is a Chinese restaurant process 
- infinity doesn't play nice with computer 
	- we use truncated infinite mixture models - put an upper limit on occupied classes 

# Gaussian Process Models 
