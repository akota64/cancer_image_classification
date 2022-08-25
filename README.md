# Cancer Image Classification

## Overview
This project uses convolutional neural networks (CNNs or ConvNets) to classify a set of histopathological images known as [LC25000](https://arxiv.org/abs/1912.12142). In its current state, the model implements a simple CNN based on the standard LeNet-5 architecture, using a few stacks of Conv2D and Max Pooling layers, followed by some fully connected (Dense) layers to combine the processes and generate a final, softmax-based prediction. The model is currently trained only on lung tissue images, and only generates predictions for these data. Future implementations will extend the process to colon tissue data, and experiment with other architectures, such as Inception-v3 and ResNet, using the advent of transfer learning. 

## Dataset Information
The LC25000 dataset includes images of lung tissue under 3 classes (benign, squamous cell carcinoma, lung adenocarcinoma) and colon tissue under 2 classes (benign, colon adenocarcinoma). The images are already appropriately scaled and have been specifically prepared for use by ML/DL/AI scientists. This has made life very easy, but has taken from the experience of struggling with the data.  
  
## Current State
The project currently uses the following CNN architecture:

- Conv2D Layer: 8 filters of 4 x 4 dimension
- ReLU Activation
- MaxPool2D Layer: 8 x 8 pool, with stride of 8
- Conv2D Layer: 16 filters of 2 x 2 dimension
- ReLU Activation
- MaxPool2D Layer: 4 x 4 pool, with stride of 4
- Fully Connected Layer (after flattening output from previous layer): Generates final output of 3 probabilities

The model has only been trained thus far on lung tissue data.
