# Deep-Learning-CNN-based-hand-gesture-recognition
This project involves building a 3D Convolutional Neural Network (CNN) to correctly recognize hand gestures by a user to control a smart TV.

The objective of this projects is to build a hand gesture recognition model that can be hosted on a camera installed in a smart TV that can understand 5 gestures. Namely, leftwards hand movement to go to previous channel, rightward hand movement to go to next channel, upward hand movement to increase the volume, downward hand movement to decrease the volume and a palm gesture to pause playing the video.

# Data set
The data set consists of training and test folders. Each of these folders contains sub-folders for each video which is of a few seconds' duration. Each sub-folder for a video consists of 30 frames of the video as images.

# Data pre-processing
A custom data pre-processing fucntion is built to generate the data in which the set of 30 images representing a single video or data point is pre-processed by normalisation, standard scaling etc. Further, a custom number of images from the set of 30 images is selected for training purposes. Further, a batch of images is created in this custom function to be fed into the 3D CNN model as a signle data point.

# Model building
A 3D CNN architecture is built with 4 convolutional layers, each followed by bacth-normalisation, max-pooling layers and dropout layers. In the end, the output of the convolutional layers is flattened and fed into a softmax layer with 5 outputs.

## Model parameters
The model so built is found to have about 9.5 million trainable parameters which is fair enough for a small model that can be hosted on a webcam.

# Model evaluation
The model is trained for 30 epochs and results in accuracy of 76%. This accuracy figure can be significantly improved if training is done for more number of epochs. The number of training epochs was limited to 30 in this implementation due to computational limitations.
