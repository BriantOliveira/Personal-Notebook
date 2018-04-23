## Key machine learning terms and concepts {#key-machine-learning-terms-and-concepts}

Machine learning terms can be confusing. Here are definitions of key terms to help you. Use comments following to tell us about any other term you'd like defined.

### Data exploration, descriptive analytics, and predictive analytics {#data-exploration-descriptive-analytics-and-predictive-analytics}

**Data exploration **is the process of gathering information about a large and often unstructured data set in order to find characteristics for focused analysis.

**Data mining **refers to automated data exploration.

**Descriptive analytics **is the process of analyzing a data set in order to summarize what happened. The vast majority of business analytics - such as sales reports, web metrics, and social networks analysis - are descriptive.

**Predictive analytics **is the process of building models from historical or current data in order to forecast future outcomes.

### Supervised and unsupervised learning {#supervised-and-unsupervised-learning}

**Supervised learning **algorithms are trained with labeled data - in other words, data comprised of examples of the answers wanted. For instance, a model that identifies fraudulent credit card use would be trained from a data set with labeled data points of known fraudulent and valid charges. Most machine learning is supervised.

**Unsupervised learning **is used on data with no labels, and the goal is to find relationships in the data. For instance, you might want to find groupings of customer demographics with similar buying habits.

#### Training data {#training-data}

When you train a model from data, you use a known data set and make adjustments to the model based on the data characteristics to get the most accurate answer. In Azure Machine Learning, a model is built from an algorithm module that processes training data and functional modules, such as a scoring module.

In supervised learning, if you're training a fraud detection model, you use a set of transactions that are labeled as either fraudulent or valid. You split your data set randomly, and use part to train the model and part to test or evaluate the model.

#### Evaluation data {#evaluation-data}

Once you have a trained model, evaluate the model using the remaining test data. You use data you already know the outcomes for, so that you can tell whether your model predicts accurately.

## Other common machine learning terms {#other-common-machine-learning-terms}

* **algorithm**: A self-contained set of rules used to solve problems through data processing, math, or automated reasoning.
* **anomaly detection**: A model that flags unusual events or values and helps you discover problems. For example, credit card fraud detection looks for unusual purchases.
* **categorical data**: Data that is organized by categories and that can be divided into groups. For example a categorical data set for autos could specify year, make, model, and price.
* **classification**: A model for organizing data points into categories based on a data set for which category groupings are already known.
* **feature engineering**: The process of extracting or selecting features related to a data set in order to enhance the data set and improve outcomes. For instance, airfare data could be enhanced by days of the week and holidays. 
  .
* **module**: A functional part in a Machine Learning Studio model, such as the Enter Data module that enables entering and editing small data sets. An algorithm is also a type of module in Machine Learning Studio.
* **model**: A supervised learning model is the product of a machine learning experiment comprised of training data, an algorithm module, and functional modules, such as a Score Model module.
* **numerical data**: Data that has meaning as measurements \(continuous data\) or counts \(discrete data\). Also referred to as
  _quantitative data_
  .
* **partition**: The method by which you divide data into samples.
* **prediction**: A prediction is a forecast of a value or values from a machine learning model. You might also see the term "predicted score." However, predicted scores are not the final output of a model. An evaluation of the model follows the score.
* **regression**: A model for predicting a value based on independent variables, such as predicting the price of a car based on its year and make.
* **score**: A predicted value generated from a trained classification or regression model, using the
  Score Model module
  in Machine Learning Studio. Classification models also return a score for the probability of the predicted value. Once you've generated scores from a model, you can evaluate the model's accuracy using the evaluate Model module.
* **sample**: A part of a data set intended to be representative of the whole. Samples can be selected randomly or based on specific features of the data set.

**What sorts of questions can machine learning answer?**

**1.Is this A or B? \(Classification\)**

This family of algorithms is called two-class classification.

It's useful for any question that has just two possible answers.

For example:

* Will this tire fail in the next 1,000 miles: Yes or no?
* Which brings in more customers: a $5 coupon or a 25% discount?

This question can also be rephrased to include more than two options: Is this A or B or C or D, etc.? This is called multiclass classification and it's useful when you have several — or several thousand — possible answers. Multiclass classification chooses the most likely one.

The goal of classification is to identify what\_class\_a sample belongs to.

A class could be something like_Windows 10 Mobile_, whereas a sample could be something like_phone_. To get classification working, you have to feed the computer a large number phone samples, some of them labeled_Windows 10 Mobile_, and others labeled, well..._non-Windows 10 Mobile_. With enough training data, a classifier will eventually be able to generalize what similarities constitute a Windows 10 Mobile phone and voilà, you've trained a computer to figure out phone types!Given a list of emails marked spam and not-spam, figure out if a newly received message is actually spam or not.

* Given many different images of your friends, perform facial recognition on a new, never-before seen image of one of your friends.
* After being trained with a few books, decide which of the before seen authors wrote an unidentified article.
* Given a list of physical symptoms, determine what ailment a person has.

