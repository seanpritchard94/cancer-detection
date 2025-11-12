# Overview #

## Project Info ##

- Developed by: Sean Pritchard
- for: CSCA 5642: Introduction to Deep Learning
- URL: https://github.com/seanpritchard94/cancer-detection
- Data Source: https://www.kaggle.com/competitions/histopathologic-cancer-detection/overview (Cukierski, 2018)
- Python version: 3.13

## Data Collection and Provenance ##

The data is a subset of the PatchCamelyon (PCam) dataset.

> The PatchCamelyon benchmark is a new and challenging image classification dataset. It consists of 327.680 color images (96 x 96px) extracted from histopathologic scans of lymph node sections. Each image is annoted with a binary label indicating presence of metastatic tissue. PCam provides a new benchmark for machine learning models: bigger than CIFAR10, smaller than imagenet, trainable on a single GPU. (Veeling, 2018)

The subset of data was curated and provided as a kaggel competition. (Cukierski, 2018) We will use the Kaggle Subset of data.

A few important notes about the Kaggle subset include:

> A positive label indicates that the center 32x32px region of a patch contains at least one pixel of tumor tissue. Tumor tissue in the outer region of the patch does not influence the label. This outer region is provided to enable fully-convolutional models that do not use zero-padding, to ensure consistent behavior when applied to a whole-slide image. (Cukierski, 2018)

> The original PCam dataset contains duplicate images due to its probabilistic sampling, however, the version presented on Kaggle does not contain duplicates. We have otherwise maintained the same data and splits as the PCam benchmark. (Cukierski, 2018)

## Deep Learning Problem Description ##

**Type of Learning and Task:** This is a **binary image classification** deep learning problem. I will build a **Convolutional Neural Network** deep learning model capable of classifying the images in the data set

**Project Goal:** Build a deep learning model capable of classifying the images with **at least 90% validation accuracy**.

## Data Description ##

The data is provided as a labeled training set and an unlabeled test set for submission to the Kaggle competition. The data consists of images in the TIFF format. The images have 3 layers (R,G.B) and are 96x96 pixels in size. There are 220,025 images in the labeled training set and 57,458 images in the unlabeled test set.

## Notebook ##

All code is contained in cancer_detaction.ipynb