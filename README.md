# Sentiment-Analysis
Sentiment Analysis on IMDB Dataset using three different models 
<h3>Data Preprocessing</h3>

We have gathered 25000 IMDB reviews for training and 25000 reviews for testing from keras.
In which, almost half of the reviews are positive and half of the reviews are negative.
We have considered 10,000 words for our dictionary.
For preprocessing, we have truncated all the reviews to first 256 words and if the reviews are of less than 256 words, then we have padded them with 0.
For names of characters used in the reviews, we assigned them to UNKNOWN words.
The words after 10,000 are considered as UNUSED.

<h2>Neural Network Model</h2>
<h3>Model 1</h3>
Input Layer: Embedding layer<br>
Global MaxPooling1D layer<br>
Hidden Dense Layer with 16 Neurons<br>
Activation function: Softmax
Output Dense layer with 1 Neuron <br>
Activation function: Sigmoid

<h4>Optimizer Used</h4>
At the beginning, we used Stochastic Gradient Decent.
But, after Adam Optimizer we got more accurate result.
<b>We have used Binary Cross Entropy as a loss function.</b>
After 20 epochs, the model started to overfit. So, we trained our model for 20 epochs.
Batch size = 512.

<h3>Model 2 (CNN)</h3>
Input Layer: Embedding layer<br> 
Dropout
Convolution Layer<br>
Activation: Relu, Stride: 1
Global MaxPooling1D Layer<br>
Hidden Dense Layer with 250 Neurons
Dropout
Activation function: tanh
Output layer with 1 Neuron<br>
Activation function: Sigmoid

<h4>Optimizer Used</h4>
At the beginning, we used Stochastic Gradient Decent.
But, after Adam Optimizer we got more accurate result.
<b>We have used Binary Cross Entropy as a loss function.</b>
After 4 epochs, the model started to overfit. So, we trained our model for 4 epochs only .
Batch size = 64.
