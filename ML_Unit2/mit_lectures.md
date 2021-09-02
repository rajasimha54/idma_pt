# Lecture 5 Linear Regression

## Introduction

- Classification can't handle every problem e.g. predicting continuous values
- Regression specification:
    - data : $\{x^i,y^i\} $, $y \in R$
    - model : $f(x, \theta_{1}, \theta_{0}) =  \sum_{t=1}^{n} \theta_{1}X_{t}+\theta_{0}$ 
    - Non linearity is handled using feature transforms (Kernel methods etc)

## Empirical Risk:
- $R_{n}(\theta) = \frac{1}{n}\sum_{t=1}^{n}Loss(y^t-\theta.x^t) $
- loss: MSE $\frac{1}{2n}\sum_{t=1}^{n}(y^t - (\theta_{1}X^t + \theta_{0}))^2$
- This loss makes sure that small deviations are not penalized as much as larger deviations from actual and predicted values

**Problem Ideas** 
- Numeric computation of loss given predicted vs actual
- Numeric computation of loss given $\theta$, $X$ and $Y$
- Comparison of loss when hinge loss or mse definition is used

## Gradient Based Approach:
- Gradient of MSE for a single example: $-(y^t-\theta_{1}.x^t).x^t$

**Problem Ideas**
- Recall the gradient descent on a simple function such as ```math 
$f(\theta) = 2.\theta - \theta^2$
```
- Show one iteration by hand
- Create dummy data and run 2 iterations by hand, focus on random selection of a single data point $(x^t,y^t)$
- Attempt to give intuition of a random batch update


## Closed form solution

**Content pointers**
- Find all possible variations of closed form derivation
- Attempt to give a general rule to create vectorized expressions

## Generalization and regularization

**Content Pointers**
- Use the graph where underlying data comes from a linear function with some noise added and argue that minimizing loss purely for training data will lead to learning random noise as well hence regularization is a good way to counter this.

## Regularization

**Content Pointers**
- Correlate the formulation with the data having trend+random noise, show effect of lambda on the parameter estimate
- Correlate the same idea with a sales example over years.
- Working example on creating a closed form solution with regularization as well as a gradient based solution.
