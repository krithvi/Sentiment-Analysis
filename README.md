# Sentiment-Analysis

Welcome to the Github repository of "Sentiment Analysis on Movie Reviews" project as completed in June 2022. This was my final year undergraduate project involving the domains of Natural Language Processing and Deep Learning. <br><br>
The project performs sentiment analysis on a large dataset of movie reviews and classifies the given movie review as 'positive' or 'negative' using Deep Learning algorithms namely **Recurrent Neural Networks**, **Long Short-Term Memory** and **Bidirectional Long Short-Term Memory**. The performance of all these algorithms is evaluated and the algorithm which comes out better in terms of accuracy is determined. This could particularly be useful when a person has to determine whether to go to a particular movie or not without having to read all the reviews for that movie. 
<br><br>
[IMDB Dataset from Kaggle](https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) was subject to Exploratory Data Analysis where we discovered that out of 50000 reviews 418 were duplicate rows. After dropping the duplicate rows, the number of positive reviews is 24884 and the number of negative reviews is 24698. Additionally, the dataset was cleaned by removing the special characters, stop words, punctuations and all the letters were made lowercase.
<br><br>
### Accuracy Table
| Model | Epochs | Batch Size | Accuracy|
|-------|--------|------------|---------|
| Single Layered RNN | 60 | 64 | 0.75 |
| Two layered RNN | 60 | 64 | 0.75 |
| Long Short-Term Memory | 50 | 64 | 0.87 |
| Bidirectional Long Short-Term Memory | 25 | 64 | 0.87 |
<br><br>
Thus, a hybrid model with LSTM is found to be comparable to a single layer of BiLSTM as accuracies obtained are more than 85% for both of these models. Therefore, a sentiment classifier user interface can be implemented around either of the models.
