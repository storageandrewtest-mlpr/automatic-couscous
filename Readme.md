# Face Detection and Clustering Lab

This repository contains a Jupyter Notebook designed for a laboratory exercise focused on **Face Detection** using Haar-Cascades and **Unsupervised Clustering** using k-Means. The project involves processing images of university faculty, extracting color features from detected faces, and classifying them into clusters.

---

## Project Overview

I have developed this notebook to demonstrate a complete pipeline for image analysis, including:

* **Face Detection:** Using OpenCV's Haar-Cascade classifiers to locate faces in a group photograph.
* **Feature Extraction:** Converting image regions from BGR to **HSV color space** and calculating mean Hue and Saturation for each face.
* **K-Means Clustering:** Grouping detected faces based on their color profiles.
* **Template Matching:** Predicting which cluster a new "template" image belongs to using distance-based logic.

---

## File Structure

* `notebook.ipynb`: The main working file containing the code, visualization, and instructions.
* `plaksha_Faculty.jpg`: The primary image used for face detection and clustering.
* `Dr_Shashi_Tharoor.jpg`: The template image used for testing the classification.

---

## Instructions for Use

To complete the lab, follow the internal comments marked with `##`. Key tasks include:

### 1. Environment Setup

I use several standard Python libraries for this project. Ensure you have them installed:

* `cv2` (OpenCV)
* `numpy`
* `matplotlib`
* `sklearn` (for k-Means)
* `scipy`

### 2. Face Detection

* Load the image and convert it to grayscale.
* Initialize the `face_cascade` with the appropriate XML file.
* Tune the `detectMultiScale` parameters (scaleFactor, minNeighbors) to accurately capture all faces.

### 3. Clustering and Visualization

* Calculate the **Hue** and **Saturation** for each detected face.
* Apply the k-Means algorithm to the feature set.
* I have included code to visualize these clusters using scatter plots where markers are replaced by the actual face thumbnails.

### 4. Prediction

* Process the template image and extract its HSV features.
* Determine its cluster label and visualize where it sits in relation to the existing data points and centroids.

---

## Learning Objectives

Within the final report section of the notebook, I address the following conceptual questions:

1. **Distance Metrics:** Understanding Euclidean, Manhattan, and Minkowski distances.
2. **Applications:** Exploring real-world uses for distance-based classification.
3. **Model Performance:** The importance of cross-validation.
4. **Bias vs. Variance:** Explaining these concepts specifically in the context of the K-Nearest Neighbors (KNN) algorithm.

---
