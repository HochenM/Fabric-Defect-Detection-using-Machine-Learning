# Fabric Defect Detection using Machine Learning

## Overview

This project implements a fabric defect detection system using two different machine learning approaches: polynomial regression based anomaly detection and unsupervised clustering using KMeans.

The goal of the project is to compare model-based and data-driven approaches for detecting defects in fabric images without using labeled data.

The system is built using classical machine learning and image processing techniques and is evaluated on both plain and patterned fabric images.

---

## Project Objectives

* Detect fabric defects using unsupervised and semi-model-based methods
* Compare polynomial regression with clustering-based segmentation
* Analyze performance on plain and striped fabric textures
* Build a full image processing and ML pipeline
* Understand limitations of different classical ML approaches for image defect detection
* 
----

Methods Used

1. Polynomial Regression Based Detection

In this method, each image is treated as a one-dimensional signal.

The workflow includes:

* Image smoothing using blur filters
* Flattening the image into a 1D intensity signal
* Applying polynomial regression to model the smooth structure
* Computing residuals between actual and predicted values
* Detecting defects based on statistical deviation from the model

This method works well for smooth and uniform fabric textures.

2. KMeans Clustering Based Detection

In this method, defect detection is treated as a clustering problem.

The workflow includes:

* Image preprocessing using median blur
* Flattening pixel intensity values
* Applying KMeans clustering with three clusters
* Identifying the smallest cluster as the defect region
* Generating a binary defect mask

This method works better on both plain and structured fabrics such as striped patterns.

-----

## Dataset

The dataset consists of grayscale fabric images including:

* Plain fabric textures
* Striped fabric patterns
* Defective fabric samples

No labeled annotations are used in the project.

---

## Technologies Used

* Python
* OpenCV
* NumPy
* Matplotlib
* Scikit-learn

---

## Results

The project generates the following outputs for each image:

* Original fabric image
* Polynomial regression based defect visualization
* Clustering based segmentation map
* Binary defect mask

---
  
## Key Observation

* Polynomial method performs better on simple and smooth fabric textures
* Clustering method performs better on both simple and structured textures
* Clustering is more robust to pattern variations
  
---

## Skills Demonstrated

* Image Processing
* Unsupervised Machine Learning
* Regression Based Anomaly Detection
* KMeans Clustering
* Feature Engineering for Images
* Model Comparison and Analysis
* Computer Vision Pipeline Design

----

## Limitations

* Polynomial method fails on structured textures such as stripes
* Clustering may confuse texture variations with defects
* Both methods are sensitive to lighting changes
* No spatial feature modeling is used
* Future Improvements
* Combine both methods into a hybrid system
* Add spatial features (x, y coordinates)
* Use texture descriptors such as LBP or GLCM
* Experiment with DBSCAN clustering
* Add evaluation metrics for quantitative comparison

---

## Author

Moein

Machine Learning | Computer Vision | Image Processing
