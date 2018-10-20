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

`P(A|B) = P(A & B) / P(B)`

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



