
# Text Analytics

Deep Learning has the potential of revolutionizing Text Analytics.

## NLP

A big field that includes:

* Lemmatization
* Named Entity Recognition
* Part of Speech Tagging
* Syntactic Parsing
* Fact Extraction
* Sentiment Analysis
* Machine Translation

These methods typically rely on a "language model" - a model that estimates the likelihood of seeing a particular component in a body of natural language.

One example is the trigram model which attempts to calculate the probability of seeing a specific sequence of 3 worlds in a natural language corpus.

## Disadvantages

Language is subjective and ambiguous: Sometimes a word can have different meanings depending on the context. 

It can also be difficult to add new words to an existing model, so NLP often requires a lot of manual curation.

This added labour comes at the cost of variable quality and consistency.

## Deep learning in NLP

Deep Learning is an important tool that overcomes the limitations of NLP.

The main difference between DL and other methods is the **use of vectors**.

To represent a word, a DL model might use a **one hot vector** implementation

### One-Hot Vector

The implementation that DL uses to represent words as vectors.

It has its roots in digital circuit design.

In this form each word is represented as a vector who's length is the size of the entire vocabulary.

Every value in the vector is set to zero except to the value of the word which is set to 1.

This can get out of hand if vocab size is large.

Large vectors can slow down processing time.

#### Google IT 

The google IT corpus has a vocab of 13m words.

To store these words as one-hot vectors, we would need 13m vectors, each of size 13m.


## Dimensionality Reduction

DR is one application for which one-hot vectors are used.

### Continuous Bag of Words

If you have a word **w**, surrounded by a fix set of words called **Context**.

In this model, the context is used as a set of features to predict what **W** might be, in a type of fill-in-the-blanks application.

A shallow Neural Network is used for this task with the input layer containing one hot vectors for the context words.

The output fires the predicted target wall.

### Skip grams

This is the reverse of the continuous bag of words model.

It provides the context words given a target word.

Since only the target word is used as input instead of the context words, the inputs of the hidden layer would be much smaller.

As a result, we can use the hidden layer's activation to represent the target word, rather than use the long one-hot vector form.

**Basically we can reduce the input vector's dimensionality**.

## Tools

There are several tools for converting words into vectors, including:

* Word2vec from google
* GloVe

## Methods 2.0

Once the words can be represented by vectors, they can be used with Deep Networks.

### Syntactic Parsing

An old problem that received a big boost from the use of Recursive Neural Tensor Networks.

* For a brief overview, the RNTN consists of a root node connected to two leaf nodes. 
* Two words are passed to the leaf nodes, with each leaf receiving its own word. 
* The leafs passes the words to the root which processes them, and produces an intermediate parse, along with the score. 
* This parse is fed into the level above, together with the following word. 
* This process is recursive, and continues until all words have been fed into the model. 

In reality the actual process is much more complex as it needs to analyse all possible subparses during the recursive step rather than just using the next word, but by doing so it's able to analyse and score every possible syntactic parse.

### Machine Translation

A recurrent net can take a sequence of inputs along with the time delay, and produce a sequence of outputs.

A properly trained recurrent net can learn the inherent syntactic and semantic relationships of multiple different languages.

When the net is fed a sequence of words in one language, it knows how to generate the appropriate sequence of words in another language.

### Sentiment Extraction

RNTNs can also be used for sentiment analysis.

Sentiment, like syntax, is hierarchical in nature, and a single word in the right place can change an entire meaning in a sentence.

An example from his thesis shows an RNTN tree with a sentence.

Whilst a normal process would label the sentence as negative as there are more negative terms than positive ones, **an RNTN** is capable of interpreting the deep semantic structure of the sentence in order to make the right prediction.
