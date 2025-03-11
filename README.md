# Kernel-SVM-Model
This repository contains a Python script that implements Kernel Support Vector Machine (SVM) with an RBF kernel to classify customer satisfaction based on survey responses.



# Kernel SVM Model

## Overview
This repository contains a Python script that implements **Kernel Support Vector Machine (SVM)** with an **RBF kernel** to classify customer satisfaction based on survey responses.

---

## **Problem Statement**
Customer satisfaction prediction is an essential aspect of business analytics. This project builds a **Kernel SVM** model to determine whether a customer is satisfied (`1`) or not (`0`) based on factors such as support rating, food quality, and delivery speed.

### **Dataset Description**
The dataset used in this project is from [**Kaggle: Customer Satisfaction Dataset**](https://www.kaggle.com/datasets/ahmedaliraja/customer-satisfaction-10k) and includes the following features:
- **Support Rating**: Customer rating of support experience (scale: 1–5).
- **Quality Rating**: Customer rating of food quality (scale: 1–5).
- **Delivery Rating**: Customer rating of delivery speed (scale: 1–5).
- **Satisfaction (Target Variable)**:
  - **1**: Satisfied.
  - **0**: Not Satisfied.

---

## **How the Script Works**
1. **Data Preprocessing**:
   - Loads the dataset and checks for missing values.
   - Drops unnecessary columns (`CustomerID`).
   - Maps categorical values (`Yes/No`) to numerical values (`1/0`).
   - Standardizes numerical features using **StandardScaler**.
2. **Model Training**:
   - Splits the dataset into **training (80%)** and **testing (20%)** sets.
   - Trains an **SVM classifier** with an **RBF kernel** using `sklearn.svm.SVC()`.
3. **Hyperparameter Tuning**:
   - Uses **GridSearchCV** to optimize:
     - **C** (Regularization parameter).
     - **Gamma** (Kernel coefficient).
4. **Prediction & Evaluation**:
   - Makes predictions on the test dataset.
   - Evaluates the model using:
     - **Confusion Matrix**
     - **Precision, Recall, and F1-score**
     - **Classification Report**
5. **Model Insights**:
   - Identifies class imbalance issues.
   - Discusses performance challenges and possible improvements.
6. **Visualization**:
   - **Confusion Matrix Heatmap**.
   - **Grid Search Best Hyperparameters**.

---

## **Dependencies**
Ensure you have the following Python libraries installed:
```sh
pip install numpy pandas matplotlib seaborn scikit-learn
```

---

## **How to Run the Script**
1. Clone the repository:
   ```sh
   git clone <repository_url>
   ```
2. Navigate to the project folder:
   ```sh
   cd <project_folder>
   ```
3. Run the Python script:
   ```sh
   python kernel_svm.py
   ```
4. Follow the output to view model predictions and evaluation results.

---

## **Contributing**
Contributions are welcome! Feel free to fork this repository and submit a pull request with improvements or additional features.

