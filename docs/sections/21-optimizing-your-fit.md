
# Fitting a model

When it comes to fitting a model to a data, our best bet is the **Goldilocks principle**.

We don't want to **underfit** our data as we'll have very low accuracy.

We also don't want to **overfit** our data and produce a model that can't generalize to new samples.

## Underfitting

Suppose we are trying to classify big cats using weight, height, presence of organs, etc.

If we develop a model that roars and has a main like a lion, since the model ignores the animal's sex, it might see a lioness or a monkey.

This would be a case of underfitting.

We can address the underfitting problem by adding more features that can help differentiate the samples.

## Overfitting

We can also create a model that analyses every conceivable attribute of a lion on intricate ways.

But this might result in a large set of arbitrary patterns that describe the set very well, but don't generalize to new sets of data.

As an example, our example might contain a lion that is 305lbs, 3.5ft height and has 2.9inch talons. A poorly trained model might state that any cat with those attributes is a lion.

This would be accurate to predict our training sample, but not new samples.

**Models that overfit data have failed to identify the true patterns that accurately differentiate the classes in the dataset.**

Moreover, if the data comes from african lions, we might struggle to find white lions.

The model must be able to identify important patterns in the data that properly differentiate the classes. This way new samples can be properly classified.

## Causes and Outcomes

### Overfitting

* The set of **input features is far too big** (Not enough nodes per layer)
* The architecture of the network is **too complex** for the problem (too many hidden layers)
* There are more hidden layers than nodes per layer

Overfitting will manifest itself in the weights and biases of the Neural Network.

During training the Neural Network assigns weights to each feature which determines their importance and the ways they will be recombined

When overfitting, the model will assign weights to features that are not needed and add unnecessary complexity to the patterns.

### Overfitting Solutions 

It's a common problem across many data science methods

#### 3 way data split
A popular method is by splitting the data into 3 sets:

* Training set
* Test set
* Cross validation set

This method ensures the model is not too dependent on any particular subset of the overall dataset.

##### Regularization

For Neural Network regularization is a common method.

Common ones include l1 and l2, but all follow the same general principle:

>The model is penalized for having weights and biases that are too large.


#### Max norm constraints

Directly adds a size limit to the weights or/and biases

#### Dropout

Randomly switches off switches off certain neurons on the network, preventing the model from becoming too dependent on a set of neurons and its associated weights and biases.

#### Overview of solutions

Whilst these methods are applied broadly across the model and don't systematically search for problem patterns or problem weights and biases, they have proven to be effective at **reducing or preventing** the problem of overfitting.



















