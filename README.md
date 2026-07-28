# Using-Machine-Learning-to-Predict-Alzheimer-s-Disease

#### The Idea :
Alzheimer's is a brain disease that slowly gets worse over time. It causes memory loss, confusion, and trouble with everyday thinking. It's the biggest cause of dementia, and it affects a large number of older adults (roughly 11% of people aged 65+ in the US). Once someone starts showing symptoms, the damage to the brain can't be undone — which is why catching it early really matters.

Right now, there isn't a simple, widely-used way to screen people for Alzheimer's before it fully develops. This project explores whether machine learning can help fill that gap by looking at MRI brain scans and predicting whether a person is likely to develop the disease.


#### Dataset :
We used the OASIS dataset (Open Access Series of Imaging Studies), which is a public collection of brain MRI scans, to train and test our models.

#### Models : 
To find the best way to make these predictions, we experimented with several different machine learning approaches:

K-Nearest Neighbors (KNN)
Ensemble Methods
Multilayer Perceptron (MLP)
Convolutional Neural Network (CNN)
Support Vector Machine (SVM)
Grad-CAM (used to visualize which parts of the brain scan the model is focusing on)

#### Goal :
Our main aim was simple: get the prediction accuracy as high as possible. Our best-performing model reached an accuracy of 98.07%.
