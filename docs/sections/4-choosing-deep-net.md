
# How to choose a Deep Net
We need to decide if we're trying to build a classifier, or if we are trying to identify patterns in our data.

## Types of classifiers

### Unlabelled data

Problem type:

* Feature extraction
* Unsupervised learning
* Pattern recognition

Suitable classifiers:

* Restricted Boltzman Machine (RBM)
* Autoencoders

### Labelled data

#### Text processing

Problem type:

* Sentiment analysis
* Parsing
* Name entity recognition

Suitable classifiers:

* Recursive Neural Tensor Network (RNTN)
* Recurrent Network (For problems that occur on character level)

#### Image recognition

Suitable classifiers:

* Deep belief network
* Convolutional network

#### Object recognition

Problem type:

* Identifying objects in a picture or video

Suitable classifiers:

* Recursive Neural Tensor Network (RNTN)
* Convolutional network

#### Speech recognition

Suitable classifiers:

* Recurrent Network

### General

#### Good for classification

* Deep Belief Networks
* Multilayered Perceptrions with Rectified Linear Units (RELU)

#### Good for time series

* Recurrent network
