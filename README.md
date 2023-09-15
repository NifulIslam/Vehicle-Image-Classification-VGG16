# Vehicle Image Classification with VGG16

![Generated Vehicle Images](https://github.com/NifulIslam/Vehicle-Image-Classification-VGG16/blob/main/Images/generated_imgs.png)

This repository contains a vehicle image classification project that classifies six types of local vehicles: Bike, Truck, Bicycle, Car, Boat, and Easy-bike. Initially, a dataset of 7554 images was collected, with some images generated using GANs.

## Model Architecture

The image classification model is based on a modified VGG16 architecture. In this modified architecture, features extracted from the 3rd, 4th, and 5th blocks of the VGG16 model are passed directly to the classification layers.

![Modified VGG16 Architecture](https://github.com/NifulIslam/Vehicle-Image-Classification-VGG16/blob/main/Images/modifiedVGG.png)

## Hugging Face Deployment

The trained model is deployed on Hugging Face for easy inference and usage. You can access the model and make predictions using the following link:

[Vehicle Classifier on Hugging Face](https://huggingface.co/spaces/NifulIslam/Vehicle-Classifier)

![Hugging Face Deployment](https://github.com/NifulIslam/Vehicle-Image-Classification-VGG16/blob/main/Images/hf.png)

## Benchmarking

Here are the benchmarking results for the proposed VGG16 and ConvNext Tiny models:

| Model           | Accuracy | Precision | Recall  | F1 Score | MCC     |
|-----------------|----------|-----------|---------|----------|---------|
| Proposed VGG16  | 0.6756   | 0.7504    | 0.6756  | 0.6791   | 0.6240  |
| ConvNext Tiny   | 0.6944   | 0.7480    | 0.6944  | 0.7079   | 0.6361  |

## Confusion Matrix

![Confusion Matrix](https://github.com/NifulIslam/Vehicle-Image-Classification-VGG16/blob/main/Images/ConMat24.png)

## Dataset

Initially, there were 14 types of images in the dataset. Due to the large size, only six types of vehicles were collected for this project (size 7554).

## Usage

To use the trained model for vehicle image classification, you can make API requests to the Hugging Face model, or you can download the model weights and use them in your own Python code. Instructions for using the model are available in the Hugging Face model repository.

## Contributing

Contributions to this project are welcome. If you would like to contribute or report issues, please feel free to create pull requests or open issues in this GitHub repository.

## Dataset Link
The original dataset, along with the generated images, can be found on Kaggle at the following link:
[Paribahan BD Dataset on Kaggle](https://www.kaggle.com/datasets/naifislam/paribahan-bd)

