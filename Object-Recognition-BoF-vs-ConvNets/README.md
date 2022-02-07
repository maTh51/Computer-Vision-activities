# Object-Recognition: BoF vs ConvNets

The goal of this quiz is to implement two object recognition approaches:

1. A classifier based on bag of features:
    * Try different sizes for the dictionary.
    * Use Random Forest as classifier.
    * To train a Neural Network using BoF as feature vectors for images.

2. A classifier using ConvNet implemented in Keras:
    * Use an architecture inspired in the LeNet5
    * To train a Random Forest using feature vectors extracted from a layer of your ConvNet.

Your code must be implemented on a notebook python and you must use the CIFAR-10
(https://www.cs.toronto.edu/~kriz/cifar.html) for training and testin.