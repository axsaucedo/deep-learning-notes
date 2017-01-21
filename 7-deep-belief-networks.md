
# Deep Belief Networks
RBMs can extract features and reconstruct inputs... but exactly does that help with the vanishing gradient?

By combining RBMs together and introducing a clever training method, we obtain a powerful new model that solves our problems: **Deep belief networks**

(Deep belief networks were also conceived by Geoff Hinton as an alternative to back propagation - he's now working on image recognition problems at Google)

## Structure of DBNs = MLP
The structure of DBNs are identical to MLPs.

However, the difference is when it comes **to training** - this is what allows them to outperform their shallow counterparts.

DBNs can be viewed as a **stack of RBMs**, where the hidden layer of one RBM is the visible layer of the one above it.

## Training

A DBN is trained as follows:
* The first RBM is trained to reconstruct its input as accurately as possible.
* The hidden layer of the first RBM is treated as the visible layer of the 2nd
* The 2nd RBM is trained using the outputs of the 1st RBM.
* This process is repeated until every layer in the network is trained.

An important note of a DBN is that each RBM layer learns the entire input

In other kinds of models like convolutional nets, early layers detect simple patterns, and later layers recombine them, like in the facial recognition example in previous chapters.

**HOWEVER** a DBN works globally by fine-tuning the entire input in succession as the model slowly improves.

The reason why a DBNs work so well is highly technical, but it suffices to say that a stack of RBMs will outperform a single unit, just like a MLP was able to outperform a perceptron working alone.


## Fine Tuning
After the initial training, the RBMs can detect inherent patterns in the data, **but we still haven't labelled the patterns**.

To finish training, we need to introduce labels to the patterns and fine tune the net with **supervised learning**.

To do this, we need a very small set of labelled samples, so that the features and patterns can be associated with a name.

The weights and biases are altered slightly, resulting in a small change in the net's perception of the patterns, and often a small increase in the total accuracy. 

Fortunately, the set of labelled data, can be small relative to the original dataset, which as discussed is extremelly helpful in real world applications.

**But do be careful of overtraining a deep network!**

## Benefits of DBNs
* Only needs a small labelled dataset, which is important to real life applications
* Training process can be completed in reasonable time thanks to GPUs
* Resulting net is very accurate compared to a shallow net

**It's a solution to the vanishing gradient problem!**




