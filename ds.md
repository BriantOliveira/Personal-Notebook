Question 1: Joma takes an STD test and the test is advertised as being 99% accurate: if you have the std you will test positive 99% of the time, and if you don't have the std, you will test negative 99% of the time. If you have 1% of all people have this std and Joma test positive, what is the probability that Joma has the disease?

```
    99% (Probability of this event happening) = 99% (Numbers of ways it can happen)/ 
                                                1%(Total numbers of outcome)

   1% x 99%/ 1% x 99% + 1% = 50%
```

Question 2: Notvine is a platform where users can share 6.1 looping videos as seen in the startup series and it's basically a feed of content you follow. Now imagine we are considering launching a share button, where can share else video and it will show to your followers. How would you evaluate this change? What metrics do you expect to change? How will you decide to launch it or not?

A: Do an experimental roll out only a few publishers first, and then a/b test it. So for some users they see it and for some they don't see the shared post.  That way we can see consumer behavior.

**Probability **

The chances of an event occuring or how likely an event is to occur, in a set of events.

In math probability is modeled by the expression:

```
P(A) = Count of A/ Sample Space
```

P is the probability of the event A occurring  in a set of observed events sample space count of A - is the number of times an certain detail was present in the whole set sample Space - total number of observed events.

**Conditional Probability**

The conditional probability of an event occurring \( called B\) is the probability that the event will occur, given the knowledge that another event \(A\) has already occurred.

`P(A|B) = P(A & B) / P(A)`

```
# To get the conditional probability
def conditional_prob(subset_count, event_count, sample_space):
    subset_prob = subset_count/ sample_space
    event_prob = event_count / sample_space
    conditional_p = (subset_prob)/ event_prob
    return 'The conditional probability of this occuring out of {} events is {}'.format(sample_space,conditional_p)



# To get the percentage of the conditional probability
def conditional_prob_percentage(cond_prob):
    percentage = cond_prob * 100
    return '{}% chance of occuring'.format(percentage)



# To get the fracitonal representation
def conditional_prob_fraction(cond_prob,sample_space):
    numerator = round(cond_prob / cond_prob)
    denominator = round(sample_space / cond_prob)
    return '{} / {} chance of occurence'.format(numerator, denominator)
```

```
 P(A|B) = P(A Ω B)/P(B)
```

Random variables X and Y are independent if and only if P\( X = x, Y=y \). How does this interact with conditional probability?

Conditional probabilities equal unconditional probabilities with independence:

P\(X = x/Y\) = P\(X=x\)

Knowing Y tell us about X

To turn a condition distribution into a joint distribution for that we'll use the chain rule and sometimes you need to flip the order of the conditionality for that we use Bayes rule the definition of condional probability let us derive what's called the chain rule.

**The chain rule** is what allow us to turn conditional probability into joint probabilities.

```
P(X, Y) = P(X, Y) P(Y)/P(Y)
        = P(X, Y) P(Y)
```

* For example, let Y be a disease and X be a symptom. We may know P\(X \| Y\) and P\(Y\) from data. Use the chain rule to obtain the probability of having the disease and the symptom. 
* In general, for any set of N variables.

##### **Bayes rule**

Bayes rule allow us to flip the rder of a conditionality.

```
P(B|A) = P(A|B)P(B)/P(A)
```

1. Start with P\(A\|B\)
2. Change outcome space from B to Ω: P\(A\|B\)P\(B\)
3. Change outcome space from Ω to A: P\(A\|B\)P\(B\)/P\(A\)

**Binomial and Discrete Distributions**

**Binomial distribution** the Bernoulli distribution is a distribution over some process that has successes and failures.

* Bernoulli:distribution over tow values \(success or failure\) from a single event. 
* Binomial: number of success from multiple Bernoulli events
* Examples:
  * The number of times "heads" comes up after flipping a coin 10 times. 
  * The number of defective TV's in a line of 10,000 TVs
* Important: each Bernoulli event is assumed to be independent. 
* Notation: let X be a random variable that describes the number of success out of N trials.

  * The possile values of X are integers from 0 to N: {0,1,2,...,N}

* Suppose we flip a coin 3 times. There are 8 possible outcomes:

```
P(HHH) = P(H)P(H)P(H) = 0.125
P(HHT) = P(H)P(H)P(T) = 0.125
P(HTH) = P(H)P(T)P(H) = 0.125
P(HTT) = P(H)P(T)P(T) = 0.125
P(THH) = P(T)P(H)P(H) = 0.125
P(THT) = P(T)P(H)P(T) = 0.125
P(TTH) = P(T)P(T)P(H) = 0.125
P(TTT) = P(T)P(T)P(T) = 0.125 
                      = .375
```

The probability mass function for the binomial distribution is:

```
f(x) = (N x) 0^x(1-)^N-x
```

* Like the Bernoulli, the binomial parameter 0 is the probability of success from one event. 
* Binomial has second parameter N: number of trials.
* The PMF important: difficult to figure out the entire distribution by hand. 

The expression \(nk\) is called a binomial coefficient. Also called a combination in combinatorics.

\(kn\) is the number of ways to choose k elements from a set of n elements.

For example, the number of ways to choose 2 heads from 3 coin flips: HTT, HTH, THH

```
(n) =  n!
(k)   k!(n-k)!
```

**Mean** - calculated the average of numbers of occurrences or the average numerical value if all the data was distributed evenly among all the samples..

```
.mean()
```

**Median** - is the medium value, that represents half of the number being above and half of the numbers being below it.

```
.median()
```

**Mode** - is the number that appears the most in dataset.

```
.mode()
```

**Null Hypothesis**

A null hypothesis is a precise statement about a population that we try to reject with sample data.

**P-values**

A p-value is the probability of finding some sample outcome or a more extreme one if the null hypothesis is true.

### **Data Mining**

**Unsupervised Learning** - Analyze the dataset patterns of the dataset without any labels. Without you being the architech of the data.\(Clusters/Reduction Analysis\) Ex: K-mean, Gaussian Mixture

* Looking for patterns in your data
* Looking for clusters in your data

**Supervised Learning - **This type of learning is a little different from Unsupervised. It assumes that you know something about your data , so you would classify your data. \(Classification/Regression\) Ex: KNN

* You provide labels for data
* Labeling new data
* Training data/ Test data 

For supervised learning it is possible to evaluate the model from train and test data. For regression, the evaluation metrics are: 

1. Mean squared Error\(MSE\)
2. Mean Absolute Error\(MAE\)

And for classification:

1. Classification Accuracy
2. Classification Recall, Precision and F1 scores.  

**Cross Validation** -  You should **always** cross validate, either with Supervised learning. Train 80% of your data against 20% and keep track of the accuracy. For unsupervised learning there are no systematic approach to evaluate to models but the are ways to do it. 



