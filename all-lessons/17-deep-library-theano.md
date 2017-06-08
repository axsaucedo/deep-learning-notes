
# Theano DL Library

Theano provides an important set of functions for building deep nets that will train quickly in your machine.

## History

Created by the ML group and the University of Montreal

Yashua Bengio was one of the leads.

Theano is a python lib that helps you define expressions with vectors and matrices.

Neural Nets and input data **can be represented as matrices.**

And all the operations can be defined as **matrix calculations.**

If you build a NN with this underlying structure, you can use a machine with a single GPU to train models fast.

## Keep in mind

**Disadvantage**
If you use theano you will have to build the net from the ground up 

Lib doesn't provide full functionality to create a specific type fo deep net. Instead you have to code the model, the layers, the activation, the training method, and any special methods for preventing overfitting.

**Advantage**
You can build your whole implementation as a set of vectorized functions, easily optimizable.

## Libraries for Theano

* Blocks - Provides a wrapper for each theano function to access functions with params
* Lasagne / Keras - Allows you to build a net on top of theano by providing the nets hyperparameters layer by layer.
* Keras - Minimalist design, create net layer by layer, train it and run it
* Passage - Used for text analysis

Training a net in hadoop is not possible at this point.
