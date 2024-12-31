# Multi-Cancer Detection with Deep Learning

This project demonstrates a deep learning approach to detect multiple types of cancer using publicly available datasets. The notebook leverages Kaggle datasets and popular Python libraries to preprocess the data, build models, and evaluate their performance.

## Project Overview
The primary goal of this project is to create a reliable multi-class cancer detection model. Using deep learning techniques, we process medical image data and develop models to classify various cancer types.

## Features
- Download and manage datasets via KaggleHub.
- Preprocess datasets for model training.
- Build and train deep learning models.
- Evaluate model performance using metrics like accuracy and loss.
- Visualize results through charts and graphs.

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/your-repo/multi-cancer-detection.git
   cd multi-cancer-detection
   ```
2. Ensure you have Kaggle credentials set up to download datasets.

## Usage
1. Open the notebook:
   ```bash
   jupyter notebook DL_final_.ipynb
   ```
2. Decide subset you want to train
   ``` python
   # subset_name 放你要處理的子類別名稱，例如 Brain Cancer 或 Cervical Cancer 等等
   subset_name = "Kidney Cancer"
   ```
3. Run the cells step-by-step to:
   - Download and prepare datasets.
   - Train the deep learning model.
   - Evaluate and visualize results.

## Data Description
The project uses the **Multi-Cancer Dataset** from Kaggle. The dataset includes:
- Medical images and associated metadata.
- Labels indicating cancer types.

You can find the dataset [here](https://www.kaggle.com/obulisainaren/multi-cancer).

## Model Architecture
The model is built using PyTorch, we use residual model and combine some techs to handle overfitting.  
Techs include:
- K-fold
  > we found that k-fold is used to prevent overfitting not handle
- Simpler model
  > Origin: 3 -> 64 -> 128 -> 256 -> 512 -> n_classes  
  > Simple: 3 -> 32 -> 64 -> 128 -> 256 -> n_classes
- Elastic Net
- Dropout

## Results
After execute you will get 6 figure and 1 json file include all model metrics:
- f1-score.png
- learning-rate.png
- test-acc.png
- train-loss.png
- valid-acc.png
- valid-loss.png
- data.json

Visualizations of the training and validation performance are included in the notebook.
