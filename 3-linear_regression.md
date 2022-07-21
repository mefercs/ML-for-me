- `Root Squared Error`: The squared root of Mean Squared Error
When our model it getting flatten out near to zero, in the loss curve, that means our model is `converged`.
<img src="https://developers.google.com/static/machine-learning/glossary/images/LossCurve.svg" width="400">


`An oscilating loss curve strongly suggest the learning rate(step size) is too high.`
- An iteration completes in the span where one batch is completed. After each iteration, the system recalculates the model's loss and adjust the model's weights and bias.
- Ex. a batch of 6, every 6 examples represents 1 iteration, and that's where the system recalculates and adjust values.
One epoch spans sufficient iterations to process every example in the dataset. For example, if the batch size is 12, then each epoch lasts one iteration. However, if the batch size is 6, then each epoch consumes two iterations.

### Gold rules to create a good model

- Training loss should steadily decrease, steeply at first, and then more slowly until the slope of the curve reaches or approaches zero.
- If the training loss does not converge, train for more epochs.
- If the training loss decreases too slowly, increase the learning rate. Note that setting the learning rate too high may also prevent training loss from converging.
- If the training loss varies wildly (that is, the training loss jumps around), decrease the learning rate.
- Lowering the learning rate while increasing the number of epochs or the batch size is often a good combination.
- Setting the batch size to a very small batch number can also cause instability. First, try large batch size values. Then, decrease the batch size until you see degradation.
- For real-world datasets consisting of a very large number of examples, the entire dataset might not fit into memory. In such cases, you'll need to reduce the batch size to enable a batch to fit into memory.

# IN A REAL DATA SET
- Datasets are often stored on disk or at a URL in .csv format.
Sometimes is useful to scale the data, which is the pre process that suffer the data, before it's treated (*Don't search analized :'(* )
- To analized in a fast way our data, use `df.describe()` method from pandas API.
- Quantile : Each bucket in a quantile bucketing.
- Quantile bucketing : Is the features distribution withing buckets, the next example have 4 buckets. They serve to expect some "behaviour". We need to avoid columns with these anomalies or at least be more careful.

<img src="https://developers.google.com/static/machine-learning/glossary/images/QuantileBucketing.svg"  width="400">

- Also remember to select the correct features that correlate the label.
- In **practice** we should make predictions that are not used in training.
- Synthetic feature : a feature not present among the input features, and it could be created scalling or combining other features.
- `training_df.corr()` produces correlations where: 
  * 1.0 : Perfect positive correlation, when 1 attribute rises, the other attribute rises.
  * 0.0 : No correlation.
  * -1.0: Perfect negative correlation, when 1 attribute rises, the other attribute falls.
In general, when a higher absolute value, the greater is the predictive power. But correlation don't tell the entire story.
