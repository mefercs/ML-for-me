---
# GOOGLE MACHINE LEARNING COURSE
---
[comment]: <> (-:red , +:green, !:orange, #:gray, @@:purple,  in the diff language)
[comment]: <> ( <details><summary>title</summary> content</details> )
<details>
<summary>
</summary>
</details>

## Introduction

- *Label*: Variable we're trying to predict - Y. 
- *Features*: Input variables describing our data - X.
- *Labeled Example*: We have  both {Features,Labels} : (x,y). They're used to train the model
- *Unlabeled example*: We have feature information, but we don't know the label, {features,?}:(x,?). Labels we want to predict.
- *Model*: Something that predicts labels: y', defined by internal features and labels.
- *Training*: Create or learning model.

### Regression vs classification 
- `Regression:` Predict continous values.
- `Classification:` Classifies
- `Loss:` Also called squared error. (y - y')^2, also know as L_2loss
```diff
+ y' = b + w1x1
```
By convention this is the machine learning way to write the slope equation where
1. y':Predicted label, output.
2. b:bias, y-intercept or sometimes write as  w0
3. w1: weight(ML)/slope(normal) of feature 1.
4. x1: is a feature/input.
 
**Empirical Risk Minimization**:
The process to learning/create the best values for the weights and bias of our model. To minimize the loss. Because loss describe how bad our model was on a single example.

#### Mean square Error (MSE) Error/Loss
- Loss : The difference between the label and the prediction, more loss, a worse model, less loss, a better model.
- L_2Loss : is the Squared loss
- L_1Loss : also called normally loss, is the absolute difference between a label and a prediction.
- Root mean squeare error: Squared root of the MSE.
- Loss curve : A graph of loss as a function of training iterations.
![MSE](https://imgs.search.brave.com/1FQng1R8dmjhaCgrW-I-kqq-NA7MJn7NKxrmOuq398Q/rs:fit:1728:225:1/g:ce/aHR0cHM6Ly90c2Uz/Lm1tLmJpbmcubmV0/L3RoP2lkPU9JUC4z/Vkp5ZlUxcUJxb0h3/YURKbTNLQUtBSGFD/QyZwaWQ9QXBp)


- Mean squeare Error : *Average *squared loss per example over the whole data set. Is calculated by dividing the squared loss by the number of examples.
- D = data set containing many labeled examples, which are ( x , y ) pairs.
- N = Number of examples in D.

Tensor flow call it Test loss and Training loss.

---
## Reducing loss
One way is the compute the **gradient** which is the derivate of the loss function with respect to the model parameters. 
And later we are taking small steps until we reduce the loss, because the gradient tell us how the loss changes. 
We call this **Gradient steps** even though, they are really negative gradient steps. 
But the technic is called **GRADIENT DESCENT**, and remember the negative gradient tell us in which direction update the model.
Here the initial value matters, because the Nearul networks are not always convex. Remember the `loss function`.
- Stochastic Gradient Descent: One example at a time
- Mini-Batch Gradient Descent: Bathes of 10-1000
  - Loss & gradiens are average over the batch10-1000
We say the model have been **CONVERGED** when the model discover the parameters that produces the lowest possible loss.
### Convex problems
These problems have exactly one point where the loss is 0, because is a convex function and that means the model converges.
### Learning rate
It's a scalar, sometimes called **step size**, that multiplies the gradient vector which has both direction and magnitude to determine the next point.
- **Hyperparameters**: The **knobs** that tweak the ML algorithms.
#### Reducing loss with Stochastic Gradient Descent (SGD)
Uses a single example( bath size of 1 ) per iteration.
The SGD works but is very noisy.
#### Reducing loss with Mini-Batch Stochastic Gradien Descent (mini-bacth SGD):
Even that could result noisy, is better than SGD and Full-batch SGD. 


`Epoch:`Is a Hyperparameter that tell us the complete passes through the training set.
It's between full-batch iteration and SGD, it uses bathches of 10-1000 stochastic examples.
Reduces the amount of noise, but it's still more efficient that SGD and full-batch. Stochastic: Ramdom value.
`noise:`How many times the model is going to see the same data.

