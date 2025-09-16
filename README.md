Anomaly-Based Intruder Detection from Mouse Movement Using Unsupervised Machine Learning
This repository contains the code for a Master's thesis on detecting intruders by analyzing mouse movement patterns with unsupervised machine learning. The project demonstrates a practical approach to continuous authentication that does not require labeled impostor data, making it suitable for real-world security applications.

The core idea is to build a profile of a user's normal mouse behavior and then flag significant deviations as potential intrusions.

## 💿 Dataset
The experiments were conducted using the Balabit Mouse Dynamics Challenge dataset. You can download the data directly from their official GitHub repository:

Link: https://github.com/balabit/Mouse-Dynamics-Challenge

Please download the data and place it in a relevant directory before running the notebooks.

## 📁 Project Structure & Code
The repository is organized into four main Jupyter Notebooks, each responsible for a specific part of the data processing and modeling pipeline.

Segmentation.ipynb

This notebook processes the raw log files from the dataset. It segments the continuous stream of mouse events into meaningful, distinct actions like movements, clicks, and drag-and-drops.

EDA.ipynb

This notebook contains the Exploratory Data Analysis. It's used to visualize and understand the characteristics of the segmented mouse actions, user behavior, and session lengths.

Feature Extraction.ipynb

This notebook takes the segmented actions and calculates a comprehensive set of 40 kinematic and geometric features (e.g., velocity, acceleration, curvature, straightness) to numerically represent each action.

Model.ipynb

This is the final notebook where the unsupervised learning models are implemented, trained, and evaluated. It builds per-user anomaly detection models and assesses their performance at both the action and session levels.

## 🚀 How to Run the Project
To reproduce the results, please follow the notebooks in the recommended order:

Download the data from the link provided above.

Run Segmentation.ipynb to process the raw data and create segmented action files.

Run Feature Extraction.ipynb to generate the feature set for modeling.

Run Model.ipynb to train the anomaly detection models and evaluate their performance.

## 🤖 Models Implemented
This project focuses on two primary unsupervised anomaly detection models:

Isolation Forest

Autoencoder
