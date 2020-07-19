# Titanic-Prediction
In this challenge, we are asked to predict whether a passenger on the titanic would have been survived or not.
## Dataset Overview
The data has been split into two groups: training set (train.csv) test set (test.csv)

The training set should be used to build our machine learning models. Our model will be based on “features” like passengers’ gender and class. we can also use feature engineering to create new features.

The test set should be used to see how well our model performs on unseen data.
## Data Dictionary
Survived: 0 = No, 1 = Yes

Pclass: A proxy for socio-economic status (SES): 1st = Upper, 2nd = Middle, 3rd = Lower

Age: Age is fractional. If less than 1. If the age is estimated, is it in the form of xx.5

SibSp: The dataset defines family relations in this way: Sibling = brother, sister, stepbrother, stepsister; Spouse = husband, wife (mistresses and fiancés were ignored)

Parch: The dataset defines family relations in this way: Parent = mother, father; Child = daughter, son, stepdaughter, stepson; Some children travelled only with a nanny, therefore parch=0 for them.
## Preprocessing Data
First of all, that we need to convert a lot of features into numeric ones later on, so that the machine learning algorithms can process them. Furthermore, the features have widely different ranges, that we will need to convert into roughly the same scale. We can also spot some more features, that contain missing values (NaN = not a number), that wee need to deal with.

First, I will drop "PassengerId","Name","Ticket","Cabin" from the train set, because it does not contribute to a persons survival probability. Then filling missing data with median because missing values effect the prediction and then transform Embarked and Sex columns to numerical values, because machine learning models work with number better.
## Building Machine Learning Models
Now we will train Machine Learning model and Predict the data. Note that because the dataset does not provide labels for their testing-set, we need to use the predictions on the training set to check the accurcy of algorithm. 

We used Random Forest Classifier and predict the values by it and get accuracy of 76%. The mean absolute error is 0.24

This code is prepared Using Jupyter Notebook.
