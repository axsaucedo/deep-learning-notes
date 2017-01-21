
# Pattern Recognition
Neural networks are ideal to identify patterns.

GPUs can train neural networks faster than ever before.

## Pattern Complexity
Simple patterns could be solved with SVMs or logistic regression.

But when there is moderate complexity, deep networks would outperform.

As patterns get more complex, neural networks with more layers **can become unusable**.
**Number of nodes required in each layer grows exponentially with the number of possible patterns in the data**
In this case training becomes **too expensive**, and **accuracy falls**.

Shallow networks are not a good option for this, the actual good choice is...

## Deep Networks

### Recognizing complex patterns
Deep networks break down complex patterns into a set of less complex patterns.

#### Example

A deep net wants to understand whether a picture contains a human face. In each layer, the computer learns to identify:
* **Layer 1:** Pixels of light and dark
* **Layer 2:** Edges and simple shapes
* **Layer 3:** More complex shapes and objects
* **Layer 4:** Shapes and objects can be used to define human face

This is what gives deep nets their strengths, and its accuracy.

## Human Brains
Deep net architectures were inspired from the structure of human brains. 

Brains have a very deep architecture like a deep net.

## CPU vs GPU
Advances in computing have reducing time required to train deep networks.

High performance GPUs can finish training nets in under a week, whilst CPUs would take weeks.