Classification falls into the realm of supervised learning because for it to work, you have to guide the computer by proving it with examples of correctly labeled records. Once you're done training the computer, you can test it by seeing how accurately it scores those new records.

**2. Is this weird? \(Anomaly detection\)**

If you have a credit card, you’ve already benefited from anomaly detection. Your credit card company analyzes your purchase patterns, so that they can alert you to possible fraud. Charges that are "weird" might be a purchase at a store where you don't normally shop or buying an unusually pricey item.

This question can be useful in lots of ways. For instance:

* If you have a car with pressure gauges, you might want to know: Is this pressure gauge reading normal?
* If you're monitoring the internet, you’d want to know: Is this message from the internet typical?

Anomaly detection flags unexpected or unusual events or behaviors. It gives clues where to look for problems.

**3. How much - or - how many? \(Regression Algorithms\)**

Now the last two questions are a bit more advanced.

Sometimes you want to understand the structure of a data set - How is this organized? For this question, you don’t have examples that you already know outcomes for.

There are a lot of ways to tease out the structure of data. One approach is clustering. It separates data into natural "clumps," for easier interpretation. With clustering, there is no one right answer.

The goal of regression is to predict\_continuous-valued\_features associated with many samples. Continuous-valued meaning small changes in the input result in small changes of the output.

Imagine driving from New York to San Francisco. As time progresses, your distance from New York increases and your distance to San Francisco decreases. Even though you stop for meals and to rest, these distance values transition smoothly. Throughout the course of your travel, you never magically teleport a large distance. Instead, you smoothly and incrementally make your way bit by bit.

With regression, a mathematical relationship is modeled for your samples so that as you gently alter an input feature, your output feature\(s\) respond by being altered as well. In our example, that would be your time journeying and your distance to your destination!

* Calculate an equation to predict the size of a house given its price, or the price of a house given its size.

* Explore if a correlation exists between the hours a student spends studying, spends watching TV, and their final exam score.

* Estimate how many power plants should be constructed in the next 50 years, based upon the historical energy consumption per household.
* Figure out how many days a person has left to live based on the severity of their symptoms.

Regression falls into the realm of supervised learning because you have to provide the computer with labeled samples. It then attempts to fit an equation to the samples' features.

**4. How this is organized? \(Clustering Algorithms\)**

Common examples of clustering questions are:

* Which viewers like the same types of movies?
* Which printer models fail the same way?

By understanding how data is organized, you can better understand - and predict - behaviors and events.

The goal of clustering is to automatically group similar samples into sets.

Since a clustering algorithm has no prior knowledge of how the sets should be defined, and furthermore, since the clustering process is unsupervised, it needs to have a way to tell which samples are the most similar so it can group them accordingly. It does this the same way we humans do: by looking at the various characteristics and features of each sample.

Match similar people on a matrimonial website based on their profile answers.

* Through examining search history, recommend houses a prospective home-buyer might be interested in buying.
* Pinpoint the most likely location for a future earthquake using past seismic data.
* Identify new characteristics shared by different people suffering from the same disease.

There are different types of clustering algorithms, some supervised, some unsupervised. There are even semi-supervised clustering methods as well.

In this course, you'll only be dealing with unsupervised clustering. In other words, the clustering algorithm you will use won't need anything except your raw data. No labels hinting at desired clustering outcome will be provided to the algorithm.

**5.What should I do next? \(Reinforcement Learning Algorithms\) **

Questions it answers are always about what action should be taken - usually by a machine or a robot. Examples are:

* If I'm a temperature control system for a house: Adjust the temperature or leave it where it is?
* If I'm a self-driving car: At a yellow light, brake or accelerate?
* For a robot vacuum: Keep vacuuming, or go back to the charging station?

Reinforcement learning algorithms gather data as they go, learning from trial and error.

The goal of reinforcement learning is to maximize a cumulative reward function--or equivalently, minimize a cost function--given a set of actions and results.

Reinforcement learning is modeled to mimic the way we learn in the real world. We try to solve problems using different techniques. Most of the time, nothing of merit results from our experiments. But occasionally, we stumble upon a set of actions that cause a sweet reward. When this happens, we attempt to repeat those actions that get us rewarded.

If we are rewarded yet again, we further associate those actions with the reward, and this is known as the reinforcement cycle. The entire process is also known as performance maximization.

Discover how to fly a quadcopter by minimizing the function which evaluates the chances of it crashing.

* Learn to beat a video game like 'Super Mario Bros.' by minimizing the time it takes to get to the castle.
* Attempt to take a photo and "re-draw" it in the style of a particular artist.
* Automate the trading of stocks and securities by maximizing profit and minimizing transaction fees.

Reinforcement learning is a bit different from regular supervised and unsupervised learning. To illustrate this difference, imagine you had a rubick's cube. With unsupervised learning, none of your data has a label. Due to this, you neither know if the cube is in a solved state, an unsolved state, or even what you need to do with it! All you can do is learn about the structure of the cube--namely that it has six distinct colors, and 9 pieces per face, all belonging to a specific color.

