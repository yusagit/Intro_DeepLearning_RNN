# Disaster Tweets Classification

This repository contains the implementation of a Natural Language Processing (NLP) model for classifying disaster-related tweets. The project is based on the Kaggle competition: [Natural Language Processing with Disaster Tweets](https://www.kaggle.com/c/nlp-getting-started).

## Overview
The goal of this project is to build a machine learning model that can distinguish between real disaster tweets and non-disaster tweets. This is useful for disaster response teams to efficiently filter and respond to critical information on social media.

## Dataset
The dataset consists of tweets labeled as either containing a real disaster (1) or not (0). The training dataset contains 7,613 tweets, while the test dataset consists of 3,263 tweets. The data includes:
- `id`: Unique identifier for each tweet
- `text`: The tweet content
- `keyword`: Disaster-related keywords (if present)
- `location`: Tweet location (if available)
- `target`: Label (1 = disaster-related, 0 = not disaster-related)

## Approach
The project follows these steps:
1. **Data Preprocessing**
   - Text cleaning (removing punctuation, URLs, stopwords, and special characters)
   - Tokenization and word embedding (pre-trained embeddings such as GloVe)
   - Handling missing values in `keyword` and `location`

2. **Feature Engineering**
   - Using word embeddings to convert text into numerical format

3. **Model Selection**
   - Deep learning models (RNN, LSTM, GRU, Bidirectional LSTM)
   - Evaluation using accuracy, precision, recall, and F1-score

4. **Evaluation and Results**
   - Comparing model performance based on validation metrics
   - Generating predictions for test data

## Results
- The best-performing model was Bidirectional LSTM with an accuracy of **78%**.
- Future improvements include experimenting with transformer-based models like BERT and improving feature engineering techniques.

## Contributing
Feel free to fork this repository, make improvements, and submit a pull request. Contributions are always welcome!

## License
This project is released under the MIT License.
