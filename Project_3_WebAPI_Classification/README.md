# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) Project 3: Web APIs & Classification

##### by: Lin Junyuan, SG-DSI-14

## Introduction
The objective is to build a classification model to distinguish posts between two subreddits.

## Problem Statement

What is the **best classification model** that is able to identify whether a post belongs to the r/science subreddit or the r/nature subreddit with **at least 80% accuracy** and what are the **top 5 features**?

## Executive Summary

The objective of this project is to create the best classification model to identify Reddit posts, with the goals as stated in the problem statement. For this project, the data has to be gathered manually using Reddit API.

For the training data set, a total of 625 posts were gathered from the r/science subreddit and 550 posts from the r/nature subreddit. As usable language data can both be found in the post title and post content, they were merged to create new variable. For the purpose of this project, models comprising of combinations of the following are considered:

```
- Pre-processing: 1) Lemmatization       2) PorterStemmer
- Transformer:    1) Count Vectorizer    2) TF-IDF Vectorizer
- Model:          1) Logistic Regression 2) Naive Bayes MultinomialNB
```

After assessing the various models, the model comprising of Lemmatization -> TF-IDF Vectorizer -> Naive Bayes MultinomialNB is found to be the most suitable model which fits our objectives. The top 5 features are 1) study 2) covid 3) new 4) researcher 5) people. After testing the selected model on data that were extracted separately, the model is still able to perform up to targeted levels.

 ## Conclusions and Recommendations

Through this exercise, we have determined that the best classification model that is able to achieve 80% accuracy is the Lemmatization -> TF-IDF Vectorizer -> Naive Bayes MultinomialNB model.

The top 5 features are 1) study 2) covid 3) new 4) researcher 5) people.

However, in view of the fact that one of the top features is `covid`, it is apparent that the model is picking up certain time-sensitive terms. These terms are likely to be irrelevant over time. Therefore, to stabilise the performance of the model, it is reccommended to build up the training data over a period of time and reinforce the model.

Secondly, the models have a high tendency to overfit the train data from the train_test_split. Though we have selected the model with the least drop in score when testing it on test data, the drop is still rather significant. Therefore, when searching through parameters for the best model using GridSearch, it might be preferable to search for the best model using the least drop in score, rather than the current highest score.

## File Navigation
```
Project_3_WebAPI_Classification
|__ datasets
|   |__ train.csv
|   |__ test.csv
|__ Web_API_Classification_notebook.ipynb
|__ WebAPI_Classification_slides.pdf
|__ README.md
```
