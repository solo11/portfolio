---
author: Solomon
pubDatetime: 2023-01-30T15:57:52.737Z
title: License plate recognition - Computer Vision
slug: project-5
featured: false
AI: true
ogImage: https://www.suny.edu/media/suny/content-assets/images/SUNY_Logo_278and424-600.jpg
tags:
 - project 
 - AI/ML
 - Computer Vision
description:  license plate detection and recognition makes use of computer vision to find and identify a license plate from an input image of a car.

---
Using computer vision to automatically find and identify a license plate from an input image of a car.



## Table of contents


## Dataset
The environment defined is a 4x4 grid where the agent has to reach the goal state from the initial state, the environment defined is identical for both deterministic and stochastic environments.

The dataset consists of images taken from the Google Open Images Dataset, the Open Images Dataset consists of millions of images that can be used to train and test AI models. For this project images of vehicles are collected.

**Google drive link:**
https://drive.google.com/drive/folders/1-KHew3PpOQpHAuA0g_RA91CgdlN50hZ3?usp=share_link

**Pre-processing of the dataset:**
- The dataset consists of 716 images which are split into train, test and validation sets
- Annotation of the images:
- The images are annotated manually to select the area of interest which is the license plate of the vehicle
- Resizing:
 The image is resized into 416x416 format
  
- Adding noise:
   - Salt and pepper noise is added to the images to make the dataset have images with noise
and blur
   - This is applied for the model to train for the noise and blurry images

- Dataset Sample
<img src="https://i.imgocean.com/Screenshot-2024-03-30-at-5.08.21PM66a61f711f716d48.png">

## Algorithm
The model is trained on the yolov7 algorithm using transfer learning and weights from the yolov7 model
**Yolov7:**
- Since its inception, YOLO has been one of the top object detection networks for three key reasons: accuracy, affordability, and usability.
- Yolov7 is the latest iteration to this model which increases the performance significantly
- YOLO first divides the image into N grids before doing object detection in a single step. These grids
are of the same SxS size. It is utilized to find and locate any objects that might be present in any of these areas. Bounding box coordinates, B, for any prospective objects are predicted for each grid along with their object labels and a likelihood rating for their presence.
- Yolo is an opensource project where we can use our own custom dataset to train
<img src="https://i.imgocean.com/Screenshot-2024-03-30-at-6.11.03PM81dcf73860cc3da8.png" alt="Screenshot-2024-03-30-at-6.11.03PM81dcf73860cc3da8.png" border="0">

## Aspects of the algorithm I've coded on my own:
- Collected and annotated the dataset manually, added salt and pepper noise to the images
- Modified the algorithm to include the custom dataset and weights
- Trained the model on google colab
- Cropping the result images bounding boxes
- Applying OCR on the cropped license plate

## Screenshots

- Example Input and Output
<img src="https://i.imgocean.com/Screenshot-2024-03-30-at-6.13.38PM820c5b24590693a8.png" alt="Screenshot-2024-03-30-at-6.13.38PM820c5b24590693a8.png" border="0">

- Cropped out license plate
<img src="https://i.imgocean.com/Screenshot-2024-03-30-at-6.14.41PM5387b610470a4a08.png" alt="Screenshot-2024-03-30-at-6.14.41PM5387b610470a4a08.png" border="0">

- Low light and blurry inputs
<img src="https://i.imgocean.com/Screenshot-2024-03-30-at-6.15.53PM98546ddc7fc753e4.png" alt="Screenshot-2024-03-30-at-6.15.53PM98546ddc7fc753e4.png" border="0">

Read more - [Project Report](https://github.com/solo11/cvip_project/blob/main/spanduga_final_report.pdf)