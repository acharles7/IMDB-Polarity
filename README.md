# Sentiment-Analysis
Sentiment Analysis on IMDB Dataset using three different models 
<h3>Data Preprocessing</h3>

We have gathered 25000 IMDB reviews for training and 25000 reviews for testing from keras.
In which, almost half of the reviews are positive and half of the reviews are negative.
We have considered 10,000 words for our dictionary.
For preprocessing, we have truncated all the reviews to first 256 words and if the reviews are of less than 256 words, then we have padded them with 0.
For names of characters used in the reviews, we assigned them to UNKNOWN words.
The words after 10,000 are considered as UNUSED
