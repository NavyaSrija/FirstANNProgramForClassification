# FirstANNProgramForClassification

Models in Keras are defined as a sequence of layers.

We create a Sequential model and add layers one at a time until we are satisfied with our network architecture.

The first thing to get right is to ensure the input layer has the right number of input features. This can be specified when creating the first layer with the input_dim argument and setting it to 8 for the 8 input variables for this dataset.

How do we know the number of layers and their types?

This is a very hard question. There are heuristics that we can use and often the best network structure is found through a process of trial and error experimentation . Generally, you need a network large enough to capture the structure of the problem.

In this example, we will use a fully-connected network structure with three layers.

Fully connected layers are defined using the Dense class. We can specify the number of neurons or nodes in the layer as the first argument, and specify the activation function using the activation argument.

The activation function is an important part of an artificial neural network. They decide whether a neuron should be activated or not and it is a non-linear transformation that can be done on the input before sending it to the next layer of neurons or finalizing the output.

We will use the rectified linear unit activation function referred to as ReLU on the first two layers and the Sigmoid function in the output layer.

Modern neural network models use non-linear activation functions (eg sigmoid, relu). They allow the model to create complex mappings between the network’s inputs and outputs, such as images, video, audio, and data sets that are non-linear or have high dimensionality.

It used to be the case that Sigmoid and Tanh activation functions were preferred for all layers. These days, better performance is achieved using the ReLU activation function. RELU avoids the vanishing gradient problem. We use a sigmoid on the output layer to ensure our network output is between 0 and 1 and easy to map to either a probability of class 1 or snap to a hard classification of either class with a default threshold of 0.5.

The model expects rows of data with 8 variables (the input_dim=8 argument) The first hidden layer has 12 nodes and uses the relu activation function. The second hidden layer has 8 nodes and uses the relu activation function. The output layer has one node and uses the sigmoid activation function.
