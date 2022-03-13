## Let's explore linear regression!

## What is linear regression?

Linear regression was created in the field of statistics. It's studied as a model for understanding the relationship between input and target continuous variables, but has been borrowed by machine learning. It is both a statistical algorithm and a machine learning algorithm.

Linear regression is a linear model, like, a model that assumes a linear relationship between the input variables X and the single output variable y. More specifically, that y can be calculated from a linear combination of the input variables X.

## How is it computed?

A simple regression problem (using a single `x` and `y`), the form of the model would be:

`y = mx + b`, where `x` and `y` are the variables on the line, `m` is the slope of the line, `b` is the y-intercept.

In higher dimensions when we have more than one input x, the line is called a plane or a hyper-plane.

Linear regression is one of the most popular, due to it's simplicity and one of the base algorithms that people learn initially when starting out with ML. Machine learning, is simply fascinating.

## Ordinary least squares loss function

Ordinary least squares or OLS is a loss function to calculate the errors while predicting and utilizing the algorithms to become accurate more.

The Ordinary Least Squares is a procedure that seeks to minimize the sum of the squared residuals.

This means that given a line through the data we get the distance from each point to the line, squaring it, and get the sum of squared errors together.

The OLS estimator is pretty popular and used more in regression rather than classificaion. They have the Gauss Markov theorem, where it's pretty optimal to generate unbiased predictions when errors are uncorrelated. The method of OLS provides minimum-variance mean-unbiased estimation when the errors have finite variances.

## Gradient descent

When there are one or more inputs you can use a process of optimizing the values of the coefficients by iteratively minimizing the error of the model on your training data.

This operation is called Gradient Descent and works with random values for each coefficient.

## Regularized LIN regression

- Lasso Regression, where OLS (Ordinary least squares) is modified to also minimize the absolute sum of the coefficients (called L1 regularization).

- Ridge Regression, where OLS (Ordinary least squares) is modified to also minimize the squared absolute sum of the coefficients (called L2 regularization).

Hope this was an awesome knowledge hunt on linear regression. You have reached the end. Thank you so much for reading! 👋 Let me know what you think of this blog! 👀

Let's connect 🌟

→ [Twitter](https://twitter.com/janaSunrise)

→ [Github](https://github.com/janaSunrise)

Catch you next time ✨