# Neural Networks

## Overview
Deep learning is about neural networks

There is an interconnected web of nodes called **neurons**.
and the **edges** that join them together.

NNs main functions get an input, process complex sets of calculations and provide an output.

This chapter focuses on classification.

Recommended resources:

* Mark Neilson's book
* Andrew Ng ML Class

## Classification

Categorising a group of objects by only using some basic data features that describe them. Examples:

* Logistic regression
* SVMs
* Naive Bayes

The firing of a classifier, or **activation**, produces a score.

### Example
If you have to say whether a patient is healthy, and all you have is height, weight and body temperature.
The classifier would get the data, process it and provide a score:

* A low score would suggest they are sick
* A high score would suggest they are healthy

## Neural Network Layers
NNs can be used in classification problems when an object can fall in 1 of 2 or more options.

Unlike other networks (like graphs, etc), a NN comes in **layers**.

* **Input layer** - the first layer
* **Output layer** - the last layer
* **Hidden layers** - the layers in the middle

A neural net can be viewed as a result of putting together a set of individual classifiers together in a layered web. Each node in the layers has an own classifier.

Inputs from one node are taken from multiple nodes in the previous layer, and the result is passed to the next layer, and this repeats until it reaches the output layer.

The results of the classification are determined by the score at each node.

**Forward Propagation** - The NN's way to classify a set of inputs through the nodes in the layers.

### Multi-layered perceptron
NNs came out from the need to improve performance of **perceptron classifiers**.
By using a layered web of perceptrons, the accuracy of predictions could be improved. 
This new breed of NNs are called Multi-layered perceptron or **MLPs**.

Since then, the nodes inside NNs have replaced perceptrons with more accurate classifiers (But the name MLP has stuck). 

### Weights and Biases
If you have a NN with nodes that have the same classifier and the nodes don't fire randomly, then the same input will get the same output every time. 
**Then why would nodes in the network have different outputs?* Because each set of inputs is modified by different sets of *weights* and *biases**.

* *Weight** - The weight in the edges that connect the nodes
* *Bias** - Extra weight that is added in each node

### Training
The prediction accuracy depends on its weights and biases.
We want the accuracy to be hight.
We want the NN to **predict an output** that is as close as possible to the **actual output**.
The process to improve a NN's accuracy is called **training**.

**Cost** - The difference between the output obtained and the actual output.

The point of training is to minimize the cost.

## Resources

* Michael Nielsen's book - http://neuralnetworksanddeeplearning.com/
* Andrew Ng's class - https://www.coursera.org/learn/machine-learning
