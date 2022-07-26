---
name: Flight Delay Predictor 
tools: [Machine Learning,sklearn, Flask]
image: https://i.ibb.co/M1VX2xc/flight.jpg
description: Machine learning based predictor that can predict whether a flight is delayed or not. 
---
# Introduction
Flight delays in today's world is a major concern. This is directly dependent on the fact that people have begun to increasingly use aviation as a mode of transportation. However the process is is still complicated, as a result of which delays in flights can cause major loss to travellers time. Our project aims to help people in this section. By providing information about flights and their respective delays people can plan and schedule activities based of it. <br> Flight delay is inevitable and it plays an important role in both profits and loss of the airlines. An accurate estimation of flight delay is critical for airlines because the results can be applied to increase customer satisfaction and incomes of airline agencies. There have been many researches on modeling and predicting flight delays, where most of them have been trying to predict the delay through extracting important characteristics and most related features. However, most of the proposed methods are not accurate enough because of massive volume data, dependencies and extreme number of parameters. In our project the aim was ultimately to be able to predict flight delays to users, witch minimal parameters possible.<br> Our project to a great extent has been able to do and possibly in future iterations would be able to be more successful.

# Dataset
We used a 2013 Flight Delay Dataset. It was published by the U.S. Department of Transportation's (DOT) Bureau of Transportation Statistics and contains flight data for 16 major airlines during 2013. The data was based on 10 parameters:<br>
1. year
2. month
3. day
4. departure time
5. carrier
6. origin
7. destination
8. temperature
9. humidity
10.  bin

# Implementation
Flight delay prediction is a complex topic as even the slightest changes, after communication may lead to various sorts of delays. The model could be build in two ways, namely:

## Batch processing based model
An efficient way of processing high/large volumes of data is what you call Batch Processing. It is processed, especially where a group of transactions is collected over a period of time.. In other words, this method also means waiting to do everything at once. Hence, it relies on the ability of the system to handle all the processing.

### Advantages
- Batch Processing is Ideal for processing large volumes of data/transaction. It also increases efficiency rather than processing each individually.
- Here, we can do processing independently. Even during less-busy times or at a desired designated time.
- For the organization by carrying out the process, it also offers cost efficiency.
- It allows a good audit trail.

### Disadvantages
- The time delay between the collection of data and getting the result after the batch process.
- In the batch processing master file is not always kept up to date.
- A one-time process can be very slow.

## Real-Time Processing based model
Real-Time Processing involves continuous input, process, and output of data. Hence, it processes in a short period of time. There are some programs which use such data processing type. For example, bank ATMs, customer services, radar systems, and Point of Sale(POS) Systems. Every transaction is directly reflected in the master file, with this data process. So, that it will always be up-to-date.

### Advantages
- In such models there is no significant delay in response.
- Information is always up to date. Hence, it makes the organization able to take immediate action. Also, when responding to an event, issue or scenario in the shortest possible span of time.
- For organization able to gain insights from the updated data. Even helps to detect patterns of possible identification of either opportunities or threats

### Disadvantages
- Real-Time processing is very complex as well as expensive processing.
- The process turns out to be very difficult for auditing.
- Real-Time processing is a bit tedious processing.
<br> In order to be able to build a real time processing system we did not have the resources to be able to manipulate and process such amounts of data. At the same time we wanted the best of both worlds and hence came up with an idea to build the project in such a manner that the model be build continuously by just the running a script, that is we build a automated pipeline, which requires the new data to be added.


# Model

## Preprocessing
Data pre-processing is a process of preparing the raw data and making it suitable for a machine learning model. It is the first and crucial step while creating a machine learning model. Doing any operation with data, it is mandatory to clean it and put in a formatted way. So for this, we use data pre-processing task. The dataset we use has both column and numeric columns, these need to go various pre-processing tasks before they can be used to train the model. 

### Simple Imputer
SimpleImputer is used to impute or replace the numerical or categorical missing data related to one or more features with appropriate values. 
> We use this for both our numeric and categorical columns.

### Standard Scaler
StandardScaler removes the mean and scales each feature/variable to unit variance. This operation is performed feature-wise in an independent way. StandardScaler standardizes a feature by subtracting the mean and then scaling to unit variance. Unit variance means dividing all the values by the standard deviation.
> We use on the numeric columns in order to normalise the data values.}=

### OneHotEncoder
This is a type of categorical encoding  transforms the categorical variables into a set of numeric variables (also known as dummy variables).In the One-Hot-Encoding method categorical data encoding technique when the features are nominal(do not have any order). In one hot encoding, for each level of a categorical feature, we create a new variable. Each category is mapped with a binary variable containing either 0 or 1. Here, 0 represents the absence, and 1 represents the presence of that category.That means for N categories in a feature, it uses N binary variables.
> We use this on the categorical columns to represent variables as numbers.

## Choosing a model

### Logistic Regression
Logistic regression is a supervised learning classification algorithm used to predict the probability of a target variable. The nature of target or dependent variable is dichotomous, which means there would be only two possible classes.\par In simple words, the dependent variable is binary in nature having data coded as either 1 (stands for success/yes) or 0 (stands for failure/no). \par Mathematically, a logistic regression model predicts P(Y=1) as a function of X.

### Naive Bayes
Naïve Bayes algorithm is a supervised learning algorithm, which is based on Bayes theorem and used for solving classification problems. It is mainly used in text 
classification that includes a high-dimensional training dataset. Naïve Bayes Classifier is one of the simple and most effective Classification algorithms which helps in building the fast machine learning models that can make quick predictions. It is a probabilistic classifier, which means it predicts on the basis of the probability of an object.Some popular examples of Naïve Bayes Algorithm are spam filtration, Sentimental analysis, and classifying articles.

### Linear SVC
The objective of a Linear SVC (Support Vector Classifier) is to fit to the data you provide, returning a "best fit" hyperplane that divides, or categorizes, your data. From there, after getting the hyperplane, you can then feed some features to your classifier to see what the "predicted" class is. This makes this specific algorithm rather suitable for our uses, though you can use this for many situations. Let's get started.

### Random Forests
Random Forest is a popular machine learning algorithm that belongs to the supervised learning technique. It can be used for both Classification and Regression problems.It is based on the concept of ensemble learning, which is a process of combining multiple classifiers to solve a complex problem and to improve the performance of the model.\par As the name suggests, "Random Forest is a classifier that contains a number of decision trees on various subsets of the given dataset and takes the average to improve the predictive accuracy of that dataset." Instead of relying on one decision tree, the random forest takes the prediction from each tree and based on the majority votes of predictions, and it predicts the final output.<br>
> The greater number of trees in the forest leads to higher accuracy and prevents the problem of over fitting.

---

After running the models and testing their classification accuracies we choose the Random Forests Algorothim. Apart from taking advantage of ensemble learning techniques it also helped in preventing over fitting of the data that occurred. 

---

<h3 align="center"> You can always take a look at the github repo in order to contribute to the project </h3>

<p class="text-center">
{% include elements/button.html link="https://github.com/SkaarFacee/Flight-Delay-Predictor" text="Github Repo" %}
</p>