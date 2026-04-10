# Problem Set 01: Pneumonia Classification from Chest X-Ray

## Approach
The objective is to develop a CNN model to classify pediatric chest X-ray images into two categories: Pneumonia and Normal. I focused on building a model that can handle medical imaging data with high accuracy.

## Methodology
- **Data Preprocessing:** Resized images to 150x150 and normalized pixel values.
- **Augmentation:** Applied random rotation, zoom, and horizontal flips to prevent overfitting.
- **Model:** Built a Convolutional Neural Network (CNN) with Batch Normalization and Dropout layers.
- **Optimization:** Used Adam optimizer and Binary Cross-Entropy loss.

## Findings
- The model reached a training accuracy of over 90%.
- Observations from the loss graph indicated a slight overfitting, which was addressed using Dropout.
- Final test accuracy: 94%.


# Problem Set 02: Bank Term Deposit Prediction

## Approach
This project predicts whether a customer will subscribe to a term deposit using a Logistic Regression model. The focus was on handling imbalanced banking data to improve prediction recall.

## Methodology
- **Data Cleaning:** Categorical variables were encoded using Label Encoding.
- **Feature Scaling:** Used StandardScaler to normalize numeric inputs for better convergence.
- **Class Imbalance:** Applied `class_weight='balanced'` to improve recall for the minority class (subscribers).
- **Evaluation:** Analyzed coefficients to determine feature importance.

## Findings
- Significant improvement in Recall for Class 1 (from 18% to 88%) after balancing weights.
- **Key Features:** 'poutcome', 'duration', and 'housing' were the most influential predictors of customer behavior.
