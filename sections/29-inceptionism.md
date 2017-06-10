
# Inceptionism

Google published a paper about inceptionism - a neural network that hallucinates.

The idea behind the project was to showcase the features learned by different levels of a Convoluted Neural Network.

This was done by applying the learned features onto different images, which yielded results that were interesting and amusing.

Jason Toy has implemented inceptionism in their marketplace.

## Convolutional Nets

A CNN learns progressively complex features by assembling simpler ones.

In the example of face detection:

* It first learns pixels
* Then edges and contrasts
* Then parts of the face
* Then finally combined to form the face

The NN does this during the training process without any direction from the person building it.

Neural Networks are almost always built with a specific task in mind, but **it is extremely important to use knowledge transfer**.

By letting the Neural Network learn on its own, the builder surrenders control by what the Neural Network learns or does.

This is an important benefit for something like facial recognition, as there are multiple ways pixels can form a face...

**HOWEVER** it is never clear upfront which filter or layer will learn **which features**, and at **what level**.

The inceptionism project's is an effort by google to figure out what a given layer learns and re-apply that onto other images.

## Generation

Up to this point we've seen how Deep Networks can discriminates between inputs, and assign them to a class or set of classes.

In image recognition for example, a Deep Network can analyse a deep net and analyze it as a cat picture, however Deep Network can also be used **in generation.**

Given an output, they can generate a set of input data that would've resulted in that output.

As an example, a cat detector model that would need to produce the original cat image - working in reverse, the model would start with the cat, then break it down to the face and legs, and then break it down into pixels.

The key insight from this project is that the learned weights and biases of the discriminative CNN model can also be used in generation.

By extracting the learned features from a network and applying them to a random image, those particular features of the image are enhanced.

So if you extract the features from the edge detecting layer, on a model trained on animals, and applied it to a natural scene, any edges in the scene that resemble **those found in animals would be enhanced.**

On the other hand if you applied higher level features like a dog face onto a nebula image, you would end up with a strange looking combination of the two.

**It's important to understand that this is not just superimposition**

The model was gradually tweaking the features in the image to look more and more like what it learned from the original network.

This actually results in an intertwining of the two.

## Relevant links

* Somatic model - http://www.somatic.io/inceptionism
* Somatic Blog post - http://www.somatic.io/blog/how-incept...
* Inceptionism - https://research.googleblog.com/2015/...
* Dog nebula - http://www.ibtimes.co.uk/google-deepd...
* Somatic URL - http://www.somatic.io/

