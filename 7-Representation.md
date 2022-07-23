# Representation 
A machine learning model can't directly see, hear, or sense input examples. Instead, you must create 
a representation of the data to provide the model with a useful vantage point into the data's key 
qualities. That is, in order to train a model, you must choose the set of features that best represent
the data.
Many machine learning models must represent the features as real-numbered vectors since the feature 
values must be multiplied by the model weights.
- The process of extracting features from raw data is called feature engineering.
  - A common process is one-hand encoding.
  - Another common process is known as `OOV bucket` out-of-vocabulary bucket.Ex. In this casese we need to use a single `weight` in our loss function for all the examples.
    * map Charleston Road to 0
    * map North Shoreline Boulevard to 1
    * map Shorebird Way to 2
    * map Rengstorff Avenue to 3
    * map everything else (OOV) to 4
- `Feature vector` represents features, and it's an ordered list of numerical properties. Because it represents input features.
- ONE-HAND encoding, to represent string features. Useful to create binary vectors. If we use more than 1 value is called multi-hot encoding.
  - one-hand : Ex. [0,0,0,1....0,0]
  - multi-hand: Ex. [0,1,0,0,1....,0,1]
- categorical data : Features having a discrete set of possible values. <a href="https://developers.google.com/machine-learning/glossary?hl=es-419#categorical_data">Info </a>
### Sparce Representation
When have many different options and one/multi-hand encoding is inefficient, we can store only non-zero values.
<img src="https://developers.google.com/static/machine-learning/crash-course/images/RawDataToFeatures4.svg?hl=es-419" alt="one-hand encoding">

## Good feature properties
- Non-zero value.
- They have clear and obvious meanining.
- Don't take "magic" values.
- stationary features : they don't change over the time.
- The distribution should not have extreme outliers.* 
* Avoid rarely used descrite vales : For example a value that appers only 5 times*
Always select features which the model can learn from it.
  - We can mark magic values with another boolean feature value.
* For variables that take a finite set of values (discrete variables), add a new value to the set and use it to signify that the feature value is missing.
* For continuous variables, ensure missing values do not affect the model by using the mean value of the feature's data.
## Binning trick
Group features to generate more correlations, and we then can apply ONE-HAND encoding.
## Know your data

* Visualize: Plot histograms, rank most to least common.
* Debug: Duplicate examples? Missing values? Outliers? Data agrees with dashboards? Training and Validation data similar?
* Monitor: Feature quantiles, number of examples over time?


Last topic cleaning the data.
