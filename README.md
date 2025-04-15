# Lung Cancer Detection Using Machine Learning and Deep Learning

This repository contains two Python scripts for detecting lung cancer using machine learning and deep learning techniques. The project includes:

1. **Image-Based Detection**: A Convolutional Neural Network (CNN) model to classify lung cancer images into Benign, Malignant, or Normal categories.
2. **Tabular Data-Based Detection**: Machine learning models to predict lung cancer likelihood based on patient survey data.

The goal is to provide a comprehensive approach to lung cancer detection using both imaging and clinical data.

## Table of Contents
- [Project Overview](#project-overview)
- [Dataset](#dataset)
- [Files](#files)
- [Installation](#installation)
- [Usage](#usage)
- [Model Details](#model-details)
- [Results](#results)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Project Overview
This project implements two distinct approaches for lung cancer detection:

1. **Image-Based Approach (`finalip.py`)**:
   - Uses a CNN to classify lung CT scan images from the IQ-OTH/NCCD Lung Cancer Dataset.
   - Additional machine learning models (Random Forest, SVM, Logistic Regression, Decision Tree) are trained on CNN-extracted features for enhanced classification.
   - Visualizations include confusion matrices, ROC curves, and performance metrics.

2. **Tabular Data-Based Approach (`text_ip.py`)**:
   - Analyzes a survey dataset containing patient features (e.g., smoking, yellow fingers, anxiety).
   - Applies multiple machine learning models (Logistic Regression, Decision Tree, KNN, Gaussian Naive Bayes, SVM, Random Forest, XGBoost, Gradient Boosting).
   - Handles data imbalance using ADASYN and performs feature engineering (e.g., combining anxiety and yellow fingers).

## Dataset
1. **IQ-OTH/NCCD Lung Cancer Dataset** (used in `finalip.py`):
   - Contains CT scan images categorized into:
     - Benign cases
     - Malignant cases
     - Normal cases
   - Source: [Kaggle IQ-OTH/NCCD Lung Cancer Dataset](https://www.kaggle.com/datasets/your-dataset-link) *(replace with actual link if available)*.
   - Images are resized to 128x128 pixels and converted to grayscale for processing.

2. **Lung Cancer Survey Dataset** (used in `text_ip.py`):
   - A CSV file (`survey lung cancer.csv`) with patient features like:
     - Gender, Age, Smoking, Yellow Fingers, Anxiety, Peer Pressure, etc.
     - Target variable: Lung Cancer (Yes/No).
   - Source: [Kaggle Lung Cancer Dataset](https://www.kaggle.com/datasets/your-dataset-link) *(replace with actual link if available)*.
   - Contains 309 records with some duplicates (handled in preprocessing).

*Note*: Due to dataset size or licensing, the datasets are not included in this repository. Please download them from the provided links and place them in the appropriate directories.

## Files
- **`finalip.py`**: Script for image-based lung cancer detection using a CNN and additional ML models.
- **`text_ip.py`**: Script for tabular data-based lung cancer prediction using multiple ML models.
- **Saved Models**:
  - `cnn_model.pkl`: Trained CNN model for image classification.
  - `logistic_regression.pkl`, `random_forest.pkl`, etc.: Trained ML models for tabular data.
- **README.md**: This file, explaining the project and how to use it.

## Installation
To run the project, ensure you have Python 3.8+ installed. Follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/your-repo-name.git
   cd your-repo-name
