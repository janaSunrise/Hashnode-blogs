## Supervised learning and about it

## So, what is supervised learning?

Supervised learning is a way of teaching the machine learning based on labelled data, like if a patient has a certain disease or not, then making it predict the labels for unseen data.
A supervised learning algorithm analyzes the training data gathers knowledge about it, and finds the patterns between the various data points, which can be used for mapping new examples. In an hypothetical situation will allow for the algorithm to correctly determine the class labels for unseen instances or the test data fed into it.

### Ah and how does it work?

For example, let's say, I have `n` columns of data, with a label for each, Where, `X` and `Y` columns are orders from `X1` and `Y1` to `Xn` to `Yn`, where `X` is the data list, which can be a single or multiple value(s) with it's paired column `Y` containing the data's label to be predicted.

### How is it represented in ML-based terms?

Now in ML terminologies, Values used for training without labels or `X` is / are called predictor variables, which is used to teach the machine and Y is called the target variable, which is supposed to predicted by machine.

### Well, Here are the types of supervised learning

There are 2 types of supervised learning.

- Classification

In this format, the labels are of a certain number of groups and have finite possibilities, like if an email is spam or not, or if a drawn digit is anything between 0 and 9. The categories can be 2 or more, but finite.

Here's an example of binary classification (consisting of 2 classes):

![EpqeOGQVEAYzP8X.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1610035387572/wEAqPN21i.png)

And here's another example of multiclass classification (consisting of more than 2 classes):

![EpqeOGPU0AAk9YI.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1610035422461/s-hAaIh0K.png)

- Regression

Unlike classification, regression is a statistical form of calculation, where the target variable can be anything, not just finite. It even might not belong to any range too.
Like if we want to calculate the stock price, we need a certain algorithm to find it.

We just cannot tell the price by just looking, we need to consider every factor, and here the target value is a continuous value since it can be anything.

Here's the formulae behind the maths of regression:

![EpqfYRyVoAIxRpZ.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1610035514367/bWzidWa8l.png)

Now it's time to end this quickbite :) Hope you enjoyed it!

Have a great day or an evening ahead!
