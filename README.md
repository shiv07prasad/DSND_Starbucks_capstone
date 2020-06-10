# Udacity Data scientist nano degree capstone project 

**Blog post :** [Starbucks capstone project](https://medium.com/@shiv07prasad/starbucks-capstone-project-c36c1ca2db87)

This repository contains all the files submitted for the capstone project.

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [Data](#data)
4. [Results](#result)
5. [Conclusion](#conclusion)
6. [Licensing, Authors, Acknowledgements, etc.](#lic)

## Installation <a name="installation"></a>

There should be no necessary libraries to run the code here beyond the Anaconda distribution of Python. The code should run with no issues using Python versions 3.*.

## Project Motivation <a name="motivation"></a>

In order to complete the Udacity Data Science course, I analyzed Starbucks customer's behavior in response to offers, and built a model that predicts whether a customer will complete an offer.

## Data<a name="data"></a><a name="data"></a>

The data is contained in three files:

i) portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* id (string) - offer id
* offer_type (string) - type of offer ie BOGO, discount, informational
* difficulty (int) - minimum required spend to complete an offer
* reward (int) - reward given for completing an offer
* duration (int) - time for offer to be open, in days
* channels (list of strings)

ii) profile.json - demographic data for each customer
* age (int) - age of the customer
* became_member_on (int) - date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

iii) transcript.json - records for transactions, offers received, offers viewed, and offers completed
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record

## Results<a name="result"></a>

Naive predictor accuracy: 0.473
Naive predictor f1-score: 0.642

LogisticRegression model accuracy: 0.699
LogisticRegression model f1-score: 0.696

RandomForestClassifier model accuracy: 0.848
RandomForestClassifier model f1-score: 0.840

## Conclusion<a name="conclusion"></a> 

The goal was to predict whether a customer would use an offer. The problem was approached by cleaning and combining the profile, portfolio and transcript datasets. Then it was followed by constructing a naive model which assumed that all the offers were successful. The accuracy and the f1 score of the model were obtained. It was followed by comparing the performance of logistic regression and random forest models. The random forest model had best accuracy and f1 score of 0.848 & 0.840 respectively. The test data accuracy of 0.735 and f1 score of 0.717 shows that the random forest model that was constructed did not overfit the training data.

## Licensing, Authors, Acknowledgements, etc.<a name="lic"></a>

Data for working with the project was provided by Udacity in association with Starbucks.
