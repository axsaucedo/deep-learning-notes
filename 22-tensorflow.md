
# Tensorflow

Good library from Google for building commercial level applications.

There is a lot of hype surrounding Tensorflow. This document contains an overview.

## History

Tensorflow came out of a Google library called disbelief V2.

This was a proprietary google library developed at the google brain project.

The project team's vision was to build a system that simplified the deployment of large scale deep learning models into a variety of different hardware setups - from smartphones, to simple servers, to giant servers with GPUs.

This library would improve the portability of ML so that research models can be more easily applied to commercial applications.

Eventhough tensorflow is 6 months all it's the most popular lib in github.

## Computational Graph

Much like the Theano library, tensorflow is based on the concept of a computational graph.

In a computational graph, **nodes** represent their persistent data or a math operation.

**Edges** represent the flow of data between nodes.

The **data** that flows through these edges is a **multidimentional array known as a TENSOR**

The output of an operation or set of operations is then fed as an input of the next. 

Eventhough Tensorflow was designed to support neural networks, it can support any domain where computation can be modeled as a data flow graph.

## Resources 

Tensorflow also adopts some useful features from Theano such as:

* Differentiation
* Common Sub-expression elimination
* Shared and Symbolic Variables 

For an open source library it has comprehensive documentation, as well as a **massive online course in udacity.**

## Network Support

Different type of Neural Networks can be supported by tensorflow.

However there is currently no support for hyperparameter configuration.

For now users can use KERAS to support hyperparameters in tensorflow.

## Interface

Currently Tensorflow has a **C++ interface**

The team hopes that community will build more programming language support with SWIG.

There was a release of Ruby.

## Performance

Tensorflow and theano seem simlar in many ways, but there are several key differences. 

When tensorflow was released in November of 2015, its compile and runtimes were much slower than theano, but the tensorflow community have fought to combat these issues.

An update in April 2015 tensorflow performed well in image category.

## Parallelism

Another improvement over theano comes in parallelism support.

Deeplearning4J supports the training of a ML model on a distributed framework through Iterative Map Reduce.

### Data Parallelism 

Data parallelism is implemented in a later release known as distributed tensorflow 0.8.

Data parallelism allows you to train different subsets of the data in different nodes in a cluster for each training pass.

Followed by parameter averaging and replacement across the cluster.

### Model Parallelism 

V0.8 also implements model parallelism.

Different portions of the model are trained in different devices in parallel.

For example you can use model parallelism to train stacked RNNs by deploying each RNN in a different device.

## OpenCL

Although many ML libraries support CUDA, few support OpenCL (A fast rising standard for GPU computing)

Tensorflow has added OpenCL support to the roadmap.

## Tensorboard

A visualisation tool for network architecture and performance.

The tool allows you to zoom in and visualize different levels of the network.

You can also view different summary level metrics, and changes overtime of the training process.


