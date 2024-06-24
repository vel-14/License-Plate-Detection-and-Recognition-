# License-Plate-Detection-and-Recognition-

## Overview

This project aims to detect and recognize vehicle license plates from images using YOLOv8 for detection and CRNN (Convolutional Recurrent Neural Network) for character recognition. The dataset consists of annotated vehicle and license plate images organized into training and test sets.

## Dataset

The dataset is structured into three sets:

### Training Set 1: 
900 vehicle images with annotated bounding boxes around license plates.
### Training Set 2: 
900 isolated license plate images with annotated alphanumeric characters.
### Test Set: 
201 images for evaluating both license plate detection and character recognition.

## Models Used

### YOLOv8: 
YOLOv8 is an object detection model known for its speed and accuracy in detecting objects like license plates within images. It utilizes a deep convolutional neural network (CNN) architecture with multiple layers of feature extraction and prediction.

#### Architecture:

YOLOv8 consists of a backbone network (such as Darknet-53) followed by detection layers.
The detection layers predict bounding boxes and class probabilities directly from full images in a single evaluation.

### CRNN: 
CRNN combines convolutional layers for feature extraction and recurrent layers for sequence modeling. It is used for recognizing  characters from license plates.

### Architecture:

CNN Layers: Extract features from input license plate images.
RNN Layers: Process the sequential nature of character recognition.
Connection: Combines CNN and RNN to recognize sequences of characters.

## Preprocessing

### Image preprocessing: 
Convert license plate images to grayscale and resize to a fixed height while maintaining aspect ratio.
### Normalization: 
Normalize pixel values to enhance model performance.

## Training 
YOLOv8 nano model is fine tuned with training set 1
CRNN model is trained with training set 2

## Evaluation
Fine tuned YOLOv8 model detects the license plate in the given image. The detected licens plates are cropped and feed to the CRNN model.
Then CRNN model perform character recognition on license plates.

### Evaluatiion for character recognition:
Accuracy: 0.8567
Precision: 0.8606
Recall: 0.8567
F1 Score: 0.8566
