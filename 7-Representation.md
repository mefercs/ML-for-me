# Representation 
A machine learning model can't directly see, hear, or sense input examples. Instead, you must create 
a representation of the data to provide the model with a useful vantage point into the data's key 
qualities. That is, in order to train a model, you must choose the set of features that best represent
the data.
Many machine learning models must represent the features as real-numbered vectors since the feature 
values must be multiplied by the model weights.
- The process of extracting features from raw data is called feature engineering.
- `Feature vector` represents features, and it's an ordered list of numerical properties. Because it represents input features.
- ONE-HAND encoding, to represent string features.
- categorical data : Features having a discrete set of possible values. <a href="https://developers.google.com/machine-learning/glossary?hl=es-419#categorical_data">Info </a>

<img src="https://developers.google.com/static/machine-learning/crash-course/images/RawDataToFeatures4.svg?hl=es-419" alt="one-hand encoding">

## Good feature properties
- Non-zero value.
- They have clear and obvious meanining.
- Don't take "magic" values.
- stationary features : they don't change over the time.
- The distribution should not have extreme outliers.
## Binning trick
Group features to generate more correlations, and we then can apply ONE-HAND encoding.
## Know your data

* Visualize: Plot histograms, rank most to least common.
* Debug: Duplicate examples? Missing values? Outliers? Data agrees with dashboards? Training and Validation data similar?
* Monitor: Feature quantiles, number of examples over time?
