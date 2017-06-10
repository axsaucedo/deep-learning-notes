
# Autoencoders
Used when there's need to understand the underlying structure of a dataset.

Having access to the most important data features gives you a lot of flexibility when you start applying labels.

Autoencoders are well suited for this task.

## Feature Extractors
We had previously looked at RBMs, which is a popular example of auto encoders.

There are other type of encoders like:
* Denoising
* Contractive
* A lot more!

Just like an RBM, the autoencoder is a neural net that takes a set of typically unlabelled inputs, and after encoding them tries to reconstruct them as accurately as possible.

In order to do this, the net must decide which of the data features are the most important.

This essentially acts as a **feature extraction engine**.


## Shallow
Autoencoders are typically very shallow, and are usually comprised of:

* Input layer
* Hidden layer
* Output layer

An RBM is an example of an autoencoder with only 2 layers.

### Example reconstruction of input
There are 2 steps in the reconstruction of the input:

* Encoding
* Decoding

Typically the same weights that are used to encode a feature in the hidden layer, are used to reconstruct an image in the output layer.

## Backpropagation with loss

Autoencoders are trained with backpropagation using a method called **LOSS**.

As opposed **to COST**, LOSS measures **the amount of information lost when trying to reconstruct the input**.

With a small loss value, the net would produce reconstructions that look very similar to the original ones.


## DEEP
Not all of these nets are shallow.

**Deep autoencoders** are very useful for **dimensionality reduction**

Consider an image containing 28x28 pixels:

* A NN would need to process over 700+ input values for just one image
* Doing this across millions of images would waste time and CPU

An autoencoder would encode this image into just 30 numbers, and still maintain information about the key image features.

When decoding the output, the net acts like a 2-way translator. 

In this example, a well trained net could translate these 30 encoded numbers back into a reconstruction that looked similar to the original image.

Certain nets also add noise to the encoding / decoding process, which has been shown to improve the robustness of the resulting patterns.

## PCA vs Autoencoders
Deep autoencoders perform better at **dimensionality reduction** than their predecessor, Principal Component Analysis (PCAs).

In the case of several newsletters with different topics, a PCA would do a much worse job than an deep autoencoder.

