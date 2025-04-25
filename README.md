# Shoes Classification with DenseNet169

This repository contains a machine learning model built to classify shoe images into different categories. The model was trained using the DenseNet169 architecture on a dataset of 13,000 shoe images.

## Dataset

The dataset used in this project is the [Shoes Classification Dataset (13k images)](https://www.kaggle.com/datasets/utkarshsaxenadn/shoes-classification-dataset-13k-images) from Kaggle. It consists of 13,517 images categorized into 5 classes which is different types of shoes (ballet flat, borgue, boat, clog, sneaker).

## Model Architecture

- **Base Model**: DenseNet169 
- **Top Model**: Custom Sequential Model with:
  - Global Average Pooling
  - Convo2D Layer
  - Dense Layer
  - Dropout (30%) to prevent overfitting
  - Softmax output layer for multi-class classification

## Training Details

- **Training Accuracy**: 93.7%
- **Test Accuracy**: 85.1%
- **Optimizer**: Adam (Learning Rate: 1e-4)
- **Loss Function**: Categorical Cross-Entropy
- **Callback**: ReduceLROnPlateau & ModelCheckpoint

