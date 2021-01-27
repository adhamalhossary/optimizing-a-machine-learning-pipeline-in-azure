# Optimizing an ML Pipeline in Azure

## Overview
This project is part of the Udacity Azure ML Nanodegree.
In this project, we build and optimize an Azure ML pipeline using the Python SDK and a provided Scikit-learn model.
This model is then compared to an Azure AutoML run.

## Summary
This project uses data from direct marketing campaigns of a Portuguese banking institution. The marketing campaigns are based on phone calls. It contains 20 features such as age, job and martial status. The target column contain only two categories, Yes and No, to determine if the client subscribed to the bank's term deposit. 

The aim of the algorithms built using the Python SDK (w/ Hyperdrive) and AutoML is to accurately predict if a potential client will subscribe to the bank's term deposit or not. This is to assist them in targeting thier resources in approaching clients that are more likely to subscribe.

The best performing model was found using the AutoML run and was a Voting Ensemble with an accuracy of 91.78%. However, the Logistic classifier trained using Hyperdrive had an accuracy of 91.44% which is very close to the accuracy of the Voting Ensemble model.

## Scikit-learn and Hyperdrive Pipeline
**Explain the pipeline architecture, including data, hyperparameter tuning, and classification algorithm.**

### Scikit-learn

A Logistic Regression model was first created and trained using Scikit-learn in the train.py. The steps taken in the python script were as follows:

1 - Import the banking dataset using Azure TabularDataset Factory

2 - Data is then cleaned and transformed using a cleaning function

3 - Processed data is then split into a training and testing set

4 - Scikit-learn was used to train an initial Logistic Regression model while specificing the value of two hyper parameters, C and max_iter. C represents the inverse of the regularization strength, while max_iter represents the maximum number of interations taken for the model to converge. These two parameters were initially passed in the python script so they can be optimised later on using Hyperdrive.

5 - The trained model is then saved


### Hyper Drive


**What are the benefits of the parameter sampler you chose?**

**What are the benefits of the early stopping policy you chose?**

## AutoML
**In 1-2 sentences, describe the model and hyperparameters generated by AutoML.**

## Pipeline comparison
**Compare the two models and their performance. What are the differences in accuracy? In architecture? If there was a difference, why do you think there was one?**

## Future work
**What are some areas of improvement for future experiments? Why might these improvements help the model?**
