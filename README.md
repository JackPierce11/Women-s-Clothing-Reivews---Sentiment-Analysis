# Women's Clothing Reviews - Sentiment Analysis

# Project Goals
The goals of this project are to:
 - **Understand and explore the dataset**, which contains reviews for women's clothing.
 - **Create a Word2Vec language model** based upon the titles and reviews left by customers.
 - Use this pretrained **Word2Vec model and a LSTM neural network** to see how well we can predict whether a customer left a 5-star rating based off of their review.

# Conclusion

3 models were made with varying complexities, but all containing some form of LSTM layer. It was found that **Model 2 has the highest accuracy score of 0.702**. Here is a table to show the results:

<img width="400" alt="image" src="https://user-images.githubusercontent.com/73466733/223437077-ddde4981-f2d0-441c-a90b-9b0365b3b680.png">

**Evaluation of Results:**  A customer rating of less than 5-stars did not always indicate customer dissatisfaction. The model had significant false positives. Though the dataset was balanced, it did not match the sentiment split of the dataset. The company should focus on understanding why customers leave a positive text review but not give a 5-star rating to improve customer experience.

For the full conclusion, see notebook: 03_LSTM_Sentiment_Analysis.ipynb

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
 - models/model_1.h5: model 1 LSTM sentiment analysis model saved by 03_LSTM_Sentiment_Analysis.ipynb.
 - models/model_2.h5: model 2 LSTM sentiment analysis model saved by 03_LSTM_Sentiment_Analysis.ipynb.
 - models/model_3.h5: model 3 LSTM sentiment analysis model saved by 03_LSTM_Sentiment_Analysis.ipynb.
 
 
## How to Use
 - Run 01_EDA.ipynb to perform exploratory data analysis and generate wcr_partially_cleaned.csv.
 - Run 02_Word2Vec.ipynb to train the Word2Vec model and generate wcr_trigrams_300features_5minwords_20context.bin and wcr_preprocessed.csv.
 - Run 03_LSTM_Sentiment_Analysis.ipynb to train the LSTM sentiment analysis model and generate the three models: model_1.h5, model_2.h5, model_3.h5.
 - To use the trained models for predictions, load the saved models from models/model_1.h5, models/model_2.h5 and models/model_3.h5 and preprocess input data using the saved Word2Vec model and wcr_preprocessed.csv.
