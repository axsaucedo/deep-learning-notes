
# Training

## The vanishing gradient
When trying to train deep networks with **back propagation**, you run into the problem of **the vanishing gradient**, or **the exploding gradient**.

## Training neural networks 
To calculate neural networks you have to calculate cost values. 
Cost value is the difference between the output of the neural networks and the actual output, from a set of training data.
The cost is used to make adjustments to the costs and biases to the NN.

### Gradients
For each node, it is the measure of the rate at which the cost will change with respect to a modification in a weight or a bias.

**Issue: Vanishing Gradient**
Deep architecture are the best and sometimes only solution for complex machine learning problems such as facial recognition.
**Until 2006** there was no way to accurately train deep networks due to a fundamental problem with the training process - **the vanishing gradient**.

#### Conflict
You can think of a gradient like a slope. The training process like a rock rolling down. When the gradient is large, the net will train quickly, and vice versa.

In a complex network with multiple layers, the gradient can **vanish / decay** as it goes through the net. 

**The gradients are much smaller in the earlier layers**.

As a result the earlier layers are the **slowest to train.** This is a fundamental problem.

The earlier layers are the ones that recognize the simple patterns and building blocks (as in the example in the prev chapter). If the earlier layers get it wrong, the rest will be bounded to be incorrect.

### Backpropagation
The process used to train a neural network.
Whilst **forwardprop** starts with the inputs and works its way forward, backprop goes the other way. 

It calculates the gradient from right to left. Each time to calculate the gradient, it uses the previous gradients up to that point.

**Example**
If we take a node in the penultimate layer, we can see its connected to multiple nodes in the output layer, and use them to calculate the gradient.

As you keep going back in the layers, we have to use a lot of gradients.

#### Backprop gradient calculation 
A gradient at any point is the product of the previous gradients up to that point. The product of two numbers between 0 and 1 gives you a smaller number...

#### Implications

* Takes a lot of time
* Accuracy is very low

## Until 2006...
Deep nets were underperforming shallow nets, but everything changed after 3 breakthrough papers, published by **Hinton, Laocoon and Bengio**.

