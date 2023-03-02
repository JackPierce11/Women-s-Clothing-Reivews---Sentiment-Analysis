# Women's Clothing Reviews - Sentiment Analysis

# Project Goals
The goals of this project are to:
 - **Understand and explore the dataset**, which contains reviews for women's clothing.
 - **Create a Word2Vec language model** based upon the titles and reviews left by customers.
 - Use this pretrained **Word2Vec model and a LSTM neural network** to see how well we can predict whether a customer left a 5-star rating based off of their review.

# Conclusion

## Data Source
https://www.kaggle.com/datasets/nicapotato/womens-ecommerce-clothing-reviews

## Notebooks
 - 01_EDA.ipynb: Exploratory data analysis notebook.
 - 02_Word2Vec.ipynb: Word2Vec model training notebook.
 - 03_LSTM_Sentiment_Analysis.ipynb: LSTM sentiment analysis model training notebook.

## Data
 - data/wcr_original_data.csv: Original data file.
 - data/wcr_partially_cleaned.csv: Cleaned data file created by 01_EDA.ipynb.
 - data/wcr_preprocessed.csv: Preprocessed vectorized data saved by 02_Word2Vec.ipynb.

## Models
 - models/wcr_trigrams_300features_5minwords_20context.bin: Word2Vec model saved by 02_Word2Vec.ipynb.
 - models/LSTM_model_30epochs.h5: LSTM sentiment analysis model saved by 03_LSTM_Sentiment_Analysis.ipynb.
 
## How to Use
 - Run 01_EDA.ipynb to perform exploratory data analysis and generate wcr_partially_cleaned.csv.
 - Run 02_Word2Vec.ipynb to train the Word2Vec model and generate wcr_trigrams_300features_5minwords_20context.bin and wcr_preprocessed.csv.
 - Run 03_LSTM_Sentiment_Analysis.ipynb to train the LSTM sentiment analysis model and generate LSTM_model_30epochs.h5.
 - To use the trained model for predictions, load the saved model from models/LSTM_model_30epochs.h5 and preprocess input data using the saved Word2Vec model and wcr_preprocessed.csv.
