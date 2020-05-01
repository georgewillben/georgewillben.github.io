---
layout: post
title:      "Recursive Feature Elimination In Python With Sklearn"
date:       2020-05-01 17:00:40 +0000
permalink:  recursive_feature_elimination_in_python_with_sklearn
---

## Introduction
Feature selection can sometimes be a difficult process. Recursive Feature Elimination (RFE) is a brute force approach to feature selection. The RFE method from sklearn can be used on any estimator with a .fit method that once fitted will produce a coef_ or feature_importances_ attribute.¹ It works by removing the feature with the least importance from the data and then reevaluates the feature importance, repeating the process until it is told to stop. First thing’s first import the RFE method from sklearn.

## Parameters
There are 3 main parameters to sklearn’s RFE method.
estimator — a machine learning model with a .fit method
n_features_to_select — the number of features that will be kept
steps — how many features are dropped every time RFE reduces features

## How to use RFE
The best approach to RFE is to use it with any number of features. Let’s say you have a data set with 5 features. Try RFE’s with n_features_to select ranging from 1 to 5 and see what the metrics of success turn out to be for each RFE. Then use take the best RFE and retrieve the features it used using RFE’s .support_ attribute which is a list of boolean values that are false if the feature was dropped.
