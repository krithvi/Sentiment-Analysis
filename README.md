# Sentiment-Analysis

Welcome to the Github repository of "Sentiment Analysis on Movie Reviews" project as completed in June 2022. This was my final year undergraduate project involving the domains of Natural Language Processing and Deep Learning. <br><br>
The project performs sentiment analysis on a large dataset of movie reviews and classifies the given movie review as 'positive' or 'negative' using Deep Learning algorithms namely **Recurrent Neural Networks**, **Long Short-Term Memory** and **Bidirectional Long Short-Term Memory**. The performance of all these algorithms is evaluated and the algorithm which comes out better in terms of accuracy is determined. This could particularly be useful when a person has to determine whether to go to a particular movie or not without having to read all the reviews for that movie. 
<br><br>
[IMDB Dataset from Kaggle](https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) was subject to Exploratory Data Analysis where we discovered that out of 50000 reviews 418 were duplicate rows. After dropping the duplicate rows, the number of positive reviews is 24884 and the number of negative reviews is 24698. Additionally, the dataset was cleaned by removing the special characters, stop words, punctuations and all the letters were made lowercase.
<br><br>
After preprocessing, vectorization is done, where the document gets transformed into vector representations. Since the machine cannot understand natural languages, we convert the reviews to a machine-readable format. The word embeddings of each word in the review is derived using Word2Vec with the help of an N-grams model. 
<br><br>
Each algorithm is then used to build each model which will be trained and tested to get the repective Confusion Matrix and Classification Report.
### Accuracy Table
| Model | Epochs | Batch Size | Accuracy|
|-------|--------|------------|---------|
| Single Layered RNN | 60 | 64 | 0.75 |
| Two layered RNN | 60 | 64 | 0.75 |
| Long Short-Term Memory | 50 | 64 | 0.87 |
| Bidirectional Long Short-Term Memory | 25 | 64 | 0.87 |

<br>
Thus, a hybrid model with LSTM is found to be comparable to a single layer of BiLSTM as accuracies obtained are more than 85% for both of these models. Therefore, a sentiment classifier user interface can be implemented around either of the models.

### Using a sentiment classifier to show Demo
In addition to the test input from the dataset, user input of a review of some movie is given to the trained model to see how it performs. For this, the model with the best accuracy is selected to implement a user interface. Such a user interface works with the help of a wrapper function. This function takes a review text string as input and returns the sentiment - "Positive" or "Negative", and the score. Inside the function, the review text undergoes the same preprocessing methods used on the dataset but for one value. After the preprocessing, the text is transformed into vectors so that it can be compared with the keyed vectors.
