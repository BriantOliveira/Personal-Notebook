# Udacity - Statistics Data Science

##### Klout Data -

* Take all samaples of size 35.

* Find mean of each sample.

* Graph distribution of sample means \(sampling distribution\) .

##### Standard deviation -

A quantity calculated to indicate the extent of deviation for a group as a whole.

Standard error:

Population Standard deviation / the square root of n \(sample size\).

Margin of error - Two times the population standard deviation divided by the root n.

#### Measures of center

Mean

* has a simple equation \(the sum of X / n\). 
* The mean will also change if any data values changes. 
* The mean will not be affected by change in the bin size

~ QUIZ

~ Which of the following is true for the normal distributions?

* The mean, media, and more are all equal. 

~ If a positively skewed distribution has a median of 50, which of the following is true?

* The mean is greater than 50. 
* The mode is less than 50
* The median is greater than the mode, but less than the mean. 

~ Which of the following is true of the mean?

* For normal distributions, it is approximately equal to the median and mode.

~ Which of the follow is true of the mode?

* It is not affected by extreme score \(outliers\).
* For normal distributions, it is approximately equal to the mean and median. 
* It is the most frequently occurring score. 
* It can be used to describe categorical data, such as gender or country of origin. 

~ Which of the following is true of the median?

* It is the exact middle of any distribution \(half the data is less than the median, half is more\)
* It is nor affected by extreme scores\(outliners\).
* For normal distributions, it is approximately equal to the mean and mode.

**Outilier** &lt; Q1 - 1.5 \(IQR\)

Q3 + 1.5 \(IQR\)

**SS** \(Sum of squares\) = M \(xi - x\)

**Variance** -

* Mean of squared deviations
* Sum of squared deviations divided by n

**Standard deviation** -

* Square root of average squared deviation. 
* Square root of \(\(Sum of square deviations\) divided by n\).

A negative **Z-Score** means:

* The original value is less than the mean. 
* The original value minus the mean is negative. 

The z-score of any value, that's one standard deviation away from the mean, will then be 1 after we standardize it.

X - M/ std

**Standard normal distribution **

When we have a normal distributions, we can standardize it by **first subtracting the mean, shifting it to 0. And then dividing by the standard deviation, which makes the standard deviation 1.**

Probability Density Function \(PDF\).

Mean - the average

Median - in the middle

Mode - The most common

To find the mean - add up the values in the data set and then divide by the number of values that you added.

To find the median - list the values of the data set in numerical order and and identify which values of the data set in numerical order and identify which value appears in the middle of the list.

To find the mode - identify which value in the data set occurs most often.

#### Conditional Probability -

Of an event B is the probability that the event will occur given the knowledge that an event A has already happen.

**If eventsAandBare not independent, then the probability of theintersection of A and B**\(the probability that both events occur\) is defined by  
P\(A and B\) = P\(A\)P\(B\|A\).

From this definition, the conditional probabilityP\(B\|A\)is easily obtained by dividing byP\(A\):

P\(B/A\) = P \(A and B\) / P\(A\)

Beer and Dippers

BI \(Business Intelligence\) uses Data mining is a process that looks for patterns in data, so in a sense it is like querying the data. The Crucial differences between simply querying the data and data mining can be summed up as intent and scale.

Different Statistical Distributions

![](/assets/Screen Shot 2018-01-16 at 3.08.50 PM.png)

##### **Regression** -

The goal of regression is to predict _continuous-valued_ features associated with many samples. Continuous-valued meaning small changes in the input result in small changes of the output.

**Clustering - **

The goal of clustering is to automatically group similar samples into sets.

Since a clustering algorithm has no prior knowledge of how the sets should be defined, and furthermore, since the clustering process is unsupervised, it needs to have a way to tell which samples are the most similar so it can group them accordingly. It does this the same way we humans do: by looking at the various characteristics and features of each sample.

**Dimensionality Reduction - **

The goal of dimensionality reduction is to systematically and intelligently reduce the number of features considered in a dataset. Stated differently, trim the fat off. Often times, in one's eagerness to collect enough data for machine learning to be effective, you might add irrelevant features to your dataset. Bad features have the effect of hindering the machine learning process, and make your data harder to understand. Dimensionality reduction attempts to trim your dataset down to the bare essentials needed for decision-making.

**Reinforcement Learning - **

The goal of reinforcement learning is to maximize a cumulative reward function -- or equivalently , minimize a cost function--given a set of actions and results.

Reinforcement learning is a bit different from regular supervised and unsupervised learning. With unsupervised learning, none of your data has a label.

#### Central Limit Theorem

You can start with any distribution that contain a well defined mean and variance. The central limit theorem states that given a distribution of the mean \(μ\) approaches a normal distribution with a mean and a variance σ²/N as N, the sample size, increases.

**With** **replacement** means that you take a value and then you return. **Without replacement** means that you take a value and you do not return.









