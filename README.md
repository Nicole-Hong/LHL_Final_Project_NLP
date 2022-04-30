[![lifecycle](https://img.shields.io/badge/lifecycle-experimental-orange.svg)](https://www.tidyverse.org/lifecycle/#experimental)
[![NSF-XXXXXXX](https://img.shields.io/badge/NSF-XXXXXXX-blue.svg)](https://nsf.gov/awardsearch/showAward?AWD_ID=XXXXXXX) 

# NLP Disaster Classification & Sentiment Analysis

This project is based on the ongoing, knowledge-based Kaggle Competition, ['Natural Language Processing (NLP) with Disaster Tweets'](https://www.kaggle.com/competitions/nlp-getting-started/overview/description), that introduces NLP to data scientists. It is designed to test and learn machine learning algorithms and techniques related to NLP with small datatsets that do not require much personal computing power.

I used this Kaggle competition to develop the base model for the [Emergency Reseponse Management System](https://www.publicsafety.gc.ca/cnt/mrgnc-mngmnt/index-en.aspx) that utilized text classification and sentiment analysis on Twitter API, where text classification predicts and identify which tweets are related to disasters and which tweets are not. Sentiment analysis was used to determine the disaster ratings and disaster classes/sub-classes from the polarity of tweets'sentiment scores, topic modeling for keywords and url extraction.

Text classification was the main task of the Kaggle Competition, whereas sentiment analysis was implemented in addition to Kaggle, and for that reason, dataset used from Kaggle was not designed for sentiment analysis, which required pre-trained model such as Vader Sentiment Lexicon to be adopted.

The base model is not fully developed yet due to the following challenges and issues, and will be ongoing project for this year:
* the model requires large size of Twitter data at least 300,000 tweets. This base model was designed based on the train dataset of 7,613 tweets with target classes manually labeled, and test dataset of 3,263 tweets without target label for text classification
* Capturing semantic context is the key in this NLP model, which requires more sophisticated model development
* Disaster class / sub-class are determined from keywords, and there is challenge in coming up with specific keywords through topic modeling. Foe example, general keywords such as 'disaster', 'annihilation' and 'destroyed' results in high negative sentiment score, but these terms are too general for the kind of identification required for the NLP model
* Tweets with neutral sentiment scores are often linked to severe disaster, which require additional data and information
* URL extraction is a key part of the model (to be implemented) to deal with neutral tweets, but the model requires a mechanism to filter out URL not significant to disaster

## How to use this repository

A description of the files and directory structure in the repository.

### Workflow Overview

Th project uses X core information, manages it and passes our some stuff.

![Project Workflow](https://github.com/Nicole-Hong/NLP_DisasterClassification_Sentiment_Analysis/blob/main/images/image_workflow.JPG)


### System Requirements

This project is developed using Python, Jupyter Notebook and Google CoLab.  It runs on a Windows system (?).  Continuous integration uses TravisCI (?).

### Data Requirements

The project pulls data from (?).
![Train Data-Target Class](https://github.com/Nicole-Hong/NLP_DisasterClassification_Sentiment_Analysis/blob/main/images/image_target_class.JPG)


### Key Outputs

This project generates (an API, some log files, what?)

## Metrics

This project is to be evaluated using the following metrics. . .
