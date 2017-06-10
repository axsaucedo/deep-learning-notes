
# H2O.ai

If you need to run different learning models alongside a Deep Network, then H2O.ai might be a good choice.

This software platform offers one deep net, the MLP, and a few other ML algorithms.

Besides a set of ML algorithms, H2o offers tools like data preprocessing.


# Deep Network Support

Currently the only Deep Network supported is the multilayered perfecption (MLP). Despite this, the platform has sofisticated data munching capabilities as well as an intuitive module management UI.

The other supported ML models include:

* GLM
* Distributed random forest
* K-means clustering
* Gradient boosting machine that uses decision trees
* CPH
* Naive Bayes classifier

Training with backpropagation is performed by the means of the **L-BFGS algorithm.**

## Training Data Loads

Fortunately, H2O comes with integration with:

* HDFS
* Amazon S3
* SQL
* NoSQL

## Interface

* It has an intuitive UI
* Plus programming env with R, Python, JSON, etc
* Model with Excel, Tableau, R studio
* H2O also offers training, which allows you to obtain a model with the optimal set of hyperparameters

## How to use

H2o is provided as a software package that needs to be installed and ran in own hardware.

To help with this, platform provides:

* In-memory map-reduce capability
* Nano-second predictions
* Columnar compression
* Query processor

These additions will help speed up training significantly.

The creators hoped that search and analytics would be interactive, but this does not apply to training. Instead, they hope that the trained nets can make predictions of new data on the fly.

## Final note

Not sure if GPU support is available at this time, but you can access the framework through an API.

## History

Started out as an open source mission by Arno Candel and Cliff Click.
