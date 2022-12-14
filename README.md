# duplicate-questions-pair-detection
 BT4222 Project
## Dataset
The dataset used in this project is available publicly on Kaggle website, provided by Quora. It consists of 404352 question pairs with 6 fields; unique identifier of the question pair, unique identifier of the first question, unique identifier of the second question, full text of first question, full text of second question, and the duplicate label. The data can be found here: [Kaggle Quora Competition Website](https://www.kaggle.com/c/quora-question-pairs/data).

## Data Preparation
1. Data Validation
2. Feature Engineering
3. Feature Encoding
4. Data Pre-processing
5. Feature Selection

For Pre-processing, we mixed around alot of different techniques. After the common pre-processing steps like removing stop words, lemmatization, etc, we used bag-of-words for topic modeling and word2vec to build our embedding layer. Other pre-processing steps include feature scaling numerical features and one-hot-encoding the topics generated.

Here are some example features:
- NLP Features
  - Latent Dirichlet Allocation, Topic Modeling
  - Common Ratio
  - Frequency
  - Doc2vec
  - Word2vec
  - Similary measures (Jaccard)
  - Sentiment
  - Fuzzy
- Distance Features
  - Canberra
  - Euclidean
  - Cosine

## Models
1. Logistic Regression
2. Random Forest
3. LightGBM
4. XGBoost
5. BERT
6. MLP
7. Siamese BiLSTM
8. Stacking

We also tried Manhantann Siamese LSTM and Support Vector Machine but these were discarded due to poor performance or long training times.

## Overview of Stacking Architecture
<img src="reports/figures/stacking arch.jpg">

## Other tasks performed
1. Web Scraping

We scraped a random sample of questions from stackoverflow (since web crawling is against Quora rules) to test how our model will perform in production.


## Results
<img src="reports/figures/standalone models.jpg">
