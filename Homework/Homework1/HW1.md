# Problem 1: Basic Probability
## (a)
>_probability of drawing a red ball from the bag_
$$
P(drawing~red~ball) =\frac{3}{10}=0.3
$$
## (b)
>_one ball blue next ball she draws is also blue_
$$
P(second~blue~|~first~blue) = \frac{4}{9}
$$
# Problem 2: Independent Events
## (a)
>_probability that 2 servers will be down at the same time?_

$$

P(\text{Both servers down}) =  P(\text{Server 1 down}) \times P(\text{Server 2 down}) = 0.05 \times 0.05 = 0.0025
$$
## (b)
> _probability that at least one of two servers will be down?_

$$
\begin{align}
P(both~down)&= 1-P(neither~down) \\
P(neither~down)&= P(!server1~down) \times P(!server2~down) \\
&= 0.95 \times 0.95 \\
&= 0.9025 \\
\\
P(both~down)&= 1-0.9025=0.0975
\end{align}
$$
# Problem 3: Conditional Probability
> 30% are data scientists; 40% data scientists have PhDs; 10% of non-data scientists have PhDs

- $P(\text{DS}) = \text{proportion of employees who are data scientists}=0.3$ 
- $P(PhD | DS) = \text{is PhD given data scientist}=0.4$
- $P(PhD|!DS)=\text{is PhD given not data scientist}=0.1$

## (a)
>_If an employee is chosen randomly, what is the probability that the employee is a Data Scientist with a PhD?_

$$
\begin{align}
P(DS~\cap~ PhD) &= P(\text{DS}) \times P(\text{PhD | DS})
\\ &= 0.3 \times 0.4 \\
&= 0.12
\end{align}
$$

## (b)
>_Given that an employee has a PhD, what is the probability that the employee is a Data Scientist?_

We use Bayes' Theorem 

$$
\begin{align}
P(DS~|~PhD) &= \frac{P(PhD|DS)*P(DS)}{P(PhD)}\\
&= \frac{P(DS~\cap~ PhD)}{P(PhD)} \\
\end{align} 

$$
$$\text{using law of total probability}$$
$$
\begin{align}
P(\text{PhD}) &= P(\text{DS}) \times P(\text{PhD | DS}) + P(!DS) \times P(\text{PhD | !DS}) \\
&= 0.3 \times 0.4+0.7\times0.1 \\
&= 0.12+0.07 \\
&= 0.19

\end{align}
$$
$$
So~P(DS~|~PhD)=0.12/0.19=0.632
$$
# Problem 4: Law of Total Probability
> A diagnostics test has a probability of 0.95 of giving a positive result when applied to a person suffering from a certain disease. It has a probability of 0.1 of giving a (false) positive result when applied to a non-sufferer. It is estimated that 0.5% of the population has this disease.

- D -> has disease
- D' -> does not have disease
- T -> test is positive

