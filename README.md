# Pix2Pix Model for Satellite Images

This repository contains an implementation of the Pix2Pix model, a type of Generative Adversarial Network (GAN), for translating satellite images. The model is designed to convert one type of satellite image to another, utilizing both generator and discriminator networks in a U-Net architecture.

![Image 0](https://github.com/saikatdas3478/pix2pix-satelite-image/blob/main/output.png)

## Table of Contents

- [Introduction](#introduction)
- [Architecture](#architecture)
- [Setup](#setup)
- [Training](#training)
- [Evaluation](#evaluation)
- [Results](#results)

## Introduction

Pix2Pix is an image-to-image translation model that uses conditional GANs to generate images from input images. Developed by Isola et al., the model has been widely used for tasks such as converting sketches to photographs, aerial images to maps, and in this project, translating between different types of satellite imagery. In this implementation, the model is trained on paired satellite images to learn the mapping from one type of satellite image to another. The generator network is tasked with creating realistic images that resemble the target satellite imagery, while the discriminator network evaluates the authenticity of the generated images against real examples. By iteratively training these two networks, the model learns to produce high-quality translated images that are visually indistinguishable from real satellite images. This project showcases the potential of GANs in remote sensing and satellite imagery analysis, providing a powerful tool for enhancing and transforming satellite data for various applications such as environmental monitoring, urban planning, and disaster management.

## Architecture


## Architecture

The Pix2Pix model consists of a Generator and a Discriminator:

- **Generator:** A U-Net architecture with encoder and decoder blocks.
- **Discriminator:** A PatchGAN classifier that determines whether the image is real or generated.

## Setup

### Prerequisites

- Python 3.x
- TensorFlow
- Keras
- NumPy
- Matplotlib

### Installation

Clone this repository and install the required dependencies:

```bash
git clone https://github.com/saikatdas3478/pix2pix-satelite-image.git
cd pix2pix-satellite
pip install -r requirements.txt
```
## Training
To train the model, follow these steps:

- Prepare your dataset and place it in the appropriate directory.
- Preprocess the images to scale them from [0, 255] to [-1, 1].
- Run the training script:

```python
python train.py
```
This will train the model and save the generated images and model weights at specified intervals.

```python
python evaluate.py
```

## Results

The model generates images by learning from the input and target satellite images. Below are some examples of the results:

![Image 1](https://github.com/saikatdas3478/pix2pix-satelite-image/blob/main/plot_010960.png)
![Image 2](https://github.com/saikatdas3478/pix2pix-satelite-image/blob/main/plot_021920.png)
