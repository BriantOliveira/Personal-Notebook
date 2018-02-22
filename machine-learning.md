## Key machine learning terms and concepts {#key-machine-learning-terms-and-concepts}

Machine learning terms can be confusing. Here are definitions of key terms to help you. Use comments following to tell us about any other term you'd like defined.

### Data exploration, descriptive analytics, and predictive analytics {#data-exploration-descriptive-analytics-and-predictive-analytics}

**Data exploration**is the process of gathering information about a large and often unstructured data set in order to find characteristics for focused analysis.

**Data mining**refers to automated data exploration.

**Descriptive analytics**is the process of analyzing a data set in order to summarize what happened. The vast majority of business analytics - such as sales reports, web metrics, and social networks analysis - are descriptive.

**Predictive analytics**is the process of building models from historical or current data in order to forecast future outcomes.

### Supervised and unsupervised learning {#supervised-and-unsupervised-learning}

**Supervised learning**algorithms are trained with labeled data - in other words, data comprised of examples of the answers wanted. For instance, a model that identifies fraudulent credit card use would be trained from a data set with labeled data points of known fraudulent and valid charges. Most machine learning is supervised.

**Unsupervised learning**is used on data with no labels, and the goal is to find relationships in the data. For instance, you might want to find groupings of customer demographics with similar buying habits.

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

  










What sorts of questions can machine learning answer?

1. Is this A or B?
2. Is this weird?
3. How much - or - how many?
4. How this is organized?
5. What should I do next?

What are some common applications of machine learning in industry today?

 What are 3-5 questions \_YOU\_ are interested in using machine learning to answer?

