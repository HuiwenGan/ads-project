# Identification of Cats and Dogs Project
Team members:He Han, Huiwen Gan
## Abstract
Cats and dogs are very common in our life and they can been found in anywhere. We would like to apply machine learning algorithms like Convolutional Neural Network(CNN) or classification to identify the cats and dogs and we will use these algorithms to accumulate a large amount of data, which will have its own graphical cognitive judgment on both cats and dogs. As a result, it will forming the concept of cats and dogs independently.
## Introduction
#### Motivation
Nowadays the statistics about endangered animals are most manually, for example, we usually count the quantity of endangered animal at a limited area, then we use the quantity to multiply  the total area to get a total data. Considering the different and changing environment, it was time consuming and most are not accurate. Like the technology of identify of cats and dogs, it can be the beginning of the endangered animals protection. We can set cameras at wild area where is not suitable for human observation, the cameras will capture and identify the species automatically, so we can get the data easier and more accurate.
#### Background

#### Algorithms
__We plan to use the algorithms below:__
A Convolutional Neural Network (CNN) is comprised of one or more convolutional layers (often with a subsampling step) and then followed by one or more fully connected layers as in a standard multilayer neural network. We will use CNN to make our images  into 3 dimensions: width, height, depth to make  the architecture in a more sensible way.Then transforms one volume of activations to another through a differentiable function.  VGG-16 model is trained on a subset of the ImageNet database , which is used in the ImageNet Large-Scale Visual Recognition Challenge (ILSVRC). VGG-16 is trained on more than a million images and can classify images into 1000 object categories. We will use the model VGG-16 to make the enough layers. Then we will get the final data to classification.
[CNN ](https://en.wikipedia.org/wiki/Convolutional_neural_network)
[VGG-16](https://gist.github.com/baraldilorenzo/07d7802847aaad0a35d3)
  
## Code with documentation
[I'm an inline-style link](https://www.google.com)
#### Dataset
We use webscraper to get the dataset from PEXELS website. PEXELS consists of documentary-style natural color photos depicting complex, we scraped a set of cats and dogs photographs from this site
## Methods
#### Preprocess
We import the package of OpenCV,use cv2.IMREAD_COLOR  to preprocess the color of our images, resize the size of images to 64*64, create the new label for our dataset and define the label of dogs is 1 and the label of cats is 0.
We check our datasets show the images of them.
## Results
First, we try the model of VGG and we use four convolution filters and activation function is ‘sigmoid’, optimizer is ‘adam’, objective is 'binary_crossentropy'.
We use eight Epochs and the final accuracy is 0.6869.

And then we try more convolution filters, we changed the number from 4 to 8 and use RMSprop as optimizer.
The final accuracy is higher than 4 convolution filters.

 We try to change the pixel from 64*64 to 256*256
 We found the epoch early stop at no.4 epoch.
 The result is not very well.
 
 We change Activation Function from 'relu' to 'sigmoid', then we get a little lower accuracy and costs a little more time.
 We change the optimizer from 'RMSprop' to 'adam', then we find the convergence speed is much slower and the the accuracy is lower.
 
 ## Discussion
The best model we find should be resize the datasets to 64*64,build eight convolution filters with RMSprop as optimizer, binary_crossentropy as objective, sigmoid as activation function.
Next we will try more convolution filters and other kernel_initializer to find if we can increase our accuracy.

