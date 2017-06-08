
# Metrics for Deep Learning

Google outperformed a human at a image recognition task.

How was the performance actually measured?

The measurement was **error**

## Error

A straightforward measurement that captures the proportion of **data-points classified incorrectly.**

Calculation is simply:
>Number of incorrect classifications made by the net divided by the total number of classifications.

### Disadvantage

Error has a significant drawback as a performance measurement.

Especially when the datapoints are skewed towards one class over another.

#### Example 1

* We are tasked with a medical model to diagnose a brain tumour that only occurs in about 1% of patience

With the objective of low error, we could design a model that gives a negative diagnosis all the time.

Whilst the model would be useless in a practical setting, the error would be a very low 1%.

The problem arises when we measure error globally across the set of all classes, rather than taking a granular view of the model's performance at a class level.

#### Example 2

Let's look at a 2 class classification, where a datapoint can be considered positive or negative.

If the model makes a positive classification, then we can either be correct (**True positive**), or it could be incorrect (**False positive**).

True negatives and false negatives are defined similarly when the model makes a negative prediction.

#### Confusion Matrix

We often place True positive, True negative, False positive and false negative in a grid.

By doing this we get a **confusion matrix**

Each square in the matrix is a placeholder for a value.

So the values are not related to any of the classes in the model.

Using this matrix can allow us to use new measurements that overcome the previous problem.

We can do this by asking 2 related questions about model performance:

* **Recall** - "What percentave of these positives was the model able to correctly identify". True Positives / Total number of positives
* **Precision** - "What percentage of these predictions were actually positive?". True Positives / Number of classified as positive

These questions give you the number of positive datapoints it was able to recall, and how precise were the actual predictions. 

Recall and precision are defined for the negative as well.

#### Going back for example

If we take our model that just gave a negative diagnose, our model had a **recall of 0**, because it failed to identify any patients with a positive diagnosis.

#### Example 3

Consider a model that examines a pool of applicants from a top 5 business school, and determines who to accept.

We will say that accepting a student is a positive, and rejecting is negative.

Only the very best will be accepted.

Given the extremely number of false positives, the model would have a **high precision value.**

But there would be a large number of qualified students that will fail, and this will be the false negatives - hence the model would have a **low recall value**

#### Example 4

Let's take a model for a state college, which would be designed a bit differently.

The goal is to accept a much larger set of students.

A few underqualified students will be accepted, so the false positive count will be high, so it would have a **low precision.**

But unlike the other model, very few qualified students will be overlooked. 

So the number of false negatives would be low, so it would have a **high recall.**

## F1 score

We can use hybrid measurements in order to achieve a balance between precision and recall.

Once of these models is the F1 score - it is calculated as the harmonic mean of precision and recall.

This outperforms the standard arithmetic mean in the presence of outliers.

The harmonic mean also offers an improvement when the features have values between 0 and 1. 

This becomes handy in the process of feature scaling.

We can also examine precision and recall graphically by plotting these values and examining the area under the curve.

**The model that maximises this area will typically be the best performing**

## Multi-class classification

We can extend this concepts to classification problems with more than two classes.

This would just need a matrix that is bigger than the usual 2x2 confusion matrix.

The definition for precision and recall remain the same - the only difference is that now a data class **can be misclassified in multiple ways**.

So false positives and false negatives must be summed through all missclassification pairs. 

So for multiclass classification:

* Precision - The number of true positives over all points classified positive
* Recall - The ratio of number of true positives over number of all positives












