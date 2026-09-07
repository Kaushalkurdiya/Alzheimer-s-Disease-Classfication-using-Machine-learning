# Alzheimer's MRI Image Classification CNN
 
A Convolutional Neural Network (CNN) built with TensorFlow/Keras to classify brain MRI images into four stages of Alzheimer's Disease severity.
 
## Overview
 
This project uses deep learning to aid in the early diagnosis of Alzheimer's Disease by classifying MRI brain scans into one of four categories:
 
1. **Non Demented**
2. **Very Mild Demented**
3. **Mild Demented**
4. **Moderate Demented**
## Dataset
 
The dataset consists of MRI images sourced from various websites, split into **Training** and **Testing** sets, containing approximately 5,000 images total across the four severity classes.
 
**Class labels:**
- `MildDemented`
- `ModerateDemented`
- `NonDemented`
- `VeryMildDemented`

## Tech Stack
 
- **Python** 3.9
- **TensorFlow / Keras** — model building and training
- **OpenCV (cv2)** — image loading and preprocessing
- **NumPy / Pandas** — data handling
- **Matplotlib / Seaborn** — visualization
- **scikit-learn** — train/test split, evaluation metrics
## Pipeline
 
1. **Data Loading** — Images loaded in grayscale from the four category folders.
2. **Preprocessing**
   - Images resized to `100x100` pixels.
   - Pixel values normalized (divided by 255).
3. **Dataset Preparation**
   - Images and labels combined and shuffled.
   - Split into training (75%) and testing (25%) sets using `train_test_split`.
4. **Model Architecture** (Sequential CNN):
   - `Conv2D(64, 3x3)` + ReLU + `MaxPooling2D`
   - `Conv2D(64, 3x3)` + ReLU + `MaxPooling2D`
   - `Flatten`
   - `Dense(64)`
   - `Dropout(0.5)`
   - `Dense(128, activation='relu')`
   - `Dense(4, activation='softmax')` (output layer)
5. **Compilation**
   - Optimizer: `adam`
   - Loss: `SparseCategoricalCrossentropy`
   - Metric: `accuracy`
6. **Training**
   - Batch size: `32`
   - Epochs: `10`
   - Validation split: `10%`
7. **Evaluation**
   - Accuracy/loss curves
   - Confusion matrix
   - Classification report (precision, recall, F1-score)
## Results
 
| Metric | Score |
|---|---|
| Accuracy | 97.76% |
| Validation Accuracy | 94.14% |
| Loss | 0.06 |
| Validation Loss | 0.19 |
| F1 Score | 95.39% |
| Precision | 95.45% |
| Recall | 95.38% |
 
The model achieves strong classification performance across all four classes, with particularly high precision for `ModerateDemented` (100%) and `NonDemented` (97%) categories.
 

 

