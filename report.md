https://docs.google.com/document/d/1hF7MfkBTu_OjHLlYseknUKi8LkTcQAFLgiQfjuPxw-4/edit?usp=sharing

# Abstract

This project is concerned with the task of analysing Tweets to detect instances that indicate a disaster (e.g. wildfire, car crash, etc.) being reported. To achieve this we applied Machine Learning Methods. In particulare XXX and a Sequential Neural Network. The best result was achieved by XXX leading to a F1-score on the validation set of XXX.

# The Problem
Due to its speed and accessibility social media, Twitter in our case, is used by users to announce emergencies in real-time. This can be a valuable resource for actors that need to respond to these emergencies (e.g. firefighters). In order to do so these Tweets need to be detected. Creating an algorithm that reliably distinguishes those kind of tweets from others is the task adressed within this project.

The task is taken from [kaggle.com](https://www.kaggle.com/c/nlp-getting-started/overview/description) and the results produced here were also submitted to their competition.

# The Data
The data consists of 7613 Tweets which have 5 features each: id, keyword, location, text and target. Those are a unique identifier, a keyword that is connected to the content of the tweet, location of the tweet (though important to notice that this is not generated via GPS, but a free format filled by the users themself), the tweeted text and the label if it is a disaster tweet or not. 3271 of those Tweets are instances of our target class. About 33% of both groups (target and non-target Tweets) are missing a location, of keywords there are only missing a few (61 in total).

In order to train our classifier we will mainly focus on the text of the Tweets, but both keyword and location could both deliver useful further information and will be added in an additional step.

# Cleaning and Tokenization
To make the text of the Tweets useable for our algorithms we first selected the tweet text column of the input data. Following this, we used a TweetTokenizer from the _ library in order to lowercase all parts of the tweet and strip away any twitter handles.
In a next step, the tweets were scanned for unwanted tokens, such as stopwords and punctuation, comparing each token with words from nltk's package english_stopwords and string's 'punctuation'. Furthermore, all '#' signs were stripped from the keywords keeping the tagged words.
The last part of preprocessing was to use a TF-IDF Vectorizer in order to have a sparse matrix with each token of the tweet as a separate feature in the models we later test.

XXX

We use the term-frequency times inverse document-frequency (tf-idf)...

# Modelling
To achieve the classification of the Tweets we used two different approaches: First we used different XXX Classifiers provided by scikit learn, second we trained a neural network (tensorflow and keras).

## Classifiers

## Neural Network




# Evaluation
# Summary
# Appendix
- plots
- git repository
