# DeepLearning

Deep Learning is the most exciting and powerful branch of Machine Learning. It's a technique that teaches computers to do what comes naturally to humans: learn by example. Deep learning is a key technology behind driverless cars, enabling them to recognize a stop sign or to distinguish a pedestrian from a lamppost. It is the key to voice control in consumer devices like phones, tablets, TVs, and hands-free speakers. Deep learning is getting lots of attention lately and for good reason. It’s achieving results that were not possible before.

In deep learning, a computer model learns to perform classification tasks directly from images, text, or sound. Deep learning models can achieve state-of-the-art accuracy, sometimes exceeding human-level performance. Models are trained by using a large set of labeled data and neural network architectures that contain many layers.

Deep Learning models can be used for a variety of complex tasks:
- Artificial Neural Networks(ANN) for Regression and classification
- Convolutional Neural Networks(CNN) for Computer Vision
- Recurrent Neural Networks(RNN) for Time Series analysis
- Self-organizing maps for Feature extraction
- Deep Boltzmann machines for Recommendation systems
- Auto Encoders for Recommendation systems

# Neurons

Biological Neurons (also called nerve cells) or simply neurons are the fundamental units of the brain and nervous system, the cells responsible for receiving sensory input from the external world via dendrites, process it and gives the output through Axons.

<p align="center">
  <img src="https://miro.medium.com/max/585/0*EqHnlkHI-Ny_O5VH.png" title="Neuron">
</p>

**Cell body (Soma):** The body of the neuron cell contains the nucleus and carries out biochemical transformation necessary to the life of neurons.

**Dendrites:** Each neuron has fine, hair-like tubular structures (extensions) around it. They branch out into a tree around the cell body. They accept incoming signals.

**Axon:** It is a long, thin, tubular structure that works like a transmission line.

**Synapse:** Neurons are connected to one another in a complex spatial arrangement. When axon reaches its final destination it branches again called terminal arborization. At the end of the axon are highly complex and specialized structures called synapses. The connection between two neurons takes place at these synapses.
Dendrites receive input through the synapses of other neurons. The soma processes these incoming signals over time and converts that processed value into an output, which is sent out to other neurons through the axon and the synapses.

The following diagram represents the general model of ANN which is inspired by a biological neuron. It is also called Perceptron.
A single layer neural network is called a Perceptron. It gives a single output.

<p align="center">
  <img src="https://miro.medium.com/max/1275/0*2AMCbOiRQfpOmmkn.png" title="Perceptron">
</p>

In the above figure, for one single observation, x0, x1, x2, x3...x(n) represents various inputs(independent variables) to the network. Each of these inputs is multiplied by a connection weight or synapse. The weights are represented as w0, w1, w2, w3….w(n) . Weight shows the strength of a particular node.

b is a bias value. A bias value allows you to shift the activation function up or down.
In the simplest case, these products are summed, fed to a transfer function (activation function) to generate a result, and this result is sent as output.

Mathematically, x1.w1 + x2.w2 + x3.w3 ...... xn.wn = ∑ xi.wi

Now activation function is applied 𝜙(∑ xi.wi)

# Activation function

The Activation function is important for an ANN to learn and make sense of something really complicated. Their main purpose is to convert an input signal of a node in an ANN to an output signal. This output signal is used as input to the next layer in the stack.


***Activation function decides whether a neuron should be activated or not by calculating the weighted sum and further adding bias to it. The motive is to introduce non-linearity into the output of a neuron.***


If we do not apply activation function then the output signal would be simply linear function(one-degree polynomial). Now, a linear function is easy to solve but they are limited in their complexity, have less power. Without activation function, our model cannot learn and model complicated data such as images, videos, audio, speech, etc.

# Types of Activation Functions:

### Threshold Activation Function — (Binary step function)

A Binary step function is a threshold-based activation function. If the input value is above or below a certain threshold, the neuron is activated and sends exactly the same signal to the next layer.

<p align="center">
  <img src="https://miro.medium.com/max/689/0*U0N4CpMEpq1Suwxq.png" title="Threshold Activation Function">
</p>

Activation function A = “activated” if Y > threshold

else not or A=1 if y>threshold 0 otherwise.

The problem with this function is for creating a binary classifier ( 1 or 0), but if you want multiple such neurons to be connected to bring in more classes, Class1, Class2, Class3, etc. In this case, all neurons will give 1, so we cannot decide.

### Sigmoid Activation Function — (Logistic function)

A Sigmoid function is a mathematical function having a characteristic “S”-shaped curve or sigmoid curve which ranges between 0 and 1, therefore it is used for models where we need to predict the probability as an output.

<p align="center">
  <img src="https://miro.medium.com/max/728/0*Q8OJJc7t3VRofJxu.png" title="Sigmoid Activation Function">
</p>

The Sigmoid function is differentiable, means we can find the slope of the curve at any 2 points.
The drawback of the Sigmoid activation function is that it can cause the neural network to get stuck at training time if strong negative input is provided.

### Hyperbolic Tangent Function — (tanh)

It is similar to Sigmoid but better in performance. It is nonlinear in nature, so great we can stack layers. The function ranges between (-1,1).

<p align="center">
  <img src="https://miro.medium.com/max/665/0*dnH9K_K4tlkNWz-p.png" title="Hyperbolic tangent function">
</p>

The main advantage of this function is that strong negative inputs will be mapped to negative output and only zero-valued inputs are mapped to near-zero outputs.,So less likely to get stuck during training.

### Rectified Linear Units — (ReLu)

ReLu is the most used activation function in CNN and ANN which ranges from zero to infinity.[0,∞)

<p align="center">
  <img src="https://miro.medium.com/max/903/0*9s238ozjLeNyzubR" title="Relu">
</p>

It gives an output ‘x’ if x is positive and 0 otherwise. It looks like having the same problem of linear function as it is linear in the positive axis. Relu is non-linear in nature and a combination of ReLu is also non-linear. In fact, it is a good approximator and any function can be approximated with a combination of Relu.
ReLu is 6 times improved over hyperbolic tangent function.
