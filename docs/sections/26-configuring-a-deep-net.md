
# Configuring a deep net

With the right design, deep nets are some of the most powerful tools in data science.

Configuring a net is never a straightforward task however.

## Layers

Each hyper-parameter of a deep net is an important design choice in terms of both, the architecture and the training approach.

The first decision is the architecture, where you need to specify the types of layers for the deep net.

### Input Layers

Generally straightforward, since they are typically constrained by the application and the dataset.

However, there are many different types of hidden layers to chose from, such as convolution, pooling, activation, and loss, etc etc.

### Convolution / Pooling

Convolution and pooling often have their own sub-parameters for the number of filters and the type of pooling respectively.

### Matrix Operations

Some networks can also have matrix operations built in if you need to change the shape of data between layers

### Output layer

When deciding an output layer, it's important to specify the **cost function** for the network, which could be **sum of squares, cross entropy, etc...**
>Cross entropy is used for multiclass classification

## Neurons

You need to determine the number of neurons you will place in each layer.

There are a few heuristics for this aspect of Neural Network design. Two which are:

* Growing 
* Pruning

### Growing 

You start with a smaller than expected neuron count, and then you keep adding neurons throughout the training process until the cost is no longer affected.

### Pruning

The reverse to growing.

You start with an excess of neurons and keep removing until there is a cost difference.

### Disadvantages of Growing & Pruning

They are computationally expensive.

If resources are limited, a better approach is to start with excess of neurons, and then use a **regulariser to prevent overfitting.**

## Activation Functions

* The most popular is the **Logistic Unit / Sigmoid**.
* Hyperbolic tangent (Tanh)
* Rectified Linear Unit (ReLU)

ReLU is an approach to fight the vanishing gradient when working with Backpropagation.

These activations all come with their own variants.

Feel free to experiment and pick the one that suits your needs.

## Regularization

An overconfigured net may lead to overfitting.

However when we combine an overconfigured network with a regularizor, we typically end up with a model that can regularize well to new datapoints.

Regularizors include:

* 3 way split
* l1 / l2 limit
* Dropout (turning off neurons)

The reason is that a net with more neurons has more ways to combine its weights and biases. 

As a result there are more possible patterns that a network can learn to recognize.

So there is a better chance of finding some kind of weight and baias configuration with the lowest possible cost.

## Gating 

This is another thing to bare in mind in regards to architecture.

If you need to build **in recurrence**, you will need to carefully consider the size of the net's input memory.

This will determine how much of the past input the net is required to remember.

Gating units such as GRUs and LSTMs are designed specifically to remember specific parts of an input sequence.

## Learning Rate

The success of the training process depends heavily on the choice of parameters.

**Backpropagation is sensitive to the learning rate**

If the rate is too large the algorithm might simply skip over the point it minimizes all cost.

If the rate is too small, the training process would take an unreasonable amount of time.

A common practice is to use a rate that changes as training processes.

Generally, the rate starts out large to speed up training, and decreases gradually as training progresses.

In this case, the net starts by learning about the patterns in a broad sense, and then ti starts fine-tuning its understanding.

Some strategies to dynamically alter the learning rate include:

* AdaGrad
* RMSProp
* AdaDelta

## Initialization

Before a net can be trained, it is necessary to assign starting values to the weights and biases in a process **called Initialization.**

The easiest solution is to simply randomize the values.

But since quality of initial weights has such a big effect on training times this is not appropriate.

Most advanced methods are beyond the scope of the video, but for example, **a Deep Belief Network may use an RBM to set the initial weights and biases.**

## Training Time

When working with RNNs, it's possible to use techniques like gradient clipping and steeper gates to speed up the training

But generally speaking, if you've exhausted all the available options, and your Deep Networks are still short of performance targets, **just raise the number of training epochs**.

**This strategy will work for any deep net**.

