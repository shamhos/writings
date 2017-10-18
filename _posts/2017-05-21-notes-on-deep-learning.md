---
layout: post
title:  "Notes on deep learning"
date:   2017-05-21 12:46:38 -0500
categories: datasci
---
This is an agglomeration of my notes from various resources on the subject of deep learning and neural networks, which I will be using in my research this summer. Some of the primary sources used are DataCamp courses. 

Introduction 

- Deep learning is used for high-dimensional datasets in which the variables often interact with one another. Deep learning uses neural networks that account for these interactions by detecting these relationships.
- Neural networks take variables that interact and calculate a function of those variables that accounts for their interaction, and use this to predict the outcome. 
- Multi-layer perception structure for neural network: input layer (variables/features) and output layers, and all non-input or non-output layers are called hidden layers. These are not observed directly from the real world. Each node in the hidden layer is an aggregation of information from the input data. Each node adds to the model’s ability to capture interactions by "distilling"- they detect the useful, deterministic patterns from the inputs and passes these on to the next later, removing redundant information 


![network structure](img https://static.wixstatic.com/media/f0c89a_4662ef36f1ab44ac9e8675c4c37aa3e4~mv2.png/v1/fill/w_630,h_353,al_c,lg_1/f0c89a_4662ef36f1ab44ac9e8675c4c37aa3e4~mv2.png"Network Structure")


Process

- Inputs have an assigned weight, a measure of their importance. 
- An activation function at each node captures a non-linear relationship between the inputs, and converts the inputs into a more useful output.
- Ex: Sigmoid activation function creates an output with values between 0 and 1. There can be other activation functions like Tanh, softmax and RELU.
- In a feed-forward network, input signals flow from first inputs to final outputs. Feedback/Recurrent networks have signals flowing from both directions. 
- The way neural networks become good models for predictions is by tuning these weights, acquiring optimal parameter values that minimize the error in approximating a final solution. 
- Ex: Using supervised train-test split, we can train the weights. We can also use Back-Propogation learning algorithms to adjust the weights based on the errors from the network. The most common method of back-propogation uses gradient descent to find the parameter that produces the least error. 

Advantages of Neural Networks 

- Are able to capture and model non-linear, complex relationships
- After learning relationships in learned data, can infer relationships between inputs in unseen data 
- Neural networks are great for data with high heteroskedasticity, or data with sub-populations that have different variabilities (variance or statistical dispersion) than other sub-populations. They don't impose restrictions on input variables and thus are suitable for modeling data with high data volatility, like stock prices. 
- Since neural networks can take in a lot of inputs and infer non-linear relationships, they're great for image processing and computer vision. 
- Forecasting applications are also viable because of detection of unseen factors and the non-restrictive manner in which neural networks process inputs. Long short-term memory networks and Recurrent Neural Networks are especially of interest in the field of finance and forecasting. 


Convolutional Neural Networks for Image Recognition

Key Terms

- CNN- feed-forward artificial neural networks that consist of an input and output layer and hidden layers that convolutional, pooling, or fully connected. 
- Convolution operation: a function derived from two given functions by integration that expresses how the shape of one is modified by the other.
- Convolutional layer: apply convolution operation to the input, passing the result into the next layer, approximates the response of an individual neuron to visual stimuli. This operation is meant to reduce the number of free parameters to improve generalizations. 
- Pooling layer: Can be included as local or global pooling layers, combining the outputs of neuron clusters in one layer into one single neuron in the next layer. Ex: Max pooling uses the the maximum value from each cluster of neurons in the previous layer. 
- Fully connected layer: connect every neuron in one layer to every neuron in another layer. 
- Feature Extraction: technique used to determine the most "important" parts of an image 
- Kernel (image processing): small matrix used to apply effects (blurring, sharpening, etc.)

Introduction 

- In essence, CNNs can be thought of as a kind of neural network that uses many identical copies of the same neuron. With more neurons, the model is able to express computationally large models while keeping the number of paramaters that need to be learned small. 
- Similar to the way we modularize code by writing functions, we can "modularize" a neuron by using it in many places after we have learned it once. 

Process 

- The simplest way to classify data with a neural network is to connect every single input with a fully connected layer 
- But in order to examine certain properties that are localized to a piece of the data, for example, the frequency for sound data, we create a group of neurons A, that will look at small segments of the data. Forming a convolutional layer, we are iterating over all such segments and computing certain features, ultimately producing outputs that are fed into a fully-connected layer F. A convolutional layer has "window", the interval or number of data points that the neuron group A is evaluating. 
- Convolutional layers can be stacked upon each other, as outputs of one can be inputs for another. The more layers you have, the network can detect more abstract features. 
- So a new group of neurons, B, can be used to form another convolutional layer on top of A's convolutional layer. Sometimes, convolutional layers can be interweaved with pooling layers (max pooling, etc.). Max pooling takes the maximum value of a particular block- helps remove effect of small transformations in the data. 

- For deep learning on images, we use a 2-dimensional convolutional neural network, in which our neuron clusters will now look at patches of the image to create features for each. This can be edge, color, or texture detection. 



Resources 
1. https://www.deeplearningtrack.com/single-post/2017/07/09/Introduction-to-NEURAL-NETWORKS-Advantages-and-Applications
2. https://en.wikipedia.org/wiki/Convolutional_neural_network
