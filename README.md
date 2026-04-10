# Problem Set 01: Pneumonia Classification from Chest X-Ray Images

## Approach
The goal of this project is to develop a Deep Learning model to classify pediatric chest X-ray images into two categories: **Normal** and **Pneumonia**. Given the complexity of medical images, a Convolutional Neural Network (CNN) was chosen as the primary approach to automatically extract spatial features and patterns from the X-rays..

## Methodology
- **Data Preprocessing:** Images were resized to 150x150 pixels and normalized to a range of [0, 1].
- **Data Augmentation:** To prevent overfitting and improve generalization, techniques like random rotation, zooming, and horizontal flipping were implemented.
- **Model Architecture:** A custom CNN was built with multiple convolutional and pooling layers. Batch Normalization and Dropout (0.5) were used to stabilize training and reduce overfitting.
- **Optimization:** The model used the Adam optimizer and Binary Cross-Entropy loss function.
- **Callbacks:** Early Stopping and Learning Rate Reduction (ReduceLROnPlateau) were implemented to optimize training time.

## Findings
- The model achieved a high training accuracy of approximately **94%**.
- The final test accuracy reached **83.33%**.
- Analysis of loss and accuracy graphs showed that while the model learns well on training data, medical imaging requires careful management of overfitting. The implementation of Dropout significantly helped in narrowing the gap between training and validation performance.



# Problem Set 02: Bank Term Deposit Prediction

## Approach
This project aims to predict whether a customer will subscribe to a bank term deposit based on their demographic and behavioral data. Since the target variable is binary (Yes/No), **Logistic Regression** was used as the primary classification algorithm to build a predictive model.

## Methodology
- **Data Encoding:** Categorical variables (e.g., job, marital status) were converted into numerical values using `LabelEncoder`.
- **Feature Scaling:** Numeric features were normalized using `StandardScaler` to ensure the Logistic Regression model converges efficiently.
- **Handling Class Imbalance:** The dataset was heavily imbalanced (more 'No' than 'Yes'). To fix this, `class_weight='balanced'` was implemented during model training.
- **Feature Importance:** Logistic Regression coefficients were analyzed to identify which banking behaviors most strongly influence a customer's decision.

## Findings
- **Performance Boost:** After balancing the class weights, the **Recall for Class 1 (Subscribers) improved significantly from 18% to 88%**.
- **Key Predictors:** Feature importance analysis revealed that `poutcome` (previous success) and `duration` (call length) are the strongest predictors of a successful subscription.
- The final model provides a reliable balance between accuracy (approx. 81%) and the ability to identify potential subscribers, making it useful for targeted marketing campaigns.
