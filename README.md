# Deep Learning Challenge

# Table of Contents

- [Overview](#overview)
  - [Purpose of the Analysis](#purpose-of-the-analysis)
  - [Results](#results)
    - [Data Preprocessing](#data-preprocessing)
    - [Compiling, Training, and Evaluating the Model](#compiling-training-and-evaluating-the-model)
  - [Overall Results](#overall-results)
  - [Recommendation](#recommendation)

## Overview

## Purpose of the Analysis:

The purpose of this analysis is to create a machine learning model that can predict whether a charitable organization will be successful based on various features provided in the dataset. This analysis involves preprocessing the data, including handling categorical variables, scaling the features, and then training and evaluating a deep learning model (a neural network) to make these predictions. The goal is to develop a predictive model that can help identify which charitable organizations are likely to be successful, which can be valuable for optimizing fundraising efforts and resource allocation.

## Results:

**Data Preprocessing**

Target Variable(s):
- The target variable for the model in this analysis is 'IS_SUCCESSFUL'. This variable represents whether a charity organization's application for funding was successful (1) or not (0).

Feature Variables:
- The feature variables for the model include all the remaining columns in the dataset except for 'IS_SUCCESSFUL', as it is the target variable. These features includes data such as the organization's application type, affiliation, classification, use case, organization type, status, income amount, special considerations, and ask amount.

Variables to Remove:
- The variables 'EIN' and 'NAME' were removed from the input data during preprocessing because they are neither target nor feature variables. These columns represent identification information for each organization and do not provide relevant predictive information for the target variable.

## Compiling, Training, and Evaluating the Model

**Model 1 Parameters**

![image](https://github.com/rkb81/deep-learning-challenge/blob/main/model1_parameters.png)

- The first hidden layer used ReLU because of its simplicity as a mathematical function. Next, the second hidden layer and output layer used sigmoid because of its effective performance of binary classification tasks.

**Model 1 Evaluation**

![image](https://github.com/rkb81/deep-learning-challenge/blob/main/model1_evaluation.png)

**Target model performance**

The target model performance is 75%. The model accuracy is approximately 72%, which falls short to the target model performance.

**Increasing model performance**

In subsequent model generation, several methods were attempted to enhance performance. The neuron count, layers and epochs were all increased in an attempt to reach the target model performance. Also, the activation function was changed to the tanh function. Increasing model complexity only improved model accuracy an additional 1%.

## Overall Results:

Initial Model Accuracy: 72%
After Increasing Complexity: 73%
Final Model: 73%

## Recommendation:

Because the added complexity to the model only marginally improved accuracy, it would be recommended to drop more columns, change the number of values for each bin and create additional bins for anomalies in the columns. Additionally, the number of neurons, layers and epochs can be lowered in order to improve accuracy.
