# Variational Autoencoder (VAE)

This repository contains code for training a Variational Autoencoder (VAE) to encode images into a normal distribution vector and decode samples from those distributions back into images. The VAE is trained using a dataset of custom images and can generate new images by sampling from the learned distributions.

## Problem Description

The task is to train a VAE to fit data onto a specified number of distributions (4 to 10 distributions) in a latent space. The length of the distribution vector represents the number of dimensions in the latent space (e.g., if the length is 6, each distribution is represented by mean and standard deviation values in a 6-dimensional space). The trained VAE is then used to generate new images by sampling from the learned distributions and decoding those samples.

## Dataset

The dataset used for training the VAE consists of custom images. The dataset contain 400 images, and the image size 256x256x3.

## VAE Training

The VAE is trained using a convolutional neural network (CNN) architecture. The network learns to encode the input images into a latent space representation using convolutional and pooling layers. The latent space is modeled as a normal distribution, and the network learns to encode the mean and standard deviation for each distribution. The network is trained to minimize the reconstruction loss, which measures the similarity between the original image and the reconstructed image generated from the sampled distributions.

## Testing and Generating Images

After training the VAE, you can test the model by providing test images and observing the reconstructed outputs. Additionally, a GUI with a slider is provided to generate new images. The slider allows the user to choose the number of images to generate, ranging from 1 to 12. The image generation process involves sampling from the learned distributions in the latent space and decoding those samples into images.
