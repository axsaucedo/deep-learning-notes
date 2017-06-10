
# Recursive Neural Tensor Nets
Used to discover the hierarchical structure of a set of data.

Examples are parse trees of groups of sentences.

RNTNs are a better fit than FFNs or RNNs.

## History

Conceived by Richard Socher at Metamind as PHD thesis at Standford.

Purpose was to analyze data that had a hierarchical structure.

Originally designed for sentiment analysis, where the sentiment doesn't just depend on its component words, but **in the order in which they are syntactically grouped".

## Structure
RNTN has 3 basic components:

* **Root** - A parent group
* **Leafs** - Child Groups

Each group is simply a **collection of neurons** where the number of neurons **depends on the complexity of the input data**.

The root is connected to both leafs, but leafs are not connected to each other.

The 3 components for a **binary tree**.

In general, the leafs receive input, and the root group uses a classifier to fire out a **class** and a **score**.

The structure might seem simple, but like in a RNN, the complexity comes from the way data moves though the net.

In the case of an RNTN, this process is **recursive**.

## Recursion
To see how the recursion works in RNTNs, here's an example:

* We feed an English sentence to an RNTN
* We receive the sentence's parse tree as an output

### Steps:

1. We feed the first 2 words into leaf groups 1 and 2 respectively.
2. The 2 vectors move across the net to the root, which processes them and fires 2 values: the **class** and the **score**.
3. This is the point where the net starts the recursion
4. The current parse is passed to the left leaf above, whilst the right leaf receives the following word in the sentence
5. At this point, the root group would output the score of a parse which is 3 words long 
6. This continues until all the inputs (words) are used up. The net has a parse tree with every single word included

### Overview of example

This simplifies the main idea behind an RNTN, but in a practical application, we typically encounter more complex recursive processes. 

Rather than using the next word in the sentence for the second leaf group, an RNTN would try all of the next words, and eventually vectors that represent entire sub-parses.

By doing this at every step of the recursive process, the net is able to analyze and score any possible syntactical parse.

### Terms

**The class**: Represents an encoding of the structure in the current parse

**The score**: Represents the quality of the current parse

**Practical note**: The leaf groups don't actually receive the words per say, but rather vector representations of the words. Particularly, good results are achieve when the numbers in the two vectors **encode the similarities** between the two words **when compared** to other words in the vocabulary.

## Choice of structure
It's possible to build a structure that holds the weight to the right, in the centre or to the left.

In order to chose the best structure, the net relies on the score value produced by the root group.

By using this score to select the best structure at each step of the recursive process, the net will produce the highest scoring parse as its final output.

## Labeling

Once the net has the final structure, it backtracks through the parse tree, in order to figure out **the right grammatical label for each part of the sentence.**

In an example "The car is fast", you could have the first two words labeled by a leaf+root group as a "noun phrase", and the last two ones as a "verb phrase". Then it would work its way up, and when it reaches the top, it adds a special label that signifies **the beginning of the parse structure**.

## Backpropagation

RNTNs are trained with backpropagation by comparing the **predictive sentence structure** with the **proper sentence structure** obtained from a set of **labeled training data**.

Once trained, it will now give higher score to structures that are more similar to the parse trees it saw during training.

## Parsing

### Text processing

RNTNs are used in NLP for both syntactic parsing and sentiment analysis.

### Image parsing

Also used to parse images, typically when an image contains a scene with many different components.

