`Activation functions` are used in artificial neural networks to introduce non-linearity in the output of each neuron. 
In simple terms, activation functions determine the output of a [`neuron`]() given an input or set of inputs. 
Without activation functions, the output of each neuron would be a simple linear function of its inputs,
making it difficult to model complex relationships between inputs and outputs in a neural network. 
By introducing non-linearity through activation functions, neural networks are able to model complex, 
non-linear relationships between inputs and outputs, making them more powerful and versatile for a wide range of tasks.


### Relu function

The relu (rectified linear unit) function is a commonly used activation function in neural network models. 
It returns the input x if x is positive, and returns 0 if x is negative. This function introduces non-linearity in 
the model, which allows the model to learn complex representations of the input data.


### Leaky_relu function

The `leaky_relu function` is a type of `activation function` used in neural networks. 
It is similar to the traditional ReLU activation function but with a slight difference -
instead of setting the value of a negative input to zero, the leaky_relu function sets it to a small negative value
(0.1 times the input, in this case). This helps in avoiding the "dying ReLU" problem, 
where a large number of neurons can become "dead" during training and stop providing any meaningful contribution 
to the model's predictions.


### Why we used relu and leaky_relu function here

The activation functions in neural networks are used to introduce non-linearity into the output of each layer. 
They transform the input signal into an output signal and the activation function decides whether a neuron should 
be activated or not. ReLU and leaky ReLU are commonly used activation functions in neural networks as they have some 
desirable mathematical properties and have been found to work well in practice for many tasks.

ReLU (rectified linear unit) function sets all negative values to 0 and all positive values unchanged, resulting in 
sparse activations and reducing the computational cost. However, the standard ReLU function has a drawback of the
"dying ReLU problem," where a neuron can get stuck in the "dead" state with output 0 if it experiences negative inputs.
To address this, the leaky ReLU function allows small negative values to "leak" through, rather than being set to 0.