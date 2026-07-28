# Using-Machine-Learning-to-Predict-Alzheimer-s-Disease

#### Overview

This project uses a Convolutional Neural Network (CNN) to classify brain MRI scans into different stages of Alzheimer's disease. The goal is to support early detection by automatically identifying how advanced the disease is from an MRI image.

#### Dataset

The model is trained on the Alzheimer MRI Preprocessed Dataset from Kaggle, containing 6,400 MRI images resized to 128 x 128 pixels, split across four classes:

Non Demented (3,200 images)
Very Mild Demented (2,240 images)
Mild Demented (896 images)
Moderate Demented (64 images)

The dataset is split into train, validation, and test sets (80/10/10).

#### Technologies Used
TensorFlow / Keras – building and training the CNN
NumPy – numerical operations
Matplotlib – visualizing training curves and results
Scikit-learn – evaluation metrics and confusion matrix
#### Model Architecture

A custom CNN built from scratch with:

Three convolutional blocks (16 → 32 → 64 filters) with ReLU activation and max-pooling
Dropout layers to reduce overfitting
Fully connected dense layers ending in a 4-class softmax output

The model was trained for up to 50 epochs with early stopping and checkpointing based on validation accuracy.

#### Results
Metric	Score
Test Loss	0.035
Test Accuracy	99.1%
Test AUC	0.999
Test Precision	0.991
Test Recall	0.991

A confusion matrix was also generated to evaluate how well the model distinguishes between the four disease stages.
