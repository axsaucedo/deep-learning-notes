
# Convoluted Neural Networks (CNN)
The deep network that has completely dominated the machine vision space in recent years.

## History
Pioneered by Yann Legun from NYU uni - director of FB AI group. They say fb uses a CNN for their face recognition

Early in 2015 by Microsoft, Google and Baidu, machine was able to beat a human in object recognition.

### Imagenet Challenge
Imagenet is a project that was inspired by the growing need for high quality data in the image processing space.

Every year, the top deep learning teams in the world compete against each other to build the best possible object recognition sofware.

In 2012 when Jeff Hinton's team took first place in the challenge, every single winner has used a CNN for their projects.

The error rate of image detection texts has dropped with CNNs.

### Resources for CNN knowledge
For deeper insight on the maths, check out **Andrej Karpathy's CS231N notes.


## Architecture

### Main components
A typical CNN has 3 sets of layers
* Convolutional layer
* RELU layer
* Pooling layers

All of which are repeated several times

These layers are followed by a few fully connected layers to support classification.

Since CNNs are such Deep Networks, they most likely need to be trained using server resources, which will probably require GPUs.

## Drawbacks
Since they are a supervised learning method, they require a **large set** of labelled data for training. 

This can be challenging to obtain in a real world application 


### Convolutional Layer

* If we have a wall which represents a digital image.
* Imagine we have a bunch of flashlights shining at the wall, creating a group of overlapping circles

The purpose of the flashlights is to seek out a certain patter in the image, like an **edge** or a **colour contrast**.

Each flashlight looks for the exact same pattern as the others, but they all search in a different section of the image, defined by the fixed region created by the circle of light.

When combined together, the flashlights form what is called a **filter**.

A **filter** is able to determine if the given pattern occurs in this image, and in what regions.

In the case of an 8x6 grid of lights, which is all considered to be one filter:
* If we take a look at the top, flashlights from multiple filters, they will all be shining at multiple spots in parallel, simultaneously detecting a wide array of patterns
* In this example, we have 4 filterns all looking at the wall, all looking for a different pattern
* This specific type of convolutional layer is an 8x6x4 3D grid of the flashlights.

Connecting the dots, why is it called a convolutional network?

The net uses the technical method of convolution to search for a particular pattern. In simple words, convolution is:
* **The process of filtering through the image for a specific pattern**

**Important note:** The weights and biases of this layer affect how this operation is performed. Tweaking these numbers impacts the effectiveness of the filtering process.

Each flashlight represents a neuron in the CNN.

Typically, neurons in a net activate or fire. In the CNN, neurons perform a **convolution operation**.

By just drawing a box around a set of flashlights, we can see that unlike with normal networks, every neuron is not connected to neurons in adjacent layers; instead, **a CNN has a flashlight structure**.

**Flashlight structure** - Each neuron is only connected to the input neuron it shines upon.

The neurons in the same filter share **the same weight and bias parameters**. This means that anywhere in the filter, a given neuron is connected to the **same number of input neurons**, and has the same **weights and biases**.

> This is what allows the filter to look for the same pattern in different sections of the image

By arranging these neurons in the same structure as the flashlight grid, we ensure that the entire image is scanned.

### Relu and Pooling

The next two layers that follow.

Both of which that help to build up the simple patterns discovered by the convolutional layer.

Each node in the convolutional layer is connected to a node that fires in other nets.

#### Rectified Linear Unit (RELU) layer
**The activation used is called Rectified Linear Unit (RELU)**

CNNs are trained using **backpropagation**, so the _vanishing gradient_ is once again a **POTENTIAL ISSUE**!

For reasons that depend on the mathematical definition of RELU, **the gradient** is held more or less constant at every layer of the net.

So the RELU activation allows the net to be properly trained without harmful slowdowns in the crucial early layers.

#### Pooling layer
The pooling layer is used for dimensionality reduction.

CNNs tile multiple instances of convolutional layers and RELU layers together in a sequence in order to build more and more complex patterns.

The problem with this is that the number of possible patterns becomes **exceedingly large**.

By introducing pooling layers, we ensure that the net focus is only on the most relevant patterns discovered by convolution and RELU.

This limits both the memory and processing requirements to running a CNN.

#### Fully Connected (FC) layer
Together, these 3 layers can discover a hose of complex patterns, but the net **won't have an understanding of what these patterns mean.**

This is why a Fully Connected (FC) layer is attached to the end of the net in order to equip the net to classify data samples.