With supervised learning, your aim might be to find if the rubick's cube is in a solved configuration or not. To teach a computer this, you'd have to show it many hundreds of examples of rubick's cubes, each labeled solved or not-solved. We refer to this 'dense' labeling.

With reinforcement learning, your goal might be something like given a rubick's cube in some initial configuration, derive a set of actions which would result in it being solved. Training a computer to do this would involve having the computer attempt to change the state of the cube many times, and then after a while, informing the computer if it's succeeded or failed. With enough trials, the computer will get better at quickly doing those actions which result in a successfully solved puzzle, irrespective of the initial configuration of the cube. As such, reinforcement is a type of 'sparsely' labeled, semi-supervised learning.

To learn more about reinforcement learning, take a look at the Dive Deeper section. We won't return to reinforcement learning in this class, but it's important to be aware of it as a data scientist. Much work has been done using reinforcement learning and deep neural networks that are of benefit to machine learning.

**6. Dimensionality Reduction**

The goal of dimensionality reduction is to systematically and intelligently reduce the number of features considered in a dataset. Stated differently, trim the fat off. Often times, in one's eagerness to collect enough data for machine learning to be effective, you might add irrelevant features to your dataset. Bad features have the effect of hindering the machine learning process, and make your data harder to understand. Dimensionality reduction attempts to trim your dataset down to the bare essentials needed for decision-making.More Examples

* Given a 100 question survey, attempt to find the gist of what is truly being assessed; then rephrase it with just 5 questions.
* Build a robot that can recognize pictures of similar objects, even if they are rotated at odd angles and orientations.
* Compress a video stream by reducing the number of colors.
* Summarize a long book.

Dimensionality reduction falls into the realm of unsupervised learning because you don't instruct the computer which features you want it to create. Rather, the computer infers this information automatically by examining your unlabeled data.

**What are some common applications of machine learning in industry today?**

Banks use machine learning to predict which transactions where made by you. Netflix uses machine learning to predict which movies you most likely would like to watch.

What are 3-5 questions \_YOU\_ are interested in using machine learning to answer?

In decision threes gini represent the enpure data.

In Machine learning when you are replacing any missing data values is -99999, most algorithms recognizes those values as outliers. Ex:

```
df.replace('?', -99999, inplace=True)
```

The **KNN algorithm **is a classic choice for classification in Machine Learning. KNN works on the assumption that things that are "near" each other are more similar, and therefore more likely to be the same class. Here's a brief explanation of how KNN actually works under the hood:

1. KNN stores all the data points and labels when
   `.fit()`
   is called. No actual computation is done at this point.
2. When used for predicting the class of an array of objects, the user passes in an array of X\_values and a value for K.
3. KNN calculates the Euclidean distance between the point in question and all other points it stored during the
   `.fit()`
   step.
4. KNN uses these Euclidean distance metrics to select the K nearest points, and looks at what class each is.
5. The algorithm predicts that the data point in question is whichever class most the majority of it's K nearest neighbors are. For instance, if
   `K=5`
   , and 3 of the neighbors for
   `X[0]`
   are class A and 2 are class B, the algorithm will predict that
   `X[0]`
   is class A.

---

**QUIZ**

1. **This course's approach to instructing data science is through:**

Arming you with the know-how needed solve data driven problems, then having you attempt to do so.

2. **Which statement makes the most sense about data analysis?**

Special care ought be dedicated to collecting data, so that you have enough of it to do effective analysis.

3. **If you want to engage the data analysis process, the best place to start is by...**

Having a question in mind to drive your data collection process.

4. **What is the difference between supervised and unsupervised learning?**

Unsupervised learning attempts to extract patterns; supervised learning tries to fit rules and equations.

5. **Select the three best applications of machine learning:**

* Getting computers to solve data driven problems.

* Using computers to solve tasks that involve fine-tuning many parameters.

* When you have many observations to train a computer against.

6. The small credit union / bank you've worked at for the past ten years is having cash-flow issues. Upon further inspection, it turns out most of their clients are defaulting on loans! In trying to rectify the business, you've been assigned the task of studying all client data, and then suggesting a method to identify which prospective borrowers are likely to default on their loans.  
**What type of machine learning would you engage to solve this problem?**

Classification

7. After doing a great job of solving the cash flow issue by denying loans to bad clients, your boss issued a client satisfaction survey to ensure that those who remained loyal customers were happy with all the new process changes. Apparently, he was really motivated while creating the survey because he came up with thirty questions. Even more amazingly, almost all the clients responded! Now your weekend plans are ruined because you have to go through thousands of survey responses to summarize how the clients are feeling about the credit union.

**What type of machine learning would you engage to solve this problem?**

Dimensionality Reduction

8. **Which of the following is an example of regression?**

Calculating the relationship between a black hole's mass and its Hawking radiation.



