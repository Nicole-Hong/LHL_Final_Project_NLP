[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![NSF-XXXXXXX](https://img.shields.io/badge/NSF-XXXXXXX-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=XXXXXXX) 

# NLP Disaster Classification & Sentiment Analysis

This project is based on the ongoing, knowledge-based Kaggle Competition, ['Natural Language Processing (NLP) with Disaster Tweets'](https://www.kaggle.com/competitions/nlp-getting-started/overview/description), that introduces NLP to data scientists. It is designed to test and learn machine learning algorithms and techniques related to NLP with small datatsets that do not require much personal computing power.

I used this Kaggle competition to develop the base model for the [Emergency Reseponse Management System](https://www.publicsafety.gc.ca/cnt/mrgnc-mngmnt/index-en.aspx) that utilized text classification and sentiment analysis on Twitter API, where text classification predicts and identify which tweets are related to disasters and which tweets are not. Sentiment analysis was used to determine the disaster ratings and disaster classes/sub-classes from the polarity of tweets, sentiment scores, topic modeling for keywords and URL extraction.

Text classification was the main task of the Kaggle Competition, whereas sentiment analysis was implemented in addition to Kaggle, and for that reason, dataset used from Kaggle was not designed for sentiment analysis, which required pre-trained model such as Vader Sentiment Lexicon to be adopted.

## How to use this repository

This repository has the following main directories:

* __data:__ Kaggle train/test data, preprocessed text data, pre-trained model for Transformer Model & other preparatory files for model development
* __figures:__ visualizations generated from EDA and sentiment analysis
* __kaggle_submission_files:__ summary of Kaggle scores / leaderboard status & Kaggle submission files
* __src:__ code for text preprocessing, model development & sentiment analysis
* __images:__ diagrams created for summary of processes and components

### Workflow Overview

For the development the base model, there were two separate procedures for the project workflow as follows:
* __Text classification:__ I followed the general processes for developing NLP using supervised machine learning, deep learning and transformer models
* __Sentiment Analysis:__ subsequent to text classification, the Vader Sentiment Lexicon was downloaded, and using this pre-trained model, sentiment scores on Kaggle train dataset were computed, which were then used for various analysis such as disaster classification / ratings, topic modeling and URL extraction

![Project Workflow](https://github.com/Nicole-Hong/NLP_DisasterClassification_Sentiment_Analysis/blob/main/images/image_workflow.JPG)


### System Requirements

This project has been developed using Python, Jupyter Notebook and Google CoLab, which are run on a Windows system. For Deep Learning and Transformer Models, GPU / TPU in Google CoLab were required.

### Data Requirements

The base model was developed, based on Kaggle datasets - the train dataset of 7,613 tweets with target classes manually labeled, and test dataset of 3,263 tweets without target label for text classification.

Target-labeled, train dataset was imbalanced, and I resampled to make train dataset balanced as follows:

![Train Data-Target Class](https://github.com/Nicole-Hong/NLP_DisasterClassification_Sentiment_Analysis/blob/main/images/image_target_class.JPG)


### Key Outputs

The key outpus for the base model are the predictions made from text classification and sentiment scores that determines the severity of disaster. The model will be further developed to facilitate the action to trigger the effective response for the Emergency Management Cycle.

## Metrics

The project's main metrics were f1 and accuracy scores - KAggle platform computed f1 scores as the main performance evaluation of text classification.

## Future Direction

The base model is not fully developed yet due to the following challenges and issues, and will be an ongoing project for this year:

* The model to be completed requires large size of Twitter data at least 300,000 tweets.
* Capturing semantic context is the key in this NLP model, which requires more sophisticated model development.
* Disaster class / sub-class are determined from keywords, and there is a challenge in coming up with specific keywords through topic modeling. Foe example, general keywords such as 'disaster', 'annihilation' and 'destroyed' results in high negative sentiment score, but these terms are too general for the kind of identification required for the NLP model.
* Tweets with neutral sentiment scores are often linked to severe disaster, which require additional data and information.
* URL extraction is a key part of the model (to be implemented) to deal with neutral tweets, but the model requires a mechanism to filter out URL not significant to disaster.
