# Scikit-learn: Creating Machine Learning Models

- Scikit-learn is the standard machine learning library to use

## Introduction

- Often called sklearn
- Is a Python machine learning library
- Helps us build machine learning models from our data
- Helps find patterns in our data and from there make predictions
- Implements tools to evaluate those predictions
- Is built on NumPy and Matplotlib
- Has many built in machine learning models
- Has methods to evaluate our machine leaning models
- Scikit-Learn workflow:
  ![Scikit-learn workflow](scikit-learn-workflow.png)

1. Get data ready
2. Pick a model to suit your problem
3. Fit the model to our data ( or find patterns in our data) and make a prediction
4. Evaluate the model. Are our discovered predictions worth holding onto?
5. Improve throuh experimentation. Maybe they weren't useful predictions.
6. Save and reload your trained model. This would allow us to put it into and application or share it.

## What is Machine Learning

- With machine learning we can teach a computer what something is.
- Where in programming we take input and write a function to give us an output, ML does the opposite.
- Machine Learning takes the input and output and figures out the function or coding in between needed to get that result.
- EG: A input is 1000 images of animals and a corresponding B output of 1000 boolean results of whether the image is a snake or not. Then ML goes and figures out the mapping of A to B. It creates the function. It creates the 'model'. It finds the patterns that that make image 1 > True (is a snake) and image 2 > False (is not a snake). ML can then use those patterns to determine whether an image is a snake in another program.
- This machine leaning model can also be called an algorithm.
- To train this model we need to give it lots of data
- Machine Learning is a computer creating it's own model, it's own function, it's own code, based on the inputs and outputs

## Data Science - Clean, Transform, Reduce

- To make our data more useful we want to take these steps:
  - Clean Data > Transform Data -> Reduce Data.
- Clean Data:
  - Remove and replace data. Eliminate missing values
  - Remove a row if it has missing value is one option
  - Or we could calculate average values for the missing fields
  - Remove outliers in our data
- Transform Data:
  - Computers don't understand concepts
  - So a computer can understand our data we need to convert it to something it understands
  - We need to convert everything to numbers, Even things like colors need to be come a number
- Reduce Data:
  - The more data we need to compute the more cpu power / energy / cost needed to run computations
  - If we can get the same result on less data and time then it will save us money and time
  - Sometimes called Dimensionality Reduction or Column Reduction
  - The more columns you have the slower computation will be. Maybe there are some irrelevant columns that can be removed.

## Feature Scaling

- A machine learning algorithm may have trouble finding patterns when the scale of numebers varies greatly. For example, 'previous repair costs', might have a range of 100 - 1700, 'odometer' a range of 6000 to 345000.
- We can make it easier for the machine learning algorithm using feature scaling
- Two types of Feature Scaling:
  - Normalization (also called min-max scaling)
    - Rescales all numerical values to between 0 and 1
    - Can be done with SciKit-Learn through the MinMaxScalar class
  - Standardization
    - This subtracts the mean value from all of the features.
    - It then scales the features to unit variance (by dividing the feature by the standard deviation.)
    - Scikit-Learn provides functionality for this in the StandardScalar class
- Feature Scaling usually isn't required for your target variable
- Feature Scaling isn't usually required for tree based models, EG RandomForest, since they can handle varying features.

## Choosing the right model for your data

- Sklearn refers to machine learnng models, algorithms as estimators
- Within those estimators are classifiers and regressors
- Classification problem:
  - Predicting a category or multiple categories
  - One thing or the other EG Heart Disease or Not
  - Needs a classification estimator
- Regression problem:
  - Predicting a number. EG Selling price
- Refer to the [sklearn machine learning map](https://scikit-learn.org/stable/machine_learning_map.html) to choose an esitmator/model.



