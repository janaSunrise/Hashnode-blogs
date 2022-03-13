## Deep learning 101

# What on earth is deep learning?

Artificial and machine learning are what's trending right now. Along with that, Deep learning is also what's gaining a lot of traction. We'll learn all about deep learning and behind-the-scenes in this articles. Let's start.

Deep learning is a subset of machine learning inspired from the Human nervous system, and uses them to function, and work to find efficient solutions to complex problems that Machine learning couldn't.

The functioning is completely inspired from our nervous system, and this enables the computer so think (some sort of!), make decisions predictions and pass information. This is termed as "neural network".

Here's an image to show how the networks are structured.

![0*_SH7tsNDTkGXWtZb.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1611848750350/k2cju9zc1.png)

## How do layers work in deep learning?

Layers are the way how neurons are connected in our brain. They form a sequence, not necessarily linear, but can be concatenated with each other forming a lot of connections with each other, based on position and tasks assigned.

Likewise, the first layer here takes in the data fed into it for learning. The final layer gives out the data. And, what remains in the middle are the neurons that take care of processing data, figuring out patterns and enhancing the predictions on the way.

Several tasks are performed in the neurons in the middle. Such as:
- Preprocessing
- Feature identification
- Enhancements in prediction

They are the part of the abstraction provided by any neural network. It performs all the computation for data passed from input, and passes the result to output layer.

And, finally, once it reaches a specific prediction, it emits that through the final layer, i.e. output layer(s).

Now let's cover neural network in a nutshell.

## Activation functions

It's a special function in neural network, which decides if a neuron / node in the network must be activated and passed in the data for calculation. It's introduced for non-linearity in the output. It's the activation function, which ultimately decides the output through the data passed, and filtered.
We indirectly refer the crude output from network as activation.

One of the popular activation function is ReLU function. It always lies above 0.

Here's the equation.

![image.png](https://cdn.hashnode.com/res/hashnode/image/upload/v1647165055726/q-VvZDwnv.png)

This is used in the middle layers that will output the input directly if it is positive, otherwise, it will output zero. As the function shows (`f(x) = max(0, x)`), The value never goes below in negative, and always stays as >= 0.

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
