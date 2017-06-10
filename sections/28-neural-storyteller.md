
# Neural Storyteller

When you look at a picture, the brain often sparks an intricate narrative based on what we know and how we feel.

Deep Learning is artificially creating this with a Neural Network.

Neural Storyteller (NS) is a fun machine vision project that will observe a digital image and then it will imagine a romance short story based on what it sees.

Jason Toy of Somatic has integrated this into their **model market place**

## About NS

Created by PHD Jamie Ryan Kiros from Toronto Uni

Getting an AI to imagine a story is not easy.

In order to put this project into motion this is what was required:

### 1) Input/Output

We feed in images as input, and as output we create sentences creating that image.

We saw how a Recurrent Neural Network can perform image captioning by taking a single image as input and generating a sequence as output.

The image captions used for training are generated from the MS coco database.

### 2) Story

We also need a mechanism that goes beyond the individual elements of the image

We need to devise a skip-thought model which will generate text in the style of a romance story.

A similar type of model is **the skiptogram**, which uses a target word to predict the surrounding words, also called the context.

The **skipthought model** predicts the surrounding text for a given sentence, **called a thought.**

The romance text for romance storyteller was taken from the book corpus.

### 3) Different styles

Image captions in romance stories usually have different word patterns due to differences in style.

Generally speaking, captions are straightforward and factual, whereas romance stories are more emotive. As a result, the word vectors for these styles tend to be dissimilar.

For this step, it's necessary to bridge this gap by building a model that can perform a transformation from one style to another.

For more details on this process, check out:

* Neural Storyteller model on Somatic - http://somatic.io/neural-storyteller
* Somatic Blog post - http://www.somatic.io/blog/how-neural...
* Neural Storyteller - https://github.com/ryankiros/neural-s...
* MSCOCO Database - http://mscoco.org/
* BookCorpus URL - http://www.cs.toronto.edu/~mbweb/
* Jamie Ryan Kiros - http://www.cs.toronto.edu/~rkiros/



