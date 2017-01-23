
# Deeplearning4J

Useful library to build commercial application.

Java-based library with large selection of deep networks, with great other tools like a distributed multi-node map-reduce procedure, and a package for vectorization.

## History

Created by Adam Gibson.

Also referred as DL4J

## Overview

Commercial library that can run in a distributed multi-node setup.

(**The J stands for Java.**)

The library allows you to build a deep net by selecting values of its hyperparameters.

It comes with built in GPU support for distributed frameworks, which is **important for training**.

Library can run on Scala and Closure as well.

## Features

The library supports all the deep nets that we've seen so far:

* DBN / MLP
* RBMs
* Convolutional Networks
* Deep Autoencoders
* Recursive Neural Tensor Networks
* RNN

It also includes a vectorization library called **"Canova"**.

## Iterative Map-Reduce

Training any ML model on a distributed framework requires a two step procedure called **iterative map-reduce**.

* **Map** - The data is distributed across all the nodes in the cluster. Each node then trains the net with a portion of the data that it receives.
* **Reduce** - The weights and biases across every node in the cluster are averaged together. Each node replaces the parameters of its net with this average

This two steps are repeated iteratively until the error is sufficiently small.

This is how DL4J trains a model on a distributed platform. 

Traditionally a map-reduce procedure is sequential, and its only run one time.

