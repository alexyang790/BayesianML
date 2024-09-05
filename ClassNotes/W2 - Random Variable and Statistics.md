
# Random Variables and Distribution 
Random vars have a **probability distribution**
- the p.d. is a function (a probability measure) that maps the values a random variable can take to probabilities
	- not technically true but good enough

> Any functions that fulfills the axioms of probability is a probability distribution

The named p.d. are just ones that are well behaved or have interesting properties

# The normal distribution 
**Support**
- the normal has **support** on all real numbers from negative infinity to positive infinity

**Parameters**
- all distributions are governed by parameters (notated by greek symbols)
- these are the numbers that control the shapes of the distribution 
- the normal is parameterized by µ 
- *Gamma distribution*

# Continuous vs Discret Distribution 
> the support determines the type of distribution 

**Poisson Distribution**
Support - non-negative integers 

## **ChatGPT Answer**
The primary difference between continuous and discrete distributions lies in the type of values that the random variables associated with these distributions can take and how probabilities are assigned to these values.

### Discrete Distribution:
- **Definition:** A discrete distribution is associated with a random variable that can take on a countable number of distinct values. These values can often be listed out explicitly, like integers or categories.
  
- **Support:** The support of a discrete distribution consists of isolated points (e.g., integers, categories).

- **Probability Assignment:** In a discrete distribution, probabilities are assigned to each specific value that the random variable can take. The sum of these probabilities is equal to 1. For example, the probability mass function (PMF) gives the probability that a discrete random variable is exactly equal to some value.

  - **Example:** The Binomial distribution is a discrete distribution where the random variable represents the number of successes in a fixed number of independent Bernoulli trials (e.g., flipping a coin 10 times and counting the number of heads).

- **Representation:** Probabilities are represented as sums. For example, \( P(X = k) \) is the probability that the random variable \(X\) takes the value \(k\).

### Continuous Distribution:
- **Definition:** A continuous distribution is associated with a random variable that can take on an infinite number of possible values within a given range. These values are typically real numbers and can include fractions or irrational numbers.

- **Support:** The support of a continuous distribution is typically an interval or union of intervals on the real number line.

- **Probability Assignment:** In a continuous distribution, the probability of the random variable taking any exact specific value is zero. Instead, probabilities are assigned to intervals of values, and these probabilities are determined using the probability density function (PDF). The area under the curve of the PDF over an interval gives the probability that the random variable falls within that interval.

  - **Example:** The Normal distribution is a continuous distribution where the random variable can take any real number, with a bell-shaped curve representing the distribution of values around a mean.

- **Representation:** Probabilities are represented as integrals. For example, \( P(a \leq X \leq b) \) is the probability that the random variable \(X\) falls within the interval \([a, b]\), which is computed as the area under the curve of the PDF from \(a\) to \(b\).

### Summary

| Aspect                     | Discrete Distribution                         | Continuous Distribution                                    |
| -------------------------- | --------------------------------------------- | ---------------------------------------------------------- |
| **Values**                 | Countable, distinct values (e.g., integers)   | Uncountable, infinite possible values (e.g., real numbers) |
| **Probability Assignment** | Assigned to individual values via PMF         | Assigned to intervals via PDF                              |
| **Sum/Integral**           | Sum of probabilities over all possible values | Integral of the PDF over a range of values                 |
| **Example**                | Binomial, Poisson                             | Normal, Uniform                                            |

# The Binomial Distribution (Discrete)

# The Poisson Distribution (Discrete)
- probability of n events occurring in a fixed interval of time, if the rate of the events happening is constant