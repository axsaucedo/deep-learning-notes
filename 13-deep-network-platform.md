
# Deep Network Platforms

Deep learning platforms come in 2 different forms:

* Software platforms
* Full platforms

## Overview

A platform is a set of tools other people can build on top of.

Deep learning platforms provides a set of tools and an interface for building custom deep nets.

### Deep Network Capability

Typically they provide the user with a selection of deep nets to choose from, such as:

* DBNs / MLPs
* RBMs
* CNNs
* Autoencoders
* RNTNs
* RNNs

They often also provide with the ability to integrate with data from different sources, manipulate data, and manage models through a UI.

### Infrastructure 

Some platforms also help with performance when it's required to train a net with a large dataset.

## Platform vs Libraries

Later chapters cover software libraries that will help code own Deep Networks.

### Advantages vs Disadvantages

#### Platform

For anyone to quickly deploy a Deep Network, a platform is the best way to go.

**Advantages**

* An out of the box application that lets you configure a deep net's hyperparameters through an intuitive UI.
* With a platform you don't need to know anything about coding in order to use tools.

**Disadvantages**
* The downside is that you are constrained by the platform's selection of deep nets as well as the configuration options.

#### Library

If you need the flexibility and you can code, libraries are the ideal resource.

**Advantages**
* A set of functions and modules that you can call from your own code. Deep Network Libraries give you a wide selection of hyperparameter config, etc.
* For example, **there aren't many platforms** that allow you to build a Recurrent Neural Tensor Network, but you can code your own with the right deep net library.

**Disadvantages**
* Coding experience required
* A bit more complexity exposed


## Platform Examples

These are the examples that will be covered later:

### Erstatz Labs
A deep learning platform that handles all the technical issues, including code, deployment, and performance. It allows the user to go straight to modeling.

### H20.ai & Dato
Both platforms offer deep learning tools. These are software platforms, and not full platforms (like Erstatz), so **they need to be installed in your own hardware.**



