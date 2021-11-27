## Deep learning 101

AI and Machine learning is the trendy topic now-a-days and there's another trendy term called "Deep learning". In this article we'll be covering All about deep learning, and how it works behind the scenes. Let's start!

Deep learning is a small part of machine learning that uses various algorithm inspired by the human nervous system, which makes us able to think, and work. It also implements the functioning like it. Deep learning algorithms work just like our nervous system enabling the computer to think, take decisions, and pass the information. Just like brain, these work in network, as the term **neural network** suggests.

Here's a basic structure, how the networks are structured:

![0*_SH7tsNDTkGXWtZb.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1611848750350/k2cju9zc1.png)

#### Now, how does the layer work?

Here, the first layer takes in the data input fed into it for learning. Then it forms the hidden neurons, that take care of various things, like:
- Pre-processing
- Feature identification
- Prediction

They are the part of the abstraction provided by any neural network. It performs all the computation for data passed from input, and passes the result to output layer.

And once it gets a prediction it reached, it displays it through one of the categories / the output layers.

Now let's cover neural network in a nutshell.

## Activation functions

It's a special function in neural network, which decides if a neuron / node in the network must be activated and passed in the data for calculation. It's introduced for non-linearity in the output. It's the activation function, which ultimately decides the output through the data passed, and filtered.
We indirectly refer the crude output from network as activation.

One of the popular activation function is sigmoid function.

Here's the equation

![Screenshot from 2021-01-29 14-07-34.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1611909469088/-Zyr9tSY3.png)

It is usually used in output layer of a binary classification, where result is either 0 or 1, as value for sigmoid function lies between 0 and 1 only so, result can be predicted easily to be 1 if value is greater than 0.5 and 0 otherwise.

## Bias

Bias is the an important component in a neural network, which helps form the predictions for the neural network trained for a certain goal.

It allows the activation function, like sigmoid, relu and others to be shifted left or right depending on the best fit for the data. It can be linear, curved, and even a squiggly line. It also affects the weights to improve the prediction one by one per epoch. Bias influences the output values a lot without interacting with the actual input data.

The output of the network is computed by multiplying the input (x) by the weight (w0) and passing the result through some kind of activation function (e.g. a sigmoid function.)

## Weights

It's a parameter element in deep learning, especially neural networks that transforms input data working along with bias, in the network's hidden layers, where most of the processing is done.

Each neural network node consists of processed input, bias and weight.

As the input is passed, it uses the following formula to calculate the next value: `input * weight + bias`
and the resulting output is either observed, or passed to the next layer in the neural network. Often the weights of a neural network are contained with in the hidden layers of the network.

![Screenshot from 2021-02-26 17-36-07.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1614341179642/4BWmZi0hy.png)

In simple words, Weights control the connections between two neurons.  A weight decides how much influence the input will have on the output.

I hope this was informative about how things work and predict behind the scenes.

You have reached the end. Thank you so much for reading! 👋 Let me know what you think of this blog! 👀

**Let's connect** 🌟

→ [Twitter](https://twitter.com/janaSunrise)

→ [Github](https://github.com/janaSunrise)

Catch you next time ✨