- P(T | D) = 0.95
- P(T | D') = 0.1
- P(D) = 0.005
- P(D') = 1-0.05 = 0.995
## (a)
> If a person tested positive in the test, what is the probability that the person actually has the disease?

$$
\text{the question asks for P(D|T)}
$$
$$
P(D | T) = \frac{P(T| D) \cdot P(D)}{P(T)} \text{ Bayes Theorm}
$$
$$\text{however P(T) is unknow but could be achieved by using law of total probability} $$
$$ 
\begin{align}
P(T) &=  P(T | D)P(D) + P(D')P(T|D') \\
P(T) &= 0.95 \times 0.005+0.995\times0.1=0.10425
\end{align}
$$
$$
So~P(D|T) = \frac{0.95\times0.005}{0.10425} = 0.0456
$$
The probability of person has the disease given positive test is 4.56%
## (b)
>What is the total probability of a person testing positive?

we know this from part a P(T) = 0.10425
# Problem 5: Bayes' Theorem
> An email filter is set up to classify emails into "spam" and "not spam". It is known that 90% of all emails received are spam. The filter correctly identifies 95% spam of the time and correctly identifies "not spam" 85% of the time.

- SP - spam
- SP' - not spam 
- FS - filter spam 
- FS' - filter not spam

- P(SP) - 0.9
- P(SP') = 0.1
- P(FS | SP) - 0.95
- P(FS' | SP') - 0.85
## (a)
> if an email is picked at random, and the filter classifies it as spam, what is the probability_that it is actually spam?

The question asks for P(FS | SP), using Bayes' Theorem:
$$
\begin{align}
P(SP|FP) &= \frac{P(FS|SP)\cdot P(SP)}{P(FS)}\\
&= \frac{P(FS|SP)\cdot P(SP)}{P(FS|SP)\cdot P(SP)+ P(FS|SP')\cdot P(SP')}\\
&= \frac{0.95\times0.9}{0.95\times0.9+ (1-0.85)\times 0.1} \\
&= 0.9828
\end{align}
$$
## (b)
> If an email is classified as "not spam", what is the probability that it is actually spam?

The question asks P(SP | FP'), using Bayes' Theorem: 
$$
\begin{align}
P(SP|FP') &= \frac{P(FS'|SP)\cdot P(SP)}{P(FS')}\\
&= \frac{P(FS'|SP)\cdot P(SP)}{P(FS'|SP)\cdot P(SP)+P(FS'|SP') \cdot P(SP')}\\
&= \frac{(1-0.95)\times0.9}{0.05\times0.9+0.85\times 0.1} \\
&= 0.3462
\end{align}
$$
# Problem 6: Expectation of a Discrete Random Variable
> Consider a dice game where you roll a fair six-sided die. If a 6 appears, you win $10. If any other number appears, you lose $2.

## (a)
> define the random variable X that models this game 

the random variable X that models the game is the amount of money won or loose by playing the game defined by the question
## (b)
> compute the expected value of X

- P(X=10) = 1/6
- P(X=-2) = 5/6
$$
\begin{align}
E(X) &= 10\times1/6+-2\times5/6\\
&= 0
\end{align}
$$
The expected value of X is 0
# Problem 7: Expectation of a Continuous Random Variable
> let X be a continuous random variable representing the time (in hours) it takes for a server to process a certain type of query. Suppose the density function of X is given by $f(x)=2e^{-2x}$  for $x\geq0$ 

## (a)
> compute the expected value $E(X)$ of X

$$
\begin{align}
E(X) &= \int_{0}^{\infty} x f(x) \, dx \\
&=  \int_{0}^{\infty} x \cdot 2e^{-2x} \, dx \\
&=  0.5 ~~\text{(answer obtained from calculator)}
\end{align}
$$
## (b)
> Compute the expected variance $Var[X]$ of X.

$$\text{Var}(X) = E(X^2) - [E(X)]^2$$
we already know E(X) from the previous question
to calculate E(X^2): 
$$ E[X^2] = \int_{0}^{\infty} x^2 \cdot 2e^{-2x} \, dx = 0.5$$
$$Var[x] = 0.5hours^2 - 0.5^2hours^2 = 0.25 hours^2$$
## (c)
> interpret your findings from parts (a) and (b) in the context of the server's processing time

Findings: 
- part (a)
	- the expected value of 0.5 means that on average the server takes 30 minutes to process this type of query
- part (b)
	- the variance of 0.25hours^2 means that the processing time could vary by 0.25hours^2 compare to the expected values
# Question 8: Markov Chain
>_Consider a simple weather model defined by a Markov chain. The weather on any given day can be either "sunny", "cloudy", or "rainy". The transition probabilities are as follows: 

-  if it is sunny today, the probabilities for tomorrow are: 0.7 for sunny, 0.2 for cloudy, and 0.1 for rainy.
- If it is cloudy today, the probabilities for tomorrow are: 0.3 for sunny, 0.4 for cloudy, and 0.3 for rainy
- if it is rainy today, the probabilities for tomorrow are: 0.2 for sunny, 0.3 for cloudy, and 0.5 for rainy

A transition matrix is a square matrix describing the transitions of a Markov chain. Each row of the matrix corresponds to a current state, and each column corresponds to a future state. Each entry in the matrix is a probability.
## (a)
> construct the transition matrix for this Markov Chain 

![[Pasted image 20240922173726.png|400]]

After many iterations or steps, the probabilities of being in each state may stabilize to a constant value. These constant values form the stationary distribution of the Markov chain. To compute the stationary distribution, find the probability vector that remains unchanged after multiplication with the transition matrix.
## (b)
> If today is sunny, what is the probability that it will be rainy two days from now?

Find two step transition probabilities 
![[Pasted image 20240922181232.png|400]]
The probability that it will be rainy two days from now if today is sunny is 0.18
## (c) 
> Find the stationary distribution of this Markov chain.

Per google search: 
![[Pasted image 20240922181608.png|450]]
![[Pasted image 20240922182248.png|500]]
## (d)
> Interpret the stationary distribution in the context of this weather model.

The results of the stationary distribution tells us that in the long run 46% of the days will be sunny, 28% of the days will be cloudy and 26% of the days will be rainy
# Question 9: Conjugate Priors and Posterior Distribution 
In Bayesian inference, the Beta distribution serves as a conjugate prior distribution for the Bernoulli, binomial, negative binomial, and geometric distributions. For a single observed data point, the Bernoulli distribution can be written as:
![[Pasted image 20240922183458.png|600]]
## (a) 
> Suppose the prior distribution for $\theta$  (the recovery rate) is Beta(2, 2). Calculate the posterior distribution after observing the results of the experiment.

we know that
- prior is beta(2,2)
- number of trials is 100
- x (success) = 30

from the lecture we know that the posterior of this situation is (conjugate prior)
![[Pasted image 20240922184118.png|200]]

the result is $Beta(2+30, 2+100-30)=Beta(32,72)$ 
## (b) 
> Based on the posterior distribution, provide an estimate for $\theta$

We know that for beta distribution the mean could be calculated as $\frac{\alpha}{\alpha + \beta}$ using the results from part (a) 
$$
\theta~estimate = \frac{32}{32+72}=0.31
$$

## (c) 
> Explain the role of the conjugate prior in simplifying the calculation of the posterior distribution

The conjugate prior entails the posterior distribution has the same distribution as the prior distribution. We can then simply use the prior distribution for the posterior distribution easily. 