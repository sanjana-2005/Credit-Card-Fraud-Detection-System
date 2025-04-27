# Credit Card Fraud Detection System

## Overview
This project implements a credit card fraud detection system using machine learning techniques. The system utilizes a Random Forest Classifier to predict whether a transaction is fraudulent based on various features.

## Technologies Used
- Python
- Flask
- Scikit-learn
- Imbalanced-learn (for SMOTE)
- Pandas
- NumPy
- Joblib

## Models and Components
1. **Random Forest Classifier**:
   - **Purpose**: Used to classify transactions as fraudulent or non-fraudulent.
   - **File**: `creditcard_Random_Forest_classifier_model.pkl`

2. **Standard Scaler**:
   - **Purpose**: Scales the input features (`Time` and `Amount`) to ensure they are on the same scale.
   - **File**: `scaler_creditcard.pkl`

3. **KMeans Clustering**:
   - **Purpose**: Assigns clusters to the input data based on PCA-reduced features.
   - **File**: `kmeans_creditcard.pkl`

4. **PCA (Principal Component Analysis)**:
   - **Purpose**: Reduces the dimensionality of the input features to improve model performance.
   - **File**: `pca_dup.pkl`

## Installation
1. Clone the repository or download the project files.
   ```bash
   git clone <repository-url>
   cd <repository-directory>
   ```
2. Install the required packages:
   ```bash
   pip install flask scikit-learn imbalanced-learn pandas numpy joblib
   ```

## Running the Project
1. Ensure that the model files are in the specified paths in the `app3.py` file.
2. Run the Flask application:
   ```bash
   python app3.py
   ```
3. Open your web browser and navigate to `http://127.0.0.1:5000/` to access the application.

## Usage
1. **Login**: Use the credentials provided in the code (admin/password123 or user/userpassword) to log in.
2. **Dashboard**: After logging in, you will be redirected to the dashboard.
3. **Predict**: Enter the `Time` and `Amount` of the transaction you want to analyze and submit the form.
4. **Results**: The application will display whether the transaction is likely fraudulent or non-fraudulent, along with the probabilities.

## Results
The model was evaluated on a dataset, and the following results were obtained:

### Training Data:
- **Accuracy**: 93.29%
- **Precision**: 
  - Class 0: 0.92
  - Class 1: 0.94
- **Recall**: 
  - Class 0: 0.95
  - Class 1: 0.92
- **F1-Score**: 
  - Class 0: 0.93
  - Class 1: 0.93

### Testing Data:
- **Accuracy**: 92.67%
- **Precision**: 
  - Class 0: 0.92
  - Class 1: 0.94
- **Recall**: 
  - Class 0: 0.94
  - Class 1: 0.92
- **F1-Score**: 
  - Class 0: 0.93
  - Class 1: 0.93

## Conclusion
This project demonstrates the use of machine learning techniques for fraud detection in credit card transactions. The Random Forest Classifier, along with PCA and KMeans clustering, provides a robust solution for identifying fraudulent activities.

