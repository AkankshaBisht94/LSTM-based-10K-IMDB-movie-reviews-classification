PROBLEM DESCRIPTION

This notebook demostrates a sequence classification of IMDB movie reviews dataset by creating a simple LSTM based classifier.

Each movie review is a variable sequence of words, and the tone of each movie review must be classified. The large movie reviews dataset (sometimes referred to as the IMDB dataset) contains 25,000 film reviews (good or bad) for training and 25,000 reviews for testing. The problem is deciding whether a given movie review is positive or negative. The data were collected by researchers at Stanford and used in a 2011 paper that used 50-50 data for training and testing. An accuracy of 88.89% is achieved.

Here, a built-in dataset of IMDB movie reviews is used. Keras provide several built-in dataset, one of them is - imdb.load_data().

Define the LSTM model

The first layer is the Embedded layer that uses 32 length vectors to represent each word. The next layer is the LSTM layer with 100 memory units (smart neurons). Subsequently, you can add more than one LSTM layer. Finally, because this is a classification problem we use a Dense output layer with a single neuron and a sigmoid activation function to make 0 or 1 predictions for the two classes (good and bad) in the problem.

Because it is a binary classification problem, log loss is used as the loss function (binary_crossentropy in Keras). The efficient ADAM optimization algorithm is used. The number of epochs and batch size can be increased as per the requirement. Here, we have taken epoch of 10 and batch size of 64.

Once the model is created, then we can test the performance on unseen reviews.
