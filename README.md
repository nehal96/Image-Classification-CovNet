# Image Classification Convolutional Neural Network
Classifying images from the CIFAR-10 dataset using a convolutional neural network

This is Project 2 of Udacity's [Deep Learning Nanodegree Foundation](https://www.udacity.com/course/deep-learning-nanodegree-foundation--nd101) program. The aim of this project is go through the entire process of building a simple convolutional neural network (CNN).

### Files
[Jupyter Notebook](https://github.com/nehal96/Image-Classification-CovNet/blob/master/dlnd_image_classification.ipynb) or [HTML](https://nehal96.github.io/Image-Classification-CovNet/dlnd_image_classification.html)


### Steps

The steps included:
* **Normalizing** data and **one-hot encoding** labels
* Building **TensorFlow Placeholders** for the `input`, `labels` and `dropout`.
* Building a CNN function which does the matrix multiplication with normalized `weights` and `bias`, applies a **rectified linear unit (ReLU)** activation function and finally applies **max pooling**.
* Creating a flatten function that converts the incoming 4-D tensor into a 2-D flattened matrix.
* Creating a **fully connected layer** function in TensorFlow
* Building the **ouput layer**
* Defining the convolutional neural network architecture. This CNN has **4 convolutional layers**, followed by **2 fully connected layers** and finally the **output layer**.
* Setting the number of `epochs`, `batch size` and `dropout` (keep probability) for training on a single batch, and then on all 5 batches.

### CNN Summary

**Layer**          | **Shape** | **Neurons**
------------------ | --------- | -----------
Input              | 32x32x3   | 3072
CNN Layer 1        | 16x16x48  | 12288
CNN Layer 2        | 8x8x192   | 12288
CNN Layer 3        | 4x4x384   | 6144
CNN Layer 4        | 2x2x512   | 2048
Fully Conn Layer 1 | 1x2048    | 512
Fully Conn Layer 2 | 1x512     | 128
Output             | 1x10      | 10

**Training on 1 batch:**
* Epochs: 600
* Batch size: 256
* Keep Probability: 0.5

**Training on all batches:**
* Epochs: 400
* Batch size: 256
* Keep Probability: 0.5

### Results

**Test Accuracy:** 55.55%
