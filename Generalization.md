# Generalization

Model needs to be as simple as possible
* Ockham's Razor principle:
  - The less complex a model is, the more likely that good empirical  result is not just due to the peculiarities of our sample.
* Empirically:
  - Asking: Will our model do well on a new sample data?
  - Evaluate: Get a new sample of data - call it the test. 
  - Good performance on the test is indicator of a good performance on the new data in general:
    - If the test is large enough.
    - If we don't cheat by using the test set over and over.

<img src="https://developers.google.com/static/machine-learning/crash-course/images/BigPicture.svg?hl=es-419">

#### Three basic assumptions in all of the above: 
1. We draw examples **independent and identically (i.i.d.)** at random from the distribution.
2. The distribution is **stationary**: It doesn't change over the time.
3. We always pull from the **same distribution**: That includes training, validation and test sets.

With that on mind we need to take care of our metrics, because these assumptions are often violated.

- And also, remember, don't over-fit your model, this could result in "bad predictions", because in that cases we don't have like a "tolerance".

---

A good low loss model in training tends to produce a poor job predicting new data, and overfitting is produced by making a model more complex than necessary.

- The fundamental tension of machine learning is between fitting our data well, but also fitting the data as simply as possible.
* Generalization bounds: A statistical description of model's ability to generalize to new data based on:
  - The complexity of the model.
  - The model's performance on training data.
---
Generalization is more about to give a model tolerance to new unseen-data.


Our last thing what training and test set (25 min)
