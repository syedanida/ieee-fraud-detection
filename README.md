# **IEEE Fraud Detection Using AutoGluon**

## **Project Overview**
This project aims to build a robust machine learning model to detect fraudulent transactions using the IEEE-CIS Fraud Detection dataset. By leveraging AutoGluon’s AutoML capabilities, we automate the entire process from data preprocessing to model selection and optimization, ensuring a high-performing classifier with minimal coding.

## **Dataset**
The dataset comprises both **transaction** and **identity** information, making it ideal for building a comprehensive fraud detection model. The key files used in this project are:

- **`train_transaction.csv`** — Transaction data with the target label (`isFraud`).
- **`train_identity.csv`** — Identity attributes corresponding to transactions.
- **`test_transaction.csv`** — Transaction data for prediction (no labels).
- **`test_identity.csv`** — Identity attributes for test transactions.
- **`sample_submission.csv`** — A template for submitting the final predictions.

## **Project Workflow**
### **1. Data Preparation**
- Merge `train_transaction.csv` with `train_identity.csv` to create the training dataset.
- Similarly, merge `test_transaction.csv` with `test_identity.csv` for the test dataset.

### **2. Model Building**
- Use AutoGluon’s `TabularPredictor` to create a classification model.
- Specify `isFraud` as the label and use `roc_auc` as the evaluation metric, given the imbalanced nature of the dataset.

### **3. Model Training**
- Train the model using a subset of the data with AutoGluon’s `presets='good_quality'` to balance model quality and training speed.

### **4. Model Evaluation & Inference**
- Generate probability scores for the test data and prepare the submission file (`my_submission.csv`).

### **5. Submission**
- Save and download the submission file for evaluation on Kaggle.


![image](https://github.com/user-attachments/assets/efb8e342-60f2-41b7-952c-f3383817697a)


**Tutorial link:** https://youtu.be/ilewdbDnjTU


