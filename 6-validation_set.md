# Validation 
A possible work flow is: 

<img src="https://developers.google.com/static/machine-learning/crash-course/images/WorkflowWithTestSet.svg?hl=es-419" width="400">

Always trying to don't overfitt pecularities of the test data.
- To avoid that we can create a validation set from the test set.

<img src="https://developers.google.com/static/machine-learning/crash-course/images/WorkflowWithValidationSet.svg?hl=es-419" width="400">

## STUFF
The validation set is gather from the training set.
If we have similar data in the training and the validation set, we'll get similiar loss curves.
If we don't, first try to shuffle the data, maybe something is sorted, or you need to do a data analisis.

RMSE of the examples
test: 230
traning: 233
val: 235

