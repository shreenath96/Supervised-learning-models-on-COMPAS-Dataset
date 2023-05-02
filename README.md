# Supervised-learning-models-on-COMPAS-Dataset
# Project Description

This project involves building a machine learning model to predict whether a defendant in a criminal case will recidivate within the next two years, based on the ProPublica COMPAS dataset. The project also includes evaluating the fairness of the model, especially in the context of bail or parole decisions. 

## Dataset

The ProPublica COMPAS dataset is available [here](https://github.com/shreenath96/Supervised-learning-models-on-COMPAS-Dataset/blob/main/recid.csv). I split the dataset into training and test sets, keeping 1/3 of the data for testing.

## Model Selection

I followed the usual steps for model selection, including feature selection and engineering, as well as choosing the model type and hyperparameters. The performance of the model was evaluated based on accuracy, and F-1 score.

## Fairness Evaluation

To evaluate fairness, I compared the false positive rates based on two metrics: opportunity cost and calibration. I computed the probabilities of an individual being predicted positive by the algorithm, given that they are categorized as African-American or Caucasian by the race variable, and did not actually recidivate. I then compared the results and reported the numerators and denominators for each calculation.

Based on the fairness evaluation, I wrote about potential biases towards African-American or Caucasian groups, and the potential societal implications of using such an algorithm.

## Protected Features

I also considered the role of the "race" variable as a protected feature, which means that discrimination based on these features is not allowed. I explored how the results changed when explicitly removing the feature from the model.

## Fair Classifier

Finally, I experimented with a fair classifier designed to achieve demographic parity or equal opportunity. I observed the tradeoff between accuracy/F-measure and the fairness objective.

Please refer to the code and documentation in this repository for more details about the project.
