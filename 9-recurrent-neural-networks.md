
# Recurrent Neural Networks
Used for datasets with patterns that change **with time.**

This Deep Learning model has a simple structure with a built-in feedback loop allowing it to act as a forecasting engine.

## Structure
All networks we've seen until this point have been **Forward Feed Neural Networks** - a network that signals flow in one direction from input to output, one layer at a time.

In a Recurrent Neural Network, the output of a layer is added to the next input and **fed back** into the same layer - which is typically **the only layer** in the entire network.

You can think of this process as a passage through time:

* If we have 4 times t
* At t = 0, we pass the input once through the layer
* At t = 1, we take the output of t = 0 and pass it again through the layer
* The net repeats for t = x

## Enabling for Sequence Inputs
Unlike FFNs, a recurrent net can receive a **sequence of values** as input, and also produce a sequence of values as output.

The ability to **operate on sequences** allows for many more applications.

### Applications
When the input is singular and the output is a sequence, a potential application is **image captioning**.

A sequence of inputs with a single output can be used for **document classification**.

A sequence of inputs and sequence of outputs, a net can **classify videos** frame by frame.

If a time delay is introduced, then that can **statistically forecast** demand in supply chain planning.


## Stacking
By stacking Recurrent Neural Networks on top of each other, you can form a net capable of more complex output than a single RNN working alone.

## Training
It's typically an extremely hard net to train.

Since these nets use backpropagation, they run into **vanishing gradient**.

The vanishing gradient is **exponentially WORSE** for RNNs because each timestep is the equivallent of an **entire layer** in a **feed forward MLP**.
> RNN with 100 steps = 100 layer MLP

This leads to **exponentially small gradients**, and a **decay of information through time.**

### Gating for training
The solution to exponentially small gradients.

It helps the net decide when to **forget** the current input and when to **remember** it for future timesteps.

The most popular gating tools today are **GRU** and **LSTM**.

Other techniques besides gating include:

* Gradient clipping
* Steeper gates
* Better optimizers

### Computing
When it comes to training a recurrent net, GPUs are an obvious choice. Teams use GPUs for training tasks on sentiment analysis and helpfulness extraction.

GPUs were able to train the nets 250 times faster ( 1 day vs 8 months training )

## When to use RNNs vs FFNs
We know that FFNs outputs ONE value, which in many cases is a **class** or a **prediction**.

A RNN is suited for time series data, where an output can be the next value in the sequence (or next set of values).

The answer depends on whether application calls for **classification, regression, or forecasting**.

## History

A lot of credit goes to Jurgen Schmidhuber and Sepp Hochreiter























