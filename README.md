# Starbucks Capstone Challenge

A Udactiy starbuk capstone Project
## Installation
Must runing with Python 3+ with libraries of numpy, pandas, json, seaborn, matplotlib and sklearn.

Github repo link: https://github.com/anandtopu/udacity_starbucks_project/

## Porject Motiviation
The motivation is trying to achieve the goal to help Starbucks, while practising my own data scientist skills. The goal of this project is to help Starbucks have a better understanding of the relationship between the promotion offers and its customers by the following two questions:

**1. Understand which demographic group or kind of members choose the rewards or offers?**

**2. What is the best offer to send to a distinct user?**

**3. How much will a user spend on the offer?**

**4. Exactly how users are accepting the offers?**

## File Descriptions
The data is contained in three files:

- portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
- profile.json - demographic data for each customer
- transcript.json - records for transactions, offers received, offers viewed, and offers completed
- Here is the schema and explanation of each variable in the files:

**portfolio.json**


- id (string) - offer id
- offer_type (string) - type of offer ie BOGO, discount, informational
- difficulty (int) - minimum required spend to complete an offer
- reward (int) - reward given for completing an offer
- duration (int) - time for offer to be open, in days
- channels (list of strings)

**profile.json**

- age (int) - age of the customer
- became_member_on (int) - date when customer created an app account
- gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
- id (str) - customer id
- income (float) - customer's income

**transcript.json**

- event (str) - record description (ie transaction, offer received, offer viewed, etc.)
- person (str) - customer id
- time (int) - time in hours since start of test. The data begins at time t=0
- value - (dict of strings) - either an offer id or transaction amount depending on the record

## Machine Learning Modelling
Two Random Forest models were built for offer viewed and offer completed.

**Algorithms:** The algorithms behind the random forest is a combination of decision trees. In the ‘forest’, each decision tree depends on the values of a random vector sampled independently with the same distribution for all trees. 

**Model Improvement by Hyper Parameter with Cross-validation:** By implement grid search, two models were able to be optimized with the best hyper parameters. 

**Metrics:**  The Metrics used to measure the model performance is the coefficient of determination R^2.  As well as the classification report for each model. 

## Results


**Medium Blog for data science perfessonals is [here](https://medium.com/@anand.goud.2020/starbucks-capstone-challenge-15146c60d3da?sk=30c55d216a1af071b4f06afc17c0932e).**

This project is mainly research on the customers who viewed and completed offers. The future improvement could be research on the customers who did not react to those offers and find why.
