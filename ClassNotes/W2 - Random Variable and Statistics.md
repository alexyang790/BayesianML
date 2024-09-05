# Why do We Need Distributions
Learning about probability distributions is fundamental to understanding and applying statistical methods and data analysis. Here are some key reasons why understanding distributions is important:

### 1. **Modeling Real-World Phenomena:**
   - **Describing Random Events:** Distributions provide a mathematical framework to describe how random variables behave. Whether it's the height of people, the time until a machine fails, or the number of emails received in an hour, distributions help model these real-world phenomena.
   - **Understanding Patterns:** By understanding distributions, we can identify patterns in data, make predictions, and draw inferences. For example, knowing that data follows a normal distribution allows us to apply techniques like hypothesis testing and confidence intervals.

### 2. **Foundation for Statistical Inference:**
   - **Hypothesis Testing and Estimation:** Many statistical methods, such as t-tests, ANOVA, and regression analysis, are based on assumptions about the underlying distributions of the data. Understanding distributions allows you to correctly apply these methods and interpret the results.
   - **Central Limit Theorem:** The central limit theorem states that the sampling distribution of the sample mean approaches a normal distribution as the sample size grows, regardless of the original distribution of the data. This is foundational for many statistical techniques.

### 3. **Decision Making Under Uncertainty:**
   - **Quantifying Risk:** Distributions allow us to quantify the likelihood of different outcomes. This is critical in fields like finance, insurance, and engineering, where decisions are often made under uncertainty.
   - **Optimizing Processes:** Understanding the distribution of outcomes can help in optimizing processes, improving quality control, and minimizing risks. For example, in manufacturing, understanding the distribution of product dimensions can help ensure that products meet quality standards.

### 4. **Basis for Machine Learning:**
   - **Probabilistic Models:** Many machine learning algorithms, especially those in the field of probabilistic modeling (like Bayesian networks), rely on the principles of probability distributions.
   - **Data Generation and Simulation:** Distributions are used to generate synthetic data, simulate different scenarios, and understand how algorithms perform under various conditions.

### 5. **Interpreting Data:**
   - **Identifying Data Characteristics:** Knowing the distribution of data helps in identifying its characteristics, such as skewness, kurtosis, and the presence of outliers. This informs the choice of statistical methods and how to interpret the results.
   - **Choosing the Right Model:** Different distributions are used to model different types of data (e.g., normal distribution for continuous data, Poisson distribution for count data). Understanding the appropriate distribution to use is critical for accurate modeling and analysis.

### 6. **Developing Intuition:**
   - **Building Statistical Intuition:** Understanding distributions helps build intuition about data and randomness. It allows you to anticipate how changes in data or model assumptions might affect outcomes.
   - **Communication and Reporting:** When analyzing data, explaining the distribution of data can help communicate findings effectively, especially when dealing with uncertainty or variability.

### 7. **Predicting Future Events:**
   - **Forecasting:** Distributions are used in forecasting future events based on historical data. For example, time series analysis often involves assuming certain distributions for the underlying processes.

### Summary:
Understanding distributions is crucial for modeling real-world phenomena, performing statistical inference, making informed decisions under uncertainty, developing machine learning models, and accurately interpreting data. They form the backbone of many statistical methods and provide the tools needed to analyze, predict, and make decisions based on data.
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

## ChatGPT on C vs D Distribution
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

## The Binomial Distribution (Discrete)

## The Poisson Distribution (Discrete)
- probability of n events occurring in a fixed interval of time, if the rate of the events happening is constant

# Categorical Distributions
## Multinomial Distribution 
- the probability that you will select a given item $i$ from a selection of $k$ categories
## Univariate vs Multivariate Distributions
> random variables don't need to output single bumbers

**Definition of *multivariate distributions*:**
- A **multivariate distribution** is a probability distribution that describes the behavior of multiple random variables simultaneously. These random variables may be dependent or independent, and the distribution captures the joint behavior and interactions between them.
### Multivariate Normal
