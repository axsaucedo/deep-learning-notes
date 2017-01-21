

# Restricted Boltzmann Machines

A method that can automatically find patterns in our data by automatically reconstructing the input.

## Geoff Hinton
Uni of Toronto, first researcher to release way to train deep nets, creating RBMs.
Because of his work, he's referred as one of the fathers of Deep Learning.

## RBM Structure
A shallow 2-layer net with:
* **Layer 1:** Visible layer
* **Layer 2:** Hidden layer

Each node in the visible layer is connected to each node in the hidden layer.

**RBMs are restricted** - An RBM is considered **restricted** because no 2 nodes in the same layer share a connection.

An RBM is a mathematical equivalent of a **two way translator**.

### RBM Process
* **Forward pass** - RBMs takes the inputs and translates into a set of numbers that encode the inputs.
* **Backwards pass** - RBM takes the set of numbers and takes it back to form the reconstructed inputs.

A well trained net would be able to perform the backwards translation with a high degree of accuracy.

_**In both steps, the weights and biases have very important roles. They:**_
* Allow RBM to decipher the interrelationships among the input features
* Help RBM decide which input features are the most important when detecting patterns.

## Recreate Input

Through several forward and backward passes, an RBM is trained to reconstruct input data.

3 steps are repeated over and over in the training process.

1. Forward pass
    * Every input is combined with an individual weight and one overall bias.
    * The result is passed into the hidden layer which may or may not activate.
2. Backwards pass
    * Each individual activation is combined with an individual weight and an overall bias.
    * The result is passed to the visible layer for reconstruction.
3. At the visible layer, the reconstruction is compared against the original input to determine the quality of the result, using **KL DIVERGENCE**.

**KL Divergence** - the method RBMs used for step 3 to compare actual to recreation

Steps 1-3 are repeated with varying weights and biases until the input and reconstruction are as close as possible.

## Pattern Recognizer
Data does not to be labelled for RBMs.

This is very important for real world datasets like photos, videos, sensors, which tend to be unlabelled.

Rather than having people labelling it manually, RBMs automatically goes through data and extract important features to reconstruct the input.

### Important Note
RBMs are actually making decisions about which input features are important and how they should be combined to form patterns

**RBMs** are part of a family of feature extraction neural networks, which are all designed to recognize patterns in unlabelled data - these are also called **autoencoders**

In a way **autoencoders** have to encode their own structure.


