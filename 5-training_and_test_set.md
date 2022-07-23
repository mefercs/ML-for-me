# Training data sets

If we have only a data set, we can trim it, trying to give a larger set to train the data, and a smaller to the test set.
<img src="https://developers.google.com/static/machine-learning/crash-course/images/PartitionTwoSets.svg?hl=es-419">

* Training set: Is large enough to produce statically meaninful results and is representative for the whole set.
* **REMEMBER** if you are getting perfect result, probably you mix the test data. It's not a very good signal. This could happen because there are duplicated information.

#### Consider
- Divide into two sets:
  - training set
  - test set
Classic gotcha: do not train on test data
  - Getting surprisingly low loss?
  - Before celebrating, check if you're accidentally training on test data
